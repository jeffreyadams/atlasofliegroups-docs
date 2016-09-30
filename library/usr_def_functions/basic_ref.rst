.. _basic.at_ref:

basic.at Function References
=======================================================
|

.. _\#_(int->[int]):

\#
-------------------------------------------------
| ``#:(int->[int])``
| 


.. _\#_(bool->int):

\#
-------------------------------------------------
| ``#:(bool->int)``
| 


.. _\^_(bool,bool->bool):

\^
-------------------------------------------------
| ``^:(bool,bool->bool)``
| 


.. _assert_(bool,string->):

assert
-------------------------------------------------
| ``assert:(bool,string->)``
| 


.. _assert_(bool->):

assert
-------------------------------------------------
| ``assert:(bool->)``
| 


.. _list_((int->bool),int->[int]):

list
-------------------------------------------------
| ``list:((int->bool),int->[int])``
| 


.. _complement_((int->bool),int->[int]):

complement
-------------------------------------------------
| ``complement:((int->bool),int->[int])``
| 


.. _count_((int->bool),int->int):

count
-------------------------------------------------
| ``count:((int->bool),int->int)``
| 


.. _all_([bool]->bool):

all
-------------------------------------------------
| ``all:([bool]->bool)``
| 


.. _none_([bool]->bool):

none
-------------------------------------------------
| ``none:([bool]->bool)``
| 


.. _first_([bool]->int):

first
-------------------------------------------------
| ``first:([bool]->int)``
| 


.. _last_([bool]->int):

last
-------------------------------------------------
| ``last:([bool]->int)``
| 


.. _all_(int,(int->bool)->bool):

all
-------------------------------------------------
| ``all:(int,(int->bool)->bool)``
| 


.. _none_(int,(int->bool)->bool):

none
-------------------------------------------------
| ``none:(int,(int->bool)->bool)``
| 


.. _first_(int,(int->bool)->int):

first
-------------------------------------------------
| ``first:(int,(int->bool)->int)``
| 


.. _last_(int,(int->bool)->int):

last
-------------------------------------------------
| ``last:(int,(int->bool)->int)``
| 


.. _all_([(->bool)]->bool):

all
-------------------------------------------------
| ``all:([(->bool)]->bool)``
| 


.. _none_([(->bool)]->bool):

none
-------------------------------------------------
| ``none:([(->bool)]->bool)``
| 


.. _first_([(->bool)]->int):

first
-------------------------------------------------
| ``first:([(->bool)]->int)``
| 


.. _last_([(->bool)]->int):

last
-------------------------------------------------
| ``last:([(->bool)]->int)``
| 


.. _abs_(int->int):

abs
-------------------------------------------------
| ``abs:(int->int)``
| 


.. _sign_(int->int):

sign
-------------------------------------------------
| ``sign:(int->int)``
| 


.. _is_odd_(int->bool):

is_odd
-------------------------------------------------
| ``is_odd:(int->bool)``
| 


.. _is_even_(int->bool):

is_even
-------------------------------------------------
| ``is_even:(int->bool)``
| 


.. _min_(int,int->int):

min
-------------------------------------------------
| ``min:(int,int->int)``
| 


.. _max_(int,int->int):

max
-------------------------------------------------
| ``max:(int,int->int)``
| 


.. _min_([int]->int):

min
-------------------------------------------------
| ``min:([int]->int)``
| 


.. _max_([int]->int):

max
-------------------------------------------------
| ``max:([int]->int)``
| 


.. _min_loc_([int]->int):

min_loc
-------------------------------------------------
| ``min_loc:([int]->int)``
| 


.. _max_loc_([int]->int):

max_loc
-------------------------------------------------
| ``max_loc:([int]->int)``
| 


.. _min_(int->([int]->int)):

min
-------------------------------------------------
| ``min:(int->([int]->int))``
| 


.. _max_(int->([int]->int)):

max
-------------------------------------------------
| ``max:(int->([int]->int))``
| 


.. _lcm_([int]->int):

lcm
-------------------------------------------------
| ``lcm:([int]->int)``
| 


.. _\=_((int,int),(int,int)->bool):

\=
-------------------------------------------------
| ``=:((int,int),(int,int)->bool)``
| 


.. _!=_((int,int),(int,int)->bool):

!=
-------------------------------------------------
| ``!=:((int,int),(int,int)->bool)``
| 


.. _numer_(rat->int):

numer
-------------------------------------------------
| ``numer:(rat->int)``
| 


.. _denom_(rat->int):

denom
-------------------------------------------------
| ``denom:(rat->int)``
| 


.. _is_integer_(rat->bool):

is_integer
-------------------------------------------------
| ``is_integer:(rat->bool)``
| 


.. _sign_(rat->int):

sign
-------------------------------------------------
| ``sign:(rat->int)``
| 


.. _abs_(rat->rat):

abs
-------------------------------------------------
| ``abs:(rat->rat)``
| 


.. _floor_(rat->int):

floor
-------------------------------------------------
| ``floor:(rat->int)``
| 


.. _ceil_(rat->int):

ceil
-------------------------------------------------
| ``ceil:(rat->int)``
| 


.. _\\_(rat,int->int):

\\
-------------------------------------------------
| ``\:(rat,int->int)``
| 


.. _\\_(rat,rat->int):

\\
-------------------------------------------------
| ``\:(rat,rat->int)``
| 


.. _\%_(rat,int->int,rat):

\%
-------------------------------------------------
| ``\%:(rat,int->int,rat)``
| 


.. _\%_(rat,rat->int,rat):

\%
-------------------------------------------------
| ``\%:(rat,rat->int,rat)``
| 


.. _floor_([rat]->vec):

floor
-------------------------------------------------
| ``floor:([rat]->vec)``
| 


.. _ceil_([rat]->vec):

ceil
-------------------------------------------------
| ``ceil:([rat]->vec)``
| 


.. _rat_as_int_(rat->int):

rat_as_int
-------------------------------------------------
| ``rat_as_int:(rat->int)``
| 


.. _\+_(string,string->string):

\+
-------------------------------------------------
| ``+:(string,string->string)``
| 


.. _\*_(string,int->string):

\*
-------------------------------------------------
| ``*:(string,int->string)``
| 


.. _\*_(int,string->string):

\*
-------------------------------------------------
| ``*:(int,string->string)``
| 


.. _\+_(string,int->string):

\+
-------------------------------------------------
| ``+:(string,int->string)``
| 


.. _\+_(int,string->string):

\+
-------------------------------------------------
| ``+:(int,string->string)``
| 


.. _\+_(string,(int,int)->string):

\+
-------------------------------------------------
| ``+:(string,(int,int)->string)``
| 


.. _plural_(int->string):

plural
-------------------------------------------------
| ``plural:(int->string)``
| 


.. _plural_(int,string->string):

plural
-------------------------------------------------
| ``plural:(int,string->string)``
| 


.. _concat_([string]->string):

concat
-------------------------------------------------
| ``concat:([string]->string)``
| 


.. _l_adjust_(int,string->string):

l_adjust
-------------------------------------------------
| ``l_adjust:(int,string->string)``
| 


.. _r_adjust_(int,string->string):

r_adjust
-------------------------------------------------
| ``r_adjust:(int,string->string)``
| 


.. _c_adjust_(int,string->string):

c_adjust
-------------------------------------------------
| ``c_adjust:(int,string->string)``
| 


.. _width_(int->int):

width
-------------------------------------------------
| ``width:(int->int)``
| 


.. _split_lines_(string->[string]):

split_lines
-------------------------------------------------
| ``split_lines:(string->[string])``
| 


.. _is_substring_(string,string->bool):

