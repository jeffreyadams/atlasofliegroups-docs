.. _ratmat.at_ref:

ratmat.at Function References
=======================================================
|

.. _gcd_(mat->int):

gcd
-------------------------------------------------
| ``gcd:(mat->int)``
| 


.. _simplify_(mat,string,int->mat,string,int):

simplify
-------------------------------------------------
| ``simplify:(mat,string,int->mat,string,int)``
| 


.. _/_(mat,int->mat,string,int):

/
-------------------------------------------------
| ``/:(mat,int->mat,string,int)``
| 


.. _\*_(rat,mat->mat,string,int):

\*
-------------------------------------------------
| ``*:(rat,mat->mat,string,int)``
| 


.. _/_(mat,rat->mat,string,int):

/
-------------------------------------------------
| ``/:(mat,rat->mat,string,int)``
| 


.. _entry_((mat,string,int),int,int->rat):

entry
-------------------------------------------------
| ``entry:((mat,string,int),int,int->rat)``
| 


.. _matrix_((int,int),(int,int->rat)->mat,string,int):

matrix
-------------------------------------------------
| ``matrix:((int,int),(int,int->rat)->mat,string,int)``
| 


.. _n_rows_(mat,string,int->int):

n_rows
-------------------------------------------------
| ``n_rows:(mat,string,int->int)``
| 


.. _n_columns_(mat,string,int->int):

n_columns
-------------------------------------------------
| ``n_columns:(mat,string,int->int)``
| 


.. _columns_(mat,string,int->[ratvec]):

columns
-------------------------------------------------
| ``columns:(mat,string,int->[ratvec])``
| 


.. _rows_(mat,string,int->[ratvec]):

rows
-------------------------------------------------
| ``rows:(mat,string,int->[ratvec])``
| 


.. _column_((mat,string,int),int->ratvec):

column
-------------------------------------------------
| ``column:((mat,string,int),int->ratvec)``
| 


.. _row_((mat,string,int),int->ratvec):

row
-------------------------------------------------
| ``row:((mat,string,int),int->ratvec)``
| 


.. _columns_with_((int,ratvec->bool),(mat,string,int)->mat,string,int):

columns_with
-------------------------------------------------
| ``columns_with:((int,ratvec->bool),(mat,string,int)->mat,string,int)``
| 


.. _columns_with_((ratvec->bool),(mat,string,int)->mat,string,int):

columns_with
-------------------------------------------------
| ``columns_with:((ratvec->bool),(mat,string,int)->mat,string,int)``
| 


.. _columns_with_((int->bool),(mat,string,int)->mat,string,int):

columns_with
-------------------------------------------------
| ``columns_with:((int->bool),(mat,string,int)->mat,string,int)``
| 


.. _rows_with_((int,ratvec->bool),(mat,string,int)->mat,string,int):

rows_with
-------------------------------------------------
| ``rows_with:((int,ratvec->bool),(mat,string,int)->mat,string,int)``
| 


.. _rows_with_((ratvec->bool),(mat,string,int)->mat,string,int):

rows_with
-------------------------------------------------
| ``rows_with:((ratvec->bool),(mat,string,int)->mat,string,int)``
| 


.. _rows_with_((int->bool),(mat,string,int)->mat,string,int):

rows_with
-------------------------------------------------
| ``rows_with:((int->bool),(mat,string,int)->mat,string,int)``
| 


.. _det_(mat,string,int->rat):

det
-------------------------------------------------
| ``det:(mat,string,int->rat)``
| 


.. _\^_(mat,string,int->mat,string,int):

\^
-------------------------------------------------
| ``^:(mat,string,int->mat,string,int)``
| 


.. _\+_((mat,string,int),(mat,string,int)->mat,string,int):

\+
-------------------------------------------------
| ``+:((mat,string,int),(mat,string,int)->mat,string,int)``
| 


.. _\-_((mat,string,int),(mat,string,int)->mat,string,int):

\-
-------------------------------------------------
| ``-:((mat,string,int),(mat,string,int)->mat,string,int)``
| 


.. _\-_(mat,string,int->mat,int,void):

\-
-------------------------------------------------
| ``-:(mat,string,int->mat,int,void)``
| 


.. _\*_(ratvec,(mat,string,int)->ratvec):

\*
-------------------------------------------------
| ``*:(ratvec,(mat,string,int)->ratvec)``
| 


.. _\*_((mat,string,int),ratvec->ratvec):

\*
-------------------------------------------------
| ``*:((mat,string,int),ratvec->ratvec)``
| 


.. _\*_((mat,string,int),mat->mat,string,int):

