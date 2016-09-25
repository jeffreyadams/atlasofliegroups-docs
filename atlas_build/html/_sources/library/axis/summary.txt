Syntax Summary
================

The formal syntax is defined in the parser generator source file "parser.y"; a
readable summary can be found at the beginning of "parser.output" which if
needed can be created by the shell command "bison --report=states parser.y".

The syntax is very largely centered around a single "part of speech", the
expression. There is no distinction between expressions and statements: every
expression may have side effects (if it contains assignments for instance) and
yields a value (although it might be void, i.e., useless). The only part of
the syntax not directly concerned with expressions is that defining commands,
which are only allowed at the outermost level. Some other categories, such as
type specifications and formal parameter lists, are used within certain kinds
of expressions, but do not themselves constitute expressions. The command level
will be described at the beginning, the other non-expressions categories at
the end. In between we enumerate the different kinds of expressions, in order
from most loosely bound to most tightly bound; using a loosely bound form in
more tightly bound context requires enclosing the expression in parentheses.

Command level
----------------

The most common command is an expression, possibly followed by a semicolon;
the case with semicolon is treated exactly as if '()' followed to form a
sequenced expression with void value (so that no value will be printed.

Another common command is the definition starting with 'set'. In it's basic
form 'set' is followed by a an identifier pattern or an operator name, an '='
and an expression. For function definitions there is an alternative form
deemed more pleasant than writing an anonymous function body after the '=';
here 'set' is followed by a single function name or operator symbol, and then
directly the (possibly empty) parameter list in parentheses, only then
followed by '=' and an expression (the function body). The latter form is
treated like the basic form of 'set' command obtained by moving the '=' in
front of the parameter list and inserting ':' where it used to be. Whether
identifiers or operator of the 'set' command will be stored in the identifier
table or in the overloading table is not directly dependent on the syntactic
form used: the rule is currently that overload table is chosen when a single
identifier or operator is set to an expression of function type, and in all
other cases the identifier table is used (this does imply the special function
syntax always overloads). So combined definitions (using a pattern) cannot
define overloads, but this rule (and the syntax) might change in the future.

A command of the form 'ident : expr' is almost equivalent to the command 'set
ident = expr', except that it adds to the identifier table in all cases.

A command of the form 'ident : type' similarly introduces an identifier
into the identifier table, with the given type but with an undefined value.

The 'forget' command removes a global identifier or overload. In the former
case 'forget' is just followed by the identifier to be removed; in the latter
case the overload to remove must be specified by writing an operator cast
(described under expressions): 'forget +@(int,int)' forgets integer addition.

The command 'whattype expression' performs type analysis of the expression,
and upon success just prints the type found, suppressing evaluation.

The command 'whattype x ?' where x is an identifier or operator symbol shows
the types of all overloads currently defined for that symbol.

A command 'showall' displays the contents of overload and identifier tables.

The command 'quit' terminates the interpreter, while 'verbose' and 'quiet'
turn on or off extra diagnostics during expression analysis.

A command starting with '>' or '>>' redirect output to a file; the symbol is
followed by a file name (either delimited by whitespace or enclosed in quotes)
and then the expression to be evaluated.

A command starting with '<' or '<<' opens a subsidiary input file as described
above; it should be followed just by the name of the file to include


Quaternary expressions: 'let', anonymous functions, casts, sequences
-------------------------------------------------------------------------

These are the expression types that end with another expression, without ever
needing parentheses around that other expression; they are themselves loosely
bound, so the might require parentheses (or equivalently a begin-end pair)
around the entire expression if used in certain contexts (as right hand side
of an assignment for instance, or as item in a semicolon-separated sequence).

Let-expressions introduce local definitions: they start with 'let', then a
list of one or more definition groups separated by 'then', followed by 'in'
and finally an expression that produces the value of the construct.
Definitions in a definition group take effect in the following group, or after
'in' in case of the last group; in other words 'then' here behaves like 'in
let'. A definition group consists of one or more definitions separated by
commas, which definitions are handled in parallel. Each basic definition
consists of an identifier pattern (see h) followed by '=' and an expression.
The variation of the 'set' syntax for function definitions (with '=' coming
after the parameter list) is also available for local function definitions.

Anonymous functions consist of a pair of parentheses enclosing a parameter
list, followed by an optional (result) type, and then ':' and a (function
body) expression. A parameter list consists of zero or more pairs of a type
followed by an identifier pattern, separated by commas.

Casts consist of a type followed by ':' and an expression. They define an
expression forced to be of the given type (possibly applying an implicit
conversion to the given expression). Like any other type of expression, an
implicit conversion may also apply to a cast itself (though this is rare);
however a cast immediately following '=' in a definition will ensure that the
entity defined (identifier or function body) will be of exactly that type.

Sequenced expressions come in two kinds: they are sequences of expressions,
separated either by 'next' or by ';'. Both are as loosely bound as let
expressions, function definitions and casts, which means that one can chain
any sequence of 'let ... then .. in' and 'expression ;' or 'expression next'
before a final expression, without requiring parentheses (also function
headings and casts can occur, but they usually only occur at the beginning or
at the end of a chain). Both 'expr1 ; expr2' and 'expr1 next expr2' evaluate
both expressions from left to right; with a (more usual) semicolon the value
is that of expr2, while with the 'next' keyword it is the value of expr1. The
purpose of next is to retain the current value of expr1 even though the later
side effect of evaluating expr2 might modify the value of expr1. It is unusual
to have more than one 'expression next' in the chain, but if one does, it is
the first one that will determine the final value (if there are none, as is
often the case, then the final expression produces the value of the clause).

Tertiary expressions: assignments
-------------------------------------

The three kinds of assignments are tertiary level expressions: simple
assignments, component assignments and compound assignments (compound
component assignments are not currently possible). Each of them end with ":="
followed by a tertiary level expression. To the left of ":=" they have
respectively an identifier, a subscripted identifier (the subscript being an
expression enclosed in '[' and ']'), and an expression followed by an operator
symbol. For a component assignment to be valid it is necessary that the type
of identifier and index are such that the subscription would be a valid
expression, but component assignments are not allowed for identifiers of type
'string', 'ratvec', or 'ParamPol'. When valid, a component assignment is
handled as a primitive operation in the evaluator. The meaning of a compound
assignment of the form 'ident # := expr' on the other hand (where # represents
any infix operator) is by definition that of 'indent := ident # (expr)'; in
other words it is determined by the overload of the operator for operand types
of the identifier and the expression, whether built-in or user-defined.
Currently compound statements are transformed into that form by the parser
(compound assignments might be handled by the evaluator instead in the future,
but only so as to achieve the same effect possibly more efficiently.)

Secondary expressions: formulas
------------------------------------

Expressions at the secondary level are formulas, consisting of an operator
applied to one or two operands. The level in fact splits into many sub-levels
corresponding to different operator precedences. This structure is not very
clear from the formal grammar (because precedence is largely handled by
formula restructuring inside parser actions), but the operators, ordered by
increasing precedence, are::

  or
  and
  not         (prefix use only)
  =,  !=,  <,  >,  <=,  >=
  +, -
  *, /, \, %, \%
  ^
  #, ~

The logical connectives in the first three lines above are somewhat different,
in that they are keywords rather than operator symbols, cannot be overloaded
or redefined, and are in fact currently handled in special ways by the parser
so as to ensure for instance the short-circuit evaluation of 'and' and 'or'.

Association (implicit grouping among operators of equal precedence) is from
left to right at all levels, with the exception of the level of '^' at which
association is from right to left. A monadic (prefix) use of an operator
symbol has the same precedence as a dyadic (infix) use of the same symbol,
except that a monadic operator symbol that is immediately preceded by a dyadic
one, thereby effectively gets the highest possible precedence (the latter
stipulation is needed to ensure consistency of precedence rules).

::

     -x+y    is parsed as    (-x)+y
     -a%p    is parsed as    -(a%p)
     -a^b    is parsed as    -(a^b)
     a+-b^c  is parsed as    a+((-b)^c)
     a/b*c   is parsed as    (a/b)*c
     a^-1    is parsed as    a^(-1)
     a/-b+c  is parsed as    (a/(-b))+c
     a/-b*c  is parsed as    (a/(-b))*c
     a/-b^c  is parsed as    a/((-b)^c)
    
All operator symbols can be used as monadic operators; doing so it may in some
cases be necessary to separate the operator by white space from a preceding
operator symbol to avoid a two-character operator symbol from being formed.

Primary expressions: subscriptions, function calls, atomic expressions
----------------------------------------------------------------------------

Primary expressions are sufficiently strongly bound to never require
parenthesis around them. They comprise subscriptions of aggregate values,
function calls, and expressions like identifiers without any subexpressions.

Subscriptions and function calls generally consist of a primary expression
(often just an identifier) followed by an expression enclosed in '[' and ']'
(for subscriptions) or '(' and ')' (for calls). If the latter expression is a
tuple display its outer parentheses can be omitted; thus selecting an entry
from a matrix 'a' can be written 'a[i,j]', and calling a function 'f' with a
3-tuple as argument can be written 'f(x,y,z)'. The initial expression (giving
the aggregate of function) can be any primary level expression, or any closed
clause, except that for technical reasons the grammar forbids writing '()'
here (this is no problem since the empty tuple is neither an aggregate nor a
function), which construct is artificially introduced at the secondary level.

Atomic expressions are identifiers, non-negative integer constants, the
keywords true, false, string constants (enclosed in quotes and on a single
line), the symbol '$' (representing the value of the last evaluated
expression) and specializations of overloaded symbols. The latter are formed
by an (overloaded) identifier or operator followed by '@' and a type.

Closed expressions: displays and groupings, conditionals, loops
---------------------------------------------------------------------

These compound expressions include delimiters at both ends, so they never need
(additional) parentheses; a single parenthesized expression also forms a closed
expression. The different forms are as follows, where '*' is any expression

if * then * fi		  	which abbreviates: if * then * else () fi)
if * then * else * fi
if * then * elif * then ... fi
while * do * od
for pattern in * do * od        optionally with ~ before do and/or od
for pattern @ ident in * do * od idem
for ident : * do * od            idem (implicit 'from 0')
for ident : * from * do * od     idem
for ident : * downto * do * od  deprecated, means 'for ident : to * ~do * od'
( * )                           a parenthesized expression
begin * end			which is equivalent to: ( * )
( * , * , ... )			which builds a tuple
[ * , ... ]   			which builds a list
[ * , ... | * , ... | ... ]     which builds a matrix by rows