is_substring
-------------------------------------------------
| ``is_substring:(string,string->bool)``
| 


.. _fgrep_(string,string->[string]):

fgrep
-------------------------------------------------
| ``fgrep:(string,string->[string])``
| 


.. _vector_(int,(int->int)->vec):

vector
-------------------------------------------------
| ``vector:(int,(int->int)->vec)``
| 


.. _ones_(int->vec):

ones
-------------------------------------------------
| ``ones:(int->vec)``
| 


.. _gcd_([int]->int):

gcd
-------------------------------------------------
| ``gcd:([int]->int)``
| 


.. _\*_(int,vec->vec):

\*
-------------------------------------------------
| ``*:(int,vec->vec)``
| 


.. _sum_(vec->int):

sum
-------------------------------------------------
| ``sum:(vec->int)``
| 


.. _product_(vec->int):

product
-------------------------------------------------
| ``product:(vec->int)``
| 


.. _reverse_(vec->vec):

reverse
-------------------------------------------------
| ``reverse:(vec->vec)``
| 


.. _lower_(int,vec->vec):

lower
-------------------------------------------------
| ``lower:(int,vec->vec)``
| 


.. _upper_(int,vec->vec):

upper
-------------------------------------------------
| ``upper:(int,vec->vec)``
| 


.. _drop_lower_(int,vec->vec):

drop_lower
-------------------------------------------------
| ``drop_lower:(int,vec->vec)``
| 


.. _drop_upper_(int,vec->vec):

drop_upper
-------------------------------------------------
| ``drop_upper:(int,vec->vec)``
| 


.. _<=_(vec->bool):

<=
-------------------------------------------------
| ``<=:(vec->bool)``
| 


.. _<_(vec->bool):

<
-------------------------------------------------
| ``<:(vec->bool)``
| 


.. _is_member_([int]->(int->bool)):

is_member
-------------------------------------------------
| ``is_member:([int]->(int->bool))``
| 


.. _contains_(int->([int]->bool)):

contains
-------------------------------------------------
| ``contains:(int->([int]->bool))``
| 


.. _all_0_1_vecs_(int->[vec]):

all_0_1_vecs
-------------------------------------------------
| ``all_0_1_vecs:(int->[vec])``
| 


.. _power_set_(int->[[int]]):

power_set
-------------------------------------------------
| ``power_set:(int->[[int]])``
| 


.. _power_set_([int]->[[int]]):

power_set
-------------------------------------------------
| ``power_set:([int]->[[int]])``
| 


.. _matrix_((int,int),(int,int->int)->mat):

matrix
-------------------------------------------------
| ``matrix:((int,int),(int,int->int)->mat)``
| 


.. _n_rows_(mat->int):

n_rows
-------------------------------------------------
| ``n_rows:(mat->int)``
| 


.. _n_columns_(mat->int):

n_columns
-------------------------------------------------
| ``n_columns:(mat->int)``
| 


.. _column_(vec->mat):

column
-------------------------------------------------
| ``column:(vec->mat)``
| 


.. _row_(vec->mat):

row
-------------------------------------------------
| ``row:(vec->mat)``
| 


.. _\=_(mat,int->bool):

\=
-------------------------------------------------
| ``=:(mat,int->bool)``
| 


.. _\#_(mat,vec->mat):

\#
-------------------------------------------------
| ``#:(mat,vec->mat)``
| 


.. _\#_(vec,mat->mat):

\#
-------------------------------------------------
| ``#:(vec,mat->mat)``
| 


.. _\^_(mat,vec->mat):

\^
-------------------------------------------------
| ``^:(mat,vec->mat)``
| 


.. _\^_(vec,mat->mat):

\^
-------------------------------------------------
| ``^:(vec,mat->mat)``
| 


.. _##_(mat,mat->mat):

##
-------------------------------------------------
| ``##:(mat,mat->mat)``
| 


.. _\^_(mat,mat->mat):

\^
-------------------------------------------------
| ``^:(mat,mat->mat)``
| 


.. _##_(int,[mat]->mat):

##
-------------------------------------------------
| ``##:(int,[mat]->mat)``
| 


.. _map_on_(mat->((int->int)->mat)):

map_on
-------------------------------------------------
| ``map_on:(mat->((int->int)->mat))``
| 


.. _\*_(int,mat->mat):

\*
-------------------------------------------------
| ``*:(int,mat->mat)``
| 


.. _\-_(mat->mat):

\-
-------------------------------------------------
| ``-:(mat->mat)``
| 


.. _\\_(mat,int->mat):

\\
-------------------------------------------------
| ``\:(mat,int->mat)``
| 


.. _%_(mat,int->mat):

%
-------------------------------------------------
| ``%:(mat,int->mat)``
| 


.. _\^_(mat,int->mat):

\^
-------------------------------------------------
| ``^:(mat,int->mat)``
| 


.. _inverse_(mat->mat):

inverse
-------------------------------------------------
| ``inverse:(mat->mat)``
| 


.. _det_(mat->int):

det
-------------------------------------------------
| ``det:(mat->int)``
| 


.. _saturated_span_(mat->bool):

saturated_span
-------------------------------------------------
| ``saturated_span:(mat->bool)``
| 


.. _all_(mat,(vec->bool)->bool):

all
-------------------------------------------------
| ``all:(mat,(vec->bool)->bool)``
| 


.. _none_(mat,(vec->bool)->bool):

none
-------------------------------------------------
| ``none:(mat,(vec->bool)->bool)``
| 


.. _first_(mat,(vec->bool)->int):

first
-------------------------------------------------
| ``first:(mat,(vec->bool)->int)``
| 


.. _last_(mat,(vec->bool)->int):

last
-------------------------------------------------
| ``last:(mat,(vec->bool)->int)``
| 


.. _columns_with_((int,vec->bool),mat->mat):

columns_with
-------------------------------------------------
| ``columns_with:((int,vec->bool),mat->mat)``
| 


.. _columns_with_((vec->bool),mat->mat):

columns_with
-------------------------------------------------
| ``columns_with:((vec->bool),mat->mat)``
| 


.. _columns_with_((int->bool),mat->mat):

columns_with
-------------------------------------------------
| ``columns_with:((int->bool),mat->mat)``
| 


.. _rows_with_((int,vec->bool),mat->mat):

rows_with
-------------------------------------------------
| ``rows_with:((int,vec->bool),mat->mat)``
| 


.. _rows_with_((vec->bool),mat->mat):

rows_with
-------------------------------------------------
| ``rows_with:((vec->bool),mat->mat)``
| 


.. _rows_with_((int->bool),mat->mat):

rows_with
-------------------------------------------------
| ``rows_with:((int->bool),mat->mat)``
| 


.. _>=_(mat->bool):

>=
-------------------------------------------------
| ``>=:(mat->bool)``
| 


.. _>_(mat->bool):

>
-------------------------------------------------
| ``>:(mat->bool)``
| 


.. _<=_(mat->bool):

<=
-------------------------------------------------
| ``<=:(mat->bool)``
| 


.. _<_(mat->bool):

<
-------------------------------------------------
| ``<:(mat->bool)``
| 


.. _lookup_column_(vec,mat->int):

lookup_column
-------------------------------------------------
| ``lookup_column:(vec,mat->int)``
| 


.. _lookup_row_(vec,mat->int):

lookup_row
-------------------------------------------------
| ``lookup_row:(vec,mat->int)``
| 


.. _sum_(mat->vec):

sum
-------------------------------------------------
| ``sum:(mat->vec)``
| 


.. _solve_(mat,vec->[vec]):

solve
-------------------------------------------------
| ``solve:(mat,vec->[vec])``
| 


.. _order_(mat->int):

