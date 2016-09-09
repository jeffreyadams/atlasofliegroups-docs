Recursion
===============

As mentioned above, axis strict scoping rules makes defining recursive
functions a bit more difficult than most programming languages do. It used to
be somewhat of an art to define a recursive function (it could, and can still,
be achieved by calling a function held in a variable to which the recursive
function itself is assigned), but starting with version 0.9 of axis there is
a keyword 'rec_fun' that make this automatic (at least for simple recursive
functions; complicated mutually recursive definitions still require some
effort). Basically take the function definition as one would write it if
recursion were directly allowed, and the insert 'rec_fun' before the recursive
name at its (function) definition. The only restriction is that the return
type must be explicitly specified (while it is option for ordinary functions);
failing to do so after rec_fun will result in a syntax error.

Here is the classical (but silly, as using a loop would do quite as well)
example of the factorial function 'fac'::

    atlas> set rec_fun fac (int n) = int: { return type int is specified }
      if n<=0 then 1 else n*fac(n-1) fi
    Defined fac: (int->int)
    atlas> fac(7)
    Value: 5040

However, in practice it is often better to achieve recursion locally rather
than directly for the function defined by 'set', as this will allow the latter
to do some preliminary things that are not to be repeated at each recursive
call. For instance if in the above definition one wants to signal negative
arguments as errors rather than returning the (mathematically meaningless)
value 1 for them, this can be done as follows (the example also shows that the
recursive function need not have the same name as the global one::

    atlas> set fac (int n) = { no return type needed here }
    if n<0 then error("factorial of negative number ",n," is not defined") fi;
    let rec_fun f(int n) = int: { return type required here }
                if n<=0 then 1 else n*f(n-1) fi
    in f(n)

Since the local function f is defined only to be immediately called, one can
even make the recursive function anonymous to the outside, as follows::

    atlas> set fac (int n) = { no return type needed here }
    if n<0 then error("factorial of negative number ",n," is not defined") fi;
    (rec_fun f(int n) = int: if n<=0 then 1 else n*f(n-1) fi) (n) { call it! }

Finally, one could avoid making a new (local) recursive function each time the
global function is called by postponing the introduction of its arguments;
this gives the following (optimal though maybe not optimally readable) style::

    atlas> set fac = { no arguments yet }
    let rec_fun f(int n) = int: if n<=0 then 1 else n*f(n-1) fi { build once }
    in { now comes that actual definition of fac, an anonymous function }
    (int n): { introduce argument of fac }
      if n<0 then error("factorial of negative number ",n," is not defined")
      else f(n) { call the recursive function }
      fi