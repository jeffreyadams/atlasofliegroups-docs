The Character Differential
===========================

To talk about the differential of a character let us use the example of a complex torus::

   atlas> set H=torus(0,1,0)
   Identifier H: RealForm (hiding previous one of type string (constant))

If we have a parameter ``p`` we can extract the coordinates of the parameter when needed::

   atlas> set p=trivial(H) 
   Identifier p: Param 
   atlas> p 
   Value: final parameter (x=0,lambda=[0,0]/1,nu=[0,0]/1) 
   atlas> x(p) 
   Value: KGB element #0 
   atlas> lambda(p) 
   Value: [ 0, 0 ]/1 
   atlas> nu(p) 
   Value: [0, 0 ]/1 
   atlas> 

And remember that for now, the important piece of information about
``x`` is th\ e Cartan involution of this Cartan::

   atlas> involution (x)
   Value: 
   | 0, 1 |
   | 1, 0 |

Now, when we have a parameter ``p``, we can ask for its infinitesimal character. The answer is of course more interesting for a non-trivial character::

    atlas> infinitesimal_character (p)
    Value: [ 0, 0 ]/1
    atlas>
    atlas> set q=parameter(x,[1,0],[2,-2])
    Identifier q: Param (hiding previous one of type Param)
    atlas> q
    Value: final parameter (x=0,lambda=[1,0]/1,nu=[2,-2]/1)
    atlas> infinitesimal_character (q)
    Value: [  5, -3 ]/2
    atlas> 

If we have ``q=(x lambda, nu)`` the differential of this character is
the infinitesimal character which equals $(1+ \theta )/2 *\lambda +(1-
\theta )/2* \nu$. But ``nu`` is already averaged so this equals
$(1+ \theta)/2 *\lambda + \nu$::

	atlas> infinitesimal_character (q)
	Value: [  5, -3 ]/2
	atlas> (1+theta)*lambda(q)/2
	Value: [ 1, 1 ]/2
	atlas> (1+theta)*lambda(q)/2+nu(q)
	Value: [  5, -3 ]/2
	atlas>

It is less information than ``lambda`` and ``nu``. This is because
$(1+ \theta )/2$ looses some of it.