order
-------------------------------------------------
| ``order:(mat->int)``
| 


.. _numer_(ratvec->vec):

numer
-------------------------------------------------
| ``numer:(ratvec->vec)``
| 


.. _denom_(ratvec->int):

denom
-------------------------------------------------
| ``denom:(ratvec->int)``
| 


.. _\*_(int,ratvec->ratvec):

\*
-------------------------------------------------
| ``*:(int,ratvec->ratvec)``
| 


.. _\*_(rat,ratvec->ratvec):

\*
-------------------------------------------------
| ``*:(rat,ratvec->ratvec)``
| 


.. _##_(ratvec,ratvec->ratvec):

##
-------------------------------------------------
| ``##:(ratvec,ratvec->ratvec)``
| 


.. _##_([ratvec]->ratvec):

##
-------------------------------------------------
| ``##:([ratvec]->ratvec)``
| 


.. _sum_([ratvec],int->ratvec):

sum
-------------------------------------------------
| ``sum:([ratvec],int->ratvec)``
| 


.. _\*_([ratvec],ratvec->ratvec):

\*
-------------------------------------------------
| ``*:([ratvec],ratvec->ratvec)``
| 


.. _is_integer_(ratvec->bool):

is_integer
-------------------------------------------------
| ``is_integer:(ratvec->bool)``
| 


.. _\*_(ratvec,ratvec->rat):

\*
-------------------------------------------------
| ``*:(ratvec,ratvec->rat)``
| 


.. _\*_(vec,ratvec->rat):

\*
-------------------------------------------------
| ``*:(vec,ratvec->rat)``
| 


.. _\\_(ratvec,int->vec):

\\
-------------------------------------------------
| ``\:(ratvec,int->vec)``
| 


.. _ratvec_as_vec_(ratvec->vec):

ratvec_as_vec
-------------------------------------------------
| ``ratvec_as_vec:(ratvec->vec)``
| 


.. _reverse_(ratvec->ratvec):

reverse
-------------------------------------------------
| ``reverse:(ratvec->ratvec)``
| 


.. _lower_(int,ratvec->ratvec):

lower
-------------------------------------------------
| ``lower:(int,ratvec->ratvec)``
| 


.. _upper_(int,ratvec->ratvec):

upper
-------------------------------------------------
| ``upper:(int,ratvec->ratvec)``
| 


.. _drop_lower_(int,ratvec->ratvec):

drop_lower
-------------------------------------------------
| ``drop_lower:(int,ratvec->ratvec)``
| 


.. _drop_upper_(int,ratvec->ratvec):

drop_upper
-------------------------------------------------
| ``drop_upper:(int,ratvec->ratvec)``
| 


.. _sum_(ratvec->rat):

sum
-------------------------------------------------
| ``sum:(ratvec->rat)``
| 


.. _<=_(ratvec->bool):

<=
-------------------------------------------------
| ``<=:(ratvec->bool)``
| 


.. _<_(ratvec->bool):

<
-------------------------------------------------
| ``<:(ratvec->bool)``
| 


.. _solve_(mat,ratvec->[ratvec]):

solve
-------------------------------------------------
| ``solve:(mat,ratvec->[ratvec])``
| 


.. _int_part_(Split->int):

int_part
-------------------------------------------------
| ``int_part:(Split->int)``
| 


.. _s_part_(Split->int):

s_part
-------------------------------------------------
| ``s_part:(Split->int)``
| 


.. _\+_(Split->int):

\+
-------------------------------------------------
| ``+:(Split->int)``
| 


.. _\^_(Split->int):

\^
-------------------------------------------------
| ``^:(Split->int)``
| 


.. _s_to_1_(Split->int):

s_to_1
-------------------------------------------------
| ``s_to_1:(Split->int)``
| 


.. _s_to_minus_1_(Split->int):

s_to_minus_1
-------------------------------------------------
| ``s_to_minus_1:(Split->int)``
| 


.. _split_as_int_(Split->int):

split_as_int
-------------------------------------------------
| ``split_as_int:(Split->int)``
| 


.. _\%_(Split,int->Split,Split):

\%
-------------------------------------------------
| ``\%:(Split,int->Split,Split)``
| 


.. _split_format_(Split->string):

split_format
-------------------------------------------------
| ``split_format:(Split->string)``
| 


.. _\^_(Split,int->Split):

\^
-------------------------------------------------
| ``^:(Split,int->Split)``
| 


.. _root_datum_([vec],[vec],int->RootDatum):

root_datum
-------------------------------------------------
| ``root_datum:([vec],[vec],int->RootDatum)``
| 


.. _root_datum_(LieType,[ratvec]->RootDatum):

root_datum
-------------------------------------------------
| ``root_datum:(LieType,[ratvec]->RootDatum)``
| 


.. _root_datum_(LieType,ratvec->RootDatum):

root_datum
-------------------------------------------------
| ``root_datum:(LieType,ratvec->RootDatum)``
| 


.. _is_root_(RootDatum,vec->bool):

is_root
-------------------------------------------------
| ``is_root:(RootDatum,vec->bool)``
| 


.. _is_coroot_(RootDatum,vec->bool):

is_coroot
-------------------------------------------------
| ``is_coroot:(RootDatum,vec->bool)``
| 


.. _is_posroot_(RootDatum,vec->bool):

is_posroot
-------------------------------------------------
| ``is_posroot:(RootDatum,vec->bool)``
| 


.. _is_poscoroot_(RootDatum,vec->bool):

is_poscoroot
-------------------------------------------------
| ``is_poscoroot:(RootDatum,vec->bool)``
| 


.. _posroot_index_(RootDatum,vec->int):

posroot_index
-------------------------------------------------
| ``posroot_index:(RootDatum,vec->int)``
| 


.. _poscoroot_index_(RootDatum,vec->int):

poscoroot_index
-------------------------------------------------
| ``poscoroot_index:(RootDatum,vec->int)``
| 


.. _rho_(RootDatum->ratvec):

rho
-------------------------------------------------
| ``rho:(RootDatum->ratvec)``
| 


.. _rho_as_vec_(RootDatum->vec):

rho_as_vec
-------------------------------------------------
| ``rho_as_vec:(RootDatum->vec)``
| 


.. _rho_check_(RootDatum->ratvec):

rho_check
-------------------------------------------------
| ``rho_check:(RootDatum->ratvec)``
| 


.. _is_positive_root_(RootDatum->(vec->bool)):

is_positive_root
-------------------------------------------------
| ``is_positive_root:(RootDatum->(vec->bool))``
| 


.. _is_positive_coroot_(RootDatum->(vec->bool)):

is_positive_coroot
-------------------------------------------------
| ``is_positive_coroot:(RootDatum->(vec->bool))``
| 


.. _is_negative_root_(RootDatum->(vec->bool)):

is_negative_root
-------------------------------------------------
| ``is_negative_root:(RootDatum->(vec->bool))``
| 


.. _is_negative_coroot_(RootDatum->(vec->bool)):

is_negative_coroot
-------------------------------------------------
| ``is_negative_coroot:(RootDatum->(vec->bool))``
| 


.. _is_positive_root_(RootDatum,vec->bool):

is_positive_root
-------------------------------------------------
| ``is_positive_root:(RootDatum,vec->bool)``
| 


.. _is_positive_coroot_(RootDatum,vec->bool):

is_positive_coroot
-------------------------------------------------
| ``is_positive_coroot:(RootDatum,vec->bool)``
| 


.. _is_negative_root_(RootDatum,vec->bool):

is_negative_root
-------------------------------------------------
| ``is_negative_root:(RootDatum,vec->bool)``
| 


.. _is_negative_coroot_(RootDatum,vec->bool):

