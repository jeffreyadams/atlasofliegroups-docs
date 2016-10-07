.. _stable.at_index:

stable.at Function Index
=======================================================
|

.. list-table::
   :widths: 10 20
   :header-rows: 1

   * - Function
     - Argument(s) -> Results
   * - :ref:`evaluate_at_1_[vec]_v->vec1`
     - ``[vec] v->vec``
   * - :ref:`evaluate_at_1_poly_mat_m->mat1`
     - ``poly_mat M->mat``
   * - :ref:`left_kernel_mat_m->mat1`
     - ``mat M->mat``
   * - :ref:`column_[[vec]]_m,int_i->for_j1`
     - ``[[vec]] M,int i->for j``
   * - :ref:`null_poly_mat_int_r,int_c->poly_mat:for_j:r_do_for_i1`
     - ``int r,int c->poly_mat:for j:r do for i``
   * - :ref:`mat_as_poly_mat_mat_a->poly_mat1`
     - ``mat A->poly_mat``
   * - :ref:`has_infinitesimal_character_[param]_params->null_module(real_form(params[0]))_in_for_p_in_params_do_p+1`
     - ``[Param] params->null_module(real_form(params[0])) in for p in params do P+``
   * - :ref:`inverse_permutation_[int]_s->for_i1`
     - ``[int] S->for i``
   * - :ref:`permutation_matrix_[int]_s->null(#s,#s)_in_for_i:#s_do_rv[s[i],i]1`
     - ``[int] S->null(#S,#S) in for i:#S do rv[S[i],i]``
   * - :ref:`permutation_matrix_[int]_s,[int]_t->null(#s,#s)_in_for_i:#s_do_rv[find(t,s[i]),find(s,s[i])]1`
     - ``[int] S,[int] T->null(#S,#S) in for i:#S do rv[find(T,S[i]),find(S,S[i])]``
   * - :ref:`permutation_matrix_sort_[int]_s->mat1`
     - ``[int] S->mat``
   * - :ref:`in_tau_int_s,param_p->bool1`
     - ``int s,Param p->bool``
   * - :ref:`in_tau_[int]_s,param_p->bool:all(for_i1`
     - ``[int] S,Param p->bool:all(for i``
   * - :ref:`in_tau_[*]_s,param_p->bool:in_tau([int]1`
     - ``[*] S,Param p->bool:in_tau([int]``
   * - :ref:`in_tau_complement_int_s,param_p->bool1`
     - ``int s,Param p->bool``
   * - :ref:`in_tau_complement_[int]_s,param_p->bool:all(for_i1`
     - ``[int] S,Param p->bool:all(for i``
   * - :ref:`in_tau_complement_[*]_s,param_p->bool:in_tau_complement([int]1`
     - ``[*] S,Param p->bool:in_tau_complement([int]``
   * - :ref:`psi_[param]_params,[int]_s->[param]:[]_in_for_p_in_params_do_if_in_tau_complement(s,p)_then_rv#1`
     - ``[Param] params,[int] S->[Param]:[] in for p in params do if in_tau_complement(S,p) then rv#``
   * - :ref:`parameters_tau_containing_[int]_s,[param]_params->[int]1`
     - ``[int] S,[Param] params->[int]``
   * - :ref:`parameters_tau_containing_[*]_s,[param]_params->[int]:_parameters_tau_containing([int]1`
     - ``[*] S,[Param] params->[int]: parameters_tau_containing([int]``
   * - :ref:`parameters_tau_contained_in_complement_[int]_s,[param]_params->[int]1`
     - ``[int] S,[Param] params->[int]``
   * - :ref:`parameters_tau_contained_in_complement_[*]_s,[param]_params->[int]:_parameters_tau_contained_in_complement([int]1`
     - ``[*] S,[Param] params->[int]: parameters_tau_contained_in_complement([int]``
   * - :ref:`permutation_[param]_b->[int]1`
     - ``[Param] B->[int]``
   * - :ref:`dual_parameters_[int]_s,[param]_b->[int]1`
     - ``[int] S,[Param] B->[int]``
   * - :ref:`dual_parameters_[*]_s,[param]_b->[int]:dual_parameters([int]1`
     - ``[*] S,[Param] B->[int]:dual_parameters([int]``
   * - :ref:`parameters_[int]_s,[param]_b->[int]1`
     - ``[int] S,[Param] B->[int]``
   * - :ref:`parameters_[*]_s,[param]_b->parameters([int]1`
     - ``[*] S,[Param] B->parameters([int]``
   * - :ref:`parameters_singular_[int]_s,[param]_b->[param]1`
     - ``[int] S,[Param] B->[Param]``
   * - :ref:`parameters_singular_[*]_s,[param]_b->[param]:parameters_singular([int]1`
     - ``[*] S,[Param] B->[Param]:parameters_singular([int]``
   * - :ref:`lengths_signs_[param]_params->[int]1`
     - ``[Param] params->[int]``
   * - :ref:`lengths_signs_matrix_[param]_params->mat1`
     - ``[Param] params->mat``
   * - :ref:`lengths_signs_[int]_s,[param]_b->[int]1`
     - ``[int] S,[Param] B->[int]``
   * - :ref:`lengths_signs_[*]_s,[param]_b->[int]:_lengths_signs([int]1`
     - ``[*] S,[Param] B->[int]: lengths_signs([int]``
   * - :ref:`lengths_signs_matrix_[int]_s,[param]_b->mat1`
     - ``[int] S,[Param] B->mat``
   * - :ref:`lengths_signs_matrix_[*]_s,[param]_b->mat:_lengths_signs_matrix([int]1`
     - ``[*] S,[Param] B->mat: lengths_signs_matrix([int]``
   * - :ref:`dual_parameters_matrix_[int]_s,[param]_b->mat1`
     - ``[int] S,[Param] B->mat``
   * - :ref:`dual_parameters_matrix_[*]_s,[param]_b->mat:dual_parameters_matrix([int]1`
     - ``[*] S,[Param] B->mat:dual_parameters_matrix([int]``
   * - :ref:`dual_parameters_matrix_[param]_b->mat1`
     - ``[Param] B->mat``
   * - :ref:`dual_parameters_matrix_[param]_b,_[int]_t->mat1`
     - ``[Param] B, [int] T->mat``
   * - :ref:`dual_parameters_standard_basis_poly_mat_[param]_b->poly_mat1`
     - ``[Param] B->poly_mat``
   * - :ref:`dual_parameters_standard_basis_[param]_b->mat1`
     - ``[Param] B->mat``
   * - :ref:`dual_parameters_standard_basis_[int]_s,[param]_b->mat1`
     - ``[int] S,[Param] B->mat``
   * - :ref:`dual_parameters_standard_basis_[*]_s,[param]_b->mat:dual_parameters_standard_basis([int]1`
     - ``[*] S,[Param] B->mat:dual_parameters_standard_basis([int]``
   * - :ref:`get_y_[param]_b->[int]1`
     - ``[Param] B->[int]``
   * - :ref:`vanishing_[int]_s,[param]_b->mat1`
     - ``[int] S,[Param] B->mat``
   * - :ref:`vanishing_[*]_s,[param]_b->vanishing([int]1`
     - ``[*] S,[Param] B->vanishing([int]``
   * - :ref:`kernel_vanishing_[int]_s,[param]_b->mat1`
     - ``[int] S,[Param] B->mat``
   * - :ref:`kernel_vanishing_[*]_s,[param]_b->mat:kernel_vanishing([int]1`
     - ``[*] S,[Param] B->mat:kernel_vanishing([int]``
   * - :ref:`stable_at_singular_unsorted_[int]_s,[param]_b->(mat,[param])1`
     - ``[int] S,[Param] B->(mat,[Param])``
   * - :ref:`stable_at_singular_unsorted_[*]_s,[param]_b->(mat,[param]):stable_at_singular_unsorted([int]1`
     - ``[*] S,[Param] B->(mat,[Param]):stable_at_singular_unsorted([int]``
   * - :ref:`stable_at_singular_[int]_s,[param]_b->(mat,[param])1`
     - ``[int] S,[Param] B->(mat,[Param])``
   * - :ref:`stable_at_singular_[*]_s,[param]_b->(mat,[param]):stable_at_singular([int]1`
     - ``[*] S,[Param] B->(mat,[Param]):stable_at_singular([int]``
   * - :ref:`print_stable_at_singular_unsorted_[int]_s,[param]_b->void1`
     - ``[int] S,[Param] B->void``
   * - :ref:`print_stable_at_singular_unsorted_[*]_s,[param]_b->void:print_stable_at_singular_unsorted([int]1`
     - ``[*] S,[Param] B->void:print_stable_at_singular_unsorted([int]``
   * - :ref:`print_stable_at_singular_[int]_s,[param]_b->void1`
     - ``[int] S,[Param] B->void``
   * - :ref:`print_stable_at_singular_[*]_s,[param]_b->void:print_stable_at_singular([int]1`
     - ``[*] S,[Param] B->void:print_stable_at_singular([int]``
   * - :ref:`subspace_injection_matrix_[param]_b,[param]_subset->mat1`
     - ``[Param] B,[Param] subset->mat``
   * - :ref:`stable_at_singular_[int]_s,[param]_b,[param]_subset_in->(mat,[param])1`
     - ``[int] S,[Param] B,[Param] subset_in->(mat,[Param])``
   * - :ref:`stable_at_singular_[*]_s,[param]_b,[param]_subset->(mat,[param]):stable_at_singular([int]1`
     - ``[*] S,[Param] B,[Param] subset->(mat,[Param]):stable_at_singular([int]``
   * - :ref:`print_stable_at_singular_[int]_s,[param]_b,[param]_subset->void1`
     - ``[int] S,[Param] B,[Param] subset->void``
   * - :ref:`print_stable_at_singular_[*]_s,[param]_b,[param]_subset->void:print_stable_at_singular([int]1`
     - ``[*] S,[Param] B,[Param] subset->void:print_stable_at_singular([int]``
   * - :ref:`stable_[param]_params->(mat,[param])1`
     - ``[Param] params->(mat,[Param])``
   * - :ref:`print_stable_[param]_params->void1`
     - ``[Param] params->void``
   * - :ref:`stable_test_aq_packet_realform_g,[int]_complex_parabolic->stable_test_aq_packet(g,complexparabolic1`
     - ``RealForm G,[int] complex_parabolic->stable_test_Aq_packet(G,ComplexParabolic``
   * - :ref:`stable_test_aq_packet_realform_g,[*]_complex_parabolic->stable_test_aq_packet(g,[int]1`
     - ``RealForm G,[*] complex_parabolic->stable_test_Aq_packet(G,[int]``