Identifier patterns
----------------------

Identifier patterns occur in parameter lists for functions, and in local
('let') or global ('set') declarations. An identifier pattern can be a single
identifier, or a parenthesized and comma-separated list of optional identifier
patterns, optionally followed by ':' and an identifier. If a pattern consist
of or ends with an identifier, that identifier names the entire value
corresponding to the pattern. If it contains a parenthesized and
comma-separated list, the corresponding value must have tuple type with as
many components as the list, and each identifier pattern in the list
corresponds to the component of that tuple value at its position. If a pattern
is absent at some position, the corresponding component is not individually
named in the pattern, nor (should it be a tuple) any of its own components.

Types
----------

In the grammar types occur in parameter lists, casts, and in specializations
of overloaded symbols. Currently possibilities of specifying types is fairly
limited: they are built up of primitive types (one of 'int', 'rat', 'bool',
'string', 'vec', 'mat', 'ratvec', 'Lie_type', 'RootDatum', 'InnerClass',
'RealForm', 'CartanClass', 'KGBElt', 'Block', 'Param, 'Split', 'ParamPol')
using three constructors: the list constructor [*], the tuple constructor
(*,*,...) (with at least two component types; around a single type parentheses
just provide redundant grouping) and the function constructor
(*,*,...->*,*,...) (here if the number of argument or result types is not
exactly one, parentheses are implicitly assumed around the list, making it
into a tuple type). There are no type names standing for non-primitive types,
with one exception: 'void' is predefined as name for the tuple type with no
component types. Because of ambiguity with empty tuple displays and ditto
parameter lists, one cannot use '()' to designate this 0-tuple type.