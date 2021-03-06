Principal Series and Discrete Series revisited
===============================================

Let us review some basic examples ::

   atlas> set G=SL(2,R)
   Variable G: RealForm
   atlas> p=trivial(G)
   atlas> set p=trivial(G)
   Variable p: Param
   atlas> p
   Value: final parameter(x=2,lambda=[1]/1,nu=[1]/1)
   atlas> set x=x(p)
   Variable x: KGBElt
   atlas> involution (x)
   Value: 
   | -1 |

So the Cartan involution acts by ``-1`` which means the Cartan subgroup is split. This is a minimal spherical principal series with infinitesimal character ``rho``.

   atlas> infinitesimal_character (p)
   Value: [ 1 ]/1
   atlas> rho(G)
   Value: [ 1 ]/1
   atlas>

This is the minimal principal series containing the trivial representation as unique irreducible quotient.

On the other end we also talked about the discrete series ::

   atlas> whattype discrete_series ?
   Overloaded instances of 'discrete_series'
     (KGBElt,ratvec)->Param
       (RealForm,ratvec)->Param
   atlas> set q=discrete_series (KGB (G,0), rho(G))
   Variable q: Param
   atlas> q
   Value: final parameter(x=0,lambda=[1]/1,nu=[0]/1)
   atlas> 

To find more representations we look at the block of the trivial representation to find other representations of this group ::

   atlas> print_block (p)
   Parameter defines element 2 of the following block:
   0:  0  [i1]  1   (2,*)  *(x=0,lam_rho= [0], nu= [0]/1)  e
   1:  0  [i1]  0   (2,*)  *(x=1,lam_rho= [0], nu= [0]/1)  e
   2:  1  [r1]  2   (0,1)  *(x=2,lam_rho= [0], nu= [1]/1)  1^e
   atlas> 

Here the trivial representation is #2 and the other two are discrete series ::

   atlas> set r=discrete_series (KGB(G,1), rho(G))
   Variable r: Param
   atlas> r
   Value: final parameter(x=1,lambda=[1]/1,nu=[0]/1)
   atlas> set x_b=KGB(G,0)
   Variable x_b: KGBElt
   atlas> hc_parameter (q,x_b)
   Value: [ 1 ]/1
   atlas> 
   atlas> hc_parameter (r,x_b)
   Value: [ -1 ]/1
   atlas> 

So, the Harish-Chandra parameter of ``q`` is ``1`` and that of ``r`` is ``-1``; the holomorphic and antiholomorphic one respectively.

But, recall there is another representation with infinitesimal character ``rho`` which is not in the trivial block ::

   atlas> set params=all_parameters_gamma (G, rho(G))
   Variable params: [Param] (overriding previous instance, which had type [Param])
   atlas> void: for p in params do prints(p) od
   final parameter(x=2,lambda=[1]/1,nu=[1]/1)
   final parameter(x=2,lambda=[2]/1,nu=[1]/1)
   final parameter(x=1,lambda=[1]/1,nu=[0]/1)
   final parameter(x=0,lambda=[1]/1,nu=[0]/1)
   atlas>

And recall that the second representation in this list corresponds to the irreducible non-spherical principal series of :math:`SL(2,R)` ::

   atlas> print_block (params[1]) 
   Parameter defines element 0 of the following block:
   0:  0  [rn]  0   (*,*)  *(x=2,lam_rho= [1], nu= [1]/1)  1^e
   atlas>

So, this representation is a singleton block. 

In any case, other than principal series or discrete series, there is
nothing else for this group at fixed infinitesimal character.


Now let us look at another group ::

   atlas> G:=PGL(2,R)
   Value: disconnected split real group with Lie algebra 'sl(2,R)'
   atlas> set p=trivial(G)
   Variable p: Param (overriding previous instance, which had type Param)
   atlas> print_block (p)
   Parameter defines element 1 of the following block:
   0:  0  [i2]  0   (1,2)  *(x=0,lam_rho= [0], nu= [0]/1)  e
   1:  1  [r2]  2   (0,*)  *(x=1,lam_rho= [0], nu= [1]/2)  1^e
   2:  1  [r2]  1   (0,*)  *(x=1,lam_rho= [1], nu= [1]/2)  1^e

In this case we only have one discrete series, namely number ``0``; and the others are minimal principal series ::

   atlas> set q=discrete_series (KGB(G,0), rho(G))
   Variable q: Param (overriding previous instance, which had type Param)
   atlas> q
   Value: final parameter(x=0,lambda=[1]/2,nu=[0]/1)
   atlas>  rho(G)
   Value: [ 1 ]/2
   atlas> 
   atlas> hc_parameter(q)
   Value: [ 1 ]/2
   atlas> 

Note that :math:`\rho=1/2` in this case. So :math:`X^* +\rho \cong \mathbb Z +1/2` 

Also there are only two KGB elements in this group ::

   atlas> print_KGB(G)
   kgbsize: 2
   Base grading: [1].
   0:  0  [n]   0    1  (0)#0 e
   1:  1  [r]   1    *  (0)#1 1^e
   atlas> 

So there is only one :math:`KGB` element to use for the compact Cartan subgroup and this means we only have one discrete series.

Equivalently, note that the simple reflection :math:`s_\alpha` is in
the Weyl group of :math:`K`, which is disconnected in this case. So :math:`s_\alpha` flips the positive and negative :math:`K` types.

On the other hand, we have two principal series in this block
associated to the ``KGB`` element ``x=1``. They both have
infinitesimal character ``rho``. But they differ in the disconnectedness of :math:`G`.

Now to know about more representations we look at other blocks ::

   atlas> block_sizes (G)
   Value: 
   | 0, 1 |
   | 1, 3 |
   
   atlas> 

This says that we have three representations for
:math:`PGL(2,R)` at infinitesimal character ``rho`` and we have one
extra at a different infinitesimal character.

More on the ``block_sizes`` command later.