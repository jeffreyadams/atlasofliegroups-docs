.. _basic.at_ref:

basic.at Function References
=======================================================
|

.. _\#_(int->[int])1:

\#
-------------------------------------------------
| ``#:(int->[int])``
| 

Generate an array of given length, starting from 0.

::

    atlas> #(10)
    Value: [0,1,2,3,4,5,6,7,8,9]



.. _\#_(bool->int)1:

\#
-------------------------------------------------
| ``#:(bool->int)``
| 

Output integers 0 or 1 from boolean values.

::

    atlas> #(true)
    Value: 1
    atlas> #(false)
    Value: 0


.. _\^_(bool,bool->bool)1:

\^
-------------------------------------------------
| ``^:(bool,bool->bool)``
| 

The xor operator.

::

    atlas> true^false
    Value: true
    atlas> true^true
    Value: false
    

.. _assert_(bool,string->)1:

assert
-------------------------------------------------
| ``assert:(bool,string->)``
| 


.. _assert_(bool->)1:

assert
-------------------------------------------------
| ``assert:(bool->)``
| 


.. _list_((int->bool),int->[int])1:

list
-------------------------------------------------
| ``list:((int->bool),int->[int])``
| 


.. _complement_((int->bool),int->[int])1:

complement
-------------------------------------------------
| ``complement:((int->bool),int->[int])``
| 


.. _count_((int->bool),int->int)1:

count
-------------------------------------------------
| ``count:((int->bool),int->int)``
| 


.. _all_([bool]->bool)1:

all
-------------------------------------------------
| ``all:([bool]->bool)``
| 


.. _none_([bool]->bool)1:

none
-------------------------------------------------
| ``none:([bool]->bool)``
| 


.. _first_([bool]->int)1:

first
-------------------------------------------------
| ``first:([bool]->int)``
| 


.. _last_([bool]->int)1:

last
-------------------------------------------------
| ``last:([bool]->int)``
| 


.. _all_(int,(int->bool)->bool)1:

all
-------------------------------------------------
| ``all:(int,(int->bool)->bool)``
| 


.. _none_(int,(int->bool)->bool)1:

none
-------------------------------------------------
| ``none:(int,(int->bool)->bool)``
| 


.. _first_(int,(int->bool)->int)1:

first
-------------------------------------------------
| ``first:(int,(int->bool)->int)``
| 


.. _last_(int,(int->bool)->int)1:

last
-------------------------------------------------
| ``last:(int,(int->bool)->int)``
| 


.. _all_([(->bool)]->bool)1:

all
-------------------------------------------------
| ``all:([(->bool)]->bool)``
| 


.. _none_([(->bool)]->bool)1:

none
-------------------------------------------------
| ``none:([(->bool)]->bool)``
| 


.. _first_([(->bool)]->int)1:

first
-------------------------------------------------
| ``first:([(->bool)]->int)``
| 


.. _last_([(->bool)]->int)1:

last
-------------------------------------------------
| ``last:([(->bool)]->int)``
| 


.. _abs_(int->int)1:

abs
-------------------------------------------------
| ``abs:(int->int)``
| 


.. _sign_(int->int)1:

sign
-------------------------------------------------
| ``sign:(int->int)``
| 


.. _is_odd_(int->bool)1:

is_odd
-------------------------------------------------
| ``is_odd:(int->bool)``
| 


.. _is_even_(int->bool)1:

is_even
-------------------------------------------------
| ``is_even:(int->bool)``
| 


.. _min_(int,int->int)1:

min
-------------------------------------------------
| ``min:(int,int->int)``
| 


.. _max_(int,int->int)1:

max
-------------------------------------------------
| ``max:(int,int->int)``
| 


.. _min_([int]->int)1:

min
-------------------------------------------------
| ``min:([int]->int)``
| 


.. _max_([int]->int)1:

max
-------------------------------------------------
| ``max:([int]->int)``
| 


.. _min_loc_([int]->int)1:

min_loc
-------------------------------------------------
| ``min_loc:([int]->int)``
| 


.. _max_loc_([int]->int)1:

max_loc
-------------------------------------------------
| ``max_loc:([int]->int)``
| 


.. _min_(int->([int]->int))1:

min
-------------------------------------------------
| ``min:(int->([int]->int))``
| 


.. _max_(int->([int]->int))1:

max
-------------------------------------------------
| ``max:(int->([int]->int))``
| 


.. _lcm_([int]->int)1:

lcm
-------------------------------------------------
| ``lcm:([int]->int)``
| 


.. _\=_((int,int),(int,int)->bool)1:

\=
-------------------------------------------------
| ``=:((int,int),(int,int)->bool)``
| 


.. _!=_((int,int),(int,int)->bool)1:

!=
-------------------------------------------------
| ``!=:((int,int),(int,int)->bool)``
| 


.. _numer_(rat->int)1:

numer
-------------------------------------------------
| ``numer:(rat->int)``
| 


.. _denom_(rat->int)1:

denom
-------------------------------------------------
| ``denom:(rat->int)``
| 


.. _is_integer_(rat->bool)1:

is_integer
-------------------------------------------------
| ``is_integer:(rat->bool)``
| 


.. _sign_(rat->int)1:

sign
-------------------------------------------------
| ``sign:(rat->int)``
| 


.. _abs_(rat->rat)1:

abs
-------------------------------------------------
| ``abs:(rat->rat)``
| 


.. _floor_(rat->int)1:

floor
-------------------------------------------------
| ``floor:(rat->int)``
| 


.. _ceil_(rat->int)1:

ceil
-------------------------------------------------
| ``ceil:(rat->int)``
| 


.. _\\_(rat,int->int)1:

\\
-------------------------------------------------
| ``\:(rat,int->int)``
| 


.. _\\_(rat,rat->int)1:

\\
-------------------------------------------------
| ``\:(rat,rat->int)``
| 


.. _\%_(rat,int->int,rat)1:

\%
-------------------------------------------------
| ``\%:(rat,int->int,rat)``
| 


.. _\%_(rat,rat->int,rat)1:

\%
-------------------------------------------------
| ``\%:(rat,rat->int,rat)``
| 


.. _floor_([rat]->vec)1:

floor
-------------------------------------------------
| ``floor:([rat]->vec)``
| 


.. _ceil_([rat]->vec)1:

ceil
-------------------------------------------------
| ``ceil:([rat]->vec)``
| 


.. _rat_as_int_(rat->int)1:

rat_as_int
-------------------------------------------------
| ``rat_as_int:(rat->int)``
| 


.. _\+_(string,string->string)1:

\+
-------------------------------------------------
| ``+:(string,string->string)``
| 


.. _\*_(string,int->string)1:

\*
-------------------------------------------------
| ``*:(string,int->string)``
| 


.. _\*_(int,string->string)1:

\*
-------------------------------------------------
| ``*:(int,string->string)``
| 


.. _\+_(string,int->string)1:

\+
-------------------------------------------------
| ``+:(string,int->string)``
| 


.. _\+_(int,string->string)1:

\+
-------------------------------------------------
| ``+:(int,string->string)``
| 


.. _\+_(string,(int,int)->string)1:

\+
-------------------------------------------------
| ``+:(string,(int,int)->string)``
| 


.. _plural_(int->string)1:

plural
-------------------------------------------------
| ``plural:(int->string)``
| 


.. _plural_(int,string->string)1:

plural
-------------------------------------------------
| ``plural:(int,string->string)``
| 


.. _concat_([string]->string)1:

concat
-------------------------------------------------
| ``concat:([string]->string)``
| 


.. _l_adjust_(int,string->string)1:

l_adjust
-------------------------------------------------
| ``l_adjust:(int,string->string)``
| 


.. _r_adjust_(int,string->string)1:

r_adjust
-------------------------------------------------
| ``r_adjust:(int,string->string)``
| 


.. _c_adjust_(int,string->string)1:

c_adjust
-------------------------------------------------
| ``c_adjust:(int,string->string)``
| 


