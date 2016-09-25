Splitting Commands
====================

Normally each complete line entered is executed as a command (an expression to
evaluate, an identifier or operator definition, or a miscellaneous command);
the type check execution are performed without the need for a symbol
signaling that a command is completed. However, commands may require more
text than fits on a line, especially if they contain function definitions, so
some simple provisions are made to not necessarily consider each end-of-line
as a command terminator. It is not practically possible, nor really desirable,
to have the parser (which already operates on partial input) decide at the end
of each line whether the input up to that point would constitute a
syntactically correct command, and to continue parsing whenever it is not.
Therefore the approach is adopted that each end-of-line is taken to terminate
a command, unless there is some simple reason (that the scanner can detect)
why the command could not possibly be completed there. Note that the same
rules apply whether the command/definition is processed interactively or is
read from a file (script), though prompting is only done in the former case.

First of all, a command is not considered complete if it contains unclosed
opening parentheses or brackets. When this happens interactively, the unclosed
symbols in question are prefixed (in order) to the continuation prompt, as an
indication to the user of what still needs to be closed; for instance if a two
parentheses are unclosed, the prompt becomes "(( >". (Should the user discover
at this point a mistake that the line entered is wrong and cannot be corrected
by adding symbols, the best strategy is to cop out by provoking a syntax
error; the history mechanism facilitates retrial with corrections.)

Similarly the opening keywords 'let', 'begin', 'if', 'while', 'for' will
suspend command termination until the corresponding closing keyword is found;
only the change of the prompt here just adds one letter, which is 'L' for
'let' and 'G' (standing for group) for any of the other ones. Another useful
provision is that, certain symbols suspend termination when they are at the
end of a line (these are symbols that cannot be the final one in any valid
input). These symbols are all (arithmetic, relational and logical) operator
symbols (including '=' and '~', even when not used as operator), and the
symbols ':', ':=', ',' (comma), ';' (semicolon), and 'in'. Interactively these
all append a marking character to the prompt, often their first character.

Usually these rules allow to fend off premature command termination easily; an
easy way to protect 'set' definitions is to break the first line after '=',
start the next line with 'begin', and end the definition with a line 'end'.
But often one can manage without the 'begin' ... 'end', as was done above.

Finally the user can force continuation of the line by typing '\' as the last
non-space character of the line. This actually uses a different mechanism that
applies even before scanning starts: it removes the backslash, optional space
and the following newline, joining together the next line with this one. This
could even happen in the middle of a string denotation or of some another
token. Note that *does not mean* that backslash is used as an escape character
in axis: the rule applies if and only of a backslash it the last visible
character on the line, and at all other occurrences '\' is just an operator
symbol (used to compute the quotient in Euclidean division). The joined lines
are considered as one long line for all purposes such as error reporting
(the joined line will be echoed for readability of the error message), after
which the line number jumps to the true line number of the following line.

