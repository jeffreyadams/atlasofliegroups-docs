:math:`K\backslash G/B` for other Cartan subgroups
===================================================

Let us look at :math:`G=Sp(4,R)`. The :math:`K\backslash G/B` elements are::

   atlas> G
   Value: connected split real group with Lie algebra 'sp(4,R)'
   atlas> print_KGB (G)
   kgbsize: 11
   Base grading: [11].
    0:  0  [n,n]    1   2     4   5  (0,0)#0 e
    1:  0  [n,n]    0   3     4   6  (1,1)#0 e
    2:  0  [c,n]    2   0     *   5  (0,1)#0 e
    3:  0  [c,n]    3   1     *   6  (1,0)#0 e
    4:  1  [r,C]    4   9     *   *  (0,0) 1 1^e
    5:  1  [C,r]    7   5     *   *  (0,0) 2 2^e
    6:  1  [C,r]    8   6     *   *  (1,0) 2 2^e
    7:  2  [C,n]    5   8     *  10  (0,0)#2 1x2^e
    8:  2  [C,n]    6   7     *  10  (0,1)#2 1x2^e
    9:  2  [n,C]    9   4    10   *  (0,0)#1 2x1^e
   10:  3  [r,r]   10  10     *   *  (0,0)#3 1^2x1^e
   atlas> 

Recall that the first four form the fundamental fiber that go to the
Cartan subgroup ``0``, the compact one. Elements ``5`` through ``8``
are attached to Cartan subgroup number ``2``, etc. The last collumn
tells us that the fiber attached to the involution ``2^e`` consists of
elements 5 and 6 and the fiber corresponding to the element ``1x2^e``
are elements ``7`` and ``8``.  Here ``2^e`` is just Cayley transform by
:math:`{\alpha}_2`, whereas ``1x2^e`` corresponds to conjugation by :math:`{\alpha}_1` composed with the Cayley transform by :math:`{\alpha}_2`.

Let us recall which Cartan subgroups and Weyl groups correspond to each fiber::

   atlas> set H=Cartan_class(G,0)
   Variable H: CartanClass (overriding previous instance, which had type string (constant))
   atlas> print_Cartan_info (H)
   compact: 2, complex: 0, split: 0
   canonical twisted involution: e
   twisted involution orbit size: 1; fiber size: 4; strong inv: 4
   imaginary root system: C2
   real root system: empty
   complex factor: empty
   atlas>

As we know this is the Compact Cartan subgroup associated to the distinguished fiber::

   atlas> print_real_Weyl (G,H)
   real weyl group is W^C.((A.W_ic) x W^R), where:
      W^C is trivial
      A is trivial
      W_ic is a Weyl group of type A1
      W^R is trivial
      
      generators for W_ic:
      2,1,2
      atlas> 

This is a Weyl group of type ``A1``. So, the number of ``KGB`` orbits for this Cartan is ``8/4=2``

Now for one of the intermediate Cartan subgroups we have::

   atlas> H:=Cartan_class(G,1)
   Value: Cartan class #1, occurring for 2 real forms and for 1 dual real form
   atlas>
   atlas> print_Cartan_info (H)
   compact: 0, complex: 1, split: 0
   canonical twisted involution: 2,1,2
   twisted involution orbit size: 2; fiber size: 1; strong inv: 2
   imaginary root system: A1
   real root system: A1
   complex factor: empty
   atlas>

   atlas> print_real_Weyl (G,H)
   real weyl group is W^C.((A.W_ic) x W^R), where:
   W^C is trivial
   A is an elementary abelian 2-group of rank 1
   W_ic is trivial
   W^R is a Weyl group of type A1
   
   generators for A
   1
   generators for W^R:
   2,1,2
   atlas>

This is a copy of :math:`{\mathbb C}^\times` with Weyl group of order
``4``. So the number of ``KGB`` orbits is ``8/4=2``

