.. _polynomial.at_index:

polynomial.at Function Index
=======================================================
|



Functions

.. list-table::
   :widths: 10 20
   :header-rows: 1

   * - Function
     - Argument(s) -> Results
   * - :ref:`strip_poly_v->poly1`
     - ``poly v->poly``
   * - :ref:`eval_poly_v,int_k->int1`
     - ``poly v,int k->int``
   * - :ref:`eval_vec_v,split_w->split1`
     - ``vec v,Split w->Split``
   * - :ref:`at_s_vec_v->split:_eval(v,split1`
     - ``vec v->Split: eval(v,Split``
   * - :ref:`transpose_poly_mat_m->poly_mat1`
     - ``poly_mat M->poly_mat``
   * - :ref:`dot_product_[poly]_v,[poly]_w->poly1`
     - ``[poly] v,[poly] w->poly``
   * - :ref:`\*_poly_mat_A,poly_mat_B->poly_mat1`
     - ``poly_mat A,poly_mat B->poly_mat``
   * - :ref:`poly_list_add_[poly]_v,[poly]_w->[poly]1`
     - ``[poly] v,[poly] w->[poly]``
   * - :ref:`poly_list_sub_[poly]_v,[poly]_w->[poly]1`
     - ``[poly] v,[poly] w->[poly]``
   * - :ref:`\-_poly_mat_M->poly_mat1`
     - ``poly_mat M->poly_mat``
   * - :ref:`\+_poly_mat_A,poly_mat_B->poly_mat1`
     - ``poly_mat A,poly_mat B->poly_mat``
   * - :ref:`\-_poly_mat_A,poly_mat_B->poly_mat1`
     - ``poly_mat A,poly_mat B->poly_mat``
   * - :ref:`scalar_multiply_[poly]_v,poly_f->[poly]1`
     - ``[poly] v,poly f->[poly]``
   * - :ref:`\*_poly_f,poly_mat_M->poly_mat1`
     - ``poly f,poly_mat M->poly_mat``
   * - :ref:`\*_int_c,_poly_mat_M->poly_mat1`
     - ``int c, poly_mat M->poly_mat``
   * - :ref:`update_row_[poly]_r,_int_j,poly_v->[poly]:_r[j]1`
     - ``[poly] R, int j,poly v->[poly]: R[j]``
   * - :ref:`update_matrix_row_poly_mat_m,_int_i,_[poly]_row->poly_mat:_m[i]1`
     - ``poly_mat M, int i, [poly] row->poly_mat: M[i]``
   * - :ref:`update_matrix_entry_poly_mat_m,_int_i,_int_j,_poly_v->poly_mat1`
     - ``poly_mat M, int i, int j, poly v->poly_mat``
   * - :ref:`zero_poly_row_int_n->[poly]:_for_i1`
     - ``int n->[poly]: for i``
   * - :ref:`zero_poly_matrix_int_n->poly_mat1`
     - ``int n->poly_mat``
   * - :ref:`scalar_poly_matrix_int_n,_int_c->poly_mat1`
     - ``int n, int c->poly_mat``
   * - :ref:`\+_poly_mat_M,_poly_p->poly_mat1`
     - ``poly_mat M, poly p->poly_mat``
   * - :ref:`\-_poly_mat_M,_poly_p->poly_mat1`
     - ``poly_mat M, poly p->poly_mat``
   * - :ref:`\=_poly_mat_A,poly_mat_B->bool1`
     - ``poly_mat A,poly_mat B->bool``
   * - :ref:`is_zero_poly_mat_m->bool1`
     - ``poly_mat M->bool``
   * - :ref:`upper_unitriangular_inverse_poly_mat_p->poly_mat1`
     - ``poly_mat P->poly_mat``
   * - :ref:`poly_permute_basis_poly_p,_poly_mat_a->poly_mat1`
     - ``poly P, poly_mat A->poly_mat``
   * - :ref:`stringpoly_poly_v,_string_q->string1`
     - ``poly v, string q->string``
   * - :ref:`printpoly_poly_v->void1`
     - ``poly v->void``
   * - :ref:`printpolymatrix_poly_mat_m,int_space_size->void1`
     - ``poly_mat M,int space_size->void``
   * - :ref:`printpolymatrix_poly_mat_m->void1`
     - ``poly_mat M->void``
   * - :ref:`sgn_poly_int_k->poly1`
     - ``int k->poly``
   * - :ref:`divide_by_int_k,_poly_v->poly1`
     - ``int k, poly v->poly``


Data Types

.. list-table::
   :widths: 10 20
   :header-rows: 1

   * - Data Type Name
     - Definition
   * - :ref:`poly1`
     - ``vec``
   * - :ref:`poly_mat1`
     - ``[[poly]]``
