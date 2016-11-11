.. _basic.at_index:

basic.at Function Index
=======================================================
|



Functions

.. list-table::
   :widths: 10 20
   :header-rows: 1

   * - Function
     - Argument(s) -> Results
   * - :ref:`\#_int_n->[int]:_for_i1`
     - ``int n->[int]: for i``
   * - :ref:`\#_bool_b->int1`
     - ``bool b->int``
   * - :ref:`assert_bool_b,string_message->void1`
     - ``bool b,string message->void``
   * - :ref:`assert_bool_b->void1`
     - ``bool b->void``
   * - :ref:`list_(int->bool)_filter,_int_limit->[int]1`
     - ``(int->bool) filter, int limit->[int]``
   * - :ref:`complement_(int->bool)_filter,_int_limit->[int]1`
     - ``(int->bool) filter, int limit->[int]``
   * - :ref:`count_(int->bool)_filter,_int_limit->int1`
     - ``(int->bool) filter, int limit->int``
   * - :ref:`all_[bool]_p->bool1`
     - ``[bool] p->bool``
   * - :ref:`none_[bool]_p->bool1`
     - ``[bool] p->bool``
   * - :ref:`first_[bool]_p->int1`
     - ``[bool] p->int``
   * - :ref:`last_[bool]_p->int1`
     - ``[bool] p->int``
   * - :ref:`all_int_limit,(int->bool)_filter->bool1`
     - ``int limit,(int->bool) filter->bool``
   * - :ref:`none_int_limit,(int->bool)_filter->bool1`
     - ``int limit,(int->bool) filter->bool``
   * - :ref:`first_int_limit,(int->bool)_filter->int1`
     - ``int limit,(int->bool) filter->int``
   * - :ref:`last_int_limit,(int->bool)_filter->int1`
     - ``int limit,(int->bool) filter->int``
   * - :ref:`all_[(->bool)]_p->bool1`
     - ``[(->bool)] p->bool``
   * - :ref:`none_[(->bool)]_p->bool1`
     - ``[(->bool)] p->bool``
   * - :ref:`first_[(->bool)]_p->int1`
     - ``[(->bool)] p->int``
   * - :ref:`last_[(->bool)]_p->int1`
     - ``[(->bool)] p->int``
   * - :ref:`binary_search_first_(int->bool)pred,_int_low,_int_high->int1`
     - ``(int->bool)pred, int low, int high->int``
   * - :ref:`from_stops_[int]_stops->(int->int)1`
     - ``[int] stops->(int->int)``
   * - :ref:`abs_int_k->int1`
     - ``int k->int``
   * - :ref:`sign_int_k->int1`
     - ``int k->int``
   * - :ref:`is_odd_int_n->bool1`
     - ``int n->bool``
   * - :ref:`is_even_int_n->bool1`
     - ``int n->bool``
   * - :ref:`min_int_k,_int_l->int1`
     - ``int k, int l->int``
   * - :ref:`max_int_k,_int_l->int1`
     - ``int k, int l->int``
   * - :ref:`min_[int]_a->int1`
     - ``[int] a->int``
   * - :ref:`max_[int]_a->int1`
     - ``[int] a->int``
   * - :ref:`min_loc_[int]_a->int1`
     - ``[int] a->int``
   * - :ref:`max_loc_[int]_a->int1`
     - ``[int] a->int``
   * - :ref:`min_int_!seed->([int]->int)1`
     - ``int !seed->([int]->int)``
   * - :ref:`max_int_!seed->([int]->int)1`
     - ``int !seed->([int]->int)``
   * - :ref:`lcm_[int]_list)_=_let_(,d->%(ratvec1`
     - ``[int] list) = let (,d->%(ratvec``
   * - :ref:`\=_(int,int)(x0,y0),(int,int)(x1,y1)->bool1`
     - ``(int,int)(x0,y0),(int,int)(x1,y1)->bool``
   * - :ref:`\!=_(int,int)(x0,y0),(int,int)(x1,y1)->bool1`
     - ``(int,int)(x0,y0),(int,int)(x1,y1)->bool``
   * - :ref:`is_integer_rat_r->bool1`
     - ``rat r->bool``
   * - :ref:`sign_rat_a->int1`
     - ``rat a->int``
   * - :ref:`abs_rat_a->rat1`
     - ``rat a->rat``
   * - :ref:`floor_rat_a->int1`
     - ``rat a->int``
   * - :ref:`ceil_rat_a->int1`
     - ``rat a->int``
   * - :ref:`\\_(rat,int)p->int1`
     - ``(rat,int)p->int``
   * - :ref:`\\_(rat,rat)p->int1`
     - ``(rat,rat)p->int``
   * - :ref:`\%_(rat,int)p->(int,rat)1`
     - ``(rat,int)p->(int,rat)``
   * - :ref:`\%_(rat,rat)p->(int,rat)1`
     - ``(rat,rat)p->(int,rat)``
   * - :ref:`floor_[rat]_v->vec1`
     - ``[rat] v->vec``
   * - :ref:`ceil_[rat]_v->vec1`
     - ``[rat] v->vec``
   * - :ref:`rat_as_int_rat_r->int1`
     - ``rat r->int``
   * - :ref:`\*_int_n,string_s->string1`
     - ``int n,string s->string``
   * - :ref:`\+_string_s,_int_i->string1`
     - ``string s, int i->string``
   * - :ref:`\+_int_i,_string_s->string1`
     - ``int i, string s->string``
   * - :ref:`plural_int_n->string1`
     - ``int n->string``
   * - :ref:`plural_int_n,string_s->string1`
     - ``int n,string s->string``
   * - :ref:`l_adjust_int_w,_string_s->string1`
     - ``int w, string s->string``
   * - :ref:`r_adjust_int_w,_string_s->string1`
     - ``int w, string s->string``
   * - :ref:`c_adjust_int_w,_string_s->string1`
     - ``int w, string s->string``
   * - :ref:`width_int_n->int1`
     - ``int n->int``
   * - :ref:`split_lines_string_text->[string]1`
     - ``string text->[string]``
   * - :ref:`is_substring_string_s,_string_text->bool1`
     - ``string s, string text->bool``
   * - :ref:`fgrep_string_s,_string_text->[string]1`
     - ``string s, string text->[string]``
   * - :ref:`vector_int_n,(int->int)f->vec:_for_i1`
     - ``int n,(int->int)f->vec: for i``
   * - :ref:`ones_int_n->vec:_for_i1`
     - ``int n->vec: for i``
   * - :ref:`gcd_[int]_v->int1`
     - ``[int] v->int``
   * - :ref:`\*_int_c,vec_v->vec1`
     - ``int c,vec v->vec``
   * - :ref:`sum_vec_v->int1`
     - ``vec v->int``
   * - :ref:`product_vec_v->1_in_for_e_in_v_do_s*1`
     - ``vec v->1 in for e in v do s*``
   * - :ref:`half_int_n->int1`
     - ``int n->int``
   * - :ref:`reverse_vec_v->vec:_v~[1`
     - ``vec v->vec: v~[``
   * - :ref:`lower_int_k,vec_v->vec:_v[1`
     - ``int k,vec v->vec: v[``
   * - :ref:`upper_int_k,vec_v->vec:_v[k~1`
     - ``int k,vec v->vec: v[k~``
   * - :ref:`drop_lower_int_k,vec_v->vec:_v[k1`
     - ``int k,vec v->vec: v[k``
   * - :ref:`drop_upper_int_k,vec_v->vec:_v[1`
     - ``int k,vec v->vec: v[``
   * - :ref:`<=_vec_v->bool1`
     - ``vec v->bool``
   * - :ref:`\<_vec_v->bool1`
     - ``vec v->bool``
   * - :ref:`is_member_[int]_v->(int->bool)1`
     - ``[int] v->(int->bool)``
   * - :ref:`contains_int_val->([int]->bool):_([int]_v)bool1`
     - ``int val->([int]->bool): ([int] v)bool``
   * - :ref:`rec_fun all_0_1_vecs_int_n->[vec]1`
     - ``int n->[vec]``
   * - :ref:`rec_fun power_set_int_n->[[int]]1`
     - ``int n->[[int]]``
   * - :ref:`power_set_[int]_s->[[int]]1`
     - ``[int] S->[[int]]``
   * - :ref:`matrix_(int,int)(r,c),(int,int->int)_f->mat1`
     - ``(int,int)(r,c),(int,int->int) f->mat``
   * - :ref:`n_rows_mat_m->int1`
     - ``mat m->int``
   * - :ref:`n_columns_mat_m->int1`
     - ``mat m->int``
   * - :ref:`column_vec_v->mat1`
     - ``vec v->mat``
   * - :ref:`row_vec_v->mat1`
     - ``vec v->mat``
   * - :ref:`\=_mat_m,int_k->bool1`
     - ``mat m,int k->bool``
   * - :ref:`\#_mat_m,_vec_v->mat:_n_rows(m)__#_(([vec]1`
     - ``mat m, vec v->mat: n_rows(m)  # (([vec]``
   * - :ref:`\#_vec_v,_mat_m->mat:_n_rows(m)__#_(v#([vec]1`
     - ``vec v, mat m->mat: n_rows(m)  # (v#([vec]``
   * - :ref:`\^_mat_m,_vec_v->mat:_n_columns(m)_^_(([vec]1`
     - ``mat m, vec v->mat: n_columns(m) ^ (([vec]``
   * - :ref:`\^_vec_v,_mat_m->mat:_n_columns(m)_^_(v#([vec]1`
     - ``vec v, mat m->mat: n_columns(m) ^ (v#([vec]``
   * - :ref:`\#\#_mat_A,_mat_B->mat1`
     - ``mat A, mat B->mat``
   * - :ref:`\^_mat_A,_mat_B->mat1`
     - ``mat A, mat B->mat``
   * - :ref:`\#\#_int_n,[mat]_L->mat1`
     - ``int n,[mat] L->mat``
   * - :ref:`map_on_mat_m->((int->int)->mat)1`
     - ``mat m->((int->int)->mat)``
   * - :ref:`\*_int_c,mat_m->mat:_map_on(m)((int_e)_int1`
     - ``int c,mat m->mat: map_on(m)((int e) int``
   * - :ref:`\-_mat_m->mat1`
     - ``mat m->mat``
   * - :ref:`\\_mat_m,int_d->mat:_map_on(m)((int_e)_int1`
     - ``mat m,int d->mat: map_on(m)((int e) int``
   * - :ref:`\%_mat_m,int_d->mat:_map_on(m)((int_e)_int1`
     - ``mat m,int d->mat: map_on(m)((int e) int``
   * - :ref:`inverse_mat_m->mat1`
     - ``mat M->mat``
   * - :ref:`det_mat_m->int1`
     - ``mat M->int``
   * - :ref:`saturated_span_mat_m->bool1`
     - ``mat M->bool``
   * - :ref:`all_mat_m,(vec->bool)_filter->bool1`
     - ``mat M,(vec->bool) filter->bool``
   * - :ref:`none_mat_m,(vec->bool)_filter->bool1`
     - ``mat M,(vec->bool) filter->bool``
   * - :ref:`first_mat_m,(vec->bool)_filter->int1`
     - ``mat M,(vec->bool) filter->int``
   * - :ref:`last_mat_m,(vec->bool)_filter->int1`
     - ``mat M,(vec->bool) filter->int``
   * - :ref:`columns_with_(int,vec->bool)_p,mat_m->mat1`
     - ``(int,vec->bool) p,mat m->mat``
   * - :ref:`columns_with_(vec->bool)_p,mat_m->mat1`
     - ``(vec->bool) p,mat m->mat``
   * - :ref:`columns_with_(int->bool)_p,mat_m->mat1`
     - ``(int->bool) p,mat m->mat``
   * - :ref:`rows_with_(int,vec->bool)_p,mat_m->mat1`
     - ``(int,vec->bool) p,mat m->mat``
   * - :ref:`rows_with_(vec->bool)_p,mat_m->mat1`
     - ``(vec->bool) p,mat m->mat``
   * - :ref:`rows_with_(int->bool)_p,mat_m->mat1`
     - ``(int->bool) p,mat m->mat``
   * - :ref:`>=_mat_m->bool1`
     - ``mat m->bool``
   * - :ref:`\>_mat_m->bool1`
     - ``mat m->bool``
   * - :ref:`<=_mat_m->bool1`
     - ``mat m->bool``
   * - :ref:`\<_mat_m->bool1`
     - ``mat m->bool``
   * - :ref:`lookup_column_vec_v,mat_m->int1`
     - ``vec v,mat m->int``
   * - :ref:`lookup_row_vec_v,mat_m->int1`
     - ``vec v,mat m->int``
   * - :ref:`sum_mat_m->vec1`
     - ``mat m->vec``
   * - :ref:`order_mat_!m->int1`
     - ``mat !M->int``
   * - :ref:`numer_ratvec_a->vec1`
     - ``ratvec a->vec``
   * - :ref:`denom_ratvec_a->int1`
     - ``ratvec a->int``
   * - :ref:`\*_int_i,ratvec_v->ratvec1`
     - ``int i,ratvec v->ratvec``
   * - :ref:`\*_rat_r,ratvec_v->ratvec1`
     - ``rat r,ratvec v->ratvec``
   * - :ref:`\#\#_ratvec_a,ratvec_b->ratvec:_##([rat]:a,[rat]1`
     - ``ratvec a,ratvec b->ratvec: ##([rat]:a,[rat]``
   * - :ref:`\#\#_[ratvec]_rs->ratvec:_##_for_r_in_rs_do_[rat]1`
     - ``[ratvec] rs->ratvec: ## for r in rs do [rat]``
   * - :ref:`sum_[ratvec]_list,_int_l->ratvec1`
     - ``[ratvec] list, int l->ratvec``
   * - :ref:`\*_[ratvec]_M,ratvec_v->ratvec1`
     - ``[ratvec] M,ratvec v->ratvec``
   * - :ref:`is_integer_ratvec_v->bool1`
     - ``ratvec v->bool``
   * - :ref:`\*_ratvec_v,_ratvec_w->rat1`
     - ``ratvec v, ratvec w->rat``
   * - :ref:`\*_vec_v,_ratvec_w->rat1`
     - ``vec v, ratvec w->rat``
   * - :ref:`\\_ratvec_v,_int_k->vec1`
     - ``ratvec v, int k->vec``
   * - :ref:`ratvec_as_vec_ratvec_v->vec1`
     - ``ratvec v->vec``
   * - :ref:`reverse_ratvec_v->ratvec:_v~[1`
     - ``ratvec v->ratvec: v~[``
   * - :ref:`lower_int_k,ratvec_v->ratvec:_v[1`
     - ``int k,ratvec v->ratvec: v[``
   * - :ref:`upper_int_k,ratvec_v->ratvec:_v[k~1`
     - ``int k,ratvec v->ratvec: v[k~``
   * - :ref:`drop_lower_int_k,ratvec_v->ratvec:_v[k1`
     - ``int k,ratvec v->ratvec: v[k``
   * - :ref:`drop_upper_int_k,ratvec_v->ratvec:_v[1`
     - ``int k,ratvec v->ratvec: v[``
   * - :ref:`sum_ratvec_v->rat1`
     - ``ratvec v->rat``
   * - :ref:`<=_ratvec_v->bool1`
     - ``ratvec v->bool``
   * - :ref:`\<_ratvec_v->bool1`
     - ``ratvec v->bool``
   * - :ref:`solve_mat_a,_ratvec_b->[ratvec]1`
     - ``mat A, ratvec b->[ratvec]``
   * - :ref:`!one_minus_s = split:_1,-1->split1`
     - ``1,-1->Split``
   * - :ref:`int_part_split_x->int1`
     - ``Split x->int``
   * - :ref:`s_part_split_x->int1`
     - ``Split x->int``
   * - :ref:`s_to_1_split_x->int1`
     - ``Split x->int``
   * - :ref:`s_to_minus_1_split_x->int1`
     - ``Split x->int``
   * - :ref:`times_s_split_x)_=_let_(a,b->%x_in_split1`
     - ``Split x) = let (a,b->%x in Split``
   * - :ref:`split_as_int_split_x->int1`
     - ``Split x->int``
   * - :ref:`\%_split_x,_int_n->(split,split)1`
     - ``Split x, int n->(Split,Split)``
   * - :ref:`half_split_w->split1`
     - ``Split w->Split``
   * - :ref:`divide_by_int_n,split_w->split1`
     - ``int n,Split w->Split``
   * - :ref:`is_pure_split_w->bool1`
     - ``Split w->bool``
   * - :ref:`split_format_split_w->string1`
     - ``Split w->string``
   * - :ref:`root_datum_[vec]_simple_roots,_[vec]_simple_coroots,_int_r->rootdatum1`
     - ``[vec] simple_roots, [vec] simple_coroots, int r->RootDatum``
   * - :ref:`root_datum_lietype_t,_[ratvec]_gens->rootdatum1`
     - ``LieType t, [ratvec] gens->RootDatum``
   * - :ref:`root_datum_lietype_t,_ratvec_gen->rootdatum1`
     - ``LieType t, ratvec gen->RootDatum``
   * - :ref:`is_root_(rootdatum,vec)_(rd,):p->bool1`
     - ``(RootDatum,vec) (rd,):p->bool``
   * - :ref:`is_coroot_(rootdatum,vec)_(rd,):p->bool1`
     - ``(RootDatum,vec) (rd,):p->bool``
   * - :ref:`is_posroot_(rootdatum,vec)(rd,):p->bool1`
     - ``(RootDatum,vec)(rd,):p->bool``
   * - :ref:`is_poscoroot_(rootdatum,vec)(rd,):p->bool1`
     - ``(RootDatum,vec)(rd,):p->bool``
   * - :ref:`posroot_index_(rootdatum,vec)p->int1`
     - ``(RootDatum,vec)p->int``
   * - :ref:`poscoroot_index_(rootdatum,vec)p->int1`
     - ``(RootDatum,vec)p->int``
   * - :ref:`rho_rootdatum_rd->ratvec1`
     - ``RootDatum rd->ratvec``
   * - :ref:`rho_as_vec_rootdatum_r->vec1`
     - ``RootDatum r->vec``
   * - :ref:`rho_check_rootdatum_rd->ratvec1`
     - ``RootDatum rd->ratvec``
   * - :ref:`is_positive_root_rootdatum_rd->(vec->bool)1`
     - ``RootDatum rd->(vec->bool)``
   * - :ref:`is_positive_coroot_rootdatum_rd->(vec->bool)1`
     - ``RootDatum rd->(vec->bool)``
   * - :ref:`is_negative_root_rootdatum_rd->(vec->bool)1`
     - ``RootDatum rd->(vec->bool)``
   * - :ref:`is_negative_coroot_rootdatum_rd->(vec->bool)1`
     - ``RootDatum rd->(vec->bool)``
   * - :ref:`is_positive_root_rootdatum_rd,vec_alpha->bool1`
     - ``RootDatum rd,vec alpha->bool``
   * - :ref:`is_positive_coroot_rootdatum_rd,vec_alphav->bool1`
     - ``RootDatum rd,vec alphav->bool``
   * - :ref:`is_negative_root_rootdatum_rd,vec_alpha->bool1`
     - ``RootDatum rd,vec alpha->bool``
   * - :ref:`is_negative_coroot_rootdatum_rd,vec_alphav->bool1`
     - ``RootDatum rd,vec alphav->bool``
   * - :ref:`roots_all_positive_rootdatum_rd->(mat->bool)1`
     - ``RootDatum rd->(mat->bool)``
   * - :ref:`coroots_all_positive_rootdatum_rd->(mat->bool)1`
     - ``RootDatum rd->(mat->bool)``
   * - :ref:`among_posroots_rootdatum_rd->(mat_m)bool1`
     - ``RootDatum rd->(mat M)bool``
   * - :ref:`among_poscoroots_rootdatum_rd->(mat_m)bool1`
     - ``RootDatum rd->(mat M)bool``
   * - :ref:`roots_rootdatum_rd->mat1`
     - ``RootDatum rd->mat``
   * - :ref:`coroots_rootdatum_rd->mat1`
     - ``RootDatum rd->mat``
   * - :ref:`root_rootdatum_rd,_vec_alpha_v->vec1`
     - ``RootDatum rd, vec alpha_v->vec``
   * - :ref:`coroot_rootdatum_rd,_vec_alpha->vec1`
     - ``RootDatum rd, vec alpha->vec``
   * - :ref:`reflection_rootdatum_rd,_int_i->mat1`
     - ``RootDatum rd, int i->mat``
   * - :ref:`reflection_(rootdatum,vec)(rd,):p->mat1`
     - ``(RootDatum,vec)(rd,):p->mat``
   * - :ref:`coreflection_rootdatum_rd,_int_i->mat1`
     - ``RootDatum rd, int i->mat``
   * - :ref:`coreflection_(rootdatum,vec)(rd,):p->mat1`
     - ``(RootDatum,vec)(rd,):p->mat``
   * - :ref:`reflect_rootdatum_rd,_int_i,_vec_v->vec1`
     - ``RootDatum rd, int i, vec v->vec``
   * - :ref:`reflect_rootdatum_rd,_vec_alpha,_vec_v->vec1`
     - ``RootDatum rd, vec alpha, vec v->vec``
   * - :ref:`coreflect_rootdatum_rd,_vec_v,_int_i->vec1`
     - ``RootDatum rd, vec v, int i->vec``
   * - :ref:`coreflect_rootdatum_rd,_vec_v,_vec_alpha->vec1`
     - ``RootDatum rd, vec v, vec alpha->vec``
   * - :ref:`reflect_rootdatum_rd,_int_i,_ratvec_v->ratvec1`
     - ``RootDatum rd, int i, ratvec v->ratvec``
   * - :ref:`reflect_rootdatum_rd,_vec_alpha,_ratvec_v->ratvec1`
     - ``RootDatum rd, vec alpha, ratvec v->ratvec``
   * - :ref:`coreflect_rootdatum_rd,_ratvec_v,_int_i->ratvec1`
     - ``RootDatum rd, ratvec v, int i->ratvec``
   * - :ref:`coreflect_rootdatum_rd,_ratvec_v,_vec_alpha->ratvec1`
     - ``RootDatum rd, ratvec v, vec alpha->ratvec``
   * - :ref:`left_reflect_rootdatum_rd,_int_i,_mat_m->mat1`
     - ``RootDatum rd, int i, mat M->mat``
   * - :ref:`left_reflect_rootdatum_rd,_vec_alpha,_mat_m->mat1`
     - ``RootDatum rd, vec alpha, mat M->mat``
   * - :ref:`right_reflect_rootdatum_rd,_mat_m,_int_i->mat1`
     - ``RootDatum rd, mat M, int i->mat``
   * - :ref:`right_reflect_rootdatum_rd,_mat_m,_vec_alpha->mat1`
     - ``RootDatum rd, mat M, vec alpha->mat``
   * - :ref:`conjugate_rootdatum_rd,_int_i,_mat_m->mat1`
     - ``RootDatum rd, int i, mat M->mat``
   * - :ref:`conjugate_rootdatum_rd,_vec_alpha,_mat_m->mat1`
     - ``RootDatum rd, vec alpha, mat M->mat``
   * - :ref:`singular_simple_indices_rootdatum_rd,ratvec_v->[int]1`
     - ``RootDatum rd,ratvec v->[int]``
   * - :ref:`is_imaginary_mat_theta->(vec->bool):_(vec_alpha)1`
     - ``mat theta->(vec->bool): (vec alpha)``
   * - :ref:`is_real_mat_theta->(vec->bool):_(vec_alpha)1`
     - ``mat theta->(vec->bool): (vec alpha)``
   * - :ref:`is_complex_mat_theta->(vec->bool):_(vec_alpha)1`
     - ``mat theta->(vec->bool): (vec alpha)``
   * - :ref:`imaginary_roots_rootdatum_rd,_mat_theta->mat1`
     - ``RootDatum rd, mat theta->mat``
   * - :ref:`real_roots_rootdatum_rd,_mat_theta->mat1`
     - ``RootDatum rd, mat theta->mat``
   * - :ref:`imaginary_coroots_rootdatum_rd,_mat_theta->mat1`
     - ``RootDatum rd, mat theta->mat``
   * - :ref:`real_coroots_rootdatum_rd,_mat_theta->mat1`
     - ``RootDatum rd, mat theta->mat``
   * - :ref:`imaginary_posroots_rootdatum_rd,mat_theta->mat1`
     - ``RootDatum rd,mat theta->mat``
   * - :ref:`real_posroots_rootdatum_rd,mat_theta->mat1`
     - ``RootDatum rd,mat theta->mat``
   * - :ref:`imaginary_poscoroots_rootdatum_rd,mat_theta->mat1`
     - ``RootDatum rd,mat theta->mat``
   * - :ref:`real_poscoroots_rootdatum_rd,mat_theta->mat1`
     - ``RootDatum rd,mat theta->mat``
   * - :ref:`imaginary_sys_(rootdatum,mat)p->(mat,mat)1`
     - ``(RootDatum,mat)p->(mat,mat)``
   * - :ref:`real_sys_(rootdatum,mat)p->(mat,mat)1`
     - ``(RootDatum,mat)p->(mat,mat)``
   * - :ref:`is_dominant_rootdatum_rd,_ratvec_v->bool1`
     - ``RootDatum rd, ratvec v->bool``
   * - :ref:`is_strictly_dominant_rootdatum_rd,_ratvec_v->bool1`
     - ``RootDatum rd, ratvec v->bool``
   * - :ref:`is_regular_rootdatum_rd,ratvec_v->bool1`
     - ``RootDatum rd,ratvec v->bool``
   * - :ref:`is_integral_rootdatum_rd,_ratvec_v->bool1`
     - ``RootDatum rd, ratvec v->bool``
   * - :ref:`radical_basis_rootdatum_rd->mat1`
     - ``RootDatum rd->mat``
   * - :ref:`coradical_basis_rootdatum_rd->mat1`
     - ``RootDatum rd->mat``
   * - :ref:`is_semisimple_rootdatum_rd->bool1`
     - ``RootDatum rd->bool``
   * - :ref:`derived_is_simply_connected_rootdatum_rd->bool1`
     - ``RootDatum rd->bool``
   * - :ref:`has_connected_center_rootdatum_rd->bool1`
     - ``RootDatum rd->bool``
   * - :ref:`is_simply_connected_rootdatum_rd->bool1`
     - ``RootDatum rd->bool``
   * - :ref:`is_adjoint_rootdatum_rd->bool1`
     - ``RootDatum rd->bool``
   * - :ref:`derived_rootdatum_rd->rootdatum1`
     - ``RootDatum rd->RootDatum``
   * - :ref:`mod_central_torus_rootdatum_rd->rootdatum1`
     - ``RootDatum rd->RootDatum``
   * - :ref:`adjoint_rootdatum_rd->rootdatum1`
     - ``RootDatum rd->RootDatum``
   * - :ref:`is_simple_for_vec_dual_two_rho->(vec->bool)1`
     - ``vec dual_two_rho->(vec->bool)``
   * - :ref:`simple_from_positive_mat_posroots,mat_poscoroots->(mat,mat)1`
     - ``mat posroots,mat poscoroots->(mat,mat)``
   * - :ref:`fundamental_weights_rootdatum_rd->[ratvec]1`
     - ``RootDatum rd->[ratvec]``
   * - :ref:`fundamental_coweights_rootdatum_rd->[ratvec]1`
     - ``RootDatum rd->[ratvec]``
   * - :ref:`\!=_InnerClass_x,InnerClass_y->bool1`
     - ``InnerClass x,InnerClass y->bool``
   * - :ref:`dual_integral_innerclass_ic,_ratvec_gamma->innerclass1`
     - ``InnerClass ic, ratvec gamma->InnerClass``
   * - :ref:`cartan_classes_innerclass_ic->[cartanclass]1`
     - ``InnerClass ic->[CartanClass]``
   * - :ref:`print_cartan_info_cartanclass_cc->void1`
     - ``CartanClass cc->void``
   * - :ref:`fundamental_cartan_innerclass_ic->cartanclass1`
     - ``InnerClass ic->CartanClass``
   * - :ref:`most_split_cartan_innerclass_ic->cartanclass1`
     - ``InnerClass ic->CartanClass``
   * - :ref:`compact_rank_cartanclass_cc->int1`
     - ``CartanClass cc->int``
   * - :ref:`split_rank_cartanclass_cc->int1`
     - ``CartanClass cc->int``
   * - :ref:`compact_rank_innerclass_ic->int1`
     - ``InnerClass ic->int``
   * - :ref:`split_rank_realform_g->int1`
     - ``RealForm G->int``
   * - :ref:`is_equal_rank_innerclass_ic->bool1`
     - ``InnerClass ic->bool``
   * - :ref:`is_split_realform_g->bool1`
     - ``RealForm G->bool``
   * - :ref:`\=_CartanClass_H,CartanClass_J->bool1`
     - ``CartanClass H,CartanClass J->bool``
   * - :ref:`number_cartanclass_h,realform_g->int1`
     - ``CartanClass H,RealForm G->int``
   * - :ref:`\!=_RealForm_f,_RealForm_g->bool1`
     - ``RealForm f, RealForm g->bool``
   * - :ref:`form_name_realform_f->string1`
     - ``RealForm f->string``
   * - :ref:`real_forms_innerclass_ic->[realform]1`
     - ``InnerClass ic->[RealForm]``
   * - :ref:`dual_real_forms_innerclass_ic->[realform]1`
     - ``InnerClass ic->[RealForm]``
   * - :ref:`is_quasisplit_realform_g->bool1`
     - ``RealForm G->bool``
   * - :ref:`is_quasicompact_realform_g->bool1`
     - ``RealForm G->bool``
   * - :ref:`split_form_rootdatum_r->realform1`
     - ``RootDatum r->RealForm``
   * - :ref:`split_form_lietype_t->realform1`
     - ``LieType t->RealForm``
   * - :ref:`quasicompact_form_innerclass_ic->realform1`
     - ``InnerClass ic->RealForm``
   * - :ref:`is_compatible_realform_f,_realform_g->bool1`
     - ``RealForm f, RealForm g->bool``
   * - :ref:`is_compact_realform_g->bool1`
     - ``RealForm G->bool``
   * - :ref:`\!=_KGBElt_x,KGBElt_y->bool1`
     - ``KGBElt x,KGBElt y->bool``
   * - :ref:`root_datum_kgbelt_x->rootdatum1`
     - ``KGBElt x->RootDatum``
   * - :ref:`inner_class_kgbelt_x->innerclass1`
     - ``KGBElt x->InnerClass``
   * - :ref:`kgb_realform_rf->[kgbelt]:_for_i1`
     - ``RealForm rf->[KGBElt]: for i``
   * - :ref:`kgb_cartanclass_h,realform_g->[kgbelt]1`
     - ``CartanClass H,RealForm G->[KGBElt]``
   * - :ref:`kgb_elt_(innerclass,_mat,_ratvec)_(,theta,v):all->kgbelt1`
     - ``(InnerClass, mat, ratvec) (,theta,v):all->KGBElt``
   * - :ref:`kgb_elt_rootdatum_rd,_mat_theta,_ratvec_v->kgbelt1`
     - ``RootDatum rd, mat theta, ratvec v->KGBElt``
   * - :ref:`cartan_class_innerclass_ic,_mat_theta->cartanclass1`
     - ``InnerClass ic, mat theta->CartanClass``
   * - :ref:`status_vec_alpha,kgbelt_x->int1`
     - ``vec alpha,KGBElt x->int``
   * - :ref:`cross_vec_alpha,kgbelt_x->kgbelt1`
     - ``vec alpha,KGBElt x->KGBElt``
   * - :ref:`cayley_vec_alpha,kgbelt_x->kgbelt1`
     - ``vec alpha,KGBElt x->KGBElt``
   * - :ref:`w_cross_[int]_w,kgbelt_x->kgbelt1`
     - ``[int] w,KGBElt x->KGBElt``
   * - :ref:`kgb_status_text_int_i->string1`
     - ``int i->string``
   * - :ref:`status_text_(int,kgbelt)p->string1`
     - ``(int,KGBElt)p->string``
   * - :ref:`status_text_(vec,kgbelt)p->string1`
     - ``(vec,KGBElt)p->string``
   * - :ref:`status_texts_kgbelt_x->[string]1`
     - ``KGBElt x->[string]``
   * - :ref:`is_imaginary_kgbelt_x->(vec->bool)1`
     - ``KGBElt x->(vec->bool)``
   * - :ref:`is_real_kgbelt_x->(vec->bool)1`
     - ``KGBElt x->(vec->bool)``
   * - :ref:`is_complex_kgbelt_x->(vec->bool)1`
     - ``KGBElt x->(vec->bool)``
   * - :ref:`imaginary_posroots_kgbelt_x->mat1`
     - ``KGBElt x->mat``
   * - :ref:`real_posroots_kgbelt_x->mat1`
     - ``KGBElt x->mat``
   * - :ref:`imaginary_poscoroots_kgbelt_x->mat1`
     - ``KGBElt x->mat``
   * - :ref:`real_poscoroots_kgbelt_x->mat1`
     - ``KGBElt x->mat``
   * - :ref:`imaginary_sys_kgbelt_x->(mat,mat)1`
     - ``KGBElt x->(mat,mat)``
   * - :ref:`real_sys_kgbelt_x->(mat,mat)1`
     - ``KGBElt x->(mat,mat)``
   * - :ref:`rho_i_kgbelt_x->ratvec1`
     - ``KGBElt x->ratvec``
   * - :ref:`rho_r_kgbelt_x->ratvec1`
     - ``KGBElt x->ratvec``
   * - :ref:`rho_check_i_kgbelt_x->ratvec1`
     - ``KGBElt x->ratvec``
   * - :ref:`rho_check_r_kgbelt_x->ratvec1`
     - ``KGBElt x->ratvec``
   * - :ref:`rho_i_(rootdatum,mat)_rd_theta->ratvec1`
     - ``(RootDatum,mat) rd_theta->ratvec``
   * - :ref:`rho_r_(rootdatum,mat)_rd_theta->ratvec1`
     - ``(RootDatum,mat) rd_theta->ratvec``
   * - :ref:`rho_check_i_(rootdatum,mat)_rd_theta->ratvec1`
     - ``(RootDatum,mat) rd_theta->ratvec``
   * - :ref:`rho_check_r_(rootdatum,mat)_rd_theta->ratvec1`
     - ``(RootDatum,mat) rd_theta->ratvec``
   * - :ref:`is_compact_kgbelt_x->(vec->bool)1`
     - ``KGBElt x->(vec->bool)``
   * - :ref:`is_noncompact_kgbelt_x->(vec->bool)1`
     - ``KGBElt x->(vec->bool)``
   * - :ref:`is_compact_imaginary_kgbelt_x->(vec->bool)1`
     - ``KGBElt x->(vec->bool)``
   * - :ref:`is_noncompact_imaginary_kgbelt_x->(vec->bool)1`
     - ``KGBElt x->(vec->bool)``
   * - :ref:`compact_posroots_kgbelt_x->mat1`
     - ``KGBElt x->mat``
   * - :ref:`noncompact_posroots_kgbelt_x->mat1`
     - ``KGBElt x->mat``
   * - :ref:`rho_ci_kgbelt_x->ratvec1`
     - ``KGBElt x->ratvec``
   * - :ref:`rho_nci_kgbelt_x->ratvec1`
     - ``KGBElt x->ratvec``
   * - :ref:`is_imaginary_vec_v,kgbelt_x->bool1`
     - ``vec v,KGBElt x->bool``
   * - :ref:`is_real_vec_v,kgbelt_x->bool1`
     - ``vec v,KGBElt x->bool``
   * - :ref:`is_complex_vec_v,kgbelt_x->bool1`
     - ``vec v,KGBElt x->bool``
   * - :ref:`is_compact_imaginary_vec_v,kgbelt_x->bool1`
     - ``vec v,KGBElt x->bool``
   * - :ref:`is_noncompact_imaginary_vec_v,kgbelt_x->bool1`
     - ``vec v,KGBElt x->bool``
   * - :ref:`print_kgb_kgbelt_x->void1`
     - ``KGBElt x->void``
   * - :ref:`no_cminus_roots_kgbelt_x->bool1`
     - ``KGBElt x->bool``
   * - :ref:`no_cplus_roots_kgbelt_x->bool1`
     - ``KGBElt x->bool``
   * - :ref:`blocks_innerclass_ic->[block]1`
     - ``InnerClass ic->[Block]``
   * - :ref:`raw_kl_(realform,realform)_p->(mat,[vec],vec)1`
     - ``(RealForm,RealForm) p->(mat,[vec],vec)``
   * - :ref:`dual_kl_(realform,realform)_p->(mat,[vec],vec)1`
     - ``(RealForm,RealForm) p->(mat,[vec],vec)``
   * - :ref:`print_block_(realform,realform)_p->void1`
     - ``(RealForm,RealForm) p->void``
   * - :ref:`print_blocku_(realform,realform)_p->void1`
     - ``(RealForm,RealForm) p->void``
   * - :ref:`print_blockd_(realform,realform)_p->void1`
     - ``(RealForm,RealForm) p->void``
   * - :ref:`print_kl_basis_(realform,realform)_p->void1`
     - ``(RealForm,RealForm) p->void``
   * - :ref:`print_prim_kl_(realform,realform)_p->void1`
     - ``(RealForm,RealForm) p->void``
   * - :ref:`print_kl_list_(realform,realform)_p->void1`
     - ``(RealForm,RealForm) p->void``
   * - :ref:`print_w_cells_(realform,realform)_p->void1`
     - ``(RealForm,RealForm) p->void``
   * - :ref:`print_w_graph_(realform,realform)_p->void1`
     - ``(RealForm,RealForm) p->void``
   * - :ref:`\!=_Param_x,Param_y->bool1`
     - ``Param x,Param y->bool``
   * - :ref:`equals_param_p,param_q->bool1`
     - ``Param p,Param q->bool``
   * - :ref:`root_datum_param_p->rootdatum1`
     - ``Param p->RootDatum``
   * - :ref:`inner_class_param_p->innerclass1`
     - ``Param p->InnerClass``
   * - :ref:`null_module_param_p->parampol1`
     - ``Param p->ParamPol``
   * - :ref:`\*_Param_p,rat_f->Param1`
     - ``Param p,rat f->Param``
   * - :ref:`x_param_p->kgbelt1`
     - ``Param p->KGBElt``
   * - :ref:`lambda_minus_rho_param_p->vec1`
     - ``Param p->vec``
   * - :ref:`lambda_param_p->ratvec1`
     - ``Param p->ratvec``
   * - :ref:`infinitesimal_character_param_p->ratvec1`
     - ``Param p->ratvec``
   * - :ref:`nu_param_p->ratvec1`
     - ``Param p->ratvec``
   * - :ref:`cartan_class_param_p->cartanclass1`
     - ``Param p->CartanClass``
   * - :ref:`integrality_datum_param_p->rootdatum1`
     - ``Param p->RootDatum``
   * - :ref:`is_regular_param_p->bool1`
     - ``Param p->bool``
   * - :ref:`survives_param_p->bool1`
     - ``Param p->bool``
   * - :ref:`trivial_realform_g->param1`
     - ``RealForm G->Param``
   * - :ref:`w_cross_[int]_w,param_p->param1`
     - ``[int] w,Param p->Param``
   * - :ref:`parameter_realform_g,int_x,ratvec_lambda,ratvec_nu->param1`
     - ``RealForm G,int x,ratvec lambda,ratvec nu->Param``
   * - :ref:`parameter_kgbelt_x,ratvec_lambda,ratvec_nu->param1`
     - ``KGBElt x,ratvec lambda,ratvec nu->Param``
   * - :ref:`parameter_gamma_kgbelt_x,_ratvec_lambda,_ratvec_gamma->param1`
     - ``KGBElt x, ratvec lambda, ratvec gamma->Param``
   * - :ref:`singular_block_param_p->([param],int)1`
     - ``Param p->([Param],int)``
   * - :ref:`block_of_param_p->[param]1`
     - ``Param p->[Param]``
   * - :ref:`singular_block_of_param_p->[param]1`
     - ``Param p->[Param]``
   * - :ref:`imaginary_type_int_s,_param_p->int1`
     - ``int s, Param p->int``
   * - :ref:`real_type_int_s,param_p->int1`
     - ``int s,Param p->int``
   * - :ref:`imaginary_type_vec_alpha,_param_p->int1`
     - ``vec alpha, Param p->int``
   * - :ref:`real_type_vec_alpha,_param_p->int1`
     - ``vec alpha, Param p->int``
   * - :ref:`is_nonparity_int_s,param_p->bool1`
     - ``int s,Param p->bool``
   * - :ref:`is_parity_int_s,param_p->bool1`
     - ``int s,Param p->bool``
   * - :ref:`is_nonparity_vec_alpha,param_p->bool1`
     - ``vec alpha,Param p->bool``
   * - :ref:`is_parity_vec_alpha,param_p->bool1`
     - ``vec alpha,Param p->bool``
   * - :ref:`status_vec_alpha,param_p->int1`
     - ``vec alpha,Param p->int``
   * - :ref:`status_int_s,param_p->int1`
     - ``int s,Param p->int``
   * - :ref:`block_status_text_int_i->string1`
     - ``int i->string``
   * - :ref:`status_text_int_s,param_p->string1`
     - ``int s,Param p->string``
   * - :ref:`status_texts_param_p->[string]1`
     - ``Param p->[string]``
   * - :ref:`status_text_(vec,param)_ap->string1`
     - ``(vec,Param) ap->string``
   * - :ref:`parity_poscoroots_param_p->mat1`
     - ``Param p->mat``
   * - :ref:`nonparity_poscoroots_param_p->mat1`
     - ``Param p->mat``
   * - :ref:`is_descent_int_s,param_p->bool1`
     - ``int s,Param p->bool``
   * - :ref:`tau_bitset_param_p->((int->bool),int)1`
     - ``Param p->((int->bool),int)``
   * - :ref:`tau_param_p->[int]1`
     - ``Param p->[int]``
   * - :ref:`tau_complement_param_p->[int]1`
     - ``Param p->[int]``
   * - :ref:`is_descent_(vec,param)_ap->bool1`
     - ``(vec,Param) ap->bool``
   * - :ref:`lookup_param_p,_[param]_block->int1`
     - ``Param p, [Param] block->int``
   * - :ref:`null_module_parampol_p->parampol1`
     - ``ParamPol P->ParamPol``
   * - :ref:`\-_ParamPol_P->ParamPol1`
     - ``ParamPol P->ParamPol``
   * - :ref:`first_param_parampol_p->param1`
     - ``ParamPol P->Param``
   * - :ref:`last_param_parampol_p->param1`
     - ``ParamPol P->Param``
   * - :ref:`s_to_1_parampol_p->parampol1`
     - ``ParamPol P->ParamPol``
   * - :ref:`s_to_minus_1_parampol_p->parampol1`
     - ``ParamPol P->ParamPol``
   * - :ref:`\-_ParamPol_a,_(Split,Param)_(c,p)->ParamPol1`
     - ``ParamPol a, (Split,Param) (c,p)->ParamPol``
   * - :ref:`\*_ParamPol_P,_rat_f->ParamPol1`
     - ``ParamPol P, rat f->ParamPol``
   * - :ref:`half_parampol_p->parampol1`
     - ``ParamPol P->ParamPol``
   * - :ref:`divide_by_int_n,_parampol_p->parampol1`
     - ``int n, ParamPol P->ParamPol``
   * - :ref:`root_datum_parampol_p->rootdatum1`
     - ``ParamPol P->RootDatum``
   * - :ref:`virtual_param_p->parampol1`
     - ``Param p->ParamPol``
   * - :ref:`virtual_realform_g,_[param]_ps->parampol1`
     - ``RealForm G, [Param] ps->ParamPol``
   * - :ref:`pol_format_parampol_p->string1`
     - ``ParamPol P->string``
   * - :ref:`infinitesimal_character_parampol_p->ratvec1`
     - ``ParamPol P->ratvec``
   * - :ref:`separate_by_infinitesimal_character_parampol_p->[(ratvec,parampol)]1`
     - ``ParamPol P->[(ratvec,ParamPol)]``
   * - :ref:`is_pure_parampol_p->bool1`
     - ``ParamPol P->bool``
   * - :ref:`purity_parampol_p->(int,int,int)1`
     - ``ParamPol P->(int,int,int)``
   * - :ref:`find_[int]_v,_int_k->int:______first(#v,(int_i)bool1`
     - ``[int] v, int k->int:      first(#v,(int i)bool``
   * - :ref:`find_[param]_p,param_p->int:___first(#p,(int_i)bool1`
     - ``[Param] P,Param p->int:   first(#P,(int i)bool``
   * - :ref:`find_[kgbelt]_s,kgbelt_x->int:_first(#s,(int_i)bool1`
     - ``[KGBElt] S,KGBElt x->int: first(#S,(int i)bool``
   * - :ref:`find_[vec]_s,vec_v->int:_______first(#s,(int_i)bool1`
     - ``[vec] S,vec v->int:       first(#S,(int i)bool``
   * - :ref:`in_string_list_string_s,[string]_s->bool1`
     - ``string s,[string] S->bool``
   * - :ref:`delete_[int]_v,_int_k->[int]:_____v[:k]##v[k+11`
     - ``[int] v, int k->[int]:     v[:k]##v[k+1``
   * - :ref:`delete_[vec]_v,_int_k->[vec]:_____v[:k]##v[k+11`
     - ``[vec] v, int k->[vec]:     v[:k]##v[k+1``
   * - :ref:`delete_[ratvec]_v,_int_k->[ratvec]:__v[:k]##v[k+11`
     - ``[ratvec] v, int k->[ratvec]:  v[:k]##v[k+1``
   * - :ref:`delete_[[ratvec]]_v,_int_k->[[ratvec]]:v[:k]##v[k+11`
     - ``[[ratvec]] v, int k->[[ratvec]]:v[:k]##v[k+1``
   * - :ref:`delete_[[vec]]_v,_int_k->[[vec]]:___v[:k]##v[k+11`
     - ``[[vec]] v, int k->[[vec]]:   v[:k]##v[k+1``
   * - :ref:`delete_[parampol]_p,_int_k->[parampol]:p[:k]##p[k+11`
     - ``[ParamPol] P, int k->[ParamPol]:P[:k]##P[k+1``
   * - :ref:`imaginary_roots_and_coroots_(rootdatum,_mat)p->(mat,mat)1`
     - ``(RootDatum, mat)p->(mat,mat)``
   * - :ref:`imaginary_roots_and_coroots_kgbelt_x->(mat,mat)1`
     - ``KGBElt x->(mat,mat)``
   * - :ref:`real_roots_and_coroots_(rootdatum,_mat)p->(mat,mat)1`
     - ``(RootDatum, mat)p->(mat,mat)``
   * - :ref:`real_roots_and_coroots_kgbelt_x->(mat,mat)1`
     - ``KGBElt x->(mat,mat)``
   * - :ref:`complex_posroots_rootdatum_rd,mat_theta->mat1`
     - ``RootDatum rd,mat theta->mat``
   * - :ref:`complex_posroots_kgbelt_x->mat1`
     - ``KGBElt x->mat``
   * - :ref:`pad_string_s,int_padding->string1`
     - ``string s,int padding->string``
   * - :ref:`monomials_parampol_p->[param]1`
     - ``ParamPol P->[Param]``
   * - :ref:`monomial_parampol_p,int_i->param1`
     - ``ParamPol P,int i->Param``
