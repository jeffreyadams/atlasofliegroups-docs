Cartan Subgroups
=================

When we give atlas a specific Lie group G, the software knows several
characteristics of the group. And depending on what you ask about G, atlas
will provide more information::

     atlas> G:=SL(2,R)
     Value: connected split real group with Lie algebra 'sl(2,R)'
     atlas>  H:=PSL(2,R)
     Value: disconnected split real group with Lie algebra 'sl(2,R)'
     atlas>

Recall that H=SO(2,1). Now, one of the main structural facts about a group is what its Cartan subgroups are. For that we can type the following sequence of commands::

     atlas> nr_of_Cartan_classes (G)
     Value: 2
     atlas> set cartans =Cartan_classes (G)
     Identifier cartans: [CartanClass] 
     atlas> #cartans
     Value: 2
     atlas> set T=cartans[0]
     Identifier T: CartanClass
     atlas>
     atlas> T
     Value: Cartan class #0, occurring for 2 real forms and for 1 dual real form
     atlas>
     atlas> print_Cartan_info (T)
     compact: 1, complex: 0, split: 0
     canonical twisted involution: e
     twisted involution orbit size: 1; fiber size: 2; strong inv: 2
     imaginary root system: A1
     real root system: empty
     complex factor: empty
     atlas>

Wich gives us the number of conjugacy classes of Cartan subgroups of G and choosing one of those subgroups atlas gives more information about the Cartan.

So this says that the first Cartan is is a real cartan subgroup, meaning a connected complex torus. It is defined over R. So, its real points form a real torus which can be written as a product of (S¹)^{a}, (C^{x})^{b} and (R^{x})^{c} factors. So, atlas gives the numbers (a,b,c). In this case the first Cartan is just a=1 circle, b=0 complex factors and c=0 real factors.

It also tells us the type of roots it has: imaginary, complex or real. Since the Cartan is compact, we only have imaginary roots. And these roots form a system of type A₁.

Note that we also see that this Cartan occurs in different real forms of complex groups of type A₁. The information about twisted involutions we will discuss later.

Now for information about the second Cartan subgroup::

    atlas> set A=cartans[1]
    Identifier A: CartanClass
    atlas> A
    Value: Cartan class #1, occurring for 1 real form and for 2 dual real forms
    atlas> print_Cartan_info (A)
    compact: 0, complex: 0, split: 1
    canonical twisted involution: 1
    twisted involution orbit size: 1; fiber size: 1; strong inv: 1
    imaginary root system: empty
    real root system: A1
    complex factor: empty
    atlas>

Here, the Cartan has just 1 copy of R^{x} and no complex or circle factors. And it just has real roots of type A₁.We will discuss later the information about involutions.

In contrast, the group SL(2,C) has only one conjugacy class of cartans::

   atlas> set G2=SL(2,C)
   Identifier G2: RealForm (hiding previous one of type string)
   atlas> nr_of_Cartan_classes (G2)
   Value: 1
   atlas> set cartans =Cartan_classes (G2)
   Identifier cartans: [CartanClass] (hiding previous one of type [CartanClass])
   atlas> cartans[0]
   Value: Cartan class #0, occurring for 1 real form and for 1 dual real form
   atlas>
   atlas> print_Cartan_info (cartans[0])
   compact: 0, complex: 1, split: 0
   canonical twisted involution: e
   twisted involution orbit size: 2; fiber size: 1; strong inv: 2
   imaginary root system: empty
   real root system: empty
   complex factor: A1

Now for a larger group like Sp(4,R), for example, we will have a
compact cartan which is a product of two circles and all its roots are compact; a split cartan, that
is, a product of R^{x}×R^{x} with all roots real; and two intermediate cartans; one complex
isomorphic to C^{x}.This is sometimes called the short root
Cartan. This is the one associated to a Levi factor Gl(2). finally,
the other Cartan is isomorphic to S¹×R^{x}. The distinction between
these two Cartans is subtle. Locally they are both isomorphic rank one
Cartans and look like S¹×R^{x}. But, one is C^{x} and atlas can
distinguish the two.

The root systems also transform accordingly::

    atlas> set G1=Sp(4,R)
    Identifier G1: RealForm
    atlas> G1
    Value: connected split real group with Lie algebra 'sp(4,R)'
    atlas> nr_of_Cartan_classes (G1)
    Value: 4
    atlas> set cartans =Cartan_classes (G1)
    Identifier cartans: [CartanClass] (hiding previous one of type [CartanClass])
    atlas>
    atlas> cartans[1]
    Value: Cartan class #1, occurring for 2 real forms and for 1 dual real form
    atlas> print_Cartan_info (cartans[1])
    compact: 0, complex: 1, split: 0
    canonical twisted involution: 2,1,2
    twisted involution orbit size: 2; fiber size: 1; strong inv: 2
    imaginary root system: A1
    real root system: A1
    complex factor: empty
    atlas>
    atlas> cartans[2]
    Value: Cartan class #2, occurring for 1 real form and for 2 dual real forms
    atlas> print_Cartan_info (cartans[2])
    compact: 1, complex: 0, split: 1
    canonical twisted involution: 1,2,1
    twisted involution orbit size: 2; fiber size: 2; strong inv: 4
    imaginary root system: A1
    real root system: A1
    complex factor: empty
    atlas>