is_negative_coroot
-------------------------------------------------
| ``is_negative_coroot:(RootDatum,vec->bool)``
| 


.. _roots_all_positive_(RootDatum->(mat->bool)):

roots_all_positive
-------------------------------------------------
| ``roots_all_positive:(RootDatum->(mat->bool))``
| 


.. _coroots_all_positive_(RootDatum->(mat->bool)):

coroots_all_positive
-------------------------------------------------
| ``coroots_all_positive:(RootDatum->(mat->bool))``
| 


.. _among_posroots_(RootDatum->(mat->bool)):

among_posroots
-------------------------------------------------
| ``among_posroots:(RootDatum->(mat->bool))``
| 


.. _among_poscoroots_(RootDatum->(mat->bool)):

among_poscoroots
-------------------------------------------------
| ``among_poscoroots:(RootDatum->(mat->bool))``
| 


.. _negative_system_(mat->mat):

negative_system
-------------------------------------------------
| ``negative_system:(mat->mat)``
| 


.. _roots_(RootDatum->mat):

roots
-------------------------------------------------
| ``roots:(RootDatum->mat)``
| 


.. _coroots_(RootDatum->mat):

coroots
-------------------------------------------------
| ``coroots:(RootDatum->mat)``
| 


.. _root_(RootDatum,vec->vec):

root
-------------------------------------------------
| ``root:(RootDatum,vec->vec)``
| 


.. _coroot_(RootDatum,vec->vec):

coroot
-------------------------------------------------
| ``coroot:(RootDatum,vec->vec)``
| 


.. _reflection_(RootDatum,int->mat):

reflection
-------------------------------------------------
| ``reflection:(RootDatum,int->mat)``
| 


.. _reflection_(RootDatum,vec->mat):

reflection
-------------------------------------------------
| ``reflection:(RootDatum,vec->mat)``
| 


.. _coreflection_(RootDatum,int->mat):

coreflection
-------------------------------------------------
| ``coreflection:(RootDatum,int->mat)``
| 


.. _coreflection_(RootDatum,vec->mat):

coreflection
-------------------------------------------------
| ``coreflection:(RootDatum,vec->mat)``
| 


.. _reflect_(RootDatum,int,vec->vec):

reflect
-------------------------------------------------
| ``reflect:(RootDatum,int,vec->vec)``
| 


.. _reflect_(RootDatum,vec,vec->vec):

reflect
-------------------------------------------------
| ``reflect:(RootDatum,vec,vec->vec)``
| 


.. _coreflect_(RootDatum,vec,int->vec):

coreflect
-------------------------------------------------
| ``coreflect:(RootDatum,vec,int->vec)``
| 


.. _coreflect_(RootDatum,vec,vec->vec):

coreflect
-------------------------------------------------
| ``coreflect:(RootDatum,vec,vec->vec)``
| 


.. _reflect_(RootDatum,int,ratvec->ratvec):

reflect
-------------------------------------------------
| ``reflect:(RootDatum,int,ratvec->ratvec)``
| 


.. _reflect_(RootDatum,vec,ratvec->ratvec):

reflect
-------------------------------------------------
| ``reflect:(RootDatum,vec,ratvec->ratvec)``
| 


.. _coreflect_(RootDatum,ratvec,int->ratvec):

coreflect
-------------------------------------------------
| ``coreflect:(RootDatum,ratvec,int->ratvec)``
| 


.. _coreflect_(RootDatum,ratvec,vec->ratvec):

coreflect
-------------------------------------------------
| ``coreflect:(RootDatum,ratvec,vec->ratvec)``
| 


.. _left_reflect_(RootDatum,int,mat->mat):

left_reflect
-------------------------------------------------
| ``left_reflect:(RootDatum,int,mat->mat)``
| 


.. _left_reflect_(RootDatum,vec,mat->mat):

left_reflect
-------------------------------------------------
| ``left_reflect:(RootDatum,vec,mat->mat)``
| 


.. _right_reflect_(RootDatum,mat,int->mat):

right_reflect
-------------------------------------------------
| ``right_reflect:(RootDatum,mat,int->mat)``
| 


.. _right_reflect_(RootDatum,mat,vec->mat):

right_reflect
-------------------------------------------------
| ``right_reflect:(RootDatum,mat,vec->mat)``
| 


.. _conjugate_(RootDatum,int,mat->mat):

conjugate
-------------------------------------------------
| ``conjugate:(RootDatum,int,mat->mat)``
| 


.. _conjugate_(RootDatum,vec,mat->mat):

conjugate
-------------------------------------------------
| ``conjugate:(RootDatum,vec,mat->mat)``
| 


.. _singular_simple_indices_(RootDatum,ratvec->[int]):

singular_simple_indices
-------------------------------------------------
| ``singular_simple_indices:(RootDatum,ratvec->[int])``
| 


.. _is_imaginary_(mat->(vec->bool)):

is_imaginary
-------------------------------------------------
| ``is_imaginary:(mat->(vec->bool))``
| 


.. _is_real_(mat->(vec->bool)):

is_real
-------------------------------------------------
| ``is_real:(mat->(vec->bool))``
| 


.. _is_complex_(mat->(vec->bool)):

is_complex
-------------------------------------------------
| ``is_complex:(mat->(vec->bool))``
| 


.. _imaginary_roots_(RootDatum,mat->mat):

imaginary_roots
-------------------------------------------------
| ``imaginary_roots:(RootDatum,mat->mat)``
| 


.. _real_roots_(RootDatum,mat->mat):

real_roots
-------------------------------------------------
| ``real_roots:(RootDatum,mat->mat)``
| 


.. _imaginary_coroots_(RootDatum,mat->mat):

imaginary_coroots
-------------------------------------------------
| ``imaginary_coroots:(RootDatum,mat->mat)``
| 


.. _real_coroots_(RootDatum,mat->mat):

real_coroots
-------------------------------------------------
| ``real_coroots:(RootDatum,mat->mat)``
| 


.. _imaginary_posroots_(RootDatum,mat->mat):

imaginary_posroots
-------------------------------------------------
| ``imaginary_posroots:(RootDatum,mat->mat)``
| 


.. _real_posroots_(RootDatum,mat->mat):

real_posroots
-------------------------------------------------
| ``real_posroots:(RootDatum,mat->mat)``
| 


.. _imaginary_poscoroots_(RootDatum,mat->mat):

imaginary_poscoroots
-------------------------------------------------
| ``imaginary_poscoroots:(RootDatum,mat->mat)``
| 


.. _real_poscoroots_(RootDatum,mat->mat):

real_poscoroots
-------------------------------------------------
| ``real_poscoroots:(RootDatum,mat->mat)``
| 


.. _imaginary_sys_(RootDatum,mat->mat,mat):

imaginary_sys
-------------------------------------------------
| ``imaginary_sys:(RootDatum,mat->mat,mat)``
| 


.. _real_sys_(RootDatum,mat->mat,mat):

real_sys
-------------------------------------------------
| ``real_sys:(RootDatum,mat->mat,mat)``
| 


.. _is_dominant_(RootDatum,ratvec->bool):

is_dominant
-------------------------------------------------
| ``is_dominant:(RootDatum,ratvec->bool)``
| 


.. _is_strictly_dominant_(RootDatum,ratvec->bool):

is_strictly_dominant
-------------------------------------------------
| ``is_strictly_dominant:(RootDatum,ratvec->bool)``
| 


.. _is_regular_(RootDatum,ratvec->bool):

is_regular
-------------------------------------------------
| ``is_regular:(RootDatum,ratvec->bool)``
| 


.. _is_integral_(RootDatum,ratvec->bool):

is_integral
-------------------------------------------------
| ``is_integral:(RootDatum,ratvec->bool)``
| 


