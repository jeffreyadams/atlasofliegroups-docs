Miscellaneous Commands
=======================

Some operations, including the type checker, can be made more verbose by
giving the command::

  atlas> set verbose

which remains in effect until a subsequent command::

  atlas> set quiet

is given.


One can ask the state of all known identifiers by typing::

  atlas> showall

which prints the type and value of every defined function and variable. If one
just needs to know the type of one expression, one can type::

  atlas> whattype expr

This performs type analysis of the expression and prints the result, but does
not evaluate anything. Overloaded function names by themselves are not a valid
expressions, so this form cannot be used to find out function overloading.
However by suffixing a question mark to the command, it will print the types
of all overloads of the given (function or operator) symbol::

  atlas> whattype + ?
  Overloaded instances of +
    (int,int)->int
    (rat,int)->rat
    (rat,rat)->rat
    (vec,vec)->vec
    (ratvec,ratvec)->ratvec
    (mat,int)->mat
    (int,mat)->mat
    (mat,mat)->mat
    (Split,Split)->Split
    (ParamPol,Param)->ParamPol
    (ParamPol,(Split,Param))->ParamPol
    (ParamPol,[(Split,Param)])->ParamPol
    (ParamPol,ParamPol)->ParamPol
    (string,string)->string
    (string,int)->string
    (int,string)->string
    (string,(int,int))->string
    Split->int

Finally when you get tired of using atlas, type::

  atlas> quit
  Bye.