Let us see what the :math:`W`-orbit of one element is, say::

   atlas> set x=KGB(G,4)
   Variable x: KGBElt
   atlas> void: for w in W do prints(cross(w,x)) od
   KGB element #4
   KGB element #4
   KGB element #9
   KGB element #9
   KGB element #9
   KGB element #9
   KGB element #4
   KGB element #4
   atlas>

Starting with element ``4`` the order of its stabilizer has four elements. And if we list all the elements of :math:`W`::

   atlas> void: for (,w) in W do prints(w) od
   []
   [0]
   [1]
   [1,0]
   [0,1]
   [0,1,0]
   [1,0,1]
   [1,0,1,0]
   atlas>

We see that the elements ``[], [0], [1,0,1], and [1,0,1,0]`` all
stabilize element ``4``. So the order of the stabilizer is ``4``. Similarly, for element ``9``. 

Now for the next Cartan subgroup::

   atlas> H:=Cartan_class(G,2)
   Value: Cartan class #2, occurring for 1 real form and for 2 dual real forms
      atlas> 
      atlas> print_Cartan_info (H)
      compact: 1, complex: 0, split: 1
      canonical twisted involution: 1,2,1
      twisted involution orbit size: 2; fiber size: 2; strong inv: 4
      imaginary root system: A1
      real root system: A1
      complex factor: empty
      atlas> 

This subgroup has order four. And its real Weyl group has order ``2``::

      atlas> print_real_Weyl (G,H)
      real weyl group is W^C.((A.W_ic) x W^R), where:
      W^C is trivial
      A is trivial
      W_ic is trivial
      W^R is a Weyl group of type A1
      
      generators for W^R:
      1,2,1
      atlas> 

Then the number of ``KGB`` orbits is ``8/2=4`` and we can verify also that each stabilizer is order 2::

   atlas> x:=KGB(G,5)
   Variable x: KGBElt
   atlas> 
   atlas> void: for w in W do prints(cross(w,x)) od
   KGB element #5
   KGB element #7
   KGB element #5
   KGB element #8
   KGB element #7
   KGB element #6
   KGB element #8
   KGB element #6
   atlas>      
   atlas> void: for (,w) in W do prints(w) od
   []
   [0]
   [1]
   [1,0]
   [0,1]
   [0,1,0]
   [1,0,1]
   [1,0,1,0]
   atlas>

Now for completeness, let us look at the split Cartan subgroup::

   atlas> H:=Cartan_class(G,3)
   Value: Cartan class #3, occurring for 1 real form and for 3 dual real forms
   atlas> 
   atlas> print_Cartan_info (H)
   compact: 0, complex: 0, split: 2
   canonical twisted involution: 2,1,2,1
   twisted involution orbit size: 1; fiber size: 1; strong inv: 1
   imaginary root system: empty
   real root system: C2
   complex factor: empty
   atlas> 
   atlas> print_real_Weyl (G,H)
   real weyl group is W^C.((A.W_ic) x W^R), where:
   W^C is trivial
   A is trivial
   W_ic is trivial
   W^R is a Weyl group of type B2
   
   generators for W^R:
   1
   2

A Cartan Subgroup isomorphic to :math:`{\mathbb C}^\times \times {\mathbb C}^\times` and Weylgroup of type ``B2``. So the number of ``KGB`` orbits is ``8/8=1``::

   atlas> set x=KGB(G,10)
   Variable x: KGBElt (overriding previous instance, which had type KGBElt)
   atlas>  x:=KGB(G,10)
   Value: KGB element #10
   atlas> 

   atlas> void: for w in W do prints(cross(w,x)) od
   KGB element #10
   KGB element #10
   KGB element #10
   KGB element #10
   KGB element #10
   KGB element #10
   KGB element #10
   KGB element #10
   atlas> 

This concludes this deiscussion on :math:`K\backslash G/B` orbits. In
the next chapter we will discuss the representations associated to the
intermediate Cartan subgroups. The parameter includes a discrete
series of a Levi factor of a parabolic subgroup. So, to some extent it
reduces to the case of discrete series.

The idea is to look at the cuspidal data of an arbitrary parameter which gives a Levi factor :math:`M` and then applying what we learned about discrete series of M. 