.. _radical_basis_(RootDatum->mat):

radical_basis
-------------------------------------------------
| ``radical_basis:(RootDatum->mat)``
| 


.. _coradical_basis_(RootDatum->mat):

coradical_basis
-------------------------------------------------
| ``coradical_basis:(RootDatum->mat)``
| 


.. _is_semisimple_(RootDatum->bool):

is_semisimple
-------------------------------------------------
| ``is_semisimple:(RootDatum->bool)``
| 


.. _derived_is_simply_connected_(RootDatum->bool):

derived_is_simply_connected
-------------------------------------------------
| ``derived_is_simply_connected:(RootDatum->bool)``
| 


.. _has_connected_center_(RootDatum->bool):

has_connected_center
-------------------------------------------------
| ``has_connected_center:(RootDatum->bool)``
| 


.. _is_simply_connected_(RootDatum->bool):

is_simply_connected
-------------------------------------------------
| ``is_simply_connected:(RootDatum->bool)``
| 


.. _is_adjoint_(RootDatum->bool):

is_adjoint
-------------------------------------------------
| ``is_adjoint:(RootDatum->bool)``
| 


.. _derived_(RootDatum->RootDatum):

derived
-------------------------------------------------
| ``derived:(RootDatum->RootDatum)``
| 


.. _mod_central_torus_(RootDatum->RootDatum):

mod_central_torus
-------------------------------------------------
| ``mod_central_torus:(RootDatum->RootDatum)``
| 


.. _adjoint_(RootDatum->RootDatum):

adjoint
-------------------------------------------------
| ``adjoint:(RootDatum->RootDatum)``
| 


.. _is_simple_for_(vec->(vec->bool)):

is_simple_for
-------------------------------------------------
| ``is_simple_for:(vec->(vec->bool))``
| 


.. _simple_from_positive_(mat,mat->mat,mat):

simple_from_positive
-------------------------------------------------
| ``simple_from_positive:(mat,mat->mat,mat)``
| 


.. _fundamental_weights_(RootDatum->[ratvec]):

fundamental_weights
-------------------------------------------------
| ``fundamental_weights:(RootDatum->[ratvec])``
| 


.. _fundamental_coweights_(RootDatum->[ratvec]):

fundamental_coweights
-------------------------------------------------
| ``fundamental_coweights:(RootDatum->[ratvec])``
| 


.. _!=_(InnerClass,InnerClass->bool):

!=
-------------------------------------------------
| ``!=:(InnerClass,InnerClass->bool)``
| 


.. _dual_integral_(InnerClass,ratvec->InnerClass):

dual_integral
-------------------------------------------------
| ``dual_integral:(InnerClass,ratvec->InnerClass)``
| 


.. _Cartan_classes_(InnerClass->[CartanClass]):

Cartan_classes
-------------------------------------------------
| ``Cartan_classes:(InnerClass->[CartanClass])``
| 


.. _print_Cartan_info_(CartanClass->):

print_Cartan_info
-------------------------------------------------
| ``print_Cartan_info:(CartanClass->)``
| 


.. _fundamental_Cartan_(InnerClass->CartanClass):

fundamental_Cartan
-------------------------------------------------
| ``fundamental_Cartan:(InnerClass->CartanClass)``
| 


.. _most_split_Cartan_(InnerClass->CartanClass):

most_split_Cartan
-------------------------------------------------
| ``most_split_Cartan:(InnerClass->CartanClass)``
| 


.. _compact_rank_(CartanClass->int):

compact_rank
-------------------------------------------------
| ``compact_rank:(CartanClass->int)``
| 


.. _split_rank_(CartanClass->int):

split_rank
-------------------------------------------------
| ``split_rank:(CartanClass->int)``
| 


.. _compact_rank_(InnerClass->int):

compact_rank
-------------------------------------------------
| ``compact_rank:(InnerClass->int)``
| 


.. _split_rank_(RealForm->int):

split_rank
-------------------------------------------------
| ``split_rank:(RealForm->int)``
| 


.. _\=_(CartanClass,CartanClass->bool):

\=
-------------------------------------------------
| ``=:(CartanClass,CartanClass->bool)``
| 


.. _number_(CartanClass,RealForm->int):

number
-------------------------------------------------
| ``number:(CartanClass,RealForm->int)``
| 


.. _!=_(RealForm,RealForm->bool):

!=
-------------------------------------------------
| ``!=:(RealForm,RealForm->bool)``
| 


.. _form_name_(RealForm->string):

form_name
-------------------------------------------------
| ``form_name:(RealForm->string)``
| 


.. _real_forms_(InnerClass->[RealForm]):

real_forms
-------------------------------------------------
| ``real_forms:(InnerClass->[RealForm])``
| 


.. _dual_real_forms_(InnerClass->[RealForm]):

dual_real_forms
-------------------------------------------------
| ``dual_real_forms:(InnerClass->[RealForm])``
| 


.. _is_quasisplit_(RealForm->bool):

is_quasisplit
-------------------------------------------------
| ``is_quasisplit:(RealForm->bool)``
| 


.. _is_quasicompact_(RealForm->bool):

is_quasicompact
-------------------------------------------------
| ``is_quasicompact:(RealForm->bool)``
| 


.. _split_form_(RootDatum->RealForm):

split_form
-------------------------------------------------
| ``split_form:(RootDatum->RealForm)``
| 


.. _split_form_(LieType->RealForm):

split_form
-------------------------------------------------
| ``split_form:(LieType->RealForm)``
| 


.. _quasicompact_form_(InnerClass->RealForm):

quasicompact_form
-------------------------------------------------
| ``quasicompact_form:(InnerClass->RealForm)``
| 


.. _is_compatible_(RealForm,RealForm->bool):

is_compatible
-------------------------------------------------
| ``is_compatible:(RealForm,RealForm->bool)``
| 


.. _is_compact_(RealForm->bool):

is_compact
-------------------------------------------------
| ``is_compact:(RealForm->bool)``
| 


.. _!=_(KGBElt,KGBElt->bool):

!=
-------------------------------------------------
| ``!=:(KGBElt,KGBElt->bool)``
| 


.. _real_form_(KGBElt->RealForm):

real_form
-------------------------------------------------
| ``real_form:(KGBElt->RealForm)``
| 


.. _\#_(KGBElt->int):

\#
-------------------------------------------------
| ``#:(KGBElt->int)``
| 


.. _root_datum_(KGBElt->RootDatum):

root_datum
-------------------------------------------------
| ``root_datum:(KGBElt->RootDatum)``
| 


.. _inner_class_(KGBElt->InnerClass):

inner_class
-------------------------------------------------
| ``inner_class:(KGBElt->InnerClass)``
| 


.. _KGB_(RealForm->[KGBElt]):

KGB
-------------------------------------------------
| ``KGB:(RealForm->[KGBElt])``
| 


.. _KGB_(CartanClass,RealForm->[KGBElt]):

KGB
-------------------------------------------------
| ``KGB:(CartanClass,RealForm->[KGBElt])``
| 


.. _KGB_elt_(InnerClass,mat,ratvec->KGBElt):

KGB_elt
-------------------------------------------------
| ``KGB_elt:(InnerClass,mat,ratvec->KGBElt)``
| 


.. _KGB_elt_(RootDatum,mat,ratvec->KGBElt):

KGB_elt
-------------------------------------------------
| ``KGB_elt:(RootDatum,mat,ratvec->KGBElt)``
| 


.. _Cartan_class_(InnerClass,mat->CartanClass):

Cartan_class
-------------------------------------------------
| ``Cartan_class:(InnerClass,mat->CartanClass)``
| 