\*
-------------------------------------------------
| ``*:((mat,string,int),mat->mat,string,int)``
| 


.. _\*_(mat,(mat,string,int)->mat,string,int):

\*
-------------------------------------------------
| ``*:(mat,(mat,string,int)->mat,string,int)``
| 


.. _\*_((mat,string,int),(mat,string,int)->mat,string,int):

\*
-------------------------------------------------
| ``*:((mat,string,int),(mat,string,int)->mat,string,int)``
| 


.. _/_(mat,string,int->mat,string,int):

/
-------------------------------------------------
| ``/:(mat,string,int->mat,string,int)``
| 


.. _\^_((mat,string,int),int->mat,string,int):

\^
-------------------------------------------------
| ``^:((mat,string,int),int->mat,string,int)``
| 


.. _ratmat_as_mat_(mat,string,int->mat):

ratmat_as_mat
-------------------------------------------------
| ``ratmat_as_mat:(mat,string,int->mat)``
| 


.. _mat_as_ratmat_(mat->mat,string,int):

mat_as_ratmat
-------------------------------------------------
| ``mat_as_ratmat:(mat->mat,string,int)``
| 


.. _diagonal_(ratvec->mat,string,int):

diagonal
-------------------------------------------------
| ``diagonal:(ratvec->mat,string,int)``
| 


.. _ratvecs_as_ratmat_([ratvec]->mat,string,int):

ratvecs_as_ratmat
-------------------------------------------------
| ``ratvecs_as_ratmat:([ratvec]->mat,string,int)``
| 


.. _det_([ratvec]->rat):

det
-------------------------------------------------
| ``det:([ratvec]->rat)``
| 


.. _\^_([ratvec]->mat,string,int):

\^
-------------------------------------------------
| ``^:([ratvec]->mat,string,int)``
| 


.. _\*_([ratvec],(mat,string,int)->mat,string,int):

\*
-------------------------------------------------
| ``*:([ratvec],(mat,string,int)->mat,string,int)``
| 


.. _\*_((mat,string,int),[ratvec]->mat,string,int):

\*
-------------------------------------------------
| ``*:((mat,string,int),[ratvec]->mat,string,int)``
| 


.. _\+_([ratvec],(mat,string,int)->mat,string,int):

\+
-------------------------------------------------
| ``+:([ratvec],(mat,string,int)->mat,string,int)``
| 


.. _\+_((mat,string,int),[ratvec]->mat,string,int):

\+
-------------------------------------------------
| ``+:((mat,string,int),[ratvec]->mat,string,int)``
| 


.. _\-_([ratvec],(mat,string,int)->mat,string,int):

\-
-------------------------------------------------
| ``-:([ratvec],(mat,string,int)->mat,string,int)``
| 


.. _\-_((mat,string,int),[ratvec]->mat,string,int):

\-
-------------------------------------------------
| ``-:((mat,string,int),[ratvec]->mat,string,int)``
| 


.. _inverse_(mat,string,int->mat,string,int):

inverse
-------------------------------------------------
| ``inverse:(mat,string,int->mat,string,int)``
| 


.. _\*_([ratvec],mat->mat,string,int):

\*
-------------------------------------------------
| ``*:([ratvec],mat->mat,string,int)``
| 


.. _\*_(mat,[ratvec]->mat,string,int):

\*
-------------------------------------------------
| ``*:(mat,[ratvec]->mat,string,int)``
| 


.. _\+_([ratvec],mat->mat,string,int):

\+
-------------------------------------------------
| ``+:([ratvec],mat->mat,string,int)``
| 


.. _\+_(mat,[ratvec]->mat,string,int):

\+
-------------------------------------------------
| ``+:(mat,[ratvec]->mat,string,int)``
| 


.. _\-_([ratvec],mat->mat,string,int):

\-
-------------------------------------------------
| ``-:([ratvec],mat->mat,string,int)``
| 


.. _\-_(mat,[ratvec]->mat,string,int):

\-
-------------------------------------------------
| ``-:(mat,[ratvec]->mat,string,int)``
| 


.. _rational_inverse_(mat->mat,string,int):

rational_inverse
-------------------------------------------------
| ``rational_inverse:(mat->mat,string,int)``
| 


.. _ratvec_to_string_(ratvec->string):

ratvec_to_string
-------------------------------------------------
| ``ratvec_to_string:(ratvec->string)``
| 


.. _show_(mat,string,int->):

show
-------------------------------------------------
| ``show:(mat,string,int->)``
| 


.. _save_s_Split:

save_s
-------------------------------------------------
| ``save_s:Split``
| 


.. _s_Split:

s
-------------------------------------------------
| ``s:Split``
| 


