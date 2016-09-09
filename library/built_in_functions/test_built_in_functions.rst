atlas Built-In Operators and Functions
==============================================

.. list-table::
   :widths: 10 20
   :header-rows: 1

   * - Function
     - Argument(s) -> Results
   * - \+
     - (int,int->int)
   * - \+
     - (rat,int->rat)
   * - \+
     - (rat,rat->rat)
   * - \+
     - (vec,vec->vec)
   * - \+
     - (ratvec,ratvec->ratvec)
   * - \+
     - (mat,int->mat)
   * - \+
     - (int,mat->mat)
   * - \+
     - (mat,mat->mat)
   * - \+
     - (Split,Split->Split)
   * - \+
     - (ParamPol,Param->ParamPol)
   * - \+
     - (ParamPol,(Split,Param)->ParamPol)
   * - \+
     - (ParamPol,[(Split,Param)]->ParamPol)
   * - \+
     - (ParamPol,ParamPol->ParamPol)
   * - \-
     - (int,int->int)
   * - \-
     - (int->int)
   * - \-
     - (rat,int->rat)
   * - \-
     - (rat,rat->rat)
   * - \-
     - (rat->rat)
   * - \-
     - (vec,vec->vec)
   * - \-
     - (vec->vec)
   * - \-
     - (ratvec,ratvec->ratvec)
   * - \-
     - (ratvec->ratvec)
   * - \-
     - (mat,int->mat)
   * - \-
     - (int,mat->mat)
   * - \-
     - (mat,mat->mat)
   * - \-
     - (Split,Split->Split)
   * - \-
     - (Split->Split)
   * - \-
     - (ParamPol,Param->ParamPol)
   * - \-
     - (ParamPol,ParamPol->ParamPol)
   * - \*
     - (int,int->int)
   * - \*
     - (rat,int->rat)
   * - \*
     - (rat,rat->rat)
   * - \*
     - (vec,int->vec)
   * - \*
     - (ratvec,int->ratvec)
   * - \*
     - (ratvec,rat->ratvec)
   * - \*
     - (vec,vec->int)
   * - \*
     - (mat,vec->vec)
   * - \*
     - (mat,ratvec->ratvec)
   * - \*
     - (mat,mat->mat)
   * - \*
     - (vec,mat->vec)
   * - \*
     - (ratvec,mat->ratvec)
   * - \*
     - (Split,Split->Split)
   * - \*
     - (int,ParamPol->ParamPol)
   * - \*
     - (Split,ParamPol->ParamPol)
   * - \\
     - (int,int->int)
   * - \\
     - (vec,int->vec)
   * - %
     - (int,int->int)
   * - %
     - (rat->int,int)
   * - %
     - (rat,int->rat)
   * - %
     - (rat,rat->rat)
   * - %
     - (vec,int->vec)
   * - %
     - (ratvec->vec,int)
   * - %
     - (ratvec,int->ratvec)
   * - %
     - (LieType->[LieType])
   * - %
     - (KGBElt->RealForm,int)
   * - %
     - (Block->RealForm,RealForm)
   * - %
     - (Param->KGBElt,vec,ratvec)
   * - %
     - (Split->int,int)
   * - \%
     - (int,int->int,int)
   * - ^
     - (int,int->int)
   * - ^
     - (rat,int->rat)
   * - ^
     - (vec->mat)
   * - ^
     - (mat->mat)
   * - ^
     - (int,[vec]->mat)
   * - /
     - (int,int->rat)
   * - /
     - (rat,int->rat)
   * - /
     - (rat,rat->rat)
   * - /
     - (rat->rat)
   * - /
     - (vec,int->ratvec)
   * - /
     - (ratvec,int->ratvec)
   * - /
     - (ratvec,rat->ratvec)
   * - =
     - (int->bool)
   * - =
     - (int,int->bool)
   * - =
     - (rat->bool)
   * - =
     - (rat,rat->bool)
   * - =
     - (bool,bool->bool)
   * - =
     - (string->bool)
   * - =
     - (string,string->bool)
   * - =
     - (vec->bool)
   * - =
     - (vec,vec->bool)
   * - =
     - (ratvec->bool)
   * - =
     - (ratvec,ratvec->bool)
   * - =
     - (mat->bool)
   * - =
     - (mat,mat->bool)
   * - =
     - (RealForm,RealForm->bool)
   * - =
     - (InnerClass,InnerClass->bool)
   * - =
     - (KGBElt,KGBElt->bool)
   * - =
     - (Param,Param->bool)
   * - =
     - (Split->bool)
   * - =
     - (Split,Split->bool)
   * - =
     - (ParamPol->bool)
   * - =
     - (ParamPol,ParamPol->bool)
   * - !=
     - (int->bool)
   * - !=
     - (int,int->bool)
   * - !=
     - (rat->bool)
   * - !=
     - (rat,rat->bool)
   * - !=
     - (bool,bool->bool)
   * - !=
     - (string->bool)
   * - !=
     - (string,string->bool)
   * - !=
     - (vec->bool)
   * - !=
     - (vec,vec->bool)
   * - !=
     - (ratvec->bool)
   * - !=
     - (ratvec,ratvec->bool)
   * - !=
     - (mat->bool)
   * - !=
     - (mat,mat->bool)
   * - !=
     - (Split->bool)
   * - !=
     - (Split,Split->bool)
   * - !=
     - (ParamPol->bool)
   * - !=
     - (ParamPol,ParamPol->bool)
   * - >=
     - (int->bool)
   * - >=
     - (int,int->bool)
   * - >=
     - (rat->bool)
   * - >=
     - (rat,rat->bool)
   * - >=
     - (string,string->bool)
   * - >=
     - (vec->bool)
   * - >=
     - (ratvec->bool)
   * - >
     - (int->bool)
   * - >
     - (int,int->bool)
   * - >
     - (rat->bool)
   * - >
     - (rat,rat->bool)
   * - >
     - (string,string->bool)
   * - >
     - (vec->bool)
   * - >
     - (ratvec->bool)
   * - <=
     - (int->bool)
   * - <=
     - (int,int->bool)
   * - <=
     - (rat->bool)
   * - <=
     - (rat,rat->bool)
   * - <=
     - (string,string->bool)
   * - <
     - (int->bool)
   * - <
     - (int,int->bool)
   * - <
     - (rat->bool)
   * - <
     - (rat,rat->bool)
   * - <
     - (string,string->bool)
   * - ##
     - (string,string->string)
   * - ##
     - ([string]->string)
   * - ##
     - (vec,vec->vec)
   * - ##
     - ([vec]->vec)
   * - int_format
     - (int->string)
   * - ascii
     - (string->int)
   * - ascii
     - (int->string)
   * - #
     - (string->int)
   * - #
     - (vec->int)
   * - #
     - (ratvec->int)
   * - #
     - (mat->int,int)
   * - #
     - (vec,int->vec)
   * - #
     - (int,vec->vec)
   * - #
     - (int,[vec]->mat)
   * - #
     - (LieType->int)
   * - #
     - (Block->int)
   * - #
     - (ParamPol->int)
   * - flex_add
     - (vec,vec->vec)
   * - flex_sub
     - (vec,vec->vec)
   * - convolve
     - (vec,vec->vec)
   * - null
     - (int->vec)
   * - null
     - (int,int->mat)
   * - transpose 
     - (mat->mat)
   * - id_mat
     - (int->mat)
   * - diagonal
     - (vec->mat)
   * - stack_rows
     - ([vec]->mat)
   * - swiss_matrix_knife
     - (int,mat,int,int,int,int->mat)
   * - matrix slicer
     - (int,mat,int,int,int,int->mat)
   * - echelon
     - (mat->mat,[int])
   * - diagonalize
     - (mat->vec,mat,mat)
   * - adapted_basis
     - (mat->mat,vec)
   * - kernel
     - (mat->mat)
   * - eigen_lattice
     - (mat,int->mat)
   * - row_saturate
     - (mat->mat)
   * - inv_fact
     - (mat->vec)
   * - Smith_basis
     - (mat->mat)
   * - Smith
     - (mat->mat,vec)
   * - invert
     - (mat->mat,int)
   * - mod2_section
     - (mat->mat)
   * - subspace_normal
     - (mat->mat,mat,mat,[int])
   * - Lie_type
     - (string->LieType)
   * - Lie_type
     - (RootDatum->LieType)
   * - Cartan_matrix
     - (LieType->mat)
   * - Cartan_matrix
     - (RootDatum->mat)
   * - Cartan_matrix_type
     - (mat->LieType,vec)
   * - rank
     - (LieType->int)
   * - rank
     - (RootDatum->int)
   * - semisimple_rank
     - (LieType->int)
   * - semisimple_rank
     - (RootDatum->int)
   * - str
     - (LieType->string)
   * - Smith_Cartan
     - (LieType->mat,vec)
   * - filter_units
     - (mat,vec->mat,vec)
   * - ann_mod
     - (mat,int->mat)
   * - replace_gen
     - ((mat,vec),mat->mat)
   * - quotient_basis
     - (LieType,[ratvec]->mat)
   * - involution
     - (LieType,string->mat)
   * - involution
     - (LieType,mat,string->mat)
   * - involution
     - (CartanClass->mat)
   * - involution
     - (KGBElt->mat)
   * - root_datum
     - (mat,mat->RootDatum)
   * - root_datum
     - (LieType,mat->RootDatum)
   * - root_datum
     - (RootDatum,mat->RootDatum)
   * - root_datum
     - (InnerClass->RootDatum)
   * - simply_connected
     - (LieType->RootDatum)
   * - adjoint
     - (LieType->RootDatum)
   * - root
     - (RootDatum,int->vec)
   * - coroot
     - (RootDatum,int->vec)
   * - simple_roots
     - (RootDatum->mat)
   * - simple_coroots
     - (RootDatum->mat)
   * - posroots
     - (RootDatum->mat)
   * - poscoroots
     - (RootDatum->mat)
   * - root_coradical
     - (RootDatum->mat)
   * - coroot_radical
     - (RootDatum->mat)
   * - fundamental_weight
     - (RootDatum,int->ratvec)
   * - fundamental_coweight
     - (RootDatum,int->ratvec)
   * - dual
     - (InnerClass->InnerClass)
   * - dual
     - (RootDatum->RootDatum)
   * - dual
     - (Block->Block)
   * - derived_info
     - (RootDatum->RootDatum,mat)
   * - mod_central_torus_info
     - (RootDatum->RootDatum,mat)
   * - nr_of_posroots
     - (RootDatum->int)
   * - root_index
     - (RootDatum,vec->int)
   * - coroot_index
     - (RootDatum,vec->int)
   * - integrality_datum
     - (RootDatum,ratvec->RootDatum)
   * - integrality_points
     - (RootDatum,ratvec->[rat])
   * - classify_involution
     - (mat->int,int,int)
   * - inner_class
     - (RootDatum,mat->InnerClass)
   * - inner_class
     - (LieType,[ratvec],string->InnerClass)
   * - inner_class
     - (RootDatum,string->InnerClass)
   * - inner_class
     - (RealForm->InnerClass)
   * - twisted_involution
     - (RootDatum,mat->InnerClass,vec)
   * - distinguished_involution
     - (InnerClass->mat)
   * - form_names
     - (InnerClass->[string])
   * - dual_form_names
     - (InnerClass->[string])
   * - nr_of_real_forms
     - (InnerClass->int)
   * - nr_of_dual_real_forms
     - (InnerClass->int)
   * - nr_of_Cartan_classes
     - (InnerClass->int)
   * - block_sizes
     - (InnerClass->mat)
   * - occurrence_matrix
     - (InnerClass->mat)
   * - dual_occurrence_matrix
     - (InnerClass->mat)
   * - real_form
     - (InnerClass,int->RealForm)
   * - real_form
     - (InnerClass,mat,ratvec->RealForm)
   * - real_form
     - (Param->RealForm)
   * - real_form
     - (ParamPol->RealForm)
   * - form_number
     - (RealForm->int)
   * - quasisplit_form
     - (InnerClass->RealForm)
   * - components_rank
     - (RealForm->int)
   * - count_Cartans
     - (RealForm->int)
   * - KGB_size
     - (RealForm->int)
   * - base_grading_vector
     - (RealForm->ratvec)
   * - Cartan_order
     - (RealForm->mat)
   * - dual_real_form
     - (InnerClass,int->RealForm)
   * - dual_quasisplit_form
     - (InnerClass->RealForm)
   * - central_fiber
     - (RealForm->[vec])
   * - initial_torus_bits
     - (RealForm->vec)
   * - Cartan_class
     - (RealForm,int->CartanClass)
   * - Cartan_class
     - (InnerClass,int->CartanClass)
   * - Cartan_class
     - (KGBElt->CartanClass)
   * - most_split_Cartan
     - (RealForm->CartanClass)
   * - Cartan_info
     - (CartanClass->(int,int,int),vec,(int,int),(LieType,LieType,LieType))
   * - real_forms
     - (CartanClass->[RealForm])
   * - dual_real_forms
     - (CartanClass->[RealForm])
   * - fiber_partition
     - (CartanClass,RealForm->[int])
   * - square_classes
     - (CartanClass->[[int]])
   * - KGB
     - (RealForm,int->KGBElt)
   * - cross
     - (int,KGBElt->KGBElt)
   * - cross
     - (int,Block,int->int)
   * - cross
     - (int,Param->Param)
   * - cross
     - (vec,Param->Param)
   * - Cayley
     - (int,KGBElt->KGBElt)
   * - Cayley
     - (int,Block,int->int)
   * - Cayley
     - (int,Param->Param)
   * - Cayley
     - (vec,Param->Param)
   * - status
     - (int,KGBElt->int)
   * - status
     - (int,Block,int->int)
   * - KGB_elt
     - (RealForm,mat,ratvec->KGBElt)
   * - twist
     - (KGBElt->KGBElt)
   * - twist
     - (Param->Param)
   * - length
     - (KGBElt->int)
   * - length
     - (Param->int)
   * - torus_bits
     - (KGBElt->vec)
   * - torus_factor
     - (KGBElt->ratvec)
   * - block
     - (RealForm,RealForm->Block)
   * - block
     - (Param->[Param],int)
   * - element
     - (Block,int->KGBElt,KGBElt)
   * - index
     - (Block,KGBElt,KGBElt->int)
   * - inverse_Cayley
     - (int,Block,int->int)
   * - param
     - (KGBElt,vec,ratvec->Param)
   * - is_standard
     - (Param->bool)
   * - is_zero
     - (Param->bool)
   * - is_final
     - (Param->bool)
   * - dominant
     - (Param->Param)
   * - inv_Cayley
     - (int,Param->Param)
   * - orientation_nr
     - (Param->int)
   * - reducibility_points
     - (Param->[rat])
   * - print_block
     - (Param->)
   * - print_block
     - (Block->)
   * - partial_block
     - (Param->[Param])
   * - KL_block
     - (Param->[Param],int,mat,[vec],vec,vec,mat)
   * - partial_KL_block
     - (Param->[Param],mat,[vec],vec,vec,mat)
   * - null_module
     - (RealForm->ParamPol)
   * - last_term
     - (ParamPol->Split,Param)
   * - first_term
     - (ParamPol->Split,Param)
   * - K_type_formula
     - (Param->ParamPol)
   * - branch
     - (Param,int->ParamPol)
   * - to_canonical
     - (Param->Param)
   * - height
     - (Param->int)
   * - deform
     - (Param->ParamPol)
   * - full_deform
     - (Param->ParamPol)
   * - KL_sum_at_s
     - (Param->ParamPol)
   * - raw_KL
     - (Block->mat,[vec],vec)
   * - dual_KL
     - (Block->mat,[vec],vec)
   * - print_gradings
     - (CartanClass,RealForm->)
   * - print_real_Weyl
     - (RealForm,CartanClass->)
   * - print_strong_real
     - (CartanClass->)
   * - print_blocku
     - (Block->)
   * - print_blockd
     - (Block->)
   * - print_blockstabilizer
     - (Block,CartanClass->)
   * - print_KGB
     - (RealForm->)
   * - print_X
     - (InnerClass->)
   * - print_KL_basis
     - (Block->)
   * - print_prim_KL
     - (Block->)
   * - print_KL_list
     - (Block->)
   * - print_W_cells
     - (Block->)
   * - print_W_graph
     - (Block->)
   * - input_path
     - [string]
   * - prelude_log
     - [string]
