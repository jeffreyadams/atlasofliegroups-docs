.. _extended.at_index:

extended.at Function Index
=======================================================
|



Functions

.. list-table::
   :widths: 10 20
   :header-rows: 1

   * - Function
     - Argument(s) -> Results
   * - :ref:`assert_bool_b,_(->string)_mess->void1`
     - ``bool b, (->string) mess->void``
   * - :ref:`e_mat_delta,_kgbelt_x,_ratvec_gamma,_ratvec_g,_ratvec_lambda->extparam1`
     - ``mat delta, KGBElt x, ratvec gamma, ratvec g, ratvec lambda->ExtParam``
   * - :ref:`e_mat_delta,_ratvec_gamma,_kgbelt_x,_ratvec_g,_kgbelt_gen_y->extparam1`
     - ``mat delta, ratvec gamma, KGBElt x, ratvec g, KGBElt_gen y->ExtParam``
   * - :ref:`e_mat_delta,_param_p,_ratvec_g->extparam1`
     - ``mat delta, Param p, ratvec g->ExtParam``
   * - :ref:`e_mat_delta,_param_p->extparam1`
     - ``mat delta, Param p->ExtParam``
   * - :ref:`e_mat_delta->(param->extparam):_(param_p)1`
     - ``mat delta->(Param->ExtParam): (Param p)``
   * - :ref:`torus_factor_extparam_e->ratvec1`
     - ``ExtParam E->ratvec``
   * - :ref:`dual_torus_factor_extparam_e->ratvec1`
     - ``ExtParam E->ratvec``
   * - :ref:`nu_extparam_e->ratvec1`
     - ``ExtParam E->ratvec``
   * - :ref:`length_extparam_e->int1`
     - ``ExtParam E->int``
   * - :ref:`sign_extparam(ic1,delta1,gamma1,lambda1,theta1,g1,l1,omega1,tau1,t1):e1,extparam(ic2,delta2,gamma2,lambda2,theta2,g2,l2,omega2,tau2,t2):e2->int1`
     - ``ExtParam(ic1,delta1,gamma1,lambda1,theta1,g1,l1,omega1,tau1,t1):E1,ExtParam(ic2,delta2,gamma2,lambda2,theta2,g2,l2,omega2,tau2,t2):E2->int``
   * - :ref:`sign_verbose_extparam(ic1,delta1,gamma1,lambda1,theta1,g1,l1,omega1,tau1,t1):e1,extparam(ic2,delta2,gamma2,lambda2,theta2,g2,l2,omega2,tau2,t2):e2->int1`
     - ``ExtParam(ic1,delta1,gamma1,lambda1,theta1,g1,l1,omega1,tau1,t1):E1,ExtParam(ic2,delta2,gamma2,lambda2,theta2,g2,l2,omega2,tau2,t2):E2->int``
   * - :ref:`dual_sign_extparam(ic1,delta1,gamma1,lambda1,theta1,g1,l1,omega1,tau1,t1):e1,extparam(ic2,delta2,gamma2,lambda2,theta2,g2,l2,omega2,tau2,t2):e2->int1`
     - ``ExtParam(ic1,delta1,gamma1,lambda1,theta1,g1,l1,omega1,tau1,t1):E1,ExtParam(ic2,delta2,gamma2,lambda2,theta2,g2,l2,omega2,tau2,t2):E2->int``
   * - :ref:`sign_extparam_e,(extparam_f1,extparam_f2)->int1`
     - ``ExtParam E,(ExtParam F1,ExtParam F2)->int``
   * - :ref:`sign_(extparam_e1,extparam_e2),extparam_f->int1`
     - ``(ExtParam E1,ExtParam E2),ExtParam F->int``
   * - :ref:`default_extparam_f->extparam1`
     - ``ExtParam F->ExtParam``
   * - :ref:`sign_extparam_e->int1`
     - ``ExtParam E->int``
   * - :ref:`dual_sign_extparam_e->int1`
     - ``ExtParam E->int``
   * - :ref:`\=_ExtParam_E,_ExtParam_F->bool1`
     - ``ExtParam E, ExtParam F->bool``
   * - :ref:`is_default_extparam_e->bool1`
     - ``ExtParam E->bool``
   * - :ref:`z_extparam_e->rat1`
     - ``ExtParam E->rat``
   * - :ref:`z_quot_extparam_e,_extparam_f->int1`
     - ``ExtParam E, ExtParam F->int``
   * - :ref:`ext_print_block_mat_delta,_[param]_b->void1`
     - ``mat delta, [Param] B->void``
   * - :ref:`ext_print_block_mat_delta,param_p->void1`
     - ``mat delta,Param p->void``
   * - :ref:`ext_print_block_param_p->void1`
     - ``Param p->void``
   * - :ref:`ext_block_of_mat_delta,_param_p,_ratvec_g->[extparam]1`
     - ``mat delta, Param p, ratvec g->[ExtParam]``
   * - :ref:`ext_block_of_mat_delta,_param_p->[extparam]1`
     - ``mat delta, Param p->[ExtParam]``
   * - :ref:`ext_block_of_param_p->[extparam]1`
     - ``Param p->[ExtParam]``
   * - :ref:`ext_block_mat_delta,_param_p,_ratvec_g->([extparam],int)1`
     - ``mat delta, Param p, ratvec g->([ExtParam],int)``
   * - :ref:`ext_block_mat_delta,_param_p->([extparam],int)1`
     - ``mat delta, Param p->([ExtParam],int)``
   * - :ref:`ext_block_param_p->([extparam],int)1`
     - ``Param p->([ExtParam],int)``
   * - :ref:`sign_find_[extparam]_list,extparam_e->(int,int)1`
     - ``[ExtParam] list,ExtParam E->(int,int)``
   * - :ref:`sign_find_extparam_e,[extparam]_list->(int,int)1`
     - ``ExtParam E,[ExtParam] list->(int,int)``
   * - :ref:`find_[extparam]_list,extparam_e->int1`
     - ``[ExtParam] list,ExtParam E->int``
   * - :ref:`find_extparam_e,[extparam]_list->int1`
     - ``ExtParam E,[ExtParam] list->int``
   * - :ref:`ext_basic_realform_g->(mat,[param],ratvec)1`
     - ``RealForm G->(mat,[Param],ratvec)``
   * - :ref:`folded_bracket_rootdatum_rd,_mat_delta,_int_i,_int_j->int1`
     - ``RootDatum rd, mat delta, int i, int j->int``
   * - :ref:`folded_m_rootdatum_rd,_mat_delta,_int_i,_int_j->int1`
     - ``RootDatum rd, mat delta, int i, int j->int``
   * - :ref:`folded_order_rootdatum_rd,_mat_delta,_int_i,_int_j->int1`
     - ``RootDatum rd, mat delta, int i, int j->int``
