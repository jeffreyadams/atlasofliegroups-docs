
Design Principles
==========================

The axis language is expression based, which means that the text entered
serves most often to designate values to be computed rather than actions to be
performed. Its design is close to that of functional programming languages:
function values are first class citizens, binding is static with no
restrictions on lifetime, semantics is value-based for all types (no
distinction betwen object and value, or between mutable and unmutable values).
The language does provide assignable variables and loops. All control
structures including loops are oriented towards construction of values rather
than towards sequencing of side-effects, although they do provide the latter.
Somewhat curiously for a language close to functional languages, ordinary
definitions cannot be recursive, which is a consequence of strict scoping
rules derived from the lambda-calculus. Nonetheless recursive function
definitions are supported through use of the rec_fun keyword.

For beginning users it is important to stress the fundamental distinction
between creating names (variables) and assigning to them. The interpreter will
never create a variable just because it appears to be used, and therefore
refuses expressions with unknown names in them: it neither creates new
variables that are being assigned to (as Python does), nor assumes new names
to be meaningful but undefined (as do many symbolic algebra packages, which
take unknown names to stand for indeterminates). Names are introduced using
the keyword 'set' (for permanent names) or using the keyword 'let' (for local
names, whose scope is limited to the current expression, or even to part of
it); in both cases the name is immediately bound to a value. Once a name is
introduced, its value can be altered by assignment, which is written ':=' (in
the tradition of Algol and Pascal, and unlike FORTRAN and C). Such assignments
are fairly rare (they are used almost exclusively for programming purposes),
and cannot alter the type of the value bound to the name. Both 'set' and 'let'
follow the name(s) being introduced by '=' (not ':='). Apart from that, '='
also serves as equality testing operator (defined for most types).

The language is strictly typed, so that type-correctness of expressions must
be established before their evaluation is attempted. This means that most
common errors are caught before execution starts, and these error messages are
usually more specific about their cause than runtime errors (which mention any
offending value, but cannot trace where that value originated). As a
consequence it can be tough to write a script in such a way that will load
without any error message, but the correction cycle is fast: atlas just stops
at the first error, with a detailed message, and reloading after correcting
the problem is easy (type up-arrow once to recover the load command from
history). Once a script is fixed to the point that loading runs to the end of
the file, most trivial errors will have been eliminated. Nonetheless, type
checking is a complicated process, which in rare cases could produce hard to
decipher error messages (but nothing compared to what C++ compilers produce).

Most of the time the system can figure out the types from the expressions, so
the user need not write them explicitly; however the types of arguments of
user-defined functions must always be specified. Types are also used to allow
overloading, which means that it is possible to give the same (natural)
function or operator name to different operations; in each expression using
these names, the type system then determines which instance is to be used.
This applies in particular to user function definitions, so that binding of
overloaded operators and functions is done statically (when the user defines
the function rather than when it gets executed). Currently types are
straightforward and therefore somewhat limited; this is quite sufficient for
using the Atlas functionality, though for advanced programming the set of
possible types might need to be enlarged in the future.

The primitive data types currently available for values cover almost all those
that the Atlas library can handle (root data, inner classes, real forms,
Cartan classes, KGB elements, parameters for (standard) modules and formal
sums of those; a notable exception is twisted involutions or Weyl group
elements but working with representing matrices suffices). For the types
available not all library functionality is available in atlas, but this can
sometimes be circumvented using a script. Some data types used internally
(such as Weyl groups, polynomials) may appear in printed output but cannot be
further manipulated. The programming language itself is fairly complete in
functionality, with constructions like variables, loops and conditionals, as
well as functions and operators (both built-in and user-defined); what is
currently the most annoying limitation is the absence of second order typing.