.. _width_(int->int)1:

width
-------------------------------------------------
| ``width:(int->int)``
| 


.. _split_lines_(string->[string])1:

split_lines
-------------------------------------------------
| ``split_lines:(string->[string])``
| 


.. _is_substring_(string,string->bool)1:

is_substring
-------------------------------------------------
| ``is_substring:(string,string->bool)``
| 


.. _fgrep_(string,string->[string])1:

fgrep
-------------------------------------------------
| ``fgrep:(string,string->[string])``
| 


.. _vector_(int,(int->int)->vec)1:

vector
-------------------------------------------------
| ``vector:(int,(int->int)->vec)``
| 


.. _ones_(int->vec)1:

ones
-------------------------------------------------
| ``ones:(int->vec)``
| 


.. _gcd_([int]->int)1:

gcd
-------------------------------------------------
| ``gcd:([int]->int)``
| 


.. _\*_(int,vec->vec)1:

\*
-------------------------------------------------
| ``*:(int,vec->vec)``
| 


.. _sum_(vec->int)1:

sum
-------------------------------------------------
| ``sum:(vec->int)``
| 


.. _product_(vec->int)1:

product
-------------------------------------------------
| ``product:(vec->int)``
| 


.. _reverse_(vec->vec)1:

reverse
-------------------------------------------------
| ``reverse:(vec->vec)``
| 


.. _lower_(int,vec->vec)1:

lower
-------------------------------------------------
| ``lower:(int,vec->vec)``
| 


.. _upper_(int,vec->vec)1:

upper
-------------------------------------------------
| ``upper:(int,vec->vec)``
| 


.. _drop_lower_(int,vec->vec)1:

drop_lower
-------------------------------------------------
| ``drop_lower:(int,vec->vec)``
| 


.. _drop_upper_(int,vec->vec)1:

drop_upper
-------------------------------------------------
| ``drop_upper:(int,vec->vec)``
| 


.. _<=_(vec->bool)1:

<=
-------------------------------------------------
| ``<=:(vec->bool)``
| 


.. _<_(vec->bool)1:

<
-------------------------------------------------
| ``<:(vec->bool)``
| 


.. _is_member_([int]->(int->bool))1:

is_member
-------------------------------------------------
| ``is_member:([int]->(int->bool))``
| 


.. _contains_(int->([int]->bool))1:

contains
-------------------------------------------------
| ``contains:(int->([int]->bool))``
| 


.. _all_0_1_vecs_(int->[vec])1:

all_0_1_vecs
-------------------------------------------------
| ``all_0_1_vecs:(int->[vec])``
| 


.. _power_set_(int->[[int]])1:

power_set
-------------------------------------------------
| ``power_set:(int->[[int]])``
| 


.. _power_set_([int]->[[int]])1:

power_set
-------------------------------------------------
| ``power_set:([int]->[[int]])``
| 


.. _matrix_((int,int),(int,int->int)->mat)1:

matrix
-------------------------------------------------
| ``matrix:((int,int),(int,int->int)->mat)``
| 


.. _n_rows_(mat->int)1:

n_rows
-------------------------------------------------
| ``n_rows:(mat->int)``
| 


.. _n_columns_(mat->int)1:

n_columns
-------------------------------------------------
| ``n_columns:(mat->int)``
| 


.. _column_(vec->mat)1:

column
-------------------------------------------------
| ``column:(vec->mat)``
| 


.. _row_(vec->mat)1:

row
-------------------------------------------------
| ``row:(vec->mat)``
| 


.. _\=_(mat,int->bool)1:

\=
-------------------------------------------------
| ``=:(mat,int->bool)``
| 


.. _\#_(mat,vec->mat)1:

\#
-------------------------------------------------
| ``#:(mat,vec->mat)``
| 


.. _\#_(vec,mat->mat)1:

\#
-------------------------------------------------
| ``#:(vec,mat->mat)``
| 


.. _\^_(mat,vec->mat)1:

\^
-------------------------------------------------
| ``^:(mat,vec->mat)``
| 


.. _\^_(vec,mat->mat)1:

\^
-------------------------------------------------
| ``^:(vec,mat->mat)``
| 


.. _##_(mat,mat->mat)1:

##
-------------------------------------------------
| ``##:(mat,mat->mat)``
| 


.. _\^_(mat,mat->mat)1:

\^
-------------------------------------------------
| ``^:(mat,mat->mat)``
| 


.. _##_(int,[mat]->mat)1:

##
-------------------------------------------------
| ``##:(int,[mat]->mat)``
| 


.. _map_on_(mat->((int->int)->mat))1:

map_on
-------------------------------------------------
| ``map_on:(mat->((int->int)->mat))``
| 


.. _\*_(int,mat->mat)1:

\*
-------------------------------------------------
| ``*:(int,mat->mat)``
| 


.. _\-_(mat->mat)1:

\-
-------------------------------------------------
| ``-:(mat->mat)``
| 


.. _\\_(mat,int->mat)1:

\\
-------------------------------------------------
| ``\:(mat,int->mat)``
| 


.. _%_(mat,int->mat)1:

%
-------------------------------------------------
| ``%:(mat,int->mat)``
| 


.. _\^_(mat,int->mat)1:

\^
-------------------------------------------------
| ``^:(mat,int->mat)``
| 


.. _inverse_(mat->mat)1:

inverse
-------------------------------------------------
| ``inverse:(mat->mat)``
| 


.. _det_(mat->int)1:

det
-------------------------------------------------
| ``det:(mat->int)``
| 


.. _saturated_span_(mat->bool)1:

saturated_span
-------------------------------------------------
| ``saturated_span:(mat->bool)``
| 


.. _all_(mat,(vec->bool)->bool)1:

all
-------------------------------------------------
| ``all:(mat,(vec->bool)->bool)``
| 


.. _none_(mat,(vec->bool)->bool)1:

none
-------------------------------------------------
| ``none:(mat,(vec->bool)->bool)``
| 


.. _first_(mat,(vec->bool)->int)1:

first
-------------------------------------------------
| ``first:(mat,(vec->bool)->int)``
| 


.. _last_(mat,(vec->bool)->int)1:

last
-------------------------------------------------
| ``last:(mat,(vec->bool)->int)``
| 


.. _columns_with_((int,vec->bool),mat->mat)1:

columns_with
-------------------------------------------------
| ``columns_with:((int,vec->bool),mat->mat)``
| 


.. _columns_with_((vec->bool),mat->mat)1:

columns_with
-------------------------------------------------
| ``columns_with:((vec->bool),mat->mat)``
| 


.. _columns_with_((int->bool),mat->mat)1:

columns_with
-------------------------------------------------
| ``columns_with:((int->bool),mat->mat)``
| 


.. _rows_with_((int,vec->bool),mat->mat)1:

rows_with
-------------------------------------------------
| ``rows_with:((int,vec->bool),mat->mat)``
| 


.. _rows_with_((vec->bool),mat->mat)1:

rows_with
-------------------------------------------------
| ``rows_with:((vec->bool),mat->mat)``
| 


.. _rows_with_((int->bool),mat->mat)1:

rows_with
-------------------------------------------------
| ``rows_with:((int->bool),mat->mat)``
| 


.. _>=_(mat->bool)1:

>=
-------------------------------------------------
| ``>=:(mat->bool)``
| 


.. _>_(mat->bool)1:

>
-------------------------------------------------
| ``>:(mat->bool)``
| 


.. _<=_(mat->bool)1:

<=
-------------------------------------------------
| ``<=:(mat->bool)``
| 


.. _<_(mat->bool)1:

<
-------------------------------------------------
| ``<:(mat->bool)``
| 


.. _lookup_column_(vec,mat->int)1:

lookup_column
-------------------------------------------------
| ``lookup_column:(vec,mat->int)``
| 


.. _lookup_row_(vec,mat->int)1:

lookup_row
-------------------------------------------------
| ``lookup_row:(vec,mat->int)``
| 