.. _status_(vec,KGBElt->int):

status
-------------------------------------------------
| ``status:(vec,KGBElt->int)``
| 


.. _cross_(vec,KGBElt->KGBElt):

cross
-------------------------------------------------
| ``cross:(vec,KGBElt->KGBElt)``
| 


.. _Cayley_(vec,KGBElt->KGBElt):

Cayley
-------------------------------------------------
| ``Cayley:(vec,KGBElt->KGBElt)``
| 


.. _W_cross_([int],KGBElt->KGBElt):

W_cross
-------------------------------------------------
| ``W_cross:([int],KGBElt->KGBElt)``
| 


.. _KGB_status_text_(int->string):

KGB_status_text
-------------------------------------------------
| ``KGB_status_text:(int->string)``
| 


.. _status_text_(int,KGBElt->string):

status_text
-------------------------------------------------
| ``status_text:(int,KGBElt->string)``
| 


.. _status_text_(vec,KGBElt->string):

status_text
-------------------------------------------------
| ``status_text:(vec,KGBElt->string)``
| 


.. _status_texts_(KGBElt->[string]):

status_texts
-------------------------------------------------
| ``status_texts:(KGBElt->[string])``
| 


.. _is_complex_(int,KGBElt->bool):

is_complex
-------------------------------------------------
| ``is_complex:(int,KGBElt->bool)``
| 


.. _is_real_(int,KGBElt->bool):

is_real
-------------------------------------------------
| ``is_real:(int,KGBElt->bool)``
| 


.. _is_imaginary_(int,KGBElt->bool):

is_imaginary
-------------------------------------------------
| ``is_imaginary:(int,KGBElt->bool)``
| 


.. _is_noncompact_(int,KGBElt->bool):

is_noncompact
-------------------------------------------------
| ``is_noncompact:(int,KGBElt->bool)``
| 


.. _is_compact_(int,KGBElt->bool):

is_compact
-------------------------------------------------
| ``is_compact:(int,KGBElt->bool)``
| 


.. _is_descent_(int,KGBElt->bool):

is_descent
-------------------------------------------------
| ``is_descent:(int,KGBElt->bool)``
| 


.. _is_ascent_(int,KGBElt->bool):

is_ascent
-------------------------------------------------
| ``is_ascent:(int,KGBElt->bool)``
| 


.. _is_strict_descent_(int,KGBElt->bool):

is_strict_descent
-------------------------------------------------
| ``is_strict_descent:(int,KGBElt->bool)``
| 


.. _is_imaginary_(KGBElt->(vec->bool)):

is_imaginary
-------------------------------------------------
| ``is_imaginary:(KGBElt->(vec->bool))``
| 


.. _is_real_(KGBElt->(vec->bool)):

is_real
-------------------------------------------------
| ``is_real:(KGBElt->(vec->bool))``
| 


.. _is_complex_(KGBElt->(vec->bool)):

is_complex
-------------------------------------------------
| ``is_complex:(KGBElt->(vec->bool))``
| 


.. _imaginary_posroots_(KGBElt->mat):

imaginary_posroots
-------------------------------------------------
| ``imaginary_posroots:(KGBElt->mat)``
| 


.. _real_posroots_(KGBElt->mat):

real_posroots
-------------------------------------------------
| ``real_posroots:(KGBElt->mat)``
| 


.. _imaginary_poscoroots_(KGBElt->mat):

imaginary_poscoroots
-------------------------------------------------
| ``imaginary_poscoroots:(KGBElt->mat)``
| 


.. _real_poscoroots_(KGBElt->mat):

real_poscoroots
-------------------------------------------------
| ``real_poscoroots:(KGBElt->mat)``
| 


.. _imaginary_sys_(KGBElt->mat,mat):

imaginary_sys
-------------------------------------------------
| ``imaginary_sys:(KGBElt->mat,mat)``
| 


.. _real_sys_(KGBElt->mat,mat):

real_sys
-------------------------------------------------
| ``real_sys:(KGBElt->mat,mat)``
| 


.. _rho_i_(KGBElt->ratvec):

rho_i
-------------------------------------------------
| ``rho_i:(KGBElt->ratvec)``
| 


.. _rho_r_(KGBElt->ratvec):

rho_r
-------------------------------------------------
| ``rho_r:(KGBElt->ratvec)``
| 


.. _rho_check_i_(KGBElt->ratvec):

rho_check_i
-------------------------------------------------
| ``rho_check_i:(KGBElt->ratvec)``
| 


.. _rho_check_r_(KGBElt->ratvec):

rho_check_r
-------------------------------------------------
| ``rho_check_r:(KGBElt->ratvec)``
| 


.. _rho_i_(RootDatum,mat->ratvec):

rho_i
-------------------------------------------------
| ``rho_i:(RootDatum,mat->ratvec)``
| 


.. _rho_r_(RootDatum,mat->ratvec):

rho_r
-------------------------------------------------
| ``rho_r:(RootDatum,mat->ratvec)``
| 


.. _rho_check_i_(RootDatum,mat->ratvec):

rho_check_i
-------------------------------------------------
| ``rho_check_i:(RootDatum,mat->ratvec)``
| 


.. _rho_check_r_(RootDatum,mat->ratvec):

rho_check_r
-------------------------------------------------
| ``rho_check_r:(RootDatum,mat->ratvec)``
| 


.. _is_compact_(KGBElt->(vec->bool)):

is_compact
-------------------------------------------------
| ``is_compact:(KGBElt->(vec->bool))``
| 


.. _is_noncompact_(KGBElt->(vec->bool)):

is_noncompact
-------------------------------------------------
| ``is_noncompact:(KGBElt->(vec->bool))``
| 


.. _is_compact_imaginary_(KGBElt->(vec->bool)):

is_compact_imaginary
-------------------------------------------------
| ``is_compact_imaginary:(KGBElt->(vec->bool))``
| 


.. _is_noncompact_imaginary_(KGBElt->(vec->bool)):

is_noncompact_imaginary
-------------------------------------------------
| ``is_noncompact_imaginary:(KGBElt->(vec->bool))``
| 


.. _compact_posroots_(KGBElt->mat):

compact_posroots
-------------------------------------------------
| ``compact_posroots:(KGBElt->mat)``
| 


.. _noncompact_posroots_(KGBElt->mat):

noncompact_posroots
-------------------------------------------------
| ``noncompact_posroots:(KGBElt->mat)``
| 


.. _rho_ci_(KGBElt->ratvec):

rho_ci
-------------------------------------------------
| ``rho_ci:(KGBElt->ratvec)``
| 


.. _rho_nci_(KGBElt->ratvec):

rho_nci
-------------------------------------------------
| ``rho_nci:(KGBElt->ratvec)``
| 


.. _is_imaginary_(vec,KGBElt->bool):

is_imaginary
-------------------------------------------------
| ``is_imaginary:(vec,KGBElt->bool)``
| 


.. _is_real_(vec,KGBElt->bool):

is_real
-------------------------------------------------
| ``is_real:(vec,KGBElt->bool)``
| 


.. _is_complex_(vec,KGBElt->bool):

is_complex
-------------------------------------------------
| ``is_complex:(vec,KGBElt->bool)``
| 


.. _is_compact_imaginary_(vec,KGBElt->bool):

is_compact_imaginary
-------------------------------------------------
| ``is_compact_imaginary:(vec,KGBElt->bool)``
| 


.. _is_noncompact_imaginary_(vec,KGBElt->bool):

is_noncompact_imaginary
-------------------------------------------------
| ``is_noncompact_imaginary:(vec,KGBElt->bool)``
| 


.. _print_KGB_(KGBElt->):

