Output, Input, and Redirection
================================

Executing commands can produce output (other than error messages) in two ways:
they can yield a value, which is then printed preceded by "Value:", and they
can themselves invoke printing actions. Functions whose purpose is to print
specific output (like tables) generally do not return a useful value (by
convention the names to such functions start with "print"). Whatever is the
manner in which output it produced, the user may decide to write the result to
a file rather than to the terminal. To that end it suffices to prefix the
command line (which must be an expression, not a 'set' definition) with ">" or
with ">>" followed by a file name (which is taken to be delimited by white
space; alternatively the file name may be enclosed in double quotes, in which
case it can contain spaces); all terminal output will be redirected to that
file for the duration of the command. In case of ">" a new file will be
created, in case of ">>" the output is appended to an existing file. For
instance::

    atlas> > output_file block_sizes(ic)
    atlas> >>output_file print_KGB(real_form(ic,2))
    atlas> >>output_file print_KL_list(real_form(ic,2),dual_quasisplit_form(ic))
    
    
will produce in the current directory the file 'output_file' with the results
of the indicated calls to block_sizes', 'print_KGB', and 'print_KL_list'.

One can also redirect command input from a file. Simply type::

    atlas> <filename

on a line by itself to execute the contents of 'filename' as a series of
commands. The output (responses to definitions, and values of expression
commands, but not any prompts) still goes to the terminal (unless the file
contains lines that themselves start with '>'); in addition messages are
printed indicating the start and end of reading from that file, so that the
user can track what source the commands producing the output (or an error) are
coming from. Files being read like this can themselves open other input files.
To keep track of this nesting, some indentation is added to normal command
output for every level of input currently active. If the file name used for
input is unknown (as searched from the current working directory), an
alternative file name formed by adding the '.at' suffix is tried (unless the
given file name already contained that suffix), and if still nothing is found
an error is reported. Any error will close all currently active input files.

Once a file is successfully input, axis remembers its file name and
suppresses subsequent attempts to read that file as input. This is so that
scripts can freely start by including other scripts whose definitions they
depend on, without having multiple dependencies on the same script result in
it being executed many times. The user can circumvent this check by writing::

    atlas> <<filename

in which case the file will be read as input, even if it had been before. This
can be useful if the file has been edited since it was last read in. Note
however that in case input of a file is terminated by an error (either from
one of its commands or from a file included by it) then the file is not yet
recorded as having been read, so a single '<' then suffices to reread it.
Realex will refuse to open a file currently already being read from, to prevent
infinite input loops in case of circular dependencies.

These input commands will search for their files in the directories specified
by the special system variable 'input_path' which is of type '[string]' (a
row of strings). This variable can be assigned to from the atlas program, but
is usually given its (initial) value through command line arguments to the
atlas program of the form '--path=file_name'

In spite of similar syntax, output and input redirection have rather different
characteristics. Output redirection only applies to a single expression
evaluation. Input redirection should not be followed by anything on the same
line, but it can invoke any number of commands from the given file. It can
even be used recursively to include commands from other files that are needed
to process the included file, it that file contains lines that start with '<'.
One cannot globally redirect the output produced from the commands of an
included file. If a command read from a file included at any level produces a
syntax or runtime error, a message reporting the place of the error is
printed, all included files are abandoned (since with some command failing, it
is usually pointless to continue); then control is given back to the terminal.