.. _sum_(mat->vec)1:

sum
-------------------------------------------------
| ``sum:(mat->vec)``
| 


.. _solve_(mat,vec->[vec])1:

solve
-------------------------------------------------
| ``solve:(mat,vec->[vec])``
| 


.. _order_(mat->int)1:

order
-------------------------------------------------
| ``order:(mat->int)``
| 


.. _numer_(ratvec->vec)1:

numer
-------------------------------------------------
| ``numer:(ratvec->vec)``
| 


.. _denom_(ratvec->int)1:

denom
-------------------------------------------------
| ``denom:(ratvec->int)``
| 


.. _\*_(int,ratvec->ratvec)1:

\*
-------------------------------------------------
| ``*:(int,ratvec->ratvec)``
| 


.. _\*_(rat,ratvec->ratvec)1:

\*
-------------------------------------------------
| ``*:(rat,ratvec->ratvec)``
| 


.. _##_(ratvec,ratvec->ratvec)1:

##
-------------------------------------------------
| ``##:(ratvec,ratvec->ratvec)``
| 


.. _##_([ratvec]->ratvec)1:

##
-------------------------------------------------
| ``##:([ratvec]->ratvec)``
| 


.. _sum_([ratvec],int->ratvec)1:

sum
-------------------------------------------------
| ``sum:([ratvec],int->ratvec)``
| 


.. _\*_([ratvec],ratvec->ratvec)1:

\*
-------------------------------------------------
| ``*:([ratvec],ratvec->ratvec)``
| 


.. _is_integer_(ratvec->bool)1:

is_integer
-------------------------------------------------
| ``is_integer:(ratvec->bool)``
| 


.. _\*_(ratvec,ratvec->rat)1:

\*
-------------------------------------------------
| ``*:(ratvec,ratvec->rat)``
| 


.. _\*_(vec,ratvec->rat)1:

\*
-------------------------------------------------
| ``*:(vec,ratvec->rat)``
| 


.. _\\_(ratvec,int->vec)1:

\\
-------------------------------------------------
| ``\:(ratvec,int->vec)``
| 


.. _ratvec_as_vec_(ratvec->vec)1:

ratvec_as_vec
-------------------------------------------------
| ``ratvec_as_vec:(ratvec->vec)``
| 


.. _reverse_(ratvec->ratvec)1:

reverse
-------------------------------------------------
| ``reverse:(ratvec->ratvec)``
| 


.. _lower_(int,ratvec->ratvec)1:

lower
-------------------------------------------------
| ``lower:(int,ratvec->ratvec)``
| 


.. _upper_(int,ratvec->ratvec)1:

upper
-------------------------------------------------
| ``upper:(int,ratvec->ratvec)``
| 


.. _drop_lower_(int,ratvec->ratvec)1:

drop_lower
-------------------------------------------------
| ``drop_lower:(int,ratvec->ratvec)``
| 


.. _drop_upper_(int,ratvec->ratvec)1:

drop_upper
-------------------------------------------------
| ``drop_upper:(int,ratvec->ratvec)``
| 


.. _sum_(ratvec->rat)1:

sum
-------------------------------------------------
| ``sum:(ratvec->rat)``
| 


.. _<=_(ratvec->bool)1:

<=
-------------------------------------------------
| ``<=:(ratvec->bool)``
| 


.. _<_(ratvec->bool)1:

<
-------------------------------------------------
| ``<:(ratvec->bool)``
| 


.. _solve_(mat,ratvec->[ratvec])1:

solve
-------------------------------------------------
| ``solve:(mat,ratvec->[ratvec])``
| 


.. _int_part_(Split->int)1:

int_part
-------------------------------------------------
| ``int_part:(Split->int)``
| 


.. _s_part_(Split->int)1:

s_part
-------------------------------------------------
| ``s_part:(Split->int)``
| 


.. _\+_(Split->int)1:

\+
-------------------------------------------------
| ``+:(Split->int)``
| 


.. _\^_(Split->int)1:

\^
-------------------------------------------------
| ``^:(Split->int)``
| 


.. _s_to_1_(Split->int)1:

s_to_1
-------------------------------------------------
| ``s_to_1:(Split->int)``
| 


.. _s_to_minus_1_(Split->int)1:

s_to_minus_1
-------------------------------------------------
| ``s_to_minus_1:(Split->int)``
| 


.. _split_as_int_(Split->int)1:

split_as_int
-------------------------------------------------
| ``split_as_int:(Split->int)``
| 


.. _\%_(Split,int->Split,Split)1:

\%
-------------------------------------------------
| ``\%:(Split,int->Split,Split)``
| 


.. _split_format_(Split->string)1:

split_format
-------------------------------------------------
| ``split_format:(Split->string)``
| 


.. _\^_(Split,int->Split)1:

\^
-------------------------------------------------
| ``^:(Split,int->Split)``
| 


.. _root_datum_([vec],[vec],int->RootDatum)1:

root_datum
-------------------------------------------------
| ``root_datum:([vec],[vec],int->RootDatum)``
| 


.. _root_datum_(LieType,[ratvec]->RootDatum)1:

root_datum
-------------------------------------------------
| ``root_datum:(LieType,[ratvec]->RootDatum)``
| 


.. _root_datum_(LieType,ratvec->RootDatum)1:

root_datum
-------------------------------------------------
| ``root_datum:(LieType,ratvec->RootDatum)``
| 


.. _is_root_(RootDatum,vec->bool)1:

is_root
-------------------------------------------------
| ``is_root:(RootDatum,vec->bool)``
| 


.. _is_coroot_(RootDatum,vec->bool)1:

is_coroot
-------------------------------------------------
| ``is_coroot:(RootDatum,vec->bool)``
| 


.. _is_posroot_(RootDatum,vec->bool)1:

is_posroot
-------------------------------------------------
| ``is_posroot:(RootDatum,vec->bool)``
| 


.. _is_poscoroot_(RootDatum,vec->bool)1:

is_poscoroot
-------------------------------------------------
| ``is_poscoroot:(RootDatum,vec->bool)``
| 


.. _posroot_index_(RootDatum,vec->int)1:

posroot_index
-------------------------------------------------
| ``posroot_index:(RootDatum,vec->int)``
| 


.. _poscoroot_index_(RootDatum,vec->int)1:

poscoroot_index
-------------------------------------------------
| ``poscoroot_index:(RootDatum,vec->int)``
| 


.. _rho_(RootDatum->ratvec)1:

rho
-------------------------------------------------
| ``rho:(RootDatum->ratvec)``
| 


.. _rho_as_vec_(RootDatum->vec)1:

rho_as_vec
-------------------------------------------------
| ``rho_as_vec:(RootDatum->vec)``
| 


.. _rho_check_(RootDatum->ratvec)1:

rho_check
-------------------------------------------------
| ``rho_check:(RootDatum->ratvec)``
| 


.. _is_positive_root_(RootDatum->(vec->bool))1:

is_positive_root
-------------------------------------------------
| ``is_positive_root:(RootDatum->(vec->bool))``
| 


.. _is_positive_coroot_(RootDatum->(vec->bool))1:

is_positive_coroot
-------------------------------------------------
| ``is_positive_coroot:(RootDatum->(vec->bool))``
| 


.. _is_negative_root_(RootDatum->(vec->bool))1:

is_negative_root
-------------------------------------------------
| ``is_negative_root:(RootDatum->(vec->bool))``
| 


.. _is_negative_coroot_(RootDatum->(vec->bool))1:

is_negative_coroot
-------------------------------------------------
| ``is_negative_coroot:(RootDatum->(vec->bool))``
| 


.. _is_positive_root_(RootDatum,vec->bool)1:

is_positive_root
-------------------------------------------------
| ``is_positive_root:(RootDatum,vec->bool)``
| 


.. _is_positive_coroot_(RootDatum,vec->bool)1:

is_positive_coroot
-------------------------------------------------
| ``is_positive_coroot:(RootDatum,vec->bool)``
| 