print_KGB
-------------------------------------------------
| ``print_KGB:(KGBElt->)``
| 


.. _no_Cminus_roots_(KGBElt->bool):

no_Cminus_roots
-------------------------------------------------
| ``no_Cminus_roots:(KGBElt->bool)``
| 


.. _no_Cplus_roots_(KGBElt->bool):

no_Cplus_roots
-------------------------------------------------
| ``no_Cplus_roots:(KGBElt->bool)``
| 


.. _blocks_(InnerClass->[Block]):

blocks
-------------------------------------------------
| ``blocks:(InnerClass->[Block])``
| 


.. _raw_KL_(RealForm,RealForm->mat,[vec],vec):

raw_KL
-------------------------------------------------
| ``raw_KL:(RealForm,RealForm->mat,[vec],vec)``
| 


.. _dual_KL_(RealForm,RealForm->mat,[vec],vec):

dual_KL
-------------------------------------------------
| ``dual_KL:(RealForm,RealForm->mat,[vec],vec)``
| 


.. _print_block_(RealForm,RealForm->):

print_block
-------------------------------------------------
| ``print_block:(RealForm,RealForm->)``
| 


.. _print_blocku_(RealForm,RealForm->):

print_blocku
-------------------------------------------------
| ``print_blocku:(RealForm,RealForm->)``
| 


.. _print_blockd_(RealForm,RealForm->):

print_blockd
-------------------------------------------------
| ``print_blockd:(RealForm,RealForm->)``
| 


.. _print_KL_basis_(RealForm,RealForm->):

print_KL_basis
-------------------------------------------------
| ``print_KL_basis:(RealForm,RealForm->)``
| 


.. _print_prim_KL_(RealForm,RealForm->):

print_prim_KL
-------------------------------------------------
| ``print_prim_KL:(RealForm,RealForm->)``
| 


.. _print_KL_list_(RealForm,RealForm->):

print_KL_list
-------------------------------------------------
| ``print_KL_list:(RealForm,RealForm->)``
| 


.. _print_W_cells_(RealForm,RealForm->):

print_W_cells
-------------------------------------------------
| ``print_W_cells:(RealForm,RealForm->)``
| 


.. _print_W_graph_(RealForm,RealForm->):

print_W_graph
-------------------------------------------------
| ``print_W_graph:(RealForm,RealForm->)``
| 


.. _!=_(Param,Param->bool):

!=
-------------------------------------------------
| ``!=:(Param,Param->bool)``
| 


.. _root_datum_(Param->RootDatum):

root_datum
-------------------------------------------------
| ``root_datum:(Param->RootDatum)``
| 


.. _inner_class_(Param->InnerClass):

inner_class
-------------------------------------------------
| ``inner_class:(Param->InnerClass)``
| 


.. _null_module_(Param->ParamPol):

null_module
-------------------------------------------------
| ``null_module:(Param->ParamPol)``
| 


.. _\*_(Param,rat->Param):

\*
-------------------------------------------------
| ``*:(Param,rat->Param)``
| 


.. _x_(Param->KGBElt):

x
-------------------------------------------------
| ``x:(Param->KGBElt)``
| 


.. _lambda_minus_rho_(Param->vec):

lambda_minus_rho
-------------------------------------------------
| ``lambda_minus_rho:(Param->vec)``
| 


.. _lambda_(Param->ratvec):

lambda
-------------------------------------------------
| ``lambda:(Param->ratvec)``
| 


.. _infinitesimal_character_(Param->ratvec):

infinitesimal_character
-------------------------------------------------
| ``infinitesimal_character:(Param->ratvec)``
| 


.. _nu_(Param->ratvec):

nu
-------------------------------------------------
| ``nu:(Param->ratvec)``
| 


.. _Cartan_class_(Param->CartanClass):

Cartan_class
-------------------------------------------------
| ``Cartan_class:(Param->CartanClass)``
| 


.. _involution_(Param->mat):

involution
-------------------------------------------------
| ``involution:(Param->mat)``
| 


.. _integrality_datum_(Param->RootDatum):

integrality_datum
-------------------------------------------------
| ``integrality_datum:(Param->RootDatum)``
| 


.. _is_regular_(Param->bool):

is_regular
-------------------------------------------------
| ``is_regular:(Param->bool)``
| 


.. _trivial_(RealForm->Param):

trivial
-------------------------------------------------
| ``trivial:(RealForm->Param)``
| 


.. _W_cross_([int],Param->Param):

W_cross
-------------------------------------------------
| ``W_cross:([int],Param->Param)``
| 


.. _parameter_(RealForm,int,ratvec,ratvec->Param):

parameter
-------------------------------------------------
| ``parameter:(RealForm,int,ratvec,ratvec->Param)``
| 


.. _parameter_(KGBElt,ratvec,ratvec->Param):

parameter
-------------------------------------------------
| ``parameter:(KGBElt,ratvec,ratvec->Param)``
| 


.. _parameter_gamma_(KGBElt,ratvec,ratvec->Param):

parameter_gamma
-------------------------------------------------
| ``parameter_gamma:(KGBElt,ratvec,ratvec->Param)``
| 


.. _block_of_(Param->[Param]):

block_of
-------------------------------------------------
| ``block_of:(Param->[Param])``
| 


.. _imaginary_type_(int,Param->int):

imaginary_type
-------------------------------------------------
| ``imaginary_type:(int,Param->int)``
| 


.. _real_type_(int,Param->int):

real_type
-------------------------------------------------
| ``real_type:(int,Param->int)``
| 


.. _imaginary_type_(vec,Param->int):

imaginary_type
-------------------------------------------------
| ``imaginary_type:(vec,Param->int)``
| 


.. _real_type_(vec,Param->int):

real_type
-------------------------------------------------
| ``real_type:(vec,Param->int)``
| 


.. _is_nonparity_(int,Param->bool):

is_nonparity
-------------------------------------------------
| ``is_nonparity:(int,Param->bool)``
| 


.. _is_parity_(int,Param->bool):

is_parity
-------------------------------------------------
| ``is_parity:(int,Param->bool)``
| 


.. _is_nonparity_(vec,Param->bool):

is_nonparity
-------------------------------------------------
| ``is_nonparity:(vec,Param->bool)``
| 


.. _is_parity_(vec,Param->bool):

is_parity
-------------------------------------------------
| ``is_parity:(vec,Param->bool)``
| 


.. _status_(vec,Param->int):

status
-------------------------------------------------
| ``status:(vec,Param->int)``
| 


.. _status_(int,Param->int):

status
-------------------------------------------------
| ``status:(int,Param->int)``
| 


.. _block_status_text_(int->string):

block_status_text
-------------------------------------------------
| ``block_status_text:(int->string)``
| 


.. _status_text_(int,Param->string):

status_text
-------------------------------------------------
| ``status_text:(int,Param->string)``
| 


.. _status_texts_(Param->[string]):

status_texts
-------------------------------------------------
| ``status_texts:(Param->[string])``
| 


.. _status_text_(vec,Param->string):

status_text
-------------------------------------------------
| ``status_text:(vec,Param->string)``
| 


.. _parity_poscoroots_(Param->mat):

parity_poscoroots
-------------------------------------------------
| ``parity_poscoroots:(Param->mat)``
| 


.. _nonparity_poscoroots_(Param->mat):

nonparity_poscoroots
-------------------------------------------------
| ``nonparity_poscoroots:(Param->mat)``
| 


.. _is_descent_(int,Param->bool):

is_descent
-------------------------------------------------
| ``is_descent:(int,Param->bool)``
| 


.. _tau_bitset_(Param->(int->bool),int):

tau_bitset
-------------------------------------------------
| ``tau_bitset:(Param->(int->bool),int)``
| 


