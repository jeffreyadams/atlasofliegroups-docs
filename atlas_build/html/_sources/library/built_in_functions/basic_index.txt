basic.at Function Index
====================================================

.. list-table::
   :widths: 10 20
   :header-rows: 1

   * - Function
     - Argument(s) -> Results
   * - :ref:`\+_(string,int->string)`
     - (string,int->string)
   * - :ref:`\+_(int,string->string)`
     - (int,string->string)
   * - :ref:`\+_(string,(int,int)->string)`
     - (string,(int,int)->string)
   * - :ref:`\+_(Split->int)`
     - (Split->int)
   * - :ref:`\-_(mat->mat)`
     - (mat->mat)
   * - :ref:`\-_(ParamPol->ParamPol)`
     - (ParamPol->ParamPol)
   * - :ref:`\-_(ParamPol,(Split,Param)->ParamPol)`
     - (ParamPol,(Split,Param)->ParamPol)
   * - :ref:`\*_(string,int->string)`
     - (string,int->string)
   * - :ref:`\*_(int,vec->vec)`
     - (int,vec->vec)
   * - :ref:`\*_(int,mat->mat)`
     - (int,mat->mat)
   * - :ref:`\*_(int,ratvec->ratvec)`
     - (int,ratvec->ratvec)
   * - :ref:`\*_(rat,ratvec->ratvec)`
     - (rat,ratvec->ratvec)
   * - :ref:`\*_([ratvec],ratvec->ratvec)`
     - ([ratvec],ratvec->ratvec)
   * - :ref:`\*_(vec,ratvec->rat)`
     - (vec,ratvec->rat)
   * - :ref:`\*_(ratvec,ratvec->rat)`
     - (ratvec,ratvec->rat)
   * - :ref:`\*_(Param,rat->Param)`
     - (Param,rat->Param)
   * - :ref:`\*_(ParamPol,rat->ParamPol)`
     - (ParamPol,rat->ParamPol)
   * - :ref:`\\_(rat,int->int)`
     - (rat,int->int)
   * - :ref:`\\_(rat,rat->int)`
     - (rat,rat->int)
   * - :ref:`\\_(mat,int->mat)`
     - (mat,int->mat)
   * - :ref:`\\_(ratvec,int->vec)`
     - (ratvec,int->vec)
   * - :ref:`%_(mat,int->mat)`
     - (mat,int->mat)
   * - :ref:`\%_(rat,int->int,rat)`
     - (rat,int->int,rat)
   * - :ref:`\%_(rat,rat->int,rat)`
     - (rat,rat->int,rat)
   * - :ref:`^_(mat,vec->mat)`
     - (mat,vec->mat)
   * - :ref:`^_(vec,mat->mat)`
     - (vec,mat->mat)
   * - :ref:`^_(mat,mat->mat)`
     - (mat,mat->mat)
   * - :ref:`^_(mat,int->mat)`
     - (mat,int->mat)
   * - :ref:`^_(Split->int)`
     - (Split->int)
   * - :ref:`^_(Split,int->Split)`
     - (Split,int->Split)
   * - :ref:`=_((int,int),(int,int)->bool)`
     - ((int,int),(int,int)->bool)
   * - :ref:`=_(mat,int->bool)`
     - (mat,int->bool)
   * - :ref:`=_(CartanClass,CartanClass->bool)`
     - (CartanClass,CartanClass->bool)
   * - :ref:`!=_((int,int),(int,int)->bool)`
     - ((int,int),(int,int)->bool)
   * - :ref:`!=_(Param,Param->bool)`
     - (Param,Param->bool)
   * - :ref:`!=_(RealForm,RealForm->bool)`
     - (RealForm,RealForm->bool)
   * - :ref:`!=_(InnerClass,InnerClass->bool)`
     - (InnerClass,InnerClass->bool)
   * - :ref:`!=_(KGBElt,KGBElt->bool)`
     - (KGBElt,KGBElt->bool)
   * - :ref:`>=_(mat->bool)`
     - (mat->bool)
   * - :ref:`>_(mat->bool)`
     - (mat->bool)
   * - :ref:`<=_(vec->bool)`
     - (vec->bool)
   * - :ref:`<=_(mat->bool)`
     - (mat->bool)
   * - :ref:`<=_(ratvec->bool)`
     - (ratvec->bool)
   * - :ref:`<_(vec->bool)`
     - (vec->bool)
   * - :ref:`<_(mat->bool)`
     - (mat->bool)
   * - :ref:`<_(ratvec->bool)`
     - (ratvec->bool)
   * - :ref:`##_(mat,mat->mat)`
     - (mat,mat->mat)
   * - :ref:`##_(int,[mat]->mat)`
     - (int,[mat]->mat)
   * - :ref:`##_(ratvec,ratvec->ratvec)`
     - (ratvec,ratvec->ratvec)
   * - :ref:`##_([ratvec]->ratvec)`
     - ([ratvec]->ratvec)
   * - :ref:`#_(ratvec->int)`
     - (ratvec->int)
   * - :ref:`#_(int->[int])`
     - (int->[int])
   * - :ref:`#_(bool->int)`
     - (bool->int)
   * - :ref:`#_(mat,vec->mat)`
     - (mat,vec->mat)
   * - :ref:`#_(vec,mat->mat)`
     - (vec,mat->mat)
   * - :ref:`#_(KGBElt->int)`
     - (KGBElt->int)
   * - :ref:`involution_(Param->mat)`
     - (Param->mat)
   * - :ref:`root_datum_([vec],[vec],int->RootDatum)`
     - ([vec],[vec],int->RootDatum)
   * - :ref:`root_datum_(LieType,[ratvec]->RootDatum)`
     - (LieType,[ratvec]->RootDatum)
   * - :ref:`root_datum_(LieType,ratvec->RootDatum)`
     - (LieType,ratvec->RootDatum)
   * - :ref:`root_datum_(KGBElt->RootDatum)`
     - (KGBElt->RootDatum)
   * - :ref:`root_datum_(Param->RootDatum)`
     - (Param->RootDatum)
   * - :ref:`root_datum_(ParamPol->RootDatum)`
     - (ParamPol->RootDatum)
   * - :ref:`adjoint_(RootDatum->RootDatum)`
     - (RootDatum->RootDatum)
   * - :ref:`root_(RootDatum,vec->vec)`
     - (RootDatum,vec->vec)
   * - :ref:`coroot_(RootDatum,vec->vec)`
     - (RootDatum,vec->vec)
   * - :ref:`integrality_datum_(Param->RootDatum)`
     - (Param->RootDatum)
   * - :ref:`inner_class_(KGBElt->InnerClass)`
     - (KGBElt->InnerClass)
   * - :ref:`inner_class_(Param->InnerClass)`
     - (Param->InnerClass)
   * - :ref:`real_form_(KGBElt->RealForm)`
     - (KGBElt->RealForm)
   * - :ref:`Cartan_class_(InnerClass,mat->CartanClass)`
     - (InnerClass,mat->CartanClass)
   * - :ref:`Cartan_class_(Param->CartanClass)`
     - (Param->CartanClass)
   * - :ref:`most_split_Cartan_(InnerClass->CartanClass)`
     - (InnerClass->CartanClass)
   * - :ref:`real_forms_(InnerClass->[RealForm])`
     - (InnerClass->[RealForm])
   * - :ref:`dual_real_forms_(InnerClass->[RealForm])`
     - (InnerClass->[RealForm])
   * - :ref:`KGB_(RealForm->[KGBElt])`
     - (RealForm->[KGBElt])
   * - :ref:`KGB_(CartanClass,RealForm->[KGBElt])`
     - (CartanClass,RealForm->[KGBElt])
   * - :ref:`cross_(vec,KGBElt->KGBElt)`
     - (vec,KGBElt->KGBElt)
   * - :ref:`Cayley_(vec,KGBElt->KGBElt)`
     - (vec,KGBElt->KGBElt)
   * - :ref:`status_(vec,KGBElt->int)`
     - (vec,KGBElt->int)
   * - :ref:`status_(vec,Param->int)`
     - (vec,Param->int)
   * - :ref:`status_(int,Param->int)`
     - (int,Param->int)
   * - :ref:`KGB_elt_(InnerClass,mat,ratvec->KGBElt)`
     - (InnerClass,mat,ratvec->KGBElt)
   * - :ref:`KGB_elt_(RootDatum,mat,ratvec->KGBElt)`
     - (RootDatum,mat,ratvec->KGBElt)
   * - :ref:`print_block_(RealForm,RealForm->)`
     - (RealForm,RealForm->)
   * - :ref:`null_module_(Param->ParamPol)`
     - (Param->ParamPol)
   * - :ref:`null_module_(ParamPol->ParamPol)`
     - (ParamPol->ParamPol)
   * - :ref:`raw_KL_(RealForm,RealForm->mat,[vec],vec)`
     - (RealForm,RealForm->mat,[vec],vec)
   * - :ref:`dual_KL_(RealForm,RealForm->mat,[vec],vec)`
     - (RealForm,RealForm->mat,[vec],vec)
   * - :ref:`print_blocku_(RealForm,RealForm->)`
     - (RealForm,RealForm->)
   * - :ref:`print_blockd_(RealForm,RealForm->)`
     - (RealForm,RealForm->)
   * - :ref:`print_KGB_(KGBElt->)`
     - (KGBElt->)
   * - :ref:`print_KL_basis_(RealForm,RealForm->)`
     - (RealForm,RealForm->)
   * - :ref:`print_prim_KL_(RealForm,RealForm->)`
     - (RealForm,RealForm->)
   * - :ref:`print_KL_list_(RealForm,RealForm->)`
     - (RealForm,RealForm->)
   * - :ref:`print_W_cells_(RealForm,RealForm->)`
     - (RealForm,RealForm->)
   * - :ref:`print_W_graph_(RealForm,RealForm->)`
     - (RealForm,RealForm->)
   * - :ref:`assert_(bool,string->)`
     - (bool,string->)
   * - :ref:`assert_(bool->)`
     - (bool->)
   * - :ref:`list_((int->bool),int->[int])`
     - ((int->bool),int->[int])
   * - :ref:`complement_((int->bool),int->[int])`
     - ((int->bool),int->[int])
   * - :ref:`count_((int->bool),int->int)`
     - ((int->bool),int->int)
   * - :ref:`all_([bool]->bool)`
     - ([bool]->bool)
   * - :ref:`all_(int,(int->bool)->bool)`
     - (int,(int->bool)->bool)
   * - :ref:`all_([(->bool)]->bool)`
     - ([(->bool)]->bool)
   * - :ref:`all_(mat,(vec->bool)->bool)`
     - (mat,(vec->bool)->bool)
   * - :ref:`x_(Param->KGBElt)`
     - (Param->KGBElt)
   * - :ref:`none_([bool]->bool)`
     - ([bool]->bool)
   * - :ref:`none_(int,(int->bool)->bool)`
     - (int,(int->bool)->bool)
   * - :ref:`none_([(->bool)]->bool)`
     - ([(->bool)]->bool)
   * - :ref:`none_(mat,(vec->bool)->bool)`
     - (mat,(vec->bool)->bool)
   * - :ref:`first_([bool]->int)`
     - ([bool]->int)
   * - :ref:`first_(int,(int->bool)->int)`
     - (int,(int->bool)->int)
   * - :ref:`first_([(->bool)]->int)`
     - ([(->bool)]->int)
   * - :ref:`first_(mat,(vec->bool)->int)`
     - (mat,(vec->bool)->int)
   * - :ref:`last_([bool]->int)`
     - ([bool]->int)
   * - :ref:`last_(int,(int->bool)->int)`
     - (int,(int->bool)->int)
   * - :ref:`last_([(->bool)]->int)`
     - ([(->bool)]->int)
   * - :ref:`last_(mat,(vec->bool)->int)`
     - (mat,(vec->bool)->int)
   * - :ref:`abs_(int->int)`
     - (int->int)
   * - :ref:`abs_(rat->rat)`
     - (rat->rat)
   * - :ref:`sign_(int->int)`
     - (int->int)
   * - :ref:`sign_(rat->int)`
     - (rat->int)
   * - :ref:`is_odd_(int->bool)`
     - (int->bool)
   * - :ref:`is_even_(int->bool)`
     - (int->bool)
   * - :ref:`min_(int,int->int)`
     - (int,int->int)
   * - :ref:`min_([int]->int)`
     - ([int]->int)
   * - :ref:`max_(int,int->int)`
     - (int,int->int)
   * - :ref:`max_([int]->int)`
     - ([int]->int)
   * - :ref:`lcm_([int]->int)`
     - ([int]->int)
   * - :ref:`numer_(rat->int)`
     - (rat->int)
   * - :ref:`numer_(ratvec->vec)`
     - (ratvec->vec)
   * - :ref:`denom_(rat->int)`
     - (rat->int)
   * - :ref:`denom_(ratvec->int)`
     - (ratvec->int)
   * - :ref:`is_integer_(rat->bool)`
     - (rat->bool)
   * - :ref:`is_integer_(ratvec->bool)`
     - (ratvec->bool)
   * - :ref:`floor_(rat->int)`
     - (rat->int)
   * - :ref:`floor_([rat]->vec)`
     - ([rat]->vec)
   * - :ref:`ceil_(rat->int)`
     - (rat->int)
   * - :ref:`ceil_([rat]->vec)`
     - ([rat]->vec)
   * - :ref:`rat_as_int_(rat->int)`
     - (rat->int)
   * - :ref:`plural_(int->string)`
     - (int->string)
   * - :ref:`split_lines_(string->[string])`
     - (string->[string])
   * - :ref:`is_substring_(string,string->bool)`
     - (string,string->bool)
   * - :ref:`fgrep_(string,string->[string])`
     - (string,string->[string])
   * - :ref:`vector_(int,(int->int)->vec)`
     - (int,(int->int)->vec)
   * - :ref:`ones_(int->vec)`
     - (int->vec)
   * - :ref:`gcd_([int]->int)`
     - ([int]->int)
   * - :ref:`sum_(vec->int)`
     - (vec->int)
   * - :ref:`sum_(mat->vec)`
     - (mat->vec)
   * - :ref:`sum_([ratvec],int->ratvec)`
     - ([ratvec],int->ratvec)
   * - :ref:`sum_(ratvec->rat)`
     - (ratvec->rat)
   * - :ref:`product_(vec->int)`
     - (vec->int)
   * - :ref:`reverse_(vec->vec)`
     - (vec->vec)
   * - :ref:`reverse_(ratvec->ratvec)`
     - (ratvec->ratvec)
   * - :ref:`lower_(int,vec->vec)`
     - (int,vec->vec)
   * - :ref:`lower_(int,ratvec->ratvec)`
     - (int,ratvec->ratvec)
   * - :ref:`upper_(int,vec->vec)`
     - (int,vec->vec)
   * - :ref:`upper_(int,ratvec->ratvec)`
     - (int,ratvec->ratvec)
   * - :ref:`drop_lower_(int,vec->vec)`
     - (int,vec->vec)
   * - :ref:`drop_lower_(int,ratvec->ratvec)`
     - (int,ratvec->ratvec)
   * - :ref:`drop_upper_(int,vec->vec)`
     - (int,vec->vec)
   * - :ref:`drop_upper_(int,ratvec->ratvec)`
     - (int,ratvec->ratvec)
   * - :ref:`is_member_([int]->(int->bool))`
     - ([int]->(int->bool))
   * - :ref:`contains_(int->([int]->bool))`
     - (int->([int]->bool))
   * - :ref:`all_0_1_vecs_(int->[vec])`
     - (int->[vec])
   * - :ref:`power_set_(int->[[int]])`
     - (int->[[int]])
   * - :ref:`power_set_([int]->[[int]])`
     - ([int]->[[int]])
   * - :ref:`matrix_((int,int),(int,int->int)->mat)`
     - ((int,int),(int,int->int)->mat)
   * - :ref:`n_rows_(mat->int)`
     - (mat->int)
   * - :ref:`n_columns_(mat->int)`
     - (mat->int)
   * - :ref:`column_(vec->mat)`
     - (vec->mat)
   * - :ref:`row_(vec->mat)`
     - (vec->mat)
   * - :ref:`map_on_(mat->((int->int)->mat))`
     - (mat->((int->int)->mat))
   * - :ref:`inverse_(mat->mat)`
     - (mat->mat)
   * - :ref:`det_(mat->int)`
     - (mat->int)
   * - :ref:`saturated_span_(mat->bool)`
     - (mat->bool)
   * - :ref:`columns_with_((int,vec->bool),mat->mat)`
     - ((int,vec->bool),mat->mat)
   * - :ref:`columns_with_((vec->bool),mat->mat)`
     - ((vec->bool),mat->mat)
   * - :ref:`columns_with_((int->bool),mat->mat)`
     - ((int->bool),mat->mat)
   * - :ref:`rows_with_((int,vec->bool),mat->mat)`
     - ((int,vec->bool),mat->mat)
   * - :ref:`rows_with_((vec->bool),mat->mat)`
     - ((vec->bool),mat->mat)
   * - :ref:`rows_with_((int->bool),mat->mat)`
     - ((int->bool),mat->mat)
   * - :ref:`lookup_column_(vec,mat->int)`
     - (vec,mat->int)
   * - :ref:`lookup_row_(vec,mat->int)`
     - (vec,mat->int)
   * - :ref:`solve_(mat,vec->[vec])`
     - (mat,vec->[vec])
   * - :ref:`solve_(mat,ratvec->[ratvec])`
     - (mat,ratvec->[ratvec])
   * - :ref:`order_(mat->int)`
     - (mat->int)
   * - :ref:`ratvec_as_vec_(ratvec->vec)`
     - (ratvec->vec)
   * - :ref:`int_part_(Split->int)`
     - (Split->int)
   * - :ref:`s_part_(Split->int)`
     - (Split->int)
   * - :ref:`s_to_1_(Split->int)`
     - (Split->int)
   * - :ref:`s_to_1_(ParamPol->ParamPol)`
     - (ParamPol->ParamPol)
   * - :ref:`s_to_minus_1_(Split->int)`
     - (Split->int)
   * - :ref:`s_to_minus_1_(ParamPol->ParamPol)`
     - (ParamPol->ParamPol)
   * - :ref:`split_as_int_(Split->int)`
     - (Split->int)
   * - :ref:`split_format_(Split->string)`
     - (Split->string)
   * - :ref:`is_root_(RootDatum,vec->bool)`
     - (RootDatum,vec->bool)
   * - :ref:`is_coroot_(RootDatum,vec->bool)`
     - (RootDatum,vec->bool)
   * - :ref:`is_posroot_(RootDatum,vec->bool)`
     - (RootDatum,vec->bool)
   * - :ref:`is_poscoroot_(RootDatum,vec->bool)`
     - (RootDatum,vec->bool)
   * - :ref:`posroot_index_(RootDatum,vec->int)`
     - (RootDatum,vec->int)
   * - :ref:`poscoroot_index_(RootDatum,vec->int)`
     - (RootDatum,vec->int)
   * - :ref:`rho_(RootDatum->ratvec)`
     - (RootDatum->ratvec)
   * - :ref:`rho_as_vec_(RootDatum->vec)`
     - (RootDatum->vec)
   * - :ref:`rho_check_(RootDatum->ratvec)`
     - (RootDatum->ratvec)
   * - :ref:`is_positive_root_(RootDatum->(vec->bool))`
     - (RootDatum->(vec->bool))
   * - :ref:`is_positive_root_(RootDatum,vec->bool)`
     - (RootDatum,vec->bool)
   * - :ref:`is_positive_coroot_(RootDatum->(vec->bool))`
     - (RootDatum->(vec->bool))
   * - :ref:`is_positive_coroot_(RootDatum,vec->bool)`
     - (RootDatum,vec->bool)
   * - :ref:`is_negative_root_(RootDatum->(vec->bool))`
     - (RootDatum->(vec->bool))
   * - :ref:`is_negative_root_(RootDatum,vec->bool)`
     - (RootDatum,vec->bool)
   * - :ref:`is_negative_coroot_(RootDatum->(vec->bool))`
     - (RootDatum->(vec->bool))
   * - :ref:`is_negative_coroot_(RootDatum,vec->bool)`
     - (RootDatum,vec->bool)
   * - :ref:`roots_all_positive_(RootDatum->(mat->bool))`
     - (RootDatum->(mat->bool))
   * - :ref:`roots_(RootDatum->mat)`
     - (RootDatum->mat)
   * - :ref:`coroots_all_positive_(RootDatum->(mat->bool))`
     - (RootDatum->(mat->bool))
   * - :ref:`coroots_(RootDatum->mat)`
     - (RootDatum->mat)
   * - :ref:`among_posroots_(RootDatum->(mat->bool))`
     - (RootDatum->(mat->bool))
   * - :ref:`among_poscoroots_(RootDatum->(mat->bool))`
     - (RootDatum->(mat->bool))
   * - :ref:`negative_system_(mat->mat)`
     - (mat->mat)
   * - :ref:`reflection_(RootDatum,int->mat)`
     - (RootDatum,int->mat)
   * - :ref:`reflection_(RootDatum,vec->mat)`
     - (RootDatum,vec->mat)
   * - :ref:`coreflection_(RootDatum,int->mat)`
     - (RootDatum,int->mat)
   * - :ref:`coreflection_(RootDatum,vec->mat)`
     - (RootDatum,vec->mat)
   * - :ref:`reflect_(RootDatum,int,vec->vec)`
     - (RootDatum,int,vec->vec)
   * - :ref:`reflect_(RootDatum,vec,vec->vec)`
     - (RootDatum,vec,vec->vec)
   * - :ref:`reflect_(RootDatum,int,ratvec->ratvec)`
     - (RootDatum,int,ratvec->ratvec)
   * - :ref:`reflect_(RootDatum,vec,ratvec->ratvec)`
     - (RootDatum,vec,ratvec->ratvec)
   * - :ref:`coreflect_(RootDatum,vec,int->vec)`
     - (RootDatum,vec,int->vec)
   * - :ref:`coreflect_(RootDatum,vec,vec->vec)`
     - (RootDatum,vec,vec->vec)
   * - :ref:`coreflect_(RootDatum,ratvec,int->ratvec)`
     - (RootDatum,ratvec,int->ratvec)
   * - :ref:`coreflect_(RootDatum,ratvec,vec->ratvec)`
     - (RootDatum,ratvec,vec->ratvec)
   * - :ref:`left_reflect_(RootDatum,int,mat->mat)`
     - (RootDatum,int,mat->mat)
   * - :ref:`left_reflect_(RootDatum,vec,mat->mat)`
     - (RootDatum,vec,mat->mat)
   * - :ref:`right_reflect_(RootDatum,mat,int->mat)`
     - (RootDatum,mat,int->mat)
   * - :ref:`right_reflect_(RootDatum,mat,vec->mat)`
     - (RootDatum,mat,vec->mat)
   * - :ref:`conjugate_(RootDatum,int,mat->mat)`
     - (RootDatum,int,mat->mat)
   * - :ref:`conjugate_(RootDatum,vec,mat->mat)`
     - (RootDatum,vec,mat->mat)
   * - :ref:`singular_simple_indices_(RootDatum,ratvec->[int])`
     - (RootDatum,ratvec->[int])
   * - :ref:`is_imaginary_(mat->(vec->bool))`
     - (mat->(vec->bool))
   * - :ref:`is_imaginary_(int,KGBElt->bool)`
     - (int,KGBElt->bool)
   * - :ref:`is_imaginary_(KGBElt->(vec->bool))`
     - (KGBElt->(vec->bool))
   * - :ref:`is_imaginary_(vec,KGBElt->bool)`
     - (vec,KGBElt->bool)
   * - :ref:`is_real_(mat->(vec->bool))`
     - (mat->(vec->bool))
   * - :ref:`is_real_(int,KGBElt->bool)`
     - (int,KGBElt->bool)
   * - :ref:`is_real_(KGBElt->(vec->bool))`
     - (KGBElt->(vec->bool))
   * - :ref:`is_real_(vec,KGBElt->bool)`
     - (vec,KGBElt->bool)
   * - :ref:`is_complex_(mat->(vec->bool))`
     - (mat->(vec->bool))
   * - :ref:`is_complex_(int,KGBElt->bool)`
     - (int,KGBElt->bool)
   * - :ref:`is_complex_(KGBElt->(vec->bool))`
     - (KGBElt->(vec->bool))
   * - :ref:`is_complex_(vec,KGBElt->bool)`
     - (vec,KGBElt->bool)
   * - :ref:`imaginary_roots_(RootDatum,mat->mat)`
     - (RootDatum,mat->mat)
   * - :ref:`real_roots_(RootDatum,mat->mat)`
     - (RootDatum,mat->mat)
   * - :ref:`imaginary_coroots_(RootDatum,mat->mat)`
     - (RootDatum,mat->mat)
   * - :ref:`real_coroots_(RootDatum,mat->mat)`
     - (RootDatum,mat->mat)
   * - :ref:`imaginary_posroots_(RootDatum,mat->mat)`
     - (RootDatum,mat->mat)
   * - :ref:`imaginary_posroots_(KGBElt->mat)`
     - (KGBElt->mat)
   * - :ref:`real_posroots_(RootDatum,mat->mat)`
     - (RootDatum,mat->mat)
   * - :ref:`real_posroots_(KGBElt->mat)`
     - (KGBElt->mat)
   * - :ref:`imaginary_poscoroots_(RootDatum,mat->mat)`
     - (RootDatum,mat->mat)
   * - :ref:`imaginary_poscoroots_(KGBElt->mat)`
     - (KGBElt->mat)
   * - :ref:`real_poscoroots_(RootDatum,mat->mat)`
     - (RootDatum,mat->mat)
   * - :ref:`real_poscoroots_(KGBElt->mat)`
     - (KGBElt->mat)
   * - :ref:`imaginary_sys_(RootDatum,mat->mat,mat)`
     - (RootDatum,mat->mat,mat)
   * - :ref:`imaginary_sys_(KGBElt->mat,mat)`
     - (KGBElt->mat,mat)
   * - :ref:`real_sys_(RootDatum,mat->mat,mat)`
     - (RootDatum,mat->mat,mat)
   * - :ref:`real_sys_(KGBElt->mat,mat)`
     - (KGBElt->mat,mat)
   * - :ref:`is_dominant_(RootDatum,ratvec->bool)`
     - (RootDatum,ratvec->bool)
   * - :ref:`is_strictly_dominant_(RootDatum,ratvec->bool)`
     - (RootDatum,ratvec->bool)
   * - :ref:`is_regular_(RootDatum,ratvec->bool)`
     - (RootDatum,ratvec->bool)
   * - :ref:`is_regular_(Param->bool)`
     - (Param->bool)
   * - :ref:`is_integral_(RootDatum,ratvec->bool)`
     - (RootDatum,ratvec->bool)
   * - :ref:`radical_basis_(RootDatum->mat)`
     - (RootDatum->mat)
   * - :ref:`coradical_basis_(RootDatum->mat)`
     - (RootDatum->mat)
   * - :ref:`is_semisimple_(RootDatum->bool)`
     - (RootDatum->bool)
   * - :ref:`derived_is_simply_connected_(RootDatum->bool)`
     - (RootDatum->bool)
   * - :ref:`has_connected_center_(RootDatum->bool)`
     - (RootDatum->bool)
   * - :ref:`is_simply_connected_(RootDatum->bool)`
     - (RootDatum->bool)
   * - :ref:`is_adjoint_(RootDatum->bool)`
     - (RootDatum->bool)
   * - :ref:`derived_(RootDatum->RootDatum)`
     - (RootDatum->RootDatum)
   * - :ref:`mod_central_torus_(RootDatum->RootDatum)`
     - (RootDatum->RootDatum)
   * - :ref:`is_simple_for_(vec->(vec->bool))`
     - (vec->(vec->bool))
   * - :ref:`simple_from_positive_(mat,mat->mat,mat)`
     - (mat,mat->mat,mat)
   * - :ref:`fundamental_weights_(RootDatum->[ratvec])`
     - (RootDatum->[ratvec])
   * - :ref:`fundamental_coweights_(RootDatum->[ratvec])`
     - (RootDatum->[ratvec])
   * - :ref:`dual_integral_(InnerClass,ratvec->InnerClass)`
     - (InnerClass,ratvec->InnerClass)
   * - :ref:`Cartan_classes_(InnerClass->[CartanClass])`
     - (InnerClass->[CartanClass])
   * - :ref:`print_Cartan_info_(CartanClass->)`
     - (CartanClass->)
   * - :ref:`fundamental_Cartan_(InnerClass->CartanClass)`
     - (InnerClass->CartanClass)
   * - :ref:`compact_rank_(CartanClass->int)`
     - (CartanClass->int)
   * - :ref:`compact_rank_(InnerClass->int)`
     - (InnerClass->int)
   * - :ref:`split_rank_(CartanClass->int)`
     - (CartanClass->int)
   * - :ref:`split_rank_(RealForm->int)`
     - (RealForm->int)
   * - :ref:`number_(CartanClass,RealForm->int)`
     - (CartanClass,RealForm->int)
   * - :ref:`form_name_(RealForm->string)`
     - (RealForm->string)
   * - :ref:`is_quasisplit_(RealForm->bool)`
     - (RealForm->bool)
   * - :ref:`is_quasicompact_(RealForm->bool)`
     - (RealForm->bool)
   * - :ref:`split_form_(RootDatum->RealForm)`
     - (RootDatum->RealForm)
   * - :ref:`split_form_(LieType->RealForm)`
     - (LieType->RealForm)
   * - :ref:`quasicompact_form_(InnerClass->RealForm)`
     - (InnerClass->RealForm)
   * - :ref:`is_compatible_(RealForm,RealForm->bool)`
     - (RealForm,RealForm->bool)
   * - :ref:`is_compact_(RealForm->bool)`
     - (RealForm->bool)
   * - :ref:`is_compact_(int,KGBElt->bool)`
     - (int,KGBElt->bool)
   * - :ref:`is_compact_(KGBElt->(vec->bool))`
     - (KGBElt->(vec->bool))
   * - :ref:`KGB_status_text_(int->string)`
     - (int->string)
   * - :ref:`status_text_(int,KGBElt->string)`
     - (int,KGBElt->string)
   * - :ref:`status_text_(vec,KGBElt->string)`
     - (vec,KGBElt->string)
   * - :ref:`status_text_(int,Param->string)`
     - (int,Param->string)
   * - :ref:`status_text_(vec,Param->string)`
     - (vec,Param->string)
   * - :ref:`status_texts_(KGBElt->[string])`
     - (KGBElt->[string])
   * - :ref:`status_texts_(Param->[string])`
     - (Param->[string])
   * - :ref:`is_noncompact_(int,KGBElt->bool)`
     - (int,KGBElt->bool)
   * - :ref:`is_noncompact_(KGBElt->(vec->bool))`
     - (KGBElt->(vec->bool))
   * - :ref:`is_descent_(int,KGBElt->bool)`
     - (int,KGBElt->bool)
   * - :ref:`is_descent_(int,Param->bool)`
     - (int,Param->bool)
   * - :ref:`is_descent_(vec,Param->bool)`
     - (vec,Param->bool)
   * - :ref:`is_ascent_(int,KGBElt->bool)`
     - (int,KGBElt->bool)
   * - :ref:`is_strict_descent_(int,KGBElt->bool)`
     - (int,KGBElt->bool)
   * - :ref:`rho_i_(KGBElt->ratvec)`
     - (KGBElt->ratvec)
   * - :ref:`rho_i_(RootDatum,mat->ratvec)`
     - (RootDatum,mat->ratvec)
   * - :ref:`rho_r_(KGBElt->ratvec)`
     - (KGBElt->ratvec)
   * - :ref:`rho_r_(RootDatum,mat->ratvec)`
     - (RootDatum,mat->ratvec)
   * - :ref:`rho_check_i_(KGBElt->ratvec)`
     - (KGBElt->ratvec)
   * - :ref:`rho_check_i_(RootDatum,mat->ratvec)`
     - (RootDatum,mat->ratvec)
   * - :ref:`rho_check_r_(KGBElt->ratvec)`
     - (KGBElt->ratvec)
   * - :ref:`rho_check_r_(RootDatum,mat->ratvec)`
     - (RootDatum,mat->ratvec)
   * - :ref:`is_compact_imaginary_(KGBElt->(vec->bool))`
     - (KGBElt->(vec->bool))
   * - :ref:`is_compact_imaginary_(vec,KGBElt->bool)`
     - (vec,KGBElt->bool)
   * - :ref:`is_noncompact_imaginary_(KGBElt->(vec->bool))`
     - (KGBElt->(vec->bool))
   * - :ref:`is_noncompact_imaginary_(vec,KGBElt->bool)`
     - (vec,KGBElt->bool)
   * - :ref:`compact_posroots_(KGBElt->mat)`
     - (KGBElt->mat)
   * - :ref:`noncompact_posroots_(KGBElt->mat)`
     - (KGBElt->mat)
   * - :ref:`rho_ci_(KGBElt->ratvec)`
     - (KGBElt->ratvec)
   * - :ref:`rho_nci_(KGBElt->ratvec)`
     - (KGBElt->ratvec)
   * - :ref:`no_Cminus_roots_(KGBElt->bool)`
     - (KGBElt->bool)
   * - :ref:`no_Cplus_roots_(KGBElt->bool)`
     - (KGBElt->bool)
   * - :ref:`blocks_(InnerClass->[Block])`
     - (InnerClass->[Block])
   * - :ref:`lambda_minus_rho_(Param->vec)`
     - (Param->vec)
   * - :ref:`lambda_(Param->ratvec)`
     - (Param->ratvec)
   * - :ref:`infinitesimal_character_(Param->ratvec)`
     - (Param->ratvec)
   * - :ref:`infinitesimal_character_(ParamPol->ratvec)`
     - (ParamPol->ratvec)
   * - :ref:`nu_(Param->ratvec)`
     - (Param->ratvec)
   * - :ref:`trivial_(RealForm->Param)`
     - (RealForm->Param)
   * - :ref:`parameter_(RealForm,int,ratvec,ratvec->Param)`
     - (RealForm,int,ratvec,ratvec->Param)
   * - :ref:`parameter_(KGBElt,ratvec,ratvec->Param)`
     - (KGBElt,ratvec,ratvec->Param)
   * - :ref:`parameter_gamma_(KGBElt,ratvec,ratvec->Param)`
     - (KGBElt,ratvec,ratvec->Param)
   * - :ref:`block_of_(Param->[Param])`
     - (Param->[Param])
   * - :ref:`imaginary_type_(int,Param->int)`
     - (int,Param->int)
   * - :ref:`imaginary_type_(vec,Param->int)`
     - (vec,Param->int)
   * - :ref:`real_type_(int,Param->int)`
     - (int,Param->int)
   * - :ref:`real_type_(vec,Param->int)`
     - (vec,Param->int)
   * - :ref:`is_nonparity_(int,Param->bool)`
     - (int,Param->bool)
   * - :ref:`is_nonparity_(vec,Param->bool)`
     - (vec,Param->bool)
   * - :ref:`is_parity_(int,Param->bool)`
     - (int,Param->bool)
   * - :ref:`is_parity_(vec,Param->bool)`
     - (vec,Param->bool)
   * - :ref:`block_status_text_(int->string)`
     - (int->string)
   * - :ref:`parity_poscoroots_(Param->mat)`
     - (Param->mat)
   * - :ref:`nonparity_poscoroots_(Param->mat)`
     - (Param->mat)
   * - :ref:`tau_bitset_(Param->(int->bool),int)`
     - (Param->(int->bool),int)
   * - :ref:`tau_(Param->[int])`
     - (Param->[int])
   * - :ref:`tau_complement_(Param->[int])`
     - (Param->[int])
   * - :ref:`lookup_(Param,[Param]->int)`
     - (Param,[Param]->int)
   * - :ref:`first_param_(ParamPol->Param)`
     - (ParamPol->Param)
   * - :ref:`last_param_(ParamPol->Param)`
     - (ParamPol->Param)
   * - :ref:`virtual_(Param->ParamPol)`
     - (Param->ParamPol)
   * - :ref:`virtual_(RealForm,[Param]->ParamPol)`
     - (RealForm,[Param]->ParamPol)
   * - :ref:`pol_format_(ParamPol->)`
     - (ParamPol->)
   * - :ref:`separate_by_infinitesimal_character_(ParamPol->[(ratvec,ParamPol)])`
     - (ParamPol->[(ratvec,ParamPol)])
   * - :ref:`in_string_list_(string,[string]->bool)`
     - (string,[string]->bool)
   * - :ref:`positive_imaginary_roots_and_coroots_(RootDatum,mat->mat,mat)`
     - (RootDatum,mat->mat,mat)
   * - :ref:`positive_imaginary_roots_and_coroots_(KGBElt->mat,mat)`
     - (KGBElt->mat,mat)
   * - :ref:`imaginary_roots_and_coroots_(RootDatum,mat->mat,mat)`
     - (RootDatum,mat->mat,mat)
   * - :ref:`imaginary_roots_and_coroots_(KGBElt->mat,mat)`
     - (KGBElt->mat,mat)
   * - :ref:`positive_real_roots_and_coroots_(RootDatum,mat->mat,mat)`
     - (RootDatum,mat->mat,mat)
   * - :ref:`positive_real_roots_and_coroots_(KGBElt->mat,mat)`
     - (KGBElt->mat,mat)
   * - :ref:`real_roots_and_coroots_(RootDatum,mat->mat,mat)`
     - (RootDatum,mat->mat,mat)
   * - :ref:`real_roots_and_coroots_(KGBElt->mat,mat)`
     - (KGBElt->mat,mat)
   * - :ref:`complex_posroots_(RootDatum,mat->mat)`
     - (RootDatum,mat->mat)
   * - :ref:`complex_posroots_(KGBElt->mat)`
     - (KGBElt->mat)
   * - :ref:`monomials_(ParamPol->[Param])`
     - (ParamPol->[Param])
   * - :ref:`monomial_(ParamPol,int->Param)`
     - (ParamPol,int->Param)
   * - :ref:`delete_([int],int->[int])`
     - ([int],int->[int])
   * - :ref:`delete_([vec],int->[vec])`
     - ([vec],int->[vec])
   * - :ref:`delete_([ratvec],int->[ratvec])`
     - ([ratvec],int->[ratvec])
   * - :ref:`delete_([[vec]],int->[[vec]])`
     - ([[vec]],int->[[vec]])
   * - :ref:`delete_([[ratvec]],int->[[ratvec]])`
     - ([[ratvec]],int->[[ratvec]])
   * - :ref:`delete_([ParamPol],int->[ParamPol])`
     - ([ParamPol],int->[ParamPol])
   * - :ref:`find_([int],int->int)`
     - ([int],int->int)
   * - :ref:`find_([Param],Param->int)`
     - ([Param],Param->int)
   * - :ref:`find_([KGBElt],KGBElt->int)`
     - ([KGBElt],KGBElt->int)
   * - :ref:`find_([[int]],[int]->int)`
     - ([[int]],[int]->int)
   * - :ref:`find_vec_([vec],vec->int)`
     - ([vec],vec->int)
   * - :ref:`pad_(string,int->string)`
     - (string,int->string)