.. _is_negative_root_(RootDatum,vec->bool)1:

is_negative_root
-------------------------------------------------
| ``is_negative_root:(RootDatum,vec->bool)``
| 


.. _is_negative_coroot_(RootDatum,vec->bool)1:

is_negative_coroot
-------------------------------------------------
| ``is_negative_coroot:(RootDatum,vec->bool)``
| 


.. _roots_all_positive_(RootDatum->(mat->bool))1:

roots_all_positive
-------------------------------------------------
| ``roots_all_positive:(RootDatum->(mat->bool))``
| 


.. _coroots_all_positive_(RootDatum->(mat->bool))1:

coroots_all_positive
-------------------------------------------------
| ``coroots_all_positive:(RootDatum->(mat->bool))``
| 


.. _among_posroots_(RootDatum->(mat->bool))1:

among_posroots
-------------------------------------------------
| ``among_posroots:(RootDatum->(mat->bool))``
| 


.. _among_poscoroots_(RootDatum->(mat->bool))1:

among_poscoroots
-------------------------------------------------
| ``among_poscoroots:(RootDatum->(mat->bool))``
| 


.. _negative_system_(mat->mat)1:

negative_system
-------------------------------------------------
| ``negative_system:(mat->mat)``
| 


.. _roots_(RootDatum->mat)1:

roots
-------------------------------------------------
| ``roots:(RootDatum->mat)``
| 


.. _coroots_(RootDatum->mat)1:

coroots
-------------------------------------------------
| ``coroots:(RootDatum->mat)``
| 


.. _root_(RootDatum,vec->vec)1:

root
-------------------------------------------------
| ``root:(RootDatum,vec->vec)``
| 


.. _coroot_(RootDatum,vec->vec)1:

coroot
-------------------------------------------------
| ``coroot:(RootDatum,vec->vec)``
| 


.. _reflection_(RootDatum,int->mat)1:

reflection
-------------------------------------------------
| ``reflection:(RootDatum,int->mat)``
| 


.. _reflection_(RootDatum,vec->mat)1:

reflection
-------------------------------------------------
| ``reflection:(RootDatum,vec->mat)``
| 


.. _coreflection_(RootDatum,int->mat)1:

coreflection
-------------------------------------------------
| ``coreflection:(RootDatum,int->mat)``
| 


.. _coreflection_(RootDatum,vec->mat)1:

coreflection
-------------------------------------------------
| ``coreflection:(RootDatum,vec->mat)``
| 


.. _reflect_(RootDatum,int,vec->vec)1:

reflect
-------------------------------------------------
| ``reflect:(RootDatum,int,vec->vec)``
| 


.. _reflect_(RootDatum,vec,vec->vec)1:

reflect
-------------------------------------------------
| ``reflect:(RootDatum,vec,vec->vec)``
| 


.. _coreflect_(RootDatum,vec,int->vec)1:

coreflect
-------------------------------------------------
| ``coreflect:(RootDatum,vec,int->vec)``
| 


.. _coreflect_(RootDatum,vec,vec->vec)1:

coreflect
-------------------------------------------------
| ``coreflect:(RootDatum,vec,vec->vec)``
| 


.. _reflect_(RootDatum,int,ratvec->ratvec)1:

reflect
-------------------------------------------------
| ``reflect:(RootDatum,int,ratvec->ratvec)``
| 


.. _reflect_(RootDatum,vec,ratvec->ratvec)1:

reflect
-------------------------------------------------
| ``reflect:(RootDatum,vec,ratvec->ratvec)``
| 


.. _coreflect_(RootDatum,ratvec,int->ratvec)1:

coreflect
-------------------------------------------------
| ``coreflect:(RootDatum,ratvec,int->ratvec)``
| 


.. _coreflect_(RootDatum,ratvec,vec->ratvec)1:

coreflect
-------------------------------------------------
| ``coreflect:(RootDatum,ratvec,vec->ratvec)``
| 


.. _left_reflect_(RootDatum,int,mat->mat)1:

left_reflect
-------------------------------------------------
| ``left_reflect:(RootDatum,int,mat->mat)``
| 


.. _left_reflect_(RootDatum,vec,mat->mat)1:

left_reflect
-------------------------------------------------
| ``left_reflect:(RootDatum,vec,mat->mat)``
| 


.. _right_reflect_(RootDatum,mat,int->mat)1:

right_reflect
-------------------------------------------------
| ``right_reflect:(RootDatum,mat,int->mat)``
| 


.. _right_reflect_(RootDatum,mat,vec->mat)1:

right_reflect
-------------------------------------------------
| ``right_reflect:(RootDatum,mat,vec->mat)``
| 


.. _conjugate_(RootDatum,int,mat->mat)1:

conjugate
-------------------------------------------------
| ``conjugate:(RootDatum,int,mat->mat)``
| 


.. _conjugate_(RootDatum,vec,mat->mat)1:

conjugate
-------------------------------------------------
| ``conjugate:(RootDatum,vec,mat->mat)``
| 


.. _singular_simple_indices_(RootDatum,ratvec->[int])1:

singular_simple_indices
-------------------------------------------------
| ``singular_simple_indices:(RootDatum,ratvec->[int])``
| 


.. _is_imaginary_(mat->(vec->bool))1:

is_imaginary
-------------------------------------------------
| ``is_imaginary:(mat->(vec->bool))``
| 


.. _is_real_(mat->(vec->bool))1:

is_real
-------------------------------------------------
| ``is_real:(mat->(vec->bool))``
| 


.. _is_complex_(mat->(vec->bool))1:

is_complex
-------------------------------------------------
| ``is_complex:(mat->(vec->bool))``
| 


.. _imaginary_roots_(RootDatum,mat->mat)1:

imaginary_roots
-------------------------------------------------
| ``imaginary_roots:(RootDatum,mat->mat)``
| 


.. _real_roots_(RootDatum,mat->mat)1:

real_roots
-------------------------------------------------
| ``real_roots:(RootDatum,mat->mat)``
| 


.. _imaginary_coroots_(RootDatum,mat->mat)1:

imaginary_coroots
-------------------------------------------------
| ``imaginary_coroots:(RootDatum,mat->mat)``
| 


.. _real_coroots_(RootDatum,mat->mat)1:

real_coroots
-------------------------------------------------
| ``real_coroots:(RootDatum,mat->mat)``
| 


.. _imaginary_posroots_(RootDatum,mat->mat)1:

imaginary_posroots
-------------------------------------------------
| ``imaginary_posroots:(RootDatum,mat->mat)``
| 


.. _real_posroots_(RootDatum,mat->mat)1:

real_posroots
-------------------------------------------------
| ``real_posroots:(RootDatum,mat->mat)``
| 


.. _imaginary_poscoroots_(RootDatum,mat->mat)1:

imaginary_poscoroots
-------------------------------------------------
| ``imaginary_poscoroots:(RootDatum,mat->mat)``
| 


.. _real_poscoroots_(RootDatum,mat->mat)1:

real_poscoroots
-------------------------------------------------
| ``real_poscoroots:(RootDatum,mat->mat)``
| 


.. _imaginary_sys_(RootDatum,mat->mat,mat)1:

imaginary_sys
-------------------------------------------------
| ``imaginary_sys:(RootDatum,mat->mat,mat)``
| 


.. _real_sys_(RootDatum,mat->mat,mat)1:

real_sys
-------------------------------------------------
| ``real_sys:(RootDatum,mat->mat,mat)``
| 


.. _is_dominant_(RootDatum,ratvec->bool)1:

is_dominant
-------------------------------------------------
| ``is_dominant:(RootDatum,ratvec->bool)``
| 


.. _is_strictly_dominant_(RootDatum,ratvec->bool)1:

is_strictly_dominant
-------------------------------------------------
| ``is_strictly_dominant:(RootDatum,ratvec->bool)``
| 


.. _is_regular_(RootDatum,ratvec->bool)1:

is_regular
-------------------------------------------------
| ``is_regular:(RootDatum,ratvec->bool)``
| 


.. _is_integral_(RootDatum,ratvec->bool)1:

is_integral
-------------------------------------------------
| ``is_integral:(RootDatum,ratvec->bool)``
| 


.. _radical_basis_(RootDatum->mat)1:

radical_basis
-------------------------------------------------
| ``radical_basis:(RootDatum->mat)``
| 


.. _coradical_basis_(RootDatum->mat)1:

coradical_basis
-------------------------------------------------
| ``coradical_basis:(RootDatum->mat)``
| 


.. _is_semisimple_(RootDatum->bool)1:

is_semisimple
-------------------------------------------------
| ``is_semisimple:(RootDatum->bool)``
| 


.. _derived_is_simply_connected_(RootDatum->bool)1:

derived_is_simply_connected
-------------------------------------------------
| ``derived_is_simply_connected:(RootDatum->bool)``
| 


.. _has_connected_center_(RootDatum->bool)1:

has_connected_center
-------------------------------------------------
| ``has_connected_center:(RootDatum->bool)``
| 


.. _is_simply_connected_(RootDatum->bool)1:

is_simply_connected
-------------------------------------------------
| ``is_simply_connected:(RootDatum->bool)``
| 


.. _is_adjoint_(RootDatum->bool)1:

is_adjoint
-------------------------------------------------
| ``is_adjoint:(RootDatum->bool)``
| 


.. _derived_(RootDatum->RootDatum)1:

derived
-------------------------------------------------
| ``derived:(RootDatum->RootDatum)``
| 


.. _mod_central_torus_(RootDatum->RootDatum)1:

mod_central_torus
-------------------------------------------------
| ``mod_central_torus:(RootDatum->RootDatum)``
| 


.. _adjoint_(RootDatum->RootDatum)1:

adjoint
-------------------------------------------------
| ``adjoint:(RootDatum->RootDatum)``
| 


.. _is_simple_for_(vec->(vec->bool))1:

is_simple_for
-------------------------------------------------
| ``is_simple_for:(vec->(vec->bool))``
| 


.. _simple_from_positive_(mat,mat->mat,mat)1:

simple_from_positive
-------------------------------------------------
| ``simple_from_positive:(mat,mat->mat,mat)``
| 


.. _fundamental_weights_(RootDatum->[ratvec])1:

fundamental_weights
-------------------------------------------------
| ``fundamental_weights:(RootDatum->[ratvec])``
| 


.. _fundamental_coweights_(RootDatum->[ratvec])1:

fundamental_coweights
-------------------------------------------------
| ``fundamental_coweights:(RootDatum->[ratvec])``
| 


.. _!=_(InnerClass,InnerClass->bool)1:

!=
-------------------------------------------------
| ``!=:(InnerClass,InnerClass->bool)``
| 


.. _dual_integral_(InnerClass,ratvec->InnerClass)1:

dual_integral
-------------------------------------------------
| ``dual_integral:(InnerClass,ratvec->InnerClass)``
| 


.. _Cartan_classes_(InnerClass->[CartanClass])1:

Cartan_classes
-------------------------------------------------
| ``Cartan_classes:(InnerClass->[CartanClass])``
| 


.. _print_Cartan_info_(CartanClass->)1:

print_Cartan_info
-------------------------------------------------
| ``print_Cartan_info:(CartanClass->)``
| 


.. _fundamental_Cartan_(InnerClass->CartanClass)1:

fundamental_Cartan
-------------------------------------------------
| ``fundamental_Cartan:(InnerClass->CartanClass)``
| 


.. _most_split_Cartan_(InnerClass->CartanClass)1:

most_split_Cartan
-------------------------------------------------
| ``most_split_Cartan:(InnerClass->CartanClass)``
| 


.. _compact_rank_(CartanClass->int)1:

compact_rank
-------------------------------------------------
| ``compact_rank:(CartanClass->int)``
| 


.. _split_rank_(CartanClass->int)1:

split_rank
-------------------------------------------------
| ``split_rank:(CartanClass->int)``
| 


.. _compact_rank_(InnerClass->int)1:

compact_rank
-------------------------------------------------
| ``compact_rank:(InnerClass->int)``
| 


.. _split_rank_(RealForm->int)1:

split_rank
-------------------------------------------------
| ``split_rank:(RealForm->int)``
| 


.. _\=_(CartanClass,CartanClass->bool)1:

\=
-------------------------------------------------
| ``=:(CartanClass,CartanClass->bool)``
| 


.. _number_(CartanClass,RealForm->int)1:

number
-------------------------------------------------
| ``number:(CartanClass,RealForm->int)``
| 


.. _!=_(RealForm,RealForm->bool)1:

!=
-------------------------------------------------
| ``!=:(RealForm,RealForm->bool)``
| 


.. _form_name_(RealForm->string)1:

form_name
-------------------------------------------------
| ``form_name:(RealForm->string)``
| 


.. _real_forms_(InnerClass->[RealForm])1:

real_forms
-------------------------------------------------
| ``real_forms:(InnerClass->[RealForm])``
| 


.. _dual_real_forms_(InnerClass->[RealForm])1:

dual_real_forms
-------------------------------------------------
| ``dual_real_forms:(InnerClass->[RealForm])``
| 


.. _is_quasisplit_(RealForm->bool)1:

is_quasisplit
-------------------------------------------------
| ``is_quasisplit:(RealForm->bool)``
| 


.. _is_quasicompact_(RealForm->bool)1:

is_quasicompact
-------------------------------------------------
| ``is_quasicompact:(RealForm->bool)``
| 


.. _split_form_(RootDatum->RealForm)1:

split_form
-------------------------------------------------
| ``split_form:(RootDatum->RealForm)``
| 


.. _split_form_(LieType->RealForm)1:

split_form
-------------------------------------------------
| ``split_form:(LieType->RealForm)``
| 


.. _quasicompact_form_(InnerClass->RealForm)1:

quasicompact_form
-------------------------------------------------
| ``quasicompact_form:(InnerClass->RealForm)``
| 


.. _is_compatible_(RealForm,RealForm->bool)1:

is_compatible
-------------------------------------------------
| ``is_compatible:(RealForm,RealForm->bool)``
| 


.. _is_compact_(RealForm->bool)1:

is_compact
-------------------------------------------------
| ``is_compact:(RealForm->bool)``
| 


.. _!=_(KGBElt,KGBElt->bool)1:

!=
-------------------------------------------------
| ``!=:(KGBElt,KGBElt->bool)``
| 


.. _real_form_(KGBElt->RealForm)1:

real_form
-------------------------------------------------
| ``real_form:(KGBElt->RealForm)``
| 


.. _\#_(KGBElt->int)1:

\#
-------------------------------------------------
| ``#:(KGBElt->int)``
| 


.. _root_datum_(KGBElt->RootDatum)1:

root_datum
-------------------------------------------------
| ``root_datum:(KGBElt->RootDatum)``
| 


.. _inner_class_(KGBElt->InnerClass)1:

inner_class
-------------------------------------------------
| ``inner_class:(KGBElt->InnerClass)``
| 


.. _KGB_(RealForm->[KGBElt])1:

KGB
-------------------------------------------------
| ``KGB:(RealForm->[KGBElt])``
| 


.. _KGB_(CartanClass,RealForm->[KGBElt])1:

KGB
-------------------------------------------------
| ``KGB:(CartanClass,RealForm->[KGBElt])``
| 


.. _KGB_elt_(InnerClass,mat,ratvec->KGBElt)1:

KGB_elt
-------------------------------------------------
| ``KGB_elt:(InnerClass,mat,ratvec->KGBElt)``
| 


.. _KGB_elt_(RootDatum,mat,ratvec->KGBElt)1:

KGB_elt
-------------------------------------------------
| ``KGB_elt:(RootDatum,mat,ratvec->KGBElt)``
| 


.. _Cartan_class_(InnerClass,mat->CartanClass)1:

Cartan_class
-------------------------------------------------
| ``Cartan_class:(InnerClass,mat->CartanClass)``
| 


.. _status_(vec,KGBElt->int)1:

status
-------------------------------------------------
| ``status:(vec,KGBElt->int)``
| 


.. _cross_(vec,KGBElt->KGBElt)1:

cross
-------------------------------------------------
| ``cross:(vec,KGBElt->KGBElt)``
| 


.. _Cayley_(vec,KGBElt->KGBElt)1:

Cayley
-------------------------------------------------
| ``Cayley:(vec,KGBElt->KGBElt)``
| 


.. _W_cross_([int],KGBElt->KGBElt)1:

W_cross
-------------------------------------------------
| ``W_cross:([int],KGBElt->KGBElt)``
| 


.. _KGB_status_text_(int->string)1:

KGB_status_text
-------------------------------------------------
| ``KGB_status_text:(int->string)``
| 


.. _status_text_(int,KGBElt->string)1:

status_text
-------------------------------------------------
| ``status_text:(int,KGBElt->string)``
| 


.. _status_text_(vec,KGBElt->string)1:

status_text
-------------------------------------------------
| ``status_text:(vec,KGBElt->string)``
| 


.. _status_texts_(KGBElt->[string])1:

status_texts
-------------------------------------------------
| ``status_texts:(KGBElt->[string])``
| 


.. _is_complex_(int,KGBElt->bool)1:

is_complex
-------------------------------------------------
| ``is_complex:(int,KGBElt->bool)``
| 


.. _is_real_(int,KGBElt->bool)1:

is_real
-------------------------------------------------
| ``is_real:(int,KGBElt->bool)``
| 


.. _is_imaginary_(int,KGBElt->bool)1:

is_imaginary
-------------------------------------------------
| ``is_imaginary:(int,KGBElt->bool)``
| 


.. _is_noncompact_(int,KGBElt->bool)1:

is_noncompact
-------------------------------------------------
| ``is_noncompact:(int,KGBElt->bool)``
| 


.. _is_compact_(int,KGBElt->bool)1:

is_compact
-------------------------------------------------
| ``is_compact:(int,KGBElt->bool)``
| 


.. _is_descent_(int,KGBElt->bool)1:

is_descent
-------------------------------------------------
| ``is_descent:(int,KGBElt->bool)``
| 


.. _is_ascent_(int,KGBElt->bool)1:

is_ascent
-------------------------------------------------
| ``is_ascent:(int,KGBElt->bool)``
| 


.. _is_strict_descent_(int,KGBElt->bool)1:

is_strict_descent
-------------------------------------------------
| ``is_strict_descent:(int,KGBElt->bool)``
| 


.. _is_imaginary_(KGBElt->(vec->bool))1:

is_imaginary
-------------------------------------------------
| ``is_imaginary:(KGBElt->(vec->bool))``
| 


.. _is_real_(KGBElt->(vec->bool))1:

is_real
-------------------------------------------------
| ``is_real:(KGBElt->(vec->bool))``
| 


.. _is_complex_(KGBElt->(vec->bool))1:

is_complex
-------------------------------------------------
| ``is_complex:(KGBElt->(vec->bool))``
| 


.. _imaginary_posroots_(KGBElt->mat)1:

imaginary_posroots
-------------------------------------------------
| ``imaginary_posroots:(KGBElt->mat)``
| 


.. _real_posroots_(KGBElt->mat)1:

real_posroots
-------------------------------------------------
| ``real_posroots:(KGBElt->mat)``
| 


.. _imaginary_poscoroots_(KGBElt->mat)1:

imaginary_poscoroots
-------------------------------------------------
| ``imaginary_poscoroots:(KGBElt->mat)``
| 


.. _real_poscoroots_(KGBElt->mat)1:

real_poscoroots
-------------------------------------------------
| ``real_poscoroots:(KGBElt->mat)``
| 


.. _imaginary_sys_(KGBElt->mat,mat)1:

imaginary_sys
-------------------------------------------------
| ``imaginary_sys:(KGBElt->mat,mat)``
| 


.. _real_sys_(KGBElt->mat,mat)1:

real_sys
-------------------------------------------------
| ``real_sys:(KGBElt->mat,mat)``
| 


.. _rho_i_(KGBElt->ratvec)1:

rho_i
-------------------------------------------------
| ``rho_i:(KGBElt->ratvec)``
| 


.. _rho_r_(KGBElt->ratvec)1:

rho_r
-------------------------------------------------
| ``rho_r:(KGBElt->ratvec)``
| 


.. _rho_check_i_(KGBElt->ratvec)1:

rho_check_i
-------------------------------------------------
| ``rho_check_i:(KGBElt->ratvec)``
| 


.. _rho_check_r_(KGBElt->ratvec)1:

rho_check_r
-------------------------------------------------
| ``rho_check_r:(KGBElt->ratvec)``
| 


.. _rho_i_(RootDatum,mat->ratvec)1:

rho_i
-------------------------------------------------
| ``rho_i:(RootDatum,mat->ratvec)``
| 


.. _rho_r_(RootDatum,mat->ratvec)1:

rho_r
-------------------------------------------------
| ``rho_r:(RootDatum,mat->ratvec)``
| 


.. _rho_check_i_(RootDatum,mat->ratvec)1:

rho_check_i
-------------------------------------------------
| ``rho_check_i:(RootDatum,mat->ratvec)``
| 


.. _rho_check_r_(RootDatum,mat->ratvec)1:

rho_check_r
-------------------------------------------------
| ``rho_check_r:(RootDatum,mat->ratvec)``
| 


.. _is_compact_(KGBElt->(vec->bool))1:

is_compact
-------------------------------------------------
| ``is_compact:(KGBElt->(vec->bool))``
| 


.. _is_noncompact_(KGBElt->(vec->bool))1:

is_noncompact
-------------------------------------------------
| ``is_noncompact:(KGBElt->(vec->bool))``
| 


.. _is_compact_imaginary_(KGBElt->(vec->bool))1:

is_compact_imaginary
-------------------------------------------------
| ``is_compact_imaginary:(KGBElt->(vec->bool))``
| 


.. _is_noncompact_imaginary_(KGBElt->(vec->bool))1:

is_noncompact_imaginary
-------------------------------------------------
| ``is_noncompact_imaginary:(KGBElt->(vec->bool))``
| 


.. _compact_posroots_(KGBElt->mat)1:

compact_posroots
-------------------------------------------------
| ``compact_posroots:(KGBElt->mat)``
| 


.. _noncompact_posroots_(KGBElt->mat)1:

noncompact_posroots
-------------------------------------------------
| ``noncompact_posroots:(KGBElt->mat)``
| 


.. _rho_ci_(KGBElt->ratvec)1:

rho_ci
-------------------------------------------------
| ``rho_ci:(KGBElt->ratvec)``
| 


.. _rho_nci_(KGBElt->ratvec)1:

rho_nci
-------------------------------------------------
| ``rho_nci:(KGBElt->ratvec)``
| 


.. _is_imaginary_(vec,KGBElt->bool)1:

is_imaginary
-------------------------------------------------
| ``is_imaginary:(vec,KGBElt->bool)``
| 


.. _is_real_(vec,KGBElt->bool)1:

is_real
-------------------------------------------------
| ``is_real:(vec,KGBElt->bool)``
| 


.. _is_complex_(vec,KGBElt->bool)1:

is_complex
-------------------------------------------------
| ``is_complex:(vec,KGBElt->bool)``
| 


.. _is_compact_imaginary_(vec,KGBElt->bool)1:

is_compact_imaginary
-------------------------------------------------
| ``is_compact_imaginary:(vec,KGBElt->bool)``
| 


.. _is_noncompact_imaginary_(vec,KGBElt->bool)1:

is_noncompact_imaginary
-------------------------------------------------
| ``is_noncompact_imaginary:(vec,KGBElt->bool)``
| 