.. _tau_(Param->[int]):

tau
-------------------------------------------------
| ``tau:(Param->[int])``
| 


.. _tau_complement_(Param->[int]):

tau_complement
-------------------------------------------------
| ``tau_complement:(Param->[int])``
| 


.. _is_descent_(vec,Param->bool):

is_descent
-------------------------------------------------
| ``is_descent:(vec,Param->bool)``
| 


.. _lookup_(Param,[Param]->int):

lookup
-------------------------------------------------
| ``lookup:(Param,[Param]->int)``
| 


.. _has_double_extended_Cayley_(int->bool):

has_double_extended_Cayley
-------------------------------------------------
| ``has_double_extended_Cayley:(int->bool)``
| 


.. _print_extended_block_(Param,mat->):

print_extended_block
-------------------------------------------------
| ``print_extended_block:(Param,mat->)``
| 


.. _null_module_(ParamPol->ParamPol):

null_module
-------------------------------------------------
| ``null_module:(ParamPol->ParamPol)``
| 


.. _\-_(ParamPol->ParamPol):

\-
-------------------------------------------------
| ``-:(ParamPol->ParamPol)``
| 


.. _first_param_(ParamPol->Param):

first_param
-------------------------------------------------
| ``first_param:(ParamPol->Param)``
| 


.. _last_param_(ParamPol->Param):

last_param
-------------------------------------------------
| ``last_param:(ParamPol->Param)``
| 


.. _s_to_1_(ParamPol->ParamPol):

s_to_1
-------------------------------------------------
| ``s_to_1:(ParamPol->ParamPol)``
| 


.. _s_to_minus_1_(ParamPol->ParamPol):

s_to_minus_1
-------------------------------------------------
| ``s_to_minus_1:(ParamPol->ParamPol)``
| 


.. _\-_(ParamPol,(Split,Param)->ParamPol):

\-
-------------------------------------------------
| ``-:(ParamPol,(Split,Param)->ParamPol)``
| 


.. _\*_(ParamPol,rat->ParamPol):

\*
-------------------------------------------------
| ``*:(ParamPol,rat->ParamPol)``
| 


.. _divide_by_(int,ParamPol->ParamPol):

divide_by
-------------------------------------------------
| ``divide_by:(int,ParamPol->ParamPol)``
| 


.. _root_datum_(ParamPol->RootDatum):

root_datum
-------------------------------------------------
| ``root_datum:(ParamPol->RootDatum)``
| 


.. _virtual_(Param->ParamPol):

virtual
-------------------------------------------------
| ``virtual:(Param->ParamPol)``
| 


.. _virtual_(RealForm,[Param]->ParamPol):

virtual
-------------------------------------------------
| ``virtual:(RealForm,[Param]->ParamPol)``
| 


.. _pol_format_(ParamPol->):

pol_format
-------------------------------------------------
| ``pol_format:(ParamPol->)``
| 


.. _infinitesimal_character_(ParamPol->ratvec):

infinitesimal_character
-------------------------------------------------
| ``infinitesimal_character:(ParamPol->ratvec)``
| 


.. _separate_by_infinitesimal_character_(ParamPol->[(ratvec,ParamPol)]):

separate_by_infinitesimal_character
-------------------------------------------------
| ``separate_by_infinitesimal_character:(ParamPol->[(ratvec,ParamPol)])``
| 


.. _in_string_list_(string,[string]->bool):

in_string_list
-------------------------------------------------
| ``in_string_list:(string,[string]->bool)``
| 


.. _positive_imaginary_roots_and_coroots_(RootDatum,mat->mat,mat):

positive_imaginary_roots_and_coroots
-------------------------------------------------
| ``positive_imaginary_roots_and_coroots:(RootDatum,mat->mat,mat)``
| 


.. _positive_imaginary_roots_and_coroots_(KGBElt->mat,mat):

positive_imaginary_roots_and_coroots
-------------------------------------------------
| ``positive_imaginary_roots_and_coroots:(KGBElt->mat,mat)``
| 


.. _imaginary_roots_and_coroots_(RootDatum,mat->mat,mat):

imaginary_roots_and_coroots
-------------------------------------------------
| ``imaginary_roots_and_coroots:(RootDatum,mat->mat,mat)``
| 


.. _imaginary_roots_and_coroots_(KGBElt->mat,mat):

imaginary_roots_and_coroots
-------------------------------------------------
| ``imaginary_roots_and_coroots:(KGBElt->mat,mat)``
| 


.. _positive_real_roots_and_coroots_(RootDatum,mat->mat,mat):

positive_real_roots_and_coroots
-------------------------------------------------
| ``positive_real_roots_and_coroots:(RootDatum,mat->mat,mat)``
| 


.. _positive_real_roots_and_coroots_(KGBElt->mat,mat):

positive_real_roots_and_coroots
-------------------------------------------------
| ``positive_real_roots_and_coroots:(KGBElt->mat,mat)``
| 


.. _real_roots_and_coroots_(RootDatum,mat->mat,mat):

real_roots_and_coroots
-------------------------------------------------
| ``real_roots_and_coroots:(RootDatum,mat->mat,mat)``
| 


.. _real_roots_and_coroots_(KGBElt->mat,mat):

real_roots_and_coroots
-------------------------------------------------
| ``real_roots_and_coroots:(KGBElt->mat,mat)``
| 


.. _complex_posroots_(RootDatum,mat->mat):

complex_posroots
-------------------------------------------------
| ``complex_posroots:(RootDatum,mat->mat)``
| 


.. _complex_posroots_(KGBElt->mat):

complex_posroots
-------------------------------------------------
| ``complex_posroots:(KGBElt->mat)``
| 


.. _monomials_(ParamPol->[Param]):

monomials
-------------------------------------------------
| ``monomials:(ParamPol->[Param])``
| 


.. _monomial_(ParamPol,int->Param):

monomial
-------------------------------------------------
| ``monomial:(ParamPol,int->Param)``
| 


.. _delete_([int],int->[int]):

delete
-------------------------------------------------
| ``delete:([int],int->[int])``
| 


.. _delete_([vec],int->[vec]):

delete
-------------------------------------------------
| ``delete:([vec],int->[vec])``
| 


.. _delete_([ratvec],int->[ratvec]):

delete
-------------------------------------------------
| ``delete:([ratvec],int->[ratvec])``
| 


.. _delete_([[ratvec]],int->[[ratvec]]):

delete
-------------------------------------------------
| ``delete:([[ratvec]],int->[[ratvec]])``
| 


.. _delete_([[vec]],int->[[vec]]):

delete
-------------------------------------------------
| ``delete:([[vec]],int->[[vec]])``
| 


.. _delete_([ParamPol],int->[ParamPol]):

delete
-------------------------------------------------
| ``delete:([ParamPol],int->[ParamPol])``
| 


.. _find_([int],int->int):

find
-------------------------------------------------
| ``find:([int],int->int)``
| 


.. _find_([Param],Param->int):

find
-------------------------------------------------
| ``find:([Param],Param->int)``
| 


.. _find_([KGBElt],KGBElt->int):

find
-------------------------------------------------
| ``find:([KGBElt],KGBElt->int)``
| 


.. _find_([[int]],[int]->int):

find
-------------------------------------------------
| ``find:([[int]],[int]->int)``
| 


.. _find_vec_([vec],vec->int):

find_vec
-------------------------------------------------
| ``find_vec:([vec],vec->int)``
| 


.. _pad_(string,int->string):

pad
-------------------------------------------------
| ``pad:(string,int->string)``
| 


.. _extended_status_texts_[string]:

extended_status_texts
-------------------------------------------------
| ``extended_status_texts:[string]``
| 


