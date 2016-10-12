.. _parabolics.at_ref:

parabolics.at Function References
=======================================================
|

.. _complex_parabolic_parabolic(s,x)->complexparabolic1:

complex_parabolic
-------------------------------------------------
| ``complex_parabolic:Parabolic(S,x)->ComplexParabolic`` Defined in line number 25.
| 
| The complex parabolic underlying P=(S,x)
| 

.. _complex_levi_rootdatum_rd,_(int->bool)_select->rootdatum1:

complex_Levi
-------------------------------------------------
| ``complex_Levi:RootDatum rd, (int->bool) select->RootDatum`` Defined in line number 28.
| 
| Auxiliary function
| 

.. _is_levi_theta_stable_parabolic_(s,x)->bool1:

is_Levi_theta_stable
-------------------------------------------------
| ``is_Levi_theta_stable:Parabolic (S,x)->bool`` Defined in line number 38.
| 
| Test if a complex Levi defined by a set of simple roots S is theta_x stable;   algorithm: H=sum of fundamental coweights with index not in S,   test whether <theta_x(alpha),H>=0 for all alpha in S
| 

.. _levi_parabolic(s,x):p->realform1:

Levi
-------------------------------------------------
| ``Levi:Parabolic(S,x):P->RealForm`` Defined in line number 50.
| 
| Make a real Levi factor from P=(S,x), the complex Levi of S must be theta_x-stable
| 

.. _is_parabolic_theta_stable_parabolic_(s,x):p->bool1:

is_parabolic_theta_stable
-------------------------------------------------
| ``is_parabolic_theta_stable:Parabolic (S,x):P->bool`` Defined in line number 60.
| 
| Test if parabolic P=(S,x) is theta-stable: <=>   1) the complex Levi factor L is theta-stable   2) the KGP element P is closed (see kgp.at)   3) alpha simple, not in S => alpha is imaginary or C+ wrt maximal(P)
| 

.. _is_parabolic_real_parabolic_(s,x):p->bool1:

is_parabolic_real
-------------------------------------------------
| ``is_parabolic_real:Parabolic (S,x):P->bool`` Defined in line number 73.
| 
| Test if parabolic P=(S,x) is real: <=>:   1) L is theta-stable   2) P is open   3) alpha simple, not in S => alpha is real or C- wrt a maximal element of P
| 

.. _rho_u_complexparabolic_p->ratvec1:

rho_u
-------------------------------------------------
| ``rho_u:ComplexParabolic P->ratvec`` Defined in line number 93.
| 
| Half sum of positive roots not in the Levi (L must be theta stable)
| 

.. _rho_u_parabolic_p->ratvec1:

rho_u
-------------------------------------------------
| ``rho_u:Parabolic P->ratvec`` Defined in line number 96.
| 
| Half sum of positive roots not in the Levi (L must be theta stable)
| 

.. _rho_l_parabolic_p->ratvec1:

rho_l
-------------------------------------------------
| ``rho_l:Parabolic P->ratvec`` Defined in line number 99.
| 
| Half sum of positive roots in the Levi (L must be theta stable)
| 

.. _nilrad_parabolic_p->mat1:

nilrad
-------------------------------------------------
| ``nilrad:Parabolic P->mat`` Defined in line number 102.
| 
| Positive coroots in the nilradical u of P (L must be theta stable)
| 

.. _nilrad_roots_parabolic_p->mat1:

nilrad_roots
-------------------------------------------------
| ``nilrad_roots:Parabolic P->mat`` Defined in line number 107.
| 
| Positive roots in the nilradical u of P (L must be theta stable)
| 

.. _zero_simple_coroots_rootdatum_rd,_vec_lambda->[int]1:

zero_simple_coroots
-------------------------------------------------
| ``zero_simple_coroots:RootDatum rd, vec lambda->[int]`` Defined in line number 120.
| 
| Simple coroots on which weight lambda (in \h^*) is zero
| 

.. _parabolic_ratvec_lambda,kgbelt_x->parabolic1:

parabolic
-------------------------------------------------
| ``parabolic:ratvec lambda,KGBElt x->Parabolic`` Defined in line number 126.
| 
| Parabolic defined by weight lambda
| 

.. _levi_ratvec_lambda,kgbelt_x->realform1:

Levi
-------------------------------------------------
| ``Levi:ratvec lambda,KGBElt x->RealForm`` Defined in line number 131.
| 
| Levi factor of parabolic defined by weight lambda
| 

.. _nilrad_ratvec_lambda,kgbelt_x->mat1:

nilrad
-------------------------------------------------
| ``nilrad:ratvec lambda,KGBElt x->mat`` Defined in line number 134.
| 
| Positive coroots in nilradical of P defined by lambda (if L theta stable)
| 

.. _nilrad_roots_ratvec_lambda,kgbelt_x->mat1:

nilrad_roots
-------------------------------------------------
| ``nilrad_roots:ratvec lambda,KGBElt x->mat`` Defined in line number 137.
| 
| Positive roots in nilradical of P defined by lambda (if L theta stable)
| 

.. _rho_u_ratvec_lambda,kgbelt_x->ratvec1:

rho_u
-------------------------------------------------
| ``rho_u:ratvec lambda,KGBElt x->ratvec`` Defined in line number 142.
| 
| Half sum of positive roots in nilradical of P defined by lambda (if L theta stable)
| 

.. _zero_simple_roots_rootdatum_rd,_vec_cowt->[int]1:

