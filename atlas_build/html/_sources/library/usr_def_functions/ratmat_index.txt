.. _ratmat.at_index:

ratmat.at Function Index
=======================================================
|

.. list-table::
   :widths: 10 20
   :header-rows: 1

   * - Function
     - Argument(s) -> Results
   * - :ref:`gcd_mat_m->int1`
     - ``mat M->int``
   * - :ref:`simplify_ratmat(m,,d)->ratmat1`
     - ``ratmat(M,,d)->ratmat``
   * - :ref:`\/_mat_m,int_d->ratmat1`
     - ``mat M,int d->ratmat``
   * - :ref:`\*_rat_f,mat_m->ratmat1`
     - ``rat f,mat M->ratmat``
   * - :ref:`\/_mat_m,rat_f->ratmat1`
     - ``mat M,rat f->ratmat``
   * - :ref:`entry_ratmat(m,,d),int_i,int_j->rat1`
     - ``ratmat(M,,d),int i,int j->rat``
   * - :ref:`matrix_(int,int)(r,c),(int,int->rat)_f->ratmat1`
     - ``(int,int)(r,c),(int,int->rat) f->ratmat``
   * - :ref:`n_rows_ratmat(m,,)->int1`
     - ``ratmat(M,,)->int``
   * - :ref:`n_columns_ratmat(m,,)->int1`
     - ``ratmat(M,,)->int``
   * - :ref:`columns_ratmat(m,,d)->[ratvec]1`
     - ``ratmat(M,,d)->[ratvec]``
   * - :ref:`rows_ratmat(m,,d)->[ratvec]1`
     - ``ratmat(M,,d)->[ratvec]``
   * - :ref:`column_ratmat(m,,d),int_j->ratvec1`
     - ``ratmat(M,,d),int j->ratvec``
   * - :ref:`row_ratmat(m,,d),int_i->ratvec1`
     - ``ratmat(M,,d),int i->ratvec``
   * - :ref:`columns_with_(int,ratvec->bool)_p,ratmat(m,,d)->ratmat1`
     - ``(int,ratvec->bool) p,ratmat(M,,d)->ratmat``
   * - :ref:`columns_with_(ratvec->bool)_p,ratmat_t->ratmat1`
     - ``(ratvec->bool) p,ratmat T->ratmat``
   * - :ref:`columns_with_(int->bool)_p,ratmat(m,,d)->ratmat1`
     - ``(int->bool) p,ratmat(M,,d)->ratmat``
   * - :ref:`rows_with_(int,ratvec->bool)_p,ratmat(m,,d)->ratmat1`
     - ``(int,ratvec->bool) p,ratmat(M,,d)->ratmat``
   * - :ref:`rows_with_(ratvec->bool)_p,ratmat_t->ratmat1`
     - ``(ratvec->bool) p,ratmat T->ratmat``
   * - :ref:`rows_with_(int->bool)_p,ratmat(m,,d)->ratmat1`
     - ``(int->bool) p,ratmat(M,,d)->ratmat``
   * - :ref:`det_ratmat(m,,d)->rat1`
     - ``ratmat(M,,d)->rat``
   * - :ref:`\^_ratmat(m,,d)->ratmat1`
     - ``ratmat(M,,d)->ratmat``
   * - :ref:`\+_ratmat(m,,d),ratmat(mm,,dd)->ratmat1`
     - ``ratmat(M,,d),ratmat(MM,,dd)->ratmat``
   * - :ref:`\-_ratmat(m,,d),ratmat(mm,,dd)->ratmat1`
     - ``ratmat(M,,d),ratmat(MM,,dd)->ratmat``
   * - :ref:`\*_ratvec_v,ratmat(m,,d)->ratvec1`
     - ``ratvec v,ratmat(M,,d)->ratvec``
   * - :ref:`\*_ratmat(m,,d),ratvec_v->ratvec1`
     - ``ratmat(M,,d),ratvec v->ratvec``
   * - :ref:`\*_ratmat(m,,d),mat_mm->ratmat1`
     - ``ratmat(M,,d),mat MM->ratmat``
   * - :ref:`\*_mat_m,ratmat(mm,,d)->ratmat1`
     - ``mat M,ratmat(MM,,d)->ratmat``
   * - :ref:`\*_ratmat(m,,d),ratmat(mm,,dd)->ratmat1`
     - ``ratmat(M,,d),ratmat(MM,,dd)->ratmat``
   * - :ref:`\/_ratmat(m,,d)->ratmat1`
     - ``ratmat(M,,d)->ratmat``
   * - :ref:`\^_ratmat(m,,d):md,int_e->ratmat1`
     - ``ratmat(M,,d):Md,int e->ratmat``
   * - :ref:`ratmat_as_mat_ratmat(m,,d)->mat1`
     - ``ratmat(M,,d)->mat``
   * - :ref:`mat_as_ratmat_mat_m->ratmat1`
     - ``mat M->ratmat``
   * - :ref:`diagonal_ratvec_v->ratmat1`
     - ``ratvec v->ratmat``
   * - :ref:`ratvecs_as_ratmat_[ratvec]_a->ratmat1`
     - ``[ratvec] A->ratmat``
   * - :ref:`det_[ratvec]_m->rat1`
     - ``[ratvec] M->rat``
   * - :ref:`\^_[ratvec]_m->ratmat1`
     - ``[ratvec] M->ratmat``
   * - :ref:`\*_[ratvec]_m,ratmat_mm->ratmat1`
     - ``[ratvec] M,ratmat MM->ratmat``
   * - :ref:`\*_ratmat_m,[ratvec]_mm->ratmat1`
     - ``ratmat M,[ratvec] MM->ratmat``
   * - :ref:`\+_[ratvec]_m,ratmat_mm->ratmat1`
     - ``[ratvec] M,ratmat MM->ratmat``
   * - :ref:`\+_ratmat_m,[ratvec]_mm->ratmat1`
     - ``ratmat M,[ratvec] MM->ratmat``
   * - :ref:`\-_[ratvec]_m,ratmat_mm->ratmat1`
     - ``[ratvec] M,ratmat MM->ratmat``
   * - :ref:`\-_ratmat_m,[ratvec]_mm->ratmat1`
     - ``ratmat M,[ratvec] MM->ratmat``
   * - :ref:`inverse_ratmat(m,,d)->ratmat1`
     - ``ratmat(M,,d)->ratmat``
   * - :ref:`\*_[ratvec]_m,mat_mm->ratmat1`
     - ``[ratvec] M,mat MM->ratmat``
   * - :ref:`\*_mat_m,[ratvec]_mm->ratmat1`
     - ``mat M,[ratvec] MM->ratmat``
   * - :ref:`\+_[ratvec]_m,mat_mm->ratmat1`
     - ``[ratvec] M,mat MM->ratmat``
   * - :ref:`\+_mat_m,[ratvec]_mm->ratmat1`
     - ``mat M,[ratvec] MM->ratmat``
   * - :ref:`\-_[ratvec]_m,mat_mm->ratmat1`
     - ``[ratvec] M,mat MM->ratmat``
   * - :ref:`\-_mat_m,[ratvec]_mm->ratmat1`
     - ``mat M,[ratvec] MM->ratmat``
   * - :ref:`rational_inverse_mat_m->ratmat1`
     - ``mat M->ratmat``
   * - :ref:`ratvec_to_string_ratvec_v->string1`
     - ``ratvec v->string``
   * - :ref:`show_ratmat(m,,d)->void1`
     - ``ratmat(M,,d)->void``