.. _print_KGB_(KGBElt->)1:

print_KGB
-------------------------------------------------
| ``print_KGB:(KGBElt->)``
| 


.. _no_Cminus_roots_(KGBElt->bool)1:

no_Cminus_roots
-------------------------------------------------
| ``no_Cminus_roots:(KGBElt->bool)``
| 


.. _no_Cplus_roots_(KGBElt->bool)1:

no_Cplus_roots
-------------------------------------------------
| ``no_Cplus_roots:(KGBElt->bool)``
| 


.. _blocks_(InnerClass->[Block])1:

blocks
-------------------------------------------------
| ``blocks:(InnerClass->[Block])``
| 


.. _raw_KL_(RealForm,RealForm->mat,[vec],vec)1:

raw_KL
-------------------------------------------------
| ``raw_KL:(RealForm,RealForm->mat,[vec],vec)``
| 


.. _dual_KL_(RealForm,RealForm->mat,[vec],vec)1:

dual_KL
-------------------------------------------------
| ``dual_KL:(RealForm,RealForm->mat,[vec],vec)``
| 


.. _print_block_(RealForm,RealForm->)1:

print_block
-------------------------------------------------
| ``print_block:(RealForm,RealForm->)``
| 


.. _print_blocku_(RealForm,RealForm->)1:

print_blocku
-------------------------------------------------
| ``print_blocku:(RealForm,RealForm->)``
| 


.. _print_blockd_(RealForm,RealForm->)1:

print_blockd
-------------------------------------------------
| ``print_blockd:(RealForm,RealForm->)``
| 


.. _print_KL_basis_(RealForm,RealForm->)1:

print_KL_basis
-------------------------------------------------
| ``print_KL_basis:(RealForm,RealForm->)``
| 


.. _print_prim_KL_(RealForm,RealForm->)1:

print_prim_KL
-------------------------------------------------
| ``print_prim_KL:(RealForm,RealForm->)``
| 


.. _print_KL_list_(RealForm,RealForm->)1:

print_KL_list
-------------------------------------------------
| ``print_KL_list:(RealForm,RealForm->)``
| 


.. _print_W_cells_(RealForm,RealForm->)1:

print_W_cells
-------------------------------------------------
| ``print_W_cells:(RealForm,RealForm->)``
| 


.. _print_W_graph_(RealForm,RealForm->)1:

print_W_graph
-------------------------------------------------
| ``print_W_graph:(RealForm,RealForm->)``
| 


.. _!=_(Param,Param->bool)1:

!=
-------------------------------------------------
| ``!=:(Param,Param->bool)``
| 


.. _root_datum_(Param->RootDatum)1:

root_datum
-------------------------------------------------
| ``root_datum:(Param->RootDatum)``
| 


.. _inner_class_(Param->InnerClass)1:

inner_class
-------------------------------------------------
| ``inner_class:(Param->InnerClass)``
| 


.. _null_module_(Param->ParamPol)1:

null_module
-------------------------------------------------
| ``null_module:(Param->ParamPol)``
| 


.. _\*_(Param,rat->Param)1:

\*
-------------------------------------------------
| ``*:(Param,rat->Param)``
| 


.. _x_(Param->KGBElt)1:

x
-------------------------------------------------
| ``x:(Param->KGBElt)``
| 


.. _lambda_minus_rho_(Param->vec)1:

lambda_minus_rho
-------------------------------------------------
| ``lambda_minus_rho:(Param->vec)``
| 


.. _lambda_(Param->ratvec)1:

lambda
-------------------------------------------------
| ``lambda:(Param->ratvec)``
| 


.. _infinitesimal_character_(Param->ratvec)1:

infinitesimal_character
-------------------------------------------------
| ``infinitesimal_character:(Param->ratvec)``
| 


.. _nu_(Param->ratvec)1:

nu
-------------------------------------------------
| ``nu:(Param->ratvec)``
| 


.. _Cartan_class_(Param->CartanClass)1:

Cartan_class
-------------------------------------------------
| ``Cartan_class:(Param->CartanClass)``
| 


.. _involution_(Param->mat)1:

involution
-------------------------------------------------
| ``involution:(Param->mat)``
| 


.. _integrality_datum_(Param->RootDatum)1:

integrality_datum
-------------------------------------------------
| ``integrality_datum:(Param->RootDatum)``
| 


.. _is_regular_(Param->bool)1:

is_regular
-------------------------------------------------
| ``is_regular:(Param->bool)``
| 


.. _trivial_(RealForm->Param)1:

trivial
-------------------------------------------------
| ``trivial:(RealForm->Param)``
| 


.. _W_cross_([int],Param->Param)1:

W_cross
-------------------------------------------------
| ``W_cross:([int],Param->Param)``
| 


.. _parameter_(RealForm,int,ratvec,ratvec->Param)1:

parameter
-------------------------------------------------
| ``parameter:(RealForm,int,ratvec,ratvec->Param)``
| 


.. _parameter_(KGBElt,ratvec,ratvec->Param)1:

parameter
-------------------------------------------------
| ``parameter:(KGBElt,ratvec,ratvec->Param)``
| 


.. _parameter_gamma_(KGBElt,ratvec,ratvec->Param)1:

parameter_gamma
-------------------------------------------------
| ``parameter_gamma:(KGBElt,ratvec,ratvec->Param)``
| 


.. _block_of_(Param->[Param])1:

block_of
-------------------------------------------------
| ``block_of:(Param->[Param])``
| 


.. _imaginary_type_(int,Param->int)1:

imaginary_type
-------------------------------------------------
| ``imaginary_type:(int,Param->int)``
| 


.. _real_type_(int,Param->int)1:

real_type
-------------------------------------------------
| ``real_type:(int,Param->int)``
| 


.. _imaginary_type_(vec,Param->int)1:

imaginary_type
-------------------------------------------------
| ``imaginary_type:(vec,Param->int)``
| 


.. _real_type_(vec,Param->int)1:

real_type
-------------------------------------------------
| ``real_type:(vec,Param->int)``
| 


.. _is_nonparity_(int,Param->bool)1:

is_nonparity
-------------------------------------------------
| ``is_nonparity:(int,Param->bool)``
| 


.. _is_parity_(int,Param->bool)1:

is_parity
-------------------------------------------------
| ``is_parity:(int,Param->bool)``
| 


.. _is_nonparity_(vec,Param->bool)1:

is_nonparity
-------------------------------------------------
| ``is_nonparity:(vec,Param->bool)``
| 


.. _is_parity_(vec,Param->bool)1:

is_parity
-------------------------------------------------
| ``is_parity:(vec,Param->bool)``
| 


.. _status_(vec,Param->int)1:

status
-------------------------------------------------
| ``status:(vec,Param->int)``
| 


.. _status_(int,Param->int)1:

status
-------------------------------------------------
| ``status:(int,Param->int)``
| 


.. _block_status_text_(int->string)1:

block_status_text
-------------------------------------------------
| ``block_status_text:(int->string)``
| 


.. _status_text_(int,Param->string)1:

status_text
-------------------------------------------------
| ``status_text:(int,Param->string)``
| 


.. _status_texts_(Param->[string])1:

status_texts
-------------------------------------------------
| ``status_texts:(Param->[string])``
| 


.. _status_text_(vec,Param->string)1:

status_text
-------------------------------------------------
| ``status_text:(vec,Param->string)``
| 


.. _parity_poscoroots_(Param->mat)1:

parity_poscoroots
-------------------------------------------------
| ``parity_poscoroots:(Param->mat)``
| 


.. _nonparity_poscoroots_(Param->mat)1:

nonparity_poscoroots
-------------------------------------------------
| ``nonparity_poscoroots:(Param->mat)``
| 


.. _is_descent_(int,Param->bool)1:

is_descent
-------------------------------------------------
| ``is_descent:(int,Param->bool)``
| 


.. _tau_bitset_(Param->(int->bool),int)1:

tau_bitset
-------------------------------------------------
| ``tau_bitset:(Param->(int->bool),int)``
| 


.. _tau_(Param->[int])1:

tau
-------------------------------------------------
| ``tau:(Param->[int])``
| 


.. _tau_complement_(Param->[int])1:

tau_complement
-------------------------------------------------
| ``tau_complement:(Param->[int])``
| 


.. _is_descent_(vec,Param->bool)1:

is_descent
-------------------------------------------------
| ``is_descent:(vec,Param->bool)``
| 


.. _lookup_(Param,[Param]->int)1:

lookup
-------------------------------------------------
| ``lookup:(Param,[Param]->int)``
| 


.. _has_double_extended_Cayley_(int->bool)1:

has_double_extended_Cayley
-------------------------------------------------
| ``has_double_extended_Cayley:(int->bool)``
| 


.. _print_extended_block_(Param,mat->)1:

print_extended_block
-------------------------------------------------
| ``print_extended_block:(Param,mat->)``
| 


.. _null_module_(ParamPol->ParamPol)1:

null_module
-------------------------------------------------
| ``null_module:(ParamPol->ParamPol)``
| 


.. _\-_(ParamPol->ParamPol)1:

\-
-------------------------------------------------
| ``-:(ParamPol->ParamPol)``
| 


.. _first_param_(ParamPol->Param)1:

first_param
-------------------------------------------------
| ``first_param:(ParamPol->Param)``
| 


.. _last_param_(ParamPol->Param)1:

last_param
-------------------------------------------------
| ``last_param:(ParamPol->Param)``
| 


.. _s_to_1_(ParamPol->ParamPol)1:

s_to_1
-------------------------------------------------
| ``s_to_1:(ParamPol->ParamPol)``
| 


.. _s_to_minus_1_(ParamPol->ParamPol)1:

s_to_minus_1
-------------------------------------------------
| ``s_to_minus_1:(ParamPol->ParamPol)``
| 


.. _\-_(ParamPol,(Split,Param)->ParamPol)1:

\-
-------------------------------------------------
| ``-:(ParamPol,(Split,Param)->ParamPol)``
| 


.. _\*_(ParamPol,rat->ParamPol)1:

\*
-------------------------------------------------
| ``*:(ParamPol,rat->ParamPol)``
| 


.. _divide_by_(int,ParamPol->ParamPol)1:

divide_by
-------------------------------------------------
| ``divide_by:(int,ParamPol->ParamPol)``
| 


.. _root_datum_(ParamPol->RootDatum)1:

root_datum
-------------------------------------------------
| ``root_datum:(ParamPol->RootDatum)``
| 


.. _virtual_(Param->ParamPol)1:

virtual
-------------------------------------------------
| ``virtual:(Param->ParamPol)``
| 


.. _virtual_(RealForm,[Param]->ParamPol)1:

virtual
-------------------------------------------------
| ``virtual:(RealForm,[Param]->ParamPol)``
| 


.. _pol_format_(ParamPol->)1:

pol_format
-------------------------------------------------
| ``pol_format:(ParamPol->)``
| 


.. _infinitesimal_character_(ParamPol->ratvec)1:

infinitesimal_character
-------------------------------------------------
| ``infinitesimal_character:(ParamPol->ratvec)``
| 


.. _separate_by_infinitesimal_character_(ParamPol->[(ratvec,ParamPol)])1:

separate_by_infinitesimal_character
-------------------------------------------------
| ``separate_by_infinitesimal_character:(ParamPol->[(ratvec,ParamPol)])``
| 


.. _in_string_list_(string,[string]->bool)1:

in_string_list
-------------------------------------------------
| ``in_string_list:(string,[string]->bool)``
| 


.. _positive_imaginary_roots_and_coroots_(RootDatum,mat->mat,mat)1:

positive_imaginary_roots_and_coroots
-------------------------------------------------
| ``positive_imaginary_roots_and_coroots:(RootDatum,mat->mat,mat)``
| 


.. _positive_imaginary_roots_and_coroots_(KGBElt->mat,mat)1:

positive_imaginary_roots_and_coroots
-------------------------------------------------
| ``positive_imaginary_roots_and_coroots:(KGBElt->mat,mat)``
| 


.. _imaginary_roots_and_coroots_(RootDatum,mat->mat,mat)1:

imaginary_roots_and_coroots
-------------------------------------------------
| ``imaginary_roots_and_coroots:(RootDatum,mat->mat,mat)``
| 


.. _imaginary_roots_and_coroots_(KGBElt->mat,mat)1:

imaginary_roots_and_coroots
-------------------------------------------------
| ``imaginary_roots_and_coroots:(KGBElt->mat,mat)``
| 


.. _positive_real_roots_and_coroots_(RootDatum,mat->mat,mat)1:

positive_real_roots_and_coroots
-------------------------------------------------
| ``positive_real_roots_and_coroots:(RootDatum,mat->mat,mat)``
| 


.. _positive_real_roots_and_coroots_(KGBElt->mat,mat)1:

positive_real_roots_and_coroots
-------------------------------------------------
| ``positive_real_roots_and_coroots:(KGBElt->mat,mat)``
| 


.. _real_roots_and_coroots_(RootDatum,mat->mat,mat)1:

real_roots_and_coroots
-------------------------------------------------
| ``real_roots_and_coroots:(RootDatum,mat->mat,mat)``
| 


.. _real_roots_and_coroots_(KGBElt->mat,mat)1:

real_roots_and_coroots
-------------------------------------------------
| ``real_roots_and_coroots:(KGBElt->mat,mat)``
| 


.. _complex_posroots_(RootDatum,mat->mat)1:

complex_posroots
-------------------------------------------------
| ``complex_posroots:(RootDatum,mat->mat)``
| 


.. _complex_posroots_(KGBElt->mat)1:

complex_posroots
-------------------------------------------------
| ``complex_posroots:(KGBElt->mat)``
| 


.. _monomials_(ParamPol->[Param])1:

monomials
-------------------------------------------------
| ``monomials:(ParamPol->[Param])``
| 


.. _monomial_(ParamPol,int->Param)1:

monomial
-------------------------------------------------
| ``monomial:(ParamPol,int->Param)``
| 


.. _delete_([int],int->[int])1:

delete
-------------------------------------------------
| ``delete:([int],int->[int])``
| 


.. _delete_([vec],int->[vec])1:

delete
-------------------------------------------------
| ``delete:([vec],int->[vec])``
| 


.. _delete_([ratvec],int->[ratvec])1:

delete
-------------------------------------------------
| ``delete:([ratvec],int->[ratvec])``
| 


.. _delete_([[ratvec]],int->[[ratvec]])1:

delete
-------------------------------------------------
| ``delete:([[ratvec]],int->[[ratvec]])``
| 


.. _delete_([[vec]],int->[[vec]])1:

delete
-------------------------------------------------
| ``delete:([[vec]],int->[[vec]])``
| 


.. _delete_([ParamPol],int->[ParamPol])1:

delete
-------------------------------------------------
| ``delete:([ParamPol],int->[ParamPol])``
| 


.. _find_([int],int->int)1:

find
-------------------------------------------------
| ``find:([int],int->int)``
| 


.. _find_([Param],Param->int)1:

find
-------------------------------------------------
| ``find:([Param],Param->int)``
| 


.. _find_([KGBElt],KGBElt->int)1:

find
-------------------------------------------------
| ``find:([KGBElt],KGBElt->int)``
| 


.. _find_([[int]],[int]->int)1:

find
-------------------------------------------------
| ``find:([[int]],[int]->int)``
| 


.. _find_vec_([vec],vec->int)1:

find_vec
-------------------------------------------------
| ``find_vec:([vec],vec->int)``
| 


.. _pad_(string,int->string)1:

pad
-------------------------------------------------
| ``pad:(string,int->string)``
| 


.. _extended_status_texts_[string]1:

extended_status_texts
-------------------------------------------------
| ``extended_status_texts:[string]``
| 