zero_simple_roots
-------------------------------------------------
| ``zero_simple_roots:RootDatum rd, vec cowt->[int]`` Defined in line number 145.
| 
| Simple roots which are zero on coweight H (in \h)
| 

.. _parabolic_alt_ratvec_h,kgbelt_x->parabolic1:

parabolic_alt
-------------------------------------------------
| ``parabolic_alt:ratvec H,KGBElt x->Parabolic`` Defined in line number 151.
| 
| Parabolic defined by coweight H
| 

.. _levi_alt_ratvec_h,kgbelt_x->realform1:

Levi_alt
-------------------------------------------------
| ``Levi_alt:ratvec H,KGBElt x->RealForm`` Defined in line number 156.
| 
| Levi factor of parabolic defined by coweight H
| 

.. _nilrad_alt_ratvec_h,kgbelt_x->mat1:

nilrad_alt
-------------------------------------------------
| ``nilrad_alt:ratvec H,KGBElt x->mat`` Defined in line number 159.
| 
| Positive coroots in nilradical of P defined by coweight H (if L theta stable)
| 

.. _nilrad_roots_alt_ratvec_h,kgbelt_x->mat1:

nilrad_roots_alt
-------------------------------------------------
| ``nilrad_roots_alt:ratvec H,KGBElt x->mat`` Defined in line number 162.
| 
| Positive roots in nilradical of P defined by coweight H (if L theta stable)
| 

.. _rho_u_alt_ratvec_h,kgbelt_x->ratvec1:

rho_u_alt
-------------------------------------------------
| ``rho_u_alt:ratvec H,KGBElt x->ratvec`` Defined in line number 166.
| 
| Half sum of roots in nilradical of P defined by H (if L theta stable)
| 

.. _rho_levi_alt_ratvec_h,kgbelt_x->ratvec1:

rho_Levi_alt
-------------------------------------------------
| ``rho_Levi_alt:ratvec H,KGBElt x->ratvec`` Defined in line number 169.
| 
| Rho(L) for Levi of P defined by H (if L theta stable
| 

.. _real_parabolic_kgbelt_x->parabolic1:

real_parabolic
-------------------------------------------------
| ``real_parabolic:KGBElt x->Parabolic`` Defined in line number 179.
| 
| Real_parabolic(x) has Levi factor M=centralizer(A)   u=positive roots not in M   for M to be stable: x must have no C+ roots   => real roots alpha are those satisfying <(1-theta_x)rho,\alpha^\vee>=0
| 

.. _theta_stable_parabolic_kgbelt_x->parabolic1:

theta_stable_parabolic
-------------------------------------------------
| ``theta_stable_parabolic:KGBElt x->Parabolic`` Defined in line number 189.
| 
| Theta_stable_parabolic(x) has Levi factor L=centralizer(T)   u=positive roots not in L   for this to be stable: no C- roots   => imaginary roots alpha are those satisfying <(1+theta_x)rho,\alpha^\vee>=0
| 

.. _real_levi_kgbelt_x->realform1:

real_Levi
-------------------------------------------------
| ``real_Levi:KGBElt x->RealForm`` Defined in line number 197.
| 
| Levi factor of real cuspidal parabolic;  M=centralizer of A in H=TA, as a RealForm
| 

.. _kgp_realform_g,complexparabolic_(rd,s)->[kgpelt]1:

KGP
-------------------------------------------------
| ``KGP:RealForm G,ComplexParabolic (rd,S)->[KGPElt]`` Defined in line number 253.
| 
| List of K-conjugacy classes of given ComplexParabolic (as KGP elts)
| 

.. _parabolics_realform_g,complexparabolic_(rd,s)->[parabolic]1:

parabolics
-------------------------------------------------
| ``parabolics:RealForm G,ComplexParabolic (rd,S)->[Parabolic]`` Defined in line number 257.
| 
| List K-conjugacy classes of given ComplesParabolic (as Parabolics)
| 

.. _theta_stable_parabolics_realform_g,complexparabolic_p->[parabolic]1:

theta_stable_parabolics
-------------------------------------------------
| ``theta_stable_parabolics:RealForm G,ComplexParabolic P->[Parabolic]`` Defined in line number 261.
| 
| List K-conjugacy classes of given ComplexParablic that are theta stable
| 

.. _theta_stable_parabolics_realform_g->[parabolic]1:

theta_stable_parabolics
-------------------------------------------------
| ``theta_stable_parabolics:RealForm G->[Parabolic]`` Defined in line number 267.
| 
| List all theta stable parabolics for G
| 

.. _theta_stable_parabolics_type_realform_g,[int]_p->[parabolic]1:

theta_stable_parabolics_type
-------------------------------------------------
| ``theta_stable_parabolics_type:RealForm G,[int] P->[Parabolic]`` Defined in line number 274.
| 
| List all theta stable parabolics of G, of type S
| 

.. _all_rel_split_theta_stable_parabolics_realform_g->[parabolic]1:

all_rel_split_theta_stable_parabolics
-------------------------------------------------
| ``all_rel_split_theta_stable_parabolics:RealForm G->[Parabolic]`` Defined in line number 280.
| 
| List all theta stable parabolics of G with relatively split L
| 

.. _print_theta_stable_parabolics_realform_g->void1:

print_theta_stable_parabolics
-------------------------------------------------
| ``print_theta_stable_parabolics:RealForm G->void`` Defined in line number 288.
| 
| For each theta stable parabolic of G, print S, Levi factor, and maximal x
| 

