basic.at References
====================================================

.. _\+_(string,int->string):

\+
---------------------------------------------

``+: (string,int->string)``
Function defined at basic.at:114:0-51
(s,i): +@(string,string)(s,int_format@int(i))


.. _\+_(int,string->string):

\+
---------------------------------------------

``+: (int,string->string)``
Function defined at basic.at:115:0-51
(i,s): +@(string,string)(int_format@int(i),s)


.. _\+_(string,(int,int)->string):

\+
---------------------------------------------

``+: (string,(int,int)->string)``
Function defined at basic.at:117:0-63
(s,(x,y)): +@(string,string)(+@(string,int)(+@(string,string)(+@(string,int)(+@(string,string)(s,"("),x),","),y),")")


.. _\+_(Split->int):

\+
---------------------------------------------

``+: (Split->int)``
Function defined at basic.at:406:4-46
(x):  let (r,)=%@Split(x) in r


.. _\-_(mat->mat):

\-
---------------------------------------------

``-: (mat->mat)``
Function defined at basic.at:222:0--223:36
(m): swiss_matrix_knife@(int,mat,int,int,int,int)(164,m,0,0,0,0)


.. _\-_(ParamPol->ParamPol):

\-
---------------------------------------------

``-: (ParamPol->ParamPol)``
Function defined at basic.at:1018:0-37
(P): *@(int,ParamPol)(-@int(1),P)


.. _\-_(ParamPol,(Split,Param)->ParamPol):

\-
---------------------------------------------

``-: (ParamPol,(Split,Param)->ParamPol)``
Function defined at basic.at:1027:0-61
(a,(c,p)): +@(ParamPol,(Split,Param))(a,(-@Split(c),p))


.. _\*_(string,int->string):

\*
---------------------------------------------

``*: (string,int->string)``
Function defined at basic.at:112:5-61
(s,n):  if <=@int(n) then "" else rep(s,n) fi


.. _\*_(int,vec->vec):

\*
---------------------------------------------

``*: (int,vec->vec)``
Function defined at basic.at:150:0-31
(c,v): *@(vec,int)(v,c)


.. _\*_(int,mat->mat):

\*
---------------------------------------------

``*: (int,mat->mat)``
Function defined at basic.at:221:0-55
(c,m): (map_on@mat(m))((e): *@(int,int)(c,e))


.. _\*_(int,ratvec->ratvec):

\*
---------------------------------------------

``*: (int,ratvec->ratvec)``
Function defined at basic.at:346:0-37
(i,v): *@(ratvec,int)(v,i)


.. _\*_(rat,ratvec->ratvec):

\*
---------------------------------------------

``*: (rat,ratvec->ratvec)``
Function defined at basic.at:347:0-37
(r,v): *@(ratvec,rat)(v,r)


.. _\*_([ratvec],ratvec->ratvec):

\*
---------------------------------------------

``*: ([ratvec],ratvec->ratvec)``
Function defined at basic.at:361:0--365:9
(M,v):  let m=#@[ratvec](M) in assert@(bool,string)( if !=@int(m) then =@(int,int)(m,#@ratvec(v)) else false fi ,"size mismatch"); let result=/@(vec,int)(null@int(#@ratvec(M[0])),1) in voided: for col@j in M do result:=+@(ratvec,ratvec)(result,*@(ratvec,rat)(col,v[j])) od ;result


.. _\*_(vec,ratvec->rat):

\*
---------------------------------------------

``*: (vec,ratvec->rat)``
Function defined at basic.at:372:0-76
(v,w):  let (nw,dw)=%@ratvec(w) in /@(int,int)(*@(vec,vec)(v,nw),dw)


.. _\*_(ratvec,ratvec->rat):

\*
---------------------------------------------

``*: (ratvec,ratvec->rat)``
Function defined at basic.at:370:0-77
(v,w):  let ((nv,dv),(nw,dw))=(%@ratvec(v),%@ratvec(w)) in /@(int,int)(*@(vec,vec)(nv,nw),*@(int,int)(dv,dw))


.. _\*_(Param,rat->Param):

\*
---------------------------------------------

``*: (Param,rat->Param)``
Function defined at basic.at:913:0--914:61
(p,f):  let (x,lambda_rho,gamma)=%@Param(p) in param@(KGBElt,vec,ratvec)(x,lambda_rho,*@(ratvec,rat)(gamma,f))


.. _\*_(ParamPol,rat->ParamPol):

\*
---------------------------------------------

``*: (ParamPol,rat->ParamPol)``
Function defined at basic.at:1030:0-71
(P,f): +@(ParamPol,[(Split,Param)])(*@(int,ParamPol)(0,P), for c@q in P do (c,*@(Param,rat)(q,f)) od )


.. _\\_(rat,int->int):

\\
---------------------------------------------

``\: (rat,int->int)``
Function defined at basic.at:86:0-36
(p): floor@rat(/@(rat,int)(p))


.. _\\_(rat,rat->int):

\\
---------------------------------------------

``\: (rat,rat->int)``
Function defined at basic.at:87:0-36
(p): floor@rat(/@(rat,rat)(p))


.. _\\_(mat,int->mat):

\\
---------------------------------------------

``\: (mat,int->mat)``
Function defined at basic.at:226:0-55
(m,d): (map_on@mat(m))((e): \@(int,int)(e,d))


.. _\\_(ratvec,int->vec):

\\
---------------------------------------------

``\: (ratvec,int->vec)``
Function defined at basic.at:376:0-55
(v,k):  let (n,d)=%@ratvec(v) in \@(vec,int)(n,*@(int,int)(k,d))


.. _%_(mat,int->mat):

\%
----------------------------------------------

``%: (mat,int->mat)``
Function defined at basic.at:229:0-55
(m,d): (map_on@mat(m))((e): %@(int,int)(e,d))


.. _\%_(rat,int->int,rat):

\\%
----------------------------------------------

``\%: (rat,int->int,rat)``
Function defined at basic.at:88:0-78
(p): (\@(rat,int)(p),%@(rat,int)(p))


.. _\%_(rat,rat->int,rat):

\\%
----------------------------------------------

``\%: (rat,rat->int,rat)``
Function defined at basic.at:89:0-41
(p): (\@(rat,rat)(p),%@(rat,rat)(p))


.. _^_(mat,vec->mat):

\^
----------------------------------------------

``^: (mat,vec->mat)``
Function defined at basic.at:203:0-58
(m,v): ^@(int,[vec])(n_columns@mat(m),#@([T],T)([V]M:^@mat(m),v))


.. _^_(vec,mat->mat):

\^
----------------------------------------------

``^: (vec,mat->mat)``
Function defined at basic.at:204:0-58
(v,m): ^@(int,[vec])(n_columns@mat(m),#@(T,[T])(v,[V]M:^@mat(m)))


.. _^_(mat,mat->mat):

\^
----------------------------------------------

``^: (mat,mat->mat)``
Function defined at basic.at:208:0--209:43
(A,B): ^@(int,[vec])(n_columns@mat(B),##@([T],[T])([V]M:^@mat(A),[V]M:^@mat(B)))


.. _^_(mat,int->mat):

\^
----------------------------------------------

``^: (mat,int->mat)``
Function defined at basic.at:241:4--249:8
(m,n): assert@(bool,string)(=@(int,int)(#@mat(m)),"Non square matrix in exponentiation"); if >@(int,int)(n,0) then matrix_power(m,n) elif =@int(n) then id_mat@int(n_rows@mat(m)) else  let (m1,d)=invert@mat(m) in  if =@(int,int)(d,1) then matrix_power(m1,-@int(n)) elif =@int(d) then error@string("Negative power of singular matrix") else error@string("Negative power of matrix not invertible over Z") fi  fi


.. _^_(Split->int):

\^
----------------------------------------------

``^: (Split->int)``
Function defined at basic.at:407:4-44
(x):  let (,y)=%@Split(x) in y


.. _^_(Split,int->Split):

\^
----------------------------------------------

``^: (Split,int->Split)``
Function defined at basic.at:435:17--440:6
(x,n):  if >@(int,int)(n,0) then split_power(x,n) elif =@int(n) then Sp(I,I):(1,0) elif  let (a,b)=%@Split(x) in =@(int,int)(+@(int,int)(abs@int(a),abs@int(b)),1) then  if is_even@int(n) then SpI:1 else x fi  else error@string(+@(string,string)(+@(string,string)(+@(string,int)("Negative power ",n)," of split integer "),split_format@Split(x))) fi


.. _=_((int,int),(int,int)->bool):

\=
----------------------------------------------

``=: ((int,int),(int,int)->bool)``
Function defined at basic.at:68:0-67
((x0,y0),(x1,y1)):  if =@(int,int)(x0,x1) then =@(int,int)(y0,y1) else false fi


.. _=_(mat,int->bool):

\=
----------------------------------------------

``=: (mat,int->bool)``
Function defined at basic.at:196:0-35
(m,k): =@mat(-@(mat,int)(m,k))


.. _=_(CartanClass,CartanClass->bool):

\=
----------------------------------------------

``=: (CartanClass,CartanClass->bool)``
Function defined at basic.at:709:0--711:56
(H,J):  let ((,theta_H,,),(,theta_J,,))=(Cartan_info@CartanClass(H),Cartan_info@CartanClass(J)) in =@(vec,vec)(theta_H,theta_J)


.. _!=_((int,int),(int,int)->bool):

\!=
----------------------------------------------

``!=: ((int,int),(int,int)->bool)``
Function defined at basic.at:69:0-68
((x0,y0),(x1,y1)):  if !=@(int,int)(x0,x1) then true else !=@(int,int)(y0,y1) fi


.. _!=_(Param,Param->bool):

\!=
----------------------------------------------

``!=: (Param,Param->bool)``
Function defined at basic.at:904:0-42
(x,y): not@bool(=@(Param,Param)(x,y))


.. _!=_(RealForm,RealForm->bool):

\!=
----------------------------------------------

``!=: (RealForm,RealForm->bool)``
Function defined at basic.at:719:0-49
(f,g): not@bool(=@(RealForm,RealForm)(f,g))


.. _!=_(InnerClass,InnerClass->bool):

\!=
----------------------------------------------

``!=: (InnerClass,InnerClass->bool)``
Function defined at basic.at:661:0-52
(x,y): not@bool(=@(InnerClass,InnerClass)(x,y))


.. _!=_(KGBElt,KGBElt->bool):

\!=
----------------------------------------------

``!=: (KGBElt,KGBElt->bool)``
Function defined at basic.at:752:0-44
(x,y): not@bool(=@(KGBElt,KGBElt)(x,y))


.. _>=_(mat->bool):

\>=
----------------------------------------------

``>=: (mat->bool)``
Function defined at basic.at:295:0--296:63
(m):  let j=-@(int,int)(n_columns@mat(m),1) in voided: while  if >=@int(j) then >=@vec(m[j]) else false fi  do j:=-@(int,int)(j,1) od ;<@int(j)


.. _>_(mat->bool):

\>
----------------------------------------------

``>: (mat->bool)``
Function defined at basic.at:297:0--298:62
(m):  let j=-@(int,int)(n_columns@mat(m),1) in voided: while  if >=@int(j) then >@vec(m[j]) else false fi  do j:=-@(int,int)(j,1) od ;<@int(j)


.. _<=_(vec->bool):

\<=
----------------------------------------------

``<=: (vec->bool)``
Function defined at basic.at:162:0-79
(v): >=@vec(-@vec(v))


.. _<=_(mat->bool):

\<=
----------------------------------------------

``<=: (mat->bool)``
Function defined at basic.at:299:0-28
(m): >=@mat(-@mat(m))


.. _<=_(ratvec->bool):

\<=
----------------------------------------------

``<=: (ratvec->bool)``
Function defined at basic.at:391:0-37
(v): <=@vec(numer@ratvec(v))


.. _<_(vec->bool):

\<
----------------------------------------------

``<: (vec->bool)``
Function defined at basic.at:163:0-55
(v): >@vec(-@vec(v))


.. _<_(mat->bool):

\<
----------------------------------------------

``<: (mat->bool)``
Function defined at basic.at:300:0-26
(m): >@mat(-@mat(m))


.. _<_(ratvec->bool):

\<
----------------------------------------------

``<: (ratvec->bool)``
Function defined at basic.at:392:0-37
(v): <@vec(numer@ratvec(v))


.. _##_(mat,mat->mat):

\##
----------------------------------------------

``##: (mat,mat->mat)``
Function defined at basic.at:206:0--207:38
(A,B): #@(int,[vec])(n_rows@mat(B),##@([T],[T])([V]M:A,[V]M:B))


.. _##_(int,[mat]->mat):

\##
----------------------------------------------

``##: (int,[mat]->mat)``
Function defined at basic.at:212:0--213:34
(n,L): #@(int,[vec])(n,##@([[T]])( for M in L do [V]M:M od ))


.. _##_(ratvec,ratvec->ratvec):

\##
----------------------------------------------

``##: (ratvec,ratvec->ratvec)``
Function defined at basic.at:350:0-57
(a,b): Qv[Q]:##@([T],[T])([Q]Qv:a,[Q]Qv:b)


.. _##_([ratvec]->ratvec):

\##
----------------------------------------------

``##: ([ratvec]->ratvec)``
Function defined at basic.at:351:0-60
(rs): Qv[Q]:##@([[T]])( for r in rs do [Q]Qv:r od )


.. _#_(ratvec->int):

\#
----------------------------------------------

``#: (ratvec->int)``
Function defined at basic.at:3:0-55
(v):  let (n,)=%@ratvec(v) in #@vec(n)


.. _#_(int->[int]):

\#
----------------------------------------------

``#: (int->[int])``
Function defined at basic.at:1:0-62
(n):  for i: n do i od


.. _#_(bool->int):

\#
----------------------------------------------

``#: (bool->int)``
Function defined at basic.at:2:0-63
(b):  if b then 1 else 0 fi


.. _#_(mat,vec->mat):

\#
----------------------------------------------

``#: (mat,vec->mat)``
Function defined at basic.at:199:0-77
(m,v): #@(int,[vec])(n_rows@mat(m),#@([T],T)([V]M:m,v))


.. _#_(vec,mat->mat):

\#
----------------------------------------------

``#: (vec,mat->mat)``
Function defined at basic.at:200:0-77
(v,m): #@(int,[vec])(n_rows@mat(m),#@(T,[T])(v,[V]M:m))


.. _#_(KGBElt->int):

\#
----------------------------------------------

``#: (KGBElt->int)``
Function defined at basic.at:754:0-38
(x):  let (,n)=%@KGBElt(x) in n


.. _involution_(Param->mat):

\involution
----------------------------------------------

``involution: (Param->mat)``
Function defined at basic.at:923:4-41
(p): involution@KGBElt(x@Param(p))


.. _root_datum_([vec],[vec],int->RootDatum):

\root_datum
----------------------------------------------

``root_datum: ([vec],[vec],int->RootDatum)``
Function defined at basic.at:446:4--447:45
(simple_roots,simple_coroots,r): root_datum@(mat,mat)(#@(int,[vec])(r,simple_roots),#@(int,[vec])(r,simple_coroots))


.. _root_datum_(LieType,[ratvec]->RootDatum):

\root_datum
----------------------------------------------

``root_datum: (LieType,[ratvec]->RootDatum)``
Function defined at basic.at:449:4--450:38
(t,gens): root_datum@(LieType,mat)(t,quotient_basis@(LieType,[ratvec])(t,gens))


.. _root_datum_(LieType,ratvec->RootDatum):

\root_datum
----------------------------------------------

``root_datum: (LieType,ratvec->RootDatum)``
Function defined at basic.at:453:4-71
(t,gen): root_datum@(LieType,[ratvec])(t,[gen])


.. _root_datum_(KGBElt->RootDatum):

\root_datum
----------------------------------------------

``root_datum: (KGBElt->RootDatum)``
Function defined at basic.at:755:4-51
(x): RdRf:real_form@KGBElt(x)


.. _root_datum_(Param->RootDatum):

\root_datum
----------------------------------------------

``root_datum: (Param->RootDatum)``
Function defined at basic.at:906:4-50
(p): RdRf:real_form@Param(p)


.. _root_datum_(ParamPol->RootDatum):

\root_datum
----------------------------------------------

``root_datum: (ParamPol->RootDatum)``
Function defined at basic.at:1033:4-53
(P): RdRf:real_form@ParamPol(P)


.. _adjoint_(RootDatum->RootDatum):

\adjoint
----------------------------------------------

``adjoint: (RootDatum->RootDatum)``
Function defined at basic.at:639:4--640:59
(rd): root_datum@(mat,mat)(id_mat@int(semisimple_rank@RootDatum(rd)),Cartan_matrix@RootDatum(rd))


.. _root_(RootDatum,vec->vec):

\root
----------------------------------------------

``root: (RootDatum,vec->vec)``
Function defined at basic.at:525:4-77
(rd,alpha_v): root@(RootDatum,int)(rd,coroot_index@(RootDatum,vec)(rd,alpha_v))


.. _coroot_(RootDatum,vec->vec):

\coroot
----------------------------------------------

``coroot: (RootDatum,vec->vec)``
Function defined at basic.at:526:4-75
(rd,alpha): coroot@(RootDatum,int)(rd,root_index@(RootDatum,vec)(rd,alpha))


.. _integrality_datum_(Param->RootDatum):

\integrality_datum
----------------------------------------------

``integrality_datum: (Param->RootDatum)``
Function defined at basic.at:925:4--926:61
(p): integrality_datum@(RootDatum,ratvec)(root_datum@Param(p),infinitesimal_character@Param(p))


.. _inner_class_(KGBElt->InnerClass):

\inner_class
----------------------------------------------

``inner_class: (KGBElt->InnerClass)``
Function defined at basic.at:756:4-53
(x): IcRf:real_form@KGBElt(x)


.. _inner_class_(Param->InnerClass):

\inner_class
----------------------------------------------

``inner_class: (Param->InnerClass)``
Function defined at basic.at:907:4-52
(p): IcRf:real_form@Param(p)


.. _real_form_(KGBElt->RealForm):

\real_form
----------------------------------------------

``real_form: (KGBElt->RealForm)``
Function defined at basic.at:753:4-47
(x):  let (rf,)=%@KGBElt(x) in rf


.. _Cartan_class_(InnerClass,mat->CartanClass):

\Cartan_class
----------------------------------------------

``Cartan_class: (InnerClass,mat->CartanClass)``
Function defined at basic.at:775:4--776:55
(ic,theta): Cartan_class@KGBElt(KGB_elt@(InnerClass,mat,ratvec)(ic,theta,QvV:null@int(rank@RootDatum(RdIc:ic))))


.. _Cartan_class_(Param->CartanClass):

\Cartan_class
----------------------------------------------

``Cartan_class: (Param->CartanClass)``
Function defined at basic.at:921:4-60
(p): Cartan_class@KGBElt(x@Param(p))


.. _most_split_Cartan_(InnerClass->CartanClass):

\most_split_Cartan
----------------------------------------------

``most_split_Cartan: (InnerClass->CartanClass)``
Function defined at basic.at:695:4--696:45
(ic): Cartan_class@(InnerClass,int)(ic,-@(int,int)(nr_of_Cartan_classes@InnerClass(ic),1))


.. _real_forms_(InnerClass->[RealForm]):

\real_forms
----------------------------------------------

``real_forms: (InnerClass->[RealForm])``
Function defined at basic.at:723:4--724:36
(ic): real_forms@CartanClass(fundamental_Cartan@InnerClass(ic))


.. _dual_real_forms_(InnerClass->[RealForm]):

\dual_real_forms
----------------------------------------------

``dual_real_forms: (InnerClass->[RealForm])``
Function defined at basic.at:725:4--726:40
(ic): dual_real_forms@CartanClass(most_split_Cartan@InnerClass(ic))


.. _KGB_(RealForm->[KGBElt]):

\KGB
----------------------------------------------

``KGB: (RealForm->[KGBElt])``
Function defined at basic.at:758:4-68
(rf):  for i: KGB_size@RealForm(rf) do KGB@(RealForm,int)(rf,i) od


.. _KGB_(CartanClass,RealForm->[KGBElt]):

\KGB
----------------------------------------------

``KGB: (CartanClass,RealForm->[KGBElt])``
Function defined at basic.at:761:4--763:71
(H,G):  let result=[] in voided: for x in KGB@RealForm(G) do  if =@(CartanClass,CartanClass)(Cartan_class@KGBElt(x),H) then result:=#@([T],T)(result,x) else () fi  od ;result


.. _cross_(vec,KGBElt->KGBElt):

\cross
----------------------------------------------

``cross: (vec,KGBElt->KGBElt)``
Function defined at basic.at:782:4--783:42
(alpha,x): cross@(int,KGBElt)(root_index@(RootDatum,vec)(root_datum@KGBElt(x),alpha),x)


.. _Cayley_(vec,KGBElt->KGBElt):

\Cayley
----------------------------------------------

``Cayley: (vec,KGBElt->KGBElt)``
Function defined at basic.at:784:4--785:42
(alpha,x): Cayley@(int,KGBElt)(root_index@(RootDatum,vec)(RdRf:real_form@KGBElt(x),alpha),x)


.. _status_(vec,KGBElt->int):

\status
----------------------------------------------

``status: (vec,KGBElt->int)``
Function defined at basic.at:780:4-79
(alpha,x): status@(int,KGBElt)(root_index@(RootDatum,vec)(RdRf:real_form@KGBElt(x),alpha),x)


.. _status_(vec,Param->int):

\status
----------------------------------------------

``status: (vec,Param->int)``
Function defined at basic.at:974:4--980:4
(alpha,p):  let st=status@(vec,KGBElt)(alpha,x@Param(p)) in  if  if <=@(int,int)(st,1) then true else =@(int,int)(st,4) fi  then st elif =@(int,int)(st,3) then +@(int,int)(5,imaginary_type@(vec,Param)(alpha,p)) elif =@(Param,Param)(Cayley@(vec,Param)(alpha,p),p) then 5 else +@(int,int)(1,real_type@(vec,Param)(alpha,p)) fi


.. _status_(int,Param->int):

\status
----------------------------------------------

``status: (int,Param->int)``
Function defined at basic.at:982:4--983:40
(s,p): status@(vec,Param)(root@(RootDatum,int)(integrality_datum@Param(p),s),p)


.. _KGB_elt_(InnerClass,mat,ratvec->KGBElt):

\KGB_elt
----------------------------------------------

``KGB_elt: (InnerClass,mat,ratvec->KGBElt)``
Function defined at basic.at:765:4--767:24
((,theta,v):all):  let rf=real_form@(InnerClass,mat,ratvec)(all) in KGB_elt@(RealForm,mat,ratvec)(rf,theta,v)


.. _KGB_elt_(RootDatum,mat,ratvec->KGBElt):

\KGB_elt
----------------------------------------------

``KGB_elt: (RootDatum,mat,ratvec->KGBElt)``
Function defined at basic.at:770:4--773:24
(rd,theta,v):  let ic=inner_class@(RootDatum,mat)(rd,theta) in  let rf=real_form@(InnerClass,mat,ratvec)(ic,theta,v) in KGB_elt@(RealForm,mat,ratvec)(rf,theta,v)


.. _print_block_(RealForm,RealForm->):

\print_block
----------------------------------------------

``print_block: (RealForm,RealForm->)``
Function defined at basic.at:892:4-71
(p): print_block@Block(block@(RealForm,RealForm)(p))


.. _null_module_(Param->ParamPol):

\null_module
----------------------------------------------

``null_module: (Param->ParamPol)``
Function defined at basic.at:909:4--910:27
(p): null_module@RealForm(real_form@Param(p))


.. _null_module_(ParamPol->ParamPol):

\null_module
----------------------------------------------

``null_module: (ParamPol->ParamPol)``
Function defined at basic.at:1017:4-44
(P): *@(int,ParamPol)(0,P)


.. _raw_KL_(RealForm,RealForm->mat,[vec],vec):

\raw_KL
----------------------------------------------

``raw_KL: (RealForm,RealForm->mat,[vec],vec)``
Function defined at basic.at:889:4-71
(p): raw_KL@Block(block@(RealForm,RealForm)(p))


.. _dual_KL_(RealForm,RealForm->mat,[vec],vec):

\dual_KL
----------------------------------------------

``dual_KL: (RealForm,RealForm->mat,[vec],vec)``
Function defined at basic.at:890:4-72
(p): dual_KL@Block(block@(RealForm,RealForm)(p))


.. _print_blocku_(RealForm,RealForm->):

\print_blocku
----------------------------------------------

``print_blocku: (RealForm,RealForm->)``
Function defined at basic.at:893:4-71
(p): print_blocku@Block(block@(RealForm,RealForm)(p))


.. _print_blockd_(RealForm,RealForm->):

\print_blockd
----------------------------------------------

``print_blockd: (RealForm,RealForm->)``
Function defined at basic.at:894:4-71
(p): print_blockd@Block(block@(RealForm,RealForm)(p))


.. _print_KGB_(KGBElt->):

\print_KGB
----------------------------------------------

``print_KGB: (KGBElt->)``
Function defined at basic.at:870:4--872:27
(x): prints@void();prints@(string,int,string)("Element is number ",#@KGBElt(x)," in following KGB set");print_KGB@RealForm(real_form@KGBElt(x))


.. _print_KL_basis_(RealForm,RealForm->):

\print_KL_basis
----------------------------------------------

``print_KL_basis: (RealForm,RealForm->)``
Function defined at basic.at:895:4-75
(p): print_KL_basis@Block(block@(RealForm,RealForm)(p))


.. _print_prim_KL_(RealForm,RealForm->):

\print_prim_KL
----------------------------------------------

``print_prim_KL: (RealForm,RealForm->)``
Function defined at basic.at:896:4-74
(p): print_prim_KL@Block(block@(RealForm,RealForm)(p))


.. _print_KL_list_(RealForm,RealForm->):

\print_KL_list
----------------------------------------------

``print_KL_list: (RealForm,RealForm->)``
Function defined at basic.at:897:4-74
(p): print_KL_list@Block(block@(RealForm,RealForm)(p))


.. _print_W_cells_(RealForm,RealForm->):

\print_W_cells
----------------------------------------------

``print_W_cells: (RealForm,RealForm->)``
Function defined at basic.at:898:4-74
(p): print_W_cells@Block(block@(RealForm,RealForm)(p))


.. _print_W_graph_(RealForm,RealForm->):

\print_W_graph
----------------------------------------------

``print_W_graph: (RealForm,RealForm->)``
Function defined at basic.at:899:4-74
(p): print_W_cells@Block(block@(RealForm,RealForm)(p))


.. _assert_(bool,string->):

\assert
----------------------------------------------

``assert: (bool,string->)``
Function defined at basic.at:7:4-74
(b,message):  if b then () else error@string(message) fi


.. _assert_(bool->):

\assert
----------------------------------------------

``assert: (bool->)``
Function defined at basic.at:8:4-56
(b): assert@(bool,string)(b,"assertion failed")


.. _list_((int->bool),int->[int]):

\list
----------------------------------------------

``list: ((int->bool),int->[int])``
Function defined at basic.at:12:4--13:55
(filter,limit): ##@([[T]])( for i: limit do  if filter(i) then [i] else [] fi  od )


.. _complement_((int->bool),int->[int]):

\complement
----------------------------------------------

``complement: ((int->bool),int->[int])``
Function defined at basic.at:14:4--15:55
(filter,limit): ##@([[T]])( for i: limit do  if filter(i) then [] else [i] fi  od )


.. _count_((int->bool),int->int):

\count
----------------------------------------------

``count: ((int->bool),int->int)``
Function defined at basic.at:17:4--18:60
(filter,limit):  let c=0 in voided: for i: limit do  if filter(i) then c:=+@(int,int)(c,1) else () fi  od ;c


.. _all_([bool]->bool):

\all
----------------------------------------------

``all: ([bool]->bool)``
Function defined at basic.at:20:4--21:54
(p): voided: for x in p do  if x then () else  return false fi  od ;true


.. _all_(int,(int->bool)->bool):

\all
----------------------------------------------

``all: (int,(int->bool)->bool)``
Function defined at basic.at:29:4--30:63
(limit,filter): voided: for i: limit do  if filter(i) then () else  return false fi  od ;true


.. _all_([(->bool)]->bool):

\all
----------------------------------------------

``all: ([(->bool)]->bool)``
Function defined at basic.at:39:4--40:56
(p): voided: for x in p do  if x() then () else  return false fi  od ;true


.. _all_(mat,(vec->bool)->bool):

\all
----------------------------------------------

``all: (mat,(vec->bool)->bool)``
Function defined at basic.at:269:4--270:68
(M,filter):  let j=-@(int,int)(n_columns@mat(M),1) in voided: while  if >=@int(j) then filter(M[j]) else false fi  do j:=-@(int,int)(j,1) od ;<@int(j)


.. _x_(Param->KGBElt):

\x
----------------------------------------------

``x: (Param->KGBElt)``
Function defined at basic.at:916:4-44
(p):  let (x,,)=%@Param(p) in x


.. _none_([bool]->bool):

\none
----------------------------------------------

``none: ([bool]->bool)``
Function defined at basic.at:22:4--23:50
(p): voided: for x in p do  if x then  return false else () fi  od ;true


.. _none_(int,(int->bool)->bool):

\none
----------------------------------------------

``none: (int,(int->bool)->bool)``
Function defined at basic.at:31:4--32:59
(limit,filter): voided: for i: limit do  if filter(i) then  return false else () fi  od ;true


.. _none_([(->bool)]->bool):

\none
----------------------------------------------

``none: ([(->bool)]->bool)``
Function defined at basic.at:41:4--42:52
(p): voided: for x in p do  if x() then  return false else () fi  od ;true


.. _none_(mat,(vec->bool)->bool):

\none
----------------------------------------------

``none: (mat,(vec->bool)->bool)``
Function defined at basic.at:271:4--272:72
(M,filter):  let j=-@(int,int)(n_columns@mat(M),1) in voided: while  if >=@int(j) then not@bool(filter(M[j])) else false fi  do j:=-@(int,int)(j,1) od ;<@int(j)


.. _first_([bool]->int):

\first
----------------------------------------------

``first: ([bool]->int)``
Function defined at basic.at:24:4--25:46
(p): voided: for x@i in p do  if x then  return i else () fi  od ;-@int(1)


.. _first_(int,(int->bool)->int):

\first
----------------------------------------------

``first: (int,(int->bool)->int)``
Function defined at basic.at:33:4--34:53
(limit,filter): voided: for i: limit do  if filter(i) then  return i else () fi  od ;-@int(1)


.. _first_([(->bool)]->int):

\first
----------------------------------------------

``first: ([(->bool)]->int)``
Function defined at basic.at:43:4--44:48
(p): voided: for x@i in p do  if x() then  return i else () fi  od ;-@int(1)


.. _first_(mat,(vec->bool)->int):

\first
----------------------------------------------

``first: (mat,(vec->bool)->int)``
Function defined at basic.at:273:4--275:69
(M,filter):  let (j,n)=(0,n_columns@mat(M)) in voided: while  if <@(int,int)(j,n) then filter(M[j]) else false fi  do j:=+@(int,int)(j,1) od ; if =@(int,int)(j,n) then -@int(1) else j fi


.. _last_([bool]->int):

\last
----------------------------------------------

``last: ([bool]->int)``
Function defined at basic.at:26:4--27:53
(p):  let i=-@(int,int)(#@[bool](p),1) in voided: while  if >=@int(i) then not@bool(p[i]) else false fi  do i:=-@(int,int)(i,1) od ;i


.. _last_(int,(int->bool)->int):

\last
----------------------------------------------

``last: (int,(int->bool)->int)``
Function defined at basic.at:35:4--36:54
(limit,filter): voided: for i: limit ~do  if filter(i) then  return i else () fi  od ;-@int(1)


.. _last_([(->bool)]->int):

\last
----------------------------------------------

``last: ([(->bool)]->int)``
Function defined at basic.at:45:4--46:55
(p):  let i=-@(int,int)(#@[(->bool)](p),1) in voided: while  if >=@int(i) then not@bool((p[i])()) else false fi  do i:=-@(int,int)(i,1) od ;i


.. _last_(mat,(vec->bool)->int):

\last
----------------------------------------------

``last: (mat,(vec->bool)->int)``
Function defined at basic.at:276:4--277:67
(M,filter):  let j=-@(int,int)(n_columns@mat(M),1) in voided: while  if >=@int(j) then filter(M[j]) else false fi  do j:=-@(int,int)(j,1) od ;j


.. _abs_(int->int):

\abs
----------------------------------------------

``abs: (int->int)``
Function defined at basic.at:52:4-45
(k):  if <@int(k) then -@int(k) else k fi


.. _abs_(rat->rat):

\abs
----------------------------------------------

``abs: (rat->rat)``
Function defined at basic.at:81:4-29
(a): *@(rat,rat)(QI:sign@rat(a),a)


.. _sign_(int->int):

\sign
----------------------------------------------

``sign: (int->int)``
Function defined at basic.at:53:4-61
(k):  if >@int(k) then 1 elif <@int(k) then -@int(1) else 0 fi


.. _sign_(rat->int):

\sign
----------------------------------------------

``sign: (rat->int)``
Function defined at basic.at:79:4-37
(a): sign@int(numer@rat(a))


.. _is_odd_(int->bool):

\is_odd
----------------------------------------------

``is_odd: (int->bool)``
Function defined at basic.at:55:4-33
(n): =@(int,int)(%@(int,int)(n,2),1)


.. _is_even_(int->bool):

\is_even
----------------------------------------------

``is_even: (int->bool)``
Function defined at basic.at:56:4-33
(n): =@(int,int)(%@(int,int)(n,2),0)


.. _min_(int,int->int):

\min
----------------------------------------------

``min: (int,int->int)``
Function defined at basic.at:58:4-53
(k,l):  if <@(int,int)(k,l) then k else l fi


.. _min_([int]->int):

\min
----------------------------------------------

``min: ([int]->int)``
Function defined at basic.at:61:4--62:61
(a):  let l=#@[int](a) in assert@(bool,string)(>=@(int,int)(l,1),"Minimum of an empty list"); let m=a~[0] in voided: for i: -@(int,int)(l,1) do  if <@(int,int)(a[i],m) then m:=a[i] else () fi  od ;m


.. _max_(int,int->int):

\max
----------------------------------------------

``max: (int,int->int)``
Function defined at basic.at:59:4-53
(k,l):  if <@(int,int)(k,l) then l else k fi


.. _max_([int]->int):

\max
----------------------------------------------

``max: ([int]->int)``
Function defined at basic.at:63:4--64:61
(a):  let l=#@[int](a) in assert@(bool,string)(>=@(int,int)(l,1),"Maximum of an empty list"); let m=a~[0] in voided: for i: -@(int,int)(l,1) do  if >@(int,int)(a[i],m) then m:=a[i] else () fi  od ;m


.. _lcm_([int]->int):

\lcm
----------------------------------------------

``lcm: ([int]->int)``
Function defined at basic.at:66:4-76
(list):  let (,d)=%@ratvec(Qv[Q]: for x in list do /@rat(QI:x) od ) in d


.. _numer_(rat->int):

\numer
----------------------------------------------

``numer: (rat->int)``
Function defined at basic.at:75:4-36
(a):  let (n,)=%@rat(a) in n


.. _numer_(ratvec->vec):

\numer
----------------------------------------------

``numer: (ratvec->vec)``
Function defined at basic.at:342:4-44
(a):  let (n,)=%@ratvec(a) in n


.. _denom_(rat->int):

\denom
----------------------------------------------

``denom: (rat->int)``
Function defined at basic.at:76:4-36
(a):  let (,d)=%@rat(a) in d


.. _denom_(ratvec->int):

\denom
----------------------------------------------

``denom: (ratvec->int)``
Function defined at basic.at:343:4-44
(a):  let (,d)=%@ratvec(a) in d


.. _is_integer_(rat->bool):

\is_integer
----------------------------------------------

``is_integer: (rat->bool)``
Function defined at basic.at:78:4-41
(r): =@(int,int)(denom@rat(r),1)


.. _is_integer_(ratvec->bool):

\is_integer
----------------------------------------------

``is_integer: (ratvec->bool)``
Function defined at basic.at:367:4-52
(v):  let (,d)=%@ratvec(v) in =@(int,int)(d,1)


.. _floor_(rat->int):

\floor
----------------------------------------------

``floor: (rat->int)``
Function defined at basic.at:83:4-29
(a): \@(int,int)(%@rat(a))


.. _floor_([rat]->vec):

\floor
----------------------------------------------

``floor: ([rat]->vec)``
Function defined at basic.at:92:4-52
(v): V[I]: for a in v do floor@rat(a) od


.. _ceil_(rat->int):

\ceil
----------------------------------------------

``ceil: (rat->int)``
Function defined at basic.at:84:4-31
(a): -@int(\@(int,int)(%@rat(-@rat(a))))


.. _ceil_([rat]->vec):

\ceil
----------------------------------------------

``ceil: ([rat]->vec)``
Function defined at basic.at:93:4-52
(v): V[I]: for a in v do ceil@rat(a) od


.. _rat_as_int_(rat->int):

\rat_as_int
----------------------------------------------

``rat_as_int: (rat->int)``
Function defined at basic.at:97:4--98:63
(r):  let (n,d)=%@rat(r) in  if =@(int,int)(d,1) then n else error@string("Not an integer") fi


.. _plural_(int->string):

\plural
----------------------------------------------

``plural: (int->string)``
Function defined at basic.at:119:4-55
(n):  if =@(int,int)(n,1) then "" else "s" fi


.. _split_lines_(string->[string]):

\split_lines
----------------------------------------------

``split_lines: (string->[string])``
Function defined at basic.at:123:4--127:12
(text):  let (result,a,last)=([], for c in text do c od ,0) in voided: for c@i in a do  if =@(string,string)(c,new_line) then result:=#@([T],T)(result,concat@[string](a[last:i]));last:=+@(int,int)(i,1) else () fi  od ;result


.. _is_substring_(string,string->bool):

\is_substring
----------------------------------------------

``is_substring: (string,string->bool)``
Function defined at basic.at:129:4--131:64
(s,text):  let (s0,t0)=( for c in s do c od , for c in text do c od ) in >=@int(last@(int,(int->bool))(-@(int,int)(#@[string](t0),#@[string](s0)),(start): all@(int,(int->bool))(#@[string](s0),(i): =@(string,string)(t0[+@(int,int)(start,i)],s0[i]))))


.. _fgrep_(string,string->[string]):

\fgrep
----------------------------------------------

``fgrep: (string,string->[string])``
Function defined at basic.at:133:4--137:12
(s,text):  let result=[] in voided: for line in split_lines@string(text) do  if is_substring@(string,string)(s,line) then result:=#@([T],T)(result,line) else () fi  od ;result


.. _vector_(int,(int->int)->vec):

\vector
----------------------------------------------

``vector: (int,(int->int)->vec)``
Function defined at basic.at:141:4-56
(n,f): V[I]: for i: n do f(i) od


.. _ones_(int->vec):

\ones
----------------------------------------------

``ones: (int->vec)``
Function defined at basic.at:143:4-38
(n): V[I]: for i: n do 1 od


.. _gcd_([int]->int):

\gcd
----------------------------------------------

``gcd: ([int]->int)``
Function defined at basic.at:146:4--147:63
(v):  let f=inv_fact@mat(stack_rows@[vec][V[I]:v]) in  if =@int(#@vec(f)) then 0 else f[0] fi


.. _sum_(vec->int):

\sum
----------------------------------------------

``sum: (vec->int)``
Function defined at basic.at:153:4-56
(v): *@(vec,vec)( let one=1 in V[I]: for x in v do one od ,v)


.. _sum_(mat->vec):

\sum
----------------------------------------------

``sum: (mat->vec)``
Function defined at basic.at:308:4-42
(m): *@(mat,vec)(m,ones@int(n_columns@mat(m)))


.. _sum_([ratvec],int->ratvec):

\sum
----------------------------------------------

``sum: ([ratvec],int->ratvec)``
Function defined at basic.at:353:4--355:40
(list,l):  let result=QvV:null@int(l) in voided: for v in list do result:=+@(ratvec,ratvec)(result,v) od ;result


.. _sum_(ratvec->rat):

\sum
----------------------------------------------

``sum: (ratvec->rat)``
Function defined at basic.at:389:4-50
(v):  let (n,d)=%@ratvec(v) in /@(int,int)(sum@vec(n),d)


.. _product_(vec->int):

\product
----------------------------------------------

``product: (vec->int)``
Function defined at basic.at:154:4-57
(v):  let s=1 in voided: for e in v do s:=*@(int,int)(s,e) od ;s


.. _reverse_(vec->vec):

\reverse
----------------------------------------------

``reverse: (vec->vec)``
Function defined at basic.at:156:4-31
(v): v~[0:0~]


.. _reverse_(ratvec->ratvec):

\reverse
----------------------------------------------

``reverse: (ratvec->ratvec)``
Function defined at basic.at:382:4-37
(v): v~[0:0~]


.. _lower_(int,vec->vec):

\lower
----------------------------------------------

``lower: (int,vec->vec)``
Function defined at basic.at:157:4-35
(k,v): v[0:k]


.. _lower_(int,ratvec->ratvec):

\lower
----------------------------------------------

``lower: (int,ratvec->ratvec)``
Function defined at basic.at:383:4-41
(k,v): v[0:k]


.. _upper_(int,vec->vec):

\upper
----------------------------------------------

``upper: (int,vec->vec)``
Function defined at basic.at:158:4-36
(k,v): v[k~:0~]


.. _upper_(int,ratvec->ratvec):

\upper
----------------------------------------------

``upper: (int,ratvec->ratvec)``
Function defined at basic.at:384:4-42
(k,v): v[k~:0~]


.. _drop_lower_(int,vec->vec):

\drop_lower
----------------------------------------------

``drop_lower: (int,vec->vec)``
Function defined at basic.at:159:4-40
(k,v): v[k:0~]


.. _drop_lower_(int,ratvec->ratvec):

\drop_lower
----------------------------------------------

``drop_lower: (int,ratvec->ratvec)``
Function defined at basic.at:385:4-46
(k,v): v[k:0~]


.. _drop_upper_(int,vec->vec):

\drop_upper
----------------------------------------------

``drop_upper: (int,vec->vec)``
Function defined at basic.at:160:4-41
(k,v): v[0:k~]


.. _drop_upper_(int,ratvec->ratvec):

\drop_upper
----------------------------------------------

``drop_upper: (int,ratvec->ratvec)``
Function defined at basic.at:386:4-47
(k,v): v[0:k~]


.. _is_member_([int]->(int->bool)):

\is_member
----------------------------------------------

``is_member: ([int]->(int->bool))``
Function defined at basic.at:165:4--167:75
(v):  let !start=-@(int,int)(#@[int](v),1) in (val):  let i=start in voided: while  if >=@int(i) then !=@(int,int)(v[i],val) else false fi  do i:=-@(int,int)(i,1) od ;>=@int(i)


.. _contains_(int->([int]->bool)):

\contains
----------------------------------------------

``contains: (int->([int]->bool))``
Function defined at basic.at:169:4-72
(val): (v): (is_member@[int](v))(val)


.. _all_0_1_vecs_(int->[vec]):

\all_0_1_vecs
----------------------------------------------

``all_0_1_vecs: (int->[vec])``
Function defined at basic.at:171:4--175:4
(n):  if <=@(int,int)(n,0) then [null@int(0)] else  let list=all_0_1_vecs(-@(int,int)(n,1)) in ##@([T],[T])( for v in list do #@(vec,int)(v,0) od , for v in list do #@(vec,int)(v,1) od ) fi


.. _power_set_(int->[[int]]):

\power_set
----------------------------------------------

``power_set: (int->[[int]])``
Function defined at basic.at:177:4--178:77
(n):  if =@int(n) then [[]] else  let p=power_set(n:=-@(int,int)(n,1)) in ##@([T],[T])(p, for S in p do #@([T],T)(S,n) od ) fi


.. _power_set_([int]->[[int]]):

\power_set
----------------------------------------------

``power_set: ([int]->[[int]])``
Function defined at basic.at:179:4--180:56
(S):  for inx in power_set@int(#@[int](S)) do  for i in inx do S[i] od  od


.. _matrix_((int,int),(int,int->int)->mat):

\matrix
----------------------------------------------

``matrix: ((int,int),(int,int->int)->mat)``
Function defined at basic.at:186:4--187:38
((r,c),f): #@(int,[vec])(r, for j: c do V[I]: for i: r do f(i,j) od  od )


.. _n_rows_(mat->int):

\n_rows
----------------------------------------------

``n_rows: (mat->int)``
Function defined at basic.at:189:4-41
(m):  let (r,)=#@mat(m) in r


.. _n_columns_(mat->int):

\n_columns
----------------------------------------------

``n_columns: (mat->int)``
Function defined at basic.at:190:4-44
(m):  let (,c)=#@mat(m) in c


.. _column_(vec->mat):

\column
----------------------------------------------

``column: (vec->mat)``
Function defined at basic.at:192:4-29
(v): M[V]:[v]


.. _row_(vec->mat):

\row
----------------------------------------------

``row: (vec->mat)``
Function defined at basic.at:193:4-28
(v): ^@vec(v)


.. _map_on_(mat->((int->int)->mat)):

\map_on
----------------------------------------------

``map_on: (mat->((int->int)->mat))``
Function defined at basic.at:216:4--218:67
(m):  let nr=n_rows@mat(m) in (f): #@(int,[vec])(nr, for c in m do V[I]: for e in c do f(e) od  od )


.. _inverse_(mat->mat):

\inverse
----------------------------------------------

``inverse: (mat->mat)``
Function defined at basic.at:252:4--254:74
(M):  let (inv,d)=invert@mat(M) in  if =@(int,int)(d,1) then inv else error@string("Matrix not invertible over the integers") fi


.. _det_(mat->int):

\det
----------------------------------------------

``det: (mat->int)``
Function defined at basic.at:256:4--262:1
(M):  let ((diag,,),(n,):shape)=(diagonalize@mat(M),#@mat(M)) in assert@(bool,string)(=@(int,int)(shape),"Determinant of non-square matrix"); if <@(int,int)(#@vec(diag),n) then 0 else product@vec(diag) fi


.. _saturated_span_(mat->bool):

\saturated_span
----------------------------------------------

``saturated_span: (mat->bool)``
Function defined at basic.at:264:4--266:24
(M):  let inv_f=inv_fact@mat(M) in  if =@int(#@vec(inv_f)) then true else =@(int,int)(inv_f~[0],1) fi


.. _columns_with_((int,vec->bool),mat->mat):

\columns_with
----------------------------------------------

``columns_with: ((int,vec->bool),mat->mat)``
Function defined at basic.at:279:4--281:69
(p,m):  let res=[] in voided: for col@j in m do  if p(j,col) then res:=#@([T],T)(res,col) else () fi  od ;#@(int,[vec])(n_rows@mat(m),res)


.. _columns_with_((vec->bool),mat->mat):

\columns_with
----------------------------------------------

``columns_with: ((vec->bool),mat->mat)``
Function defined at basic.at:282:4--283:47
(p,m): columns_with@((int,vec->bool),mat)((,col): p(col),m)


.. _columns_with_((int->bool),mat->mat):

\columns_with
----------------------------------------------

``columns_with: ((int->bool),mat->mat)``
Function defined at basic.at:284:4--285:43
(p,m): columns_with@((int,vec->bool),mat)((j,): p(j),m)


.. _rows_with_((int,vec->bool),mat->mat):

\rows_with
----------------------------------------------

``rows_with: ((int,vec->bool),mat->mat)``
Function defined at basic.at:287:4--289:73
(p,m):  let res=[] in voided: for row@i in ^@mat(m) do  if p(i,row) then res:=#@([T],T)(res,row) else () fi  od ;^@(int,[vec])(n_columns@mat(m),res)


.. _rows_with_((vec->bool),mat->mat):

\rows_with
----------------------------------------------

``rows_with: ((vec->bool),mat->mat)``
Function defined at basic.at:290:4--291:44
(p,m): rows_with@((int,vec->bool),mat)((,row): p(row),m)


.. _rows_with_((int->bool),mat->mat):

\rows_with
----------------------------------------------

``rows_with: ((int->bool),mat->mat)``
Function defined at basic.at:292:4--293:40
(p,m): rows_with@((int,vec->bool),mat)((i,): p(i),m)


.. _lookup_column_(vec,mat->int):

\lookup_column
----------------------------------------------

``lookup_column: (vec,mat->int)``
Function defined at basic.at:302:4--303:62
(v,m):  let i=-@(int,int)(n_columns@mat(m),1) in voided: while  if >=@int(i) then !=@(vec,vec)(m[i],v) else false fi  do i:=-@(int,int)(i,1) od ;i


.. _lookup_row_(vec,mat->int):

\lookup_row
----------------------------------------------

``lookup_row: (vec,mat->int)``
Function defined at basic.at:304:4--305:21
(v,m): lookup_column@(vec,mat)(v,^@mat(m))


.. _solve_(mat,vec->[vec]):

\solve
----------------------------------------------

``solve: (mat,vec->[vec])``
Function defined at basic.at:328:2--330:78
(A,b):  let (ds,L,R)=diagonalize@mat(A) in  for sol in divide_factors(*@(mat,vec)(L,b),ds) do *@(mat,vec)(columns_with@((int->bool),mat)((j): <@(int,int)(j,#@vec(sol)),R),sol) od


.. _solve_(mat,ratvec->[ratvec]):

\solve
----------------------------------------------

``solve: (mat,ratvec->[ratvec])``
Function defined at basic.at:395:4--399:4
(A,b):  let ((ds,L,R),(v,denom))=(diagonalize@mat(A),%@ratvec(b)) in  let (d,target)=(#@vec(ds),*@(mat,vec)(L,v)) in  if !=@vec(target[d:0~]) then [] else [*@(mat,ratvec)(columns_with@((int->bool),mat)((j): <@(int,int)(j,d),R),Qv[Q]: for d@i in *@(vec,int)(ds,denom) do /@(int,int)(target[i],d) od )] fi


.. _order_(mat->int):

\order
----------------------------------------------

``order: (mat->int)``
Function defined at basic.at:333:4--336:44
(!!M):  let (n,):p=#@mat(M) in assert@(bool,string)(=@(int,int)(p),"Matrix is not square"); let (N,order,I)=(M,1,id_mat@int(n)) in voided: while !=@(mat,mat)(N,I) do N:=*@(mat,mat)(N,M);order:=+@(int,int)(order,1) od ;order


.. _ratvec_as_vec_(ratvec->vec):

\ratvec_as_vec
----------------------------------------------

``ratvec_as_vec: (ratvec->vec)``
Function defined at basic.at:379:4--380:56
(v):  let (w,d)=%@ratvec(v) in assert@(bool,string)(=@(int,int)(d,1),"Not an integer vector");w


.. _int_part_(Split->int):

\int_part
----------------------------------------------

``int_part: (Split->int)``
Function defined at basic.at:406:4-46
(x):  let (r,)=%@Split(x) in r


.. _s_part_(Split->int):

\s_part
----------------------------------------------

``s_part: (Split->int)``
Function defined at basic.at:407:4-44
(x):  let (,y)=%@Split(x) in y


.. _s_to_1_(Split->int):

\s_to_1
----------------------------------------------

``s_to_1: (Split->int)``
Function defined at basic.at:412:4-31
(x): +@(int,int)(%@Split(x))


.. _s_to_1_(ParamPol->ParamPol):

\s_to_1
----------------------------------------------

``s_to_1: (ParamPol->ParamPol)``
Function defined at basic.at:1023:4-74
(P): +@(ParamPol,[(Split,Param)])(*@(int,ParamPol)(0,P), for x@q in P do (SpI:+@(int,int)(%@Split(x)),q) od )


.. _s_to_minus_1_(Split->int):

\s_to_minus_1
----------------------------------------------

``s_to_minus_1: (Split->int)``
Function defined at basic.at:413:4-37
(x): -@(int,int)(%@Split(x))


.. _s_to_minus_1_(ParamPol->ParamPol):

\s_to_minus_1
----------------------------------------------

``s_to_minus_1: (ParamPol->ParamPol)``
Function defined at basic.at:1024:4-74
(P): +@(ParamPol,[(Split,Param)])(*@(int,ParamPol)(0,P), for x@q in P do (SpI:-@(int,int)(%@Split(x)),q) od )


.. _split_as_int_(Split->int):

\split_as_int
----------------------------------------------

``split_as_int: (Split->int)``
Function defined at basic.at:415:4--416:57
(x):  let (r,y)=%@Split(x) in assert@(bool,string)(=@int(y),"split is not an integer");r


.. _split_format_(Split->string):

\split_format
----------------------------------------------

``split_format: (Split->string)``
Function defined at basic.at:419:4--427:4
(w):  let (a,b)=%@Split(w) in  if  if =@int(a) then !=@int(b) else false fi  then +@(string,string)( if >@(int,int)(abs@int(b),1) then int_format@int(b) elif =@(int,int)(b,1) then "" else "-" fi ,"s") else +@(string,string)(int_format@int(a), if >@(int,int)(abs@int(b),1) then +@(string,string)(+@(string,string)( if <@int(b) then "" else "+" fi ,int_format@int(b)),"s") elif =@int(b) then "" elif =@(int,int)(b,1) then "+s" else "-s" fi ) fi


.. _is_root_(RootDatum,vec->bool):

\is_root
----------------------------------------------

``is_root: (RootDatum,vec->bool)``
Function defined at basic.at:456:4--457:34
((rd,):p): <@(int,int)(root_index@(RootDatum,vec)(p),nr_of_posroots@RootDatum(rd))


.. _is_coroot_(RootDatum,vec->bool):

\is_coroot
----------------------------------------------

``is_coroot: (RootDatum,vec->bool)``
Function defined at basic.at:458:4--459:36
((rd,):p): <@(int,int)(coroot_index@(RootDatum,vec)(p),nr_of_posroots@RootDatum(rd))


.. _is_posroot_(RootDatum,vec->bool):

\is_posroot
----------------------------------------------

``is_posroot: (RootDatum,vec->bool)``
Function defined at basic.at:460:4--461:56
((rd,):p):  let ri=root_index@(RootDatum,vec)(p) in  if >=@int(ri) then <@(int,int)(ri,nr_of_posroots@RootDatum(rd)) else false fi


.. _is_poscoroot_(RootDatum,vec->bool):

\is_poscoroot
----------------------------------------------

``is_poscoroot: (RootDatum,vec->bool)``
Function defined at basic.at:462:4--463:61
((rd,):p):  let cri=coroot_index@(RootDatum,vec)(p) in  if >=@int(cri) then <@(int,int)(cri,nr_of_posroots@RootDatum(rd)) else false fi


.. _posroot_index_(RootDatum,vec->int):

\posroot_index
----------------------------------------------

``posroot_index: (RootDatum,vec->int)``
Function defined at basic.at:465:4--466:50
(p):  let i=root_index@(RootDatum,vec)(p) in  if <@int(i) then -@(int,int)(-@int(1),i) else i fi


.. _poscoroot_index_(RootDatum,vec->int):

\poscoroot_index
----------------------------------------------

``poscoroot_index: (RootDatum,vec->int)``
Function defined at basic.at:467:4--468:52
(p):  let i=coroot_index@(RootDatum,vec)(p) in  if <@int(i) then -@(int,int)(-@int(1),i) else i fi


.. _rho_(RootDatum->ratvec):

\rho
----------------------------------------------

``rho: (RootDatum->ratvec)``
Function defined at basic.at:471:4--473:74
(rd):  let res=QvV:null@int(rank@RootDatum(rd)) in voided: for i: semisimple_rank@RootDatum(rd) do res:=+@(ratvec,ratvec)(res,fundamental_weight@(RootDatum,int)(rd,i)) od ;res


.. _rho_as_vec_(RootDatum->vec):

\rho_as_vec
----------------------------------------------

``rho_as_vec: (RootDatum->vec)``
Function defined at basic.at:477:4-56
(r): ratvec_as_vec@ratvec(rho@RootDatum(r))


.. _rho_check_(RootDatum->ratvec):

\rho_check
----------------------------------------------

``rho_check: (RootDatum->ratvec)``
Function defined at basic.at:479:4--481:76
(rd):  let res=QvV:null@int(rank@RootDatum(rd)) in voided: for i: semisimple_rank@RootDatum(rd) do res:=+@(ratvec,ratvec)(res,fundamental_coweight@(RootDatum,int)(rd,i)) od ;res


.. _is_positive_root_(RootDatum->(vec->bool)):

\is_positive_root
----------------------------------------------

``is_positive_root: (RootDatum->(vec->bool))``
Function defined at basic.at:486:4--487:55
(rd):  let rc=rho_check@RootDatum(rd) in (alpha): >@rat(*@(ratvec,ratvec)(rc,QvV:alpha))


.. _is_positive_root_(RootDatum,vec->bool):

\is_positive_root
----------------------------------------------

``is_positive_root: (RootDatum,vec->bool)``
Function defined at basic.at:495:4--496:29
(rd,alpha): (is_positive_root@RootDatum(rd))(alpha)


.. _is_positive_coroot_(RootDatum->(vec->bool)):

\is_positive_coroot
----------------------------------------------

``is_positive_coroot: (RootDatum->(vec->bool))``
Function defined at basic.at:488:4--489:53
(rd):  let rho=rho@RootDatum(rd) in (alphav): >@rat(*@(vec,ratvec)(alphav,rho))


.. _is_positive_coroot_(RootDatum,vec->bool):

\is_positive_coroot
----------------------------------------------

``is_positive_coroot: (RootDatum,vec->bool)``
Function defined at basic.at:497:4--498:32
(rd,alphav): (is_positive_coroot@RootDatum(rd))(alphav)


.. _is_negative_root_(RootDatum->(vec->bool)):

\is_negative_root
----------------------------------------------

``is_negative_root: (RootDatum->(vec->bool))``
Function defined at basic.at:490:4--491:55
(rd):  let rc=rho_check@RootDatum(rd) in (alpha): <@rat(*@(ratvec,ratvec)(rc,QvV:alpha))


.. _is_negative_root_(RootDatum,vec->bool):

\is_negative_root
----------------------------------------------

``is_negative_root: (RootDatum,vec->bool)``
Function defined at basic.at:499:4--500:29
(rd,alpha): (is_negative_root@RootDatum(rd))(alpha)


.. _is_negative_coroot_(RootDatum->(vec->bool)):

\is_negative_coroot
----------------------------------------------

``is_negative_coroot: (RootDatum->(vec->bool))``
Function defined at basic.at:492:4--493:53
(rd):  let rho=rho@RootDatum(rd) in (alphav): <@rat(*@(vec,ratvec)(alphav,rho))


.. _is_negative_coroot_(RootDatum,vec->bool):

\is_negative_coroot
----------------------------------------------

``is_negative_coroot: (RootDatum,vec->bool)``
Function defined at basic.at:501:4--502:32
(rd,alphav): (is_negative_coroot@RootDatum(rd))(alphav)


.. _roots_all_positive_(RootDatum->(mat->bool)):

\roots_all_positive
----------------------------------------------

``roots_all_positive: (RootDatum->(mat->bool))``
Function defined at basic.at:505:4--506:76
(rd):  let are_pos=is_positive_root@RootDatum(rd) in (roots): all@(mat,(vec->bool))(roots,are_pos)


.. _roots_(RootDatum->mat):

\roots
----------------------------------------------

``roots: (RootDatum->mat)``
Function defined at basic.at:519:4--520:50
(rd):  let pr=posroots@RootDatum(rd) in ##@(mat,mat)(negative_system@mat(pr),pr)


.. _coroots_all_positive_(RootDatum->(mat->bool)):

\coroots_all_positive
----------------------------------------------

``coroots_all_positive: (RootDatum->(mat->bool))``
Function defined at basic.at:507:4--509:42
(rd):  let are_pos=is_positive_coroot@RootDatum(rd) in (coroots): all@(mat,(vec->bool))(coroots,are_pos)


.. _coroots_(RootDatum->mat):

\coroots
----------------------------------------------

``coroots: (RootDatum->mat)``
Function defined at basic.at:521:4--522:55
(rd):  let pcr=poscoroots@RootDatum(rd) in ##@(mat,mat)(negative_system@mat(pcr),pcr)


.. _among_posroots_(RootDatum->(mat->bool)):

\among_posroots
----------------------------------------------

``among_posroots: (RootDatum->(mat->bool))``
Function defined at basic.at:510:4--511:38
(rd): (M): all@(mat,(vec->bool))(M,(v): is_posroot@(RootDatum,vec)(rd,v))


.. _among_poscoroots_(RootDatum->(mat->bool)):

\among_poscoroots
----------------------------------------------

``among_poscoroots: (RootDatum->(mat->bool))``
Function defined at basic.at:512:4--513:40
(rd): (M): all@(mat,(vec->bool))(M,(v): is_poscoroot@(RootDatum,vec)(rd,v))


.. _negative_system_(mat->mat):

\negative_system
----------------------------------------------

``negative_system: (mat->mat)``
Function defined at basic.at:515:4--516:42
(posroots): swiss_matrix_knife@(int,mat,int,int,int,int)(172,posroots,0,0,0,0)


.. _reflection_(RootDatum,int->mat):

\reflection
----------------------------------------------

``reflection: (RootDatum,int->mat)``
Function defined at basic.at:529:4--530:42
(rd,i): -@(int,mat)(1,*@(mat,mat)(column@vec(root@(RootDatum,int)(rd,i)),row@vec(coroot@(RootDatum,int)(rd,i))))


.. _reflection_(RootDatum,vec->mat):

\reflection
----------------------------------------------

``reflection: (RootDatum,vec->mat)``
Function defined at basic.at:531:4--532:30
((rd,):p): reflection@(RootDatum,int)(rd,root_index@(RootDatum,vec)(p))


.. _coreflection_(RootDatum,int->mat):

\coreflection
----------------------------------------------

``coreflection: (RootDatum,int->mat)``
Function defined at basic.at:533:4--534:42
(rd,i): -@(int,mat)(1,*@(mat,mat)(column@vec(coroot@(RootDatum,int)(rd,i)),row@vec(root@(RootDatum,int)(rd,i))))


.. _coreflection_(RootDatum,vec->mat):

\coreflection
----------------------------------------------

``coreflection: (RootDatum,vec->mat)``
Function defined at basic.at:535:4--536:32
((rd,):p): coreflection@(RootDatum,int)(rd,root_index@(RootDatum,vec)(p))


.. _reflect_(RootDatum,int,vec->vec):

\reflect
----------------------------------------------

``reflect: (RootDatum,int,vec->vec)``
Function defined at basic.at:537:4--538:37
(rd,i,v): v:=-@(vec,vec)(v,*@(vec,int)(root@(RootDatum,int)(rd,i),*@(vec,vec)(coroot@(RootDatum,int)(rd,i),v)))


.. _reflect_(RootDatum,vec,vec->vec):

\reflect
----------------------------------------------

``reflect: (RootDatum,vec,vec->vec)``
Function defined at basic.at:539:4--540:36
(rd,alpha,v): v:=-@(vec,vec)(v,*@(vec,int)(alpha,*@(vec,vec)(coroot@(RootDatum,vec)(rd,alpha),v)))


.. _reflect_(RootDatum,int,ratvec->ratvec):

\reflect
----------------------------------------------

``reflect: (RootDatum,int,ratvec->ratvec)``
Function defined at basic.at:546:4--547:37
(rd,i,v):  let (n,d)=%@ratvec(v) in /@(vec,int)(reflect@(RootDatum,int,vec)(rd,i,n),d)


.. _reflect_(RootDatum,vec,ratvec->ratvec):

\reflect
----------------------------------------------

``reflect: (RootDatum,vec,ratvec->ratvec)``
Function defined at basic.at:548:4--549:41
(rd,alpha,v):  let (n,d)=%@ratvec(v) in /@(vec,int)(reflect@(RootDatum,vec,vec)(rd,alpha,n),d)


.. _coreflect_(RootDatum,vec,int->vec):

\coreflect
----------------------------------------------

``coreflect: (RootDatum,vec,int->vec)``
Function defined at basic.at:541:4--542:37
(rd,v,i): v:=-@(vec,vec)(v,*@(int,vec)(*@(vec,vec)(v,root@(RootDatum,int)(rd,i)),coroot@(RootDatum,int)(rd,i)))


.. _coreflect_(RootDatum,vec,vec->vec):

\coreflect
----------------------------------------------

``coreflect: (RootDatum,vec,vec->vec)``
Function defined at basic.at:543:4--544:36
(rd,v,alpha): v:=-@(vec,vec)(v,*@(int,vec)(*@(vec,vec)(v,alpha),coroot@(RootDatum,vec)(rd,alpha)))


.. _coreflect_(RootDatum,ratvec,int->ratvec):

\coreflect
----------------------------------------------

``coreflect: (RootDatum,ratvec,int->ratvec)``
Function defined at basic.at:550:4--551:39
(rd,v,i):  let (n,d)=%@ratvec(v) in /@(vec,int)(coreflect@(RootDatum,vec,int)(rd,n,i),d)


.. _coreflect_(RootDatum,ratvec,vec->ratvec):

\coreflect
----------------------------------------------

``coreflect: (RootDatum,ratvec,vec->ratvec)``
Function defined at basic.at:552:4--553:43
(rd,v,alpha):  let (n,d)=%@ratvec(v) in /@(vec,int)(coreflect@(RootDatum,vec,vec)(rd,n,alpha),d)


.. _left_reflect_(RootDatum,int,mat->mat):

\left_reflect
----------------------------------------------

``left_reflect: (RootDatum,int,mat->mat)``
Function defined at basic.at:556:4--557:46
(rd,i,M): #@(int,[vec])(n_rows@mat(M), for v in M do reflect@(RootDatum,int,vec)(rd,i,v) od )


.. _left_reflect_(RootDatum,vec,mat->mat):

\left_reflect
----------------------------------------------

``left_reflect: (RootDatum,vec,mat->mat)``
Function defined at basic.at:558:4--559:41
(rd,alpha,M): left_reflect@(RootDatum,int,mat)(rd,root_index@(RootDatum,vec)(rd,alpha),M)


.. _right_reflect_(RootDatum,mat,int->mat):

\right_reflect
----------------------------------------------

``right_reflect: (RootDatum,mat,int->mat)``
Function defined at basic.at:560:4--561:56
(rd,M,i): ^@(int,[vec])(n_columns@mat(M), for row in ^@mat(M) do coreflect@(RootDatum,vec,int)(rd,row,i) od )


.. _right_reflect_(RootDatum,mat,vec->mat):

\right_reflect
----------------------------------------------

``right_reflect: (RootDatum,mat,vec->mat)``
Function defined at basic.at:562:4--563:42
(rd,M,alpha): right_reflect@(RootDatum,mat,int)(rd,M,root_index@(RootDatum,vec)(rd,alpha))


.. _conjugate_(RootDatum,int,mat->mat):

\conjugate
----------------------------------------------

``conjugate: (RootDatum,int,mat->mat)``
Function defined at basic.at:565:4--566:42
(rd,i,M): left_reflect@(RootDatum,int,mat)(rd,i,right_reflect@(RootDatum,mat,int)(rd,M,i))


.. _conjugate_(RootDatum,vec,mat->mat):

\conjugate
----------------------------------------------

``conjugate: (RootDatum,vec,mat->mat)``
Function defined at basic.at:567:4--568:38
(rd,alpha,M): conjugate@(RootDatum,int,mat)(rd,root_index@(RootDatum,vec)(rd,alpha),M)


.. _singular_simple_indices_(RootDatum,ratvec->[int]):

\singular_simple_indices
----------------------------------------------

``singular_simple_indices: (RootDatum,ratvec->[int])``
Function defined at basic.at:571:4--573:69
(rd,v):  let rv=[] in voided: for a@j in simple_coroots@RootDatum(rd) do  if =@rat(*@(vec,ratvec)(a,v)) then rv:=#@([T],T)(rv,j) else () fi  od ;rv


.. _is_imaginary_(mat->(vec->bool)):

\is_imaginary
----------------------------------------------

``is_imaginary: (mat->(vec->bool))``
Function defined at basic.at:575:4-74
(theta): (alpha): =@(vec,vec)(*@(mat,vec)(theta,alpha),alpha)


.. _is_imaginary_(int,KGBElt->bool):

\is_imaginary
----------------------------------------------

``is_imaginary: (int,KGBElt->bool)``
Function defined at basic.at:796:4-48
(p): =@(int,int)(%@(int,int)(status@(int,KGBElt)(p),2),1)


.. _is_imaginary_(KGBElt->(vec->bool)):

\is_imaginary
----------------------------------------------

``is_imaginary: (KGBElt->(vec->bool))``
Function defined at basic.at:805:4-70
(x): is_imaginary@mat(involution@KGBElt(x))


.. _is_imaginary_(vec,KGBElt->bool):

\is_imaginary
----------------------------------------------

``is_imaginary: (vec,KGBElt->bool)``
Function defined at basic.at:863:4-60
(v,x): (is_imaginary@KGBElt(x))(v)


.. _is_real_(mat->(vec->bool)):

\is_real
----------------------------------------------

``is_real: (mat->(vec->bool))``
Function defined at basic.at:576:4-75
(theta): (alpha): =@(vec,vec)(*@(mat,vec)(theta,alpha),-@vec(alpha))


.. _is_real_(int,KGBElt->bool):

\is_real
----------------------------------------------

``is_real: (int,KGBElt->bool)``
Function defined at basic.at:795:4-41
(p): =@(int,int)(status@(int,KGBElt)(p),2)


.. _is_real_(KGBElt->(vec->bool)):

\is_real
----------------------------------------------

``is_real: (KGBElt->(vec->bool))``
Function defined at basic.at:806:4-65
(x): is_real@mat(involution@KGBElt(x))


.. _is_real_(vec,KGBElt->bool):

\is_real
----------------------------------------------

``is_real: (vec,KGBElt->bool)``
Function defined at basic.at:864:4-55
(v,x): (is_real@KGBElt(x))(v)


.. _is_complex_(mat->(vec->bool)):

\is_complex
----------------------------------------------

``is_complex: (mat->(vec->bool))``
Function defined at basic.at:577:4--578:50
(theta): (alpha):  let ta=*@(mat,vec)(theta,alpha) in  if !=@(vec,vec)(ta,alpha) then !=@(vec,vec)(ta,-@vec(alpha)) else false fi


.. _is_complex_(int,KGBElt->bool):

\is_complex
----------------------------------------------

``is_complex: (int,KGBElt->bool)``
Function defined at basic.at:794:4-46
(p): =@(int,int)(%@(int,int)(status@(int,KGBElt)(p),4),0)


.. _is_complex_(KGBElt->(vec->bool)):

\is_complex
----------------------------------------------

``is_complex: (KGBElt->(vec->bool))``
Function defined at basic.at:807:4-68
(x): is_complex@mat(involution@KGBElt(x))


.. _is_complex_(vec,KGBElt->bool):

\is_complex
----------------------------------------------

``is_complex: (vec,KGBElt->bool)``
Function defined at basic.at:865:4-58
(v,x): (is_complex@KGBElt(x))(v)


.. _imaginary_roots_(RootDatum,mat->mat):

\imaginary_roots
----------------------------------------------

``imaginary_roots: (RootDatum,mat->mat)``
Function defined at basic.at:581:4--582:45
(rd,theta): columns_with@((vec->bool),mat)(is_imaginary@mat(theta),roots@RootDatum(rd))


.. _real_roots_(RootDatum,mat->mat):

\real_roots
----------------------------------------------

``real_roots: (RootDatum,mat->mat)``
Function defined at basic.at:583:4--584:40
(rd,theta): columns_with@((vec->bool),mat)(is_real@mat(theta),roots@RootDatum(rd))


.. _imaginary_coroots_(RootDatum,mat->mat):

\imaginary_coroots
----------------------------------------------

``imaginary_coroots: (RootDatum,mat->mat)``
Function defined at basic.at:587:4--588:48
(rd,theta): columns_with@((vec->bool),mat)(is_imaginary@mat(^@mat(theta)),coroots@RootDatum(rd))


.. _real_coroots_(RootDatum,mat->mat):

\real_coroots
----------------------------------------------

``real_coroots: (RootDatum,mat->mat)``
Function defined at basic.at:589:4--590:43
(rd,theta): columns_with@((vec->bool),mat)(is_real@mat(^@mat(theta)),coroots@RootDatum(rd))


.. _imaginary_posroots_(RootDatum,mat->mat):

\imaginary_posroots
----------------------------------------------

``imaginary_posroots: (RootDatum,mat->mat)``
Function defined at basic.at:593:4--594:48
(rd,theta): columns_with@((vec->bool),mat)(is_imaginary@mat(theta),posroots@RootDatum(rd))


.. _imaginary_posroots_(KGBElt->mat):

\imaginary_posroots
----------------------------------------------

``imaginary_posroots: (KGBElt->mat)``
Function defined at basic.at:810:4--811:49
(x): imaginary_posroots@(RootDatum,mat)(root_datum@KGBElt(x),involution@KGBElt(x))


.. _real_posroots_(RootDatum,mat->mat):

\real_posroots
----------------------------------------------

``real_posroots: (RootDatum,mat->mat)``
Function defined at basic.at:595:4--596:43
(rd,theta): columns_with@((vec->bool),mat)(is_real@mat(theta),posroots@RootDatum(rd))


.. _real_posroots_(KGBElt->mat):

\real_posroots
----------------------------------------------

``real_posroots: (KGBElt->mat)``
Function defined at basic.at:812:4--813:44
(x): real_posroots@(RootDatum,mat)(root_datum@KGBElt(x),involution@KGBElt(x))


.. _imaginary_poscoroots_(RootDatum,mat->mat):

\imaginary_poscoroots
----------------------------------------------

``imaginary_poscoroots: (RootDatum,mat->mat)``
Function defined at basic.at:597:4--598:51
(rd,theta): columns_with@((vec->bool),mat)(is_imaginary@mat(^@mat(theta)),poscoroots@RootDatum(rd))


.. _imaginary_poscoroots_(KGBElt->mat):

\imaginary_poscoroots
----------------------------------------------

``imaginary_poscoroots: (KGBElt->mat)``
Function defined at basic.at:814:4--815:51
(x): imaginary_poscoroots@(RootDatum,mat)(root_datum@KGBElt(x),involution@KGBElt(x))


.. _real_poscoroots_(RootDatum,mat->mat):

\real_poscoroots
----------------------------------------------

``real_poscoroots: (RootDatum,mat->mat)``
Function defined at basic.at:599:4--600:46
(rd,theta): columns_with@((vec->bool),mat)(is_real@mat(^@mat(theta)),poscoroots@RootDatum(rd))


.. _real_poscoroots_(KGBElt->mat):

\real_poscoroots
----------------------------------------------

``real_poscoroots: (KGBElt->mat)``
Function defined at basic.at:816:4--817:46
(x): real_poscoroots@(RootDatum,mat)(root_datum@KGBElt(x),involution@KGBElt(x))


.. _imaginary_sys_(RootDatum,mat->mat,mat):

\imaginary_sys
----------------------------------------------

``imaginary_sys: (RootDatum,mat->mat,mat)``
Function defined at basic.at:601:4--602:49
(p): (imaginary_posroots@(RootDatum,mat)(p),imaginary_poscoroots@(RootDatum,mat)(p))


.. _imaginary_sys_(KGBElt->mat,mat):

\imaginary_sys
----------------------------------------------

``imaginary_sys: (KGBElt->mat,mat)``
Function defined at basic.at:818:4--820:52
(x):  let p=(root_datum@KGBElt(x),involution@KGBElt(x)) in (imaginary_posroots@(RootDatum,mat)(p),imaginary_poscoroots@(RootDatum,mat)(p))


.. _real_sys_(RootDatum,mat->mat,mat):

\real_sys
----------------------------------------------

``real_sys: (RootDatum,mat->mat,mat)``
Function defined at basic.at:603:4--604:39
(p): (real_posroots@(RootDatum,mat)(p),real_poscoroots@(RootDatum,mat)(p))


.. _real_sys_(KGBElt->mat,mat):

\real_sys
----------------------------------------------

``real_sys: (KGBElt->mat,mat)``
Function defined at basic.at:821:4--823:42
(x):  let p=(root_datum@KGBElt(x),involution@KGBElt(x)) in (real_posroots@(RootDatum,mat)(p),real_poscoroots@(RootDatum,mat)(p))


.. _is_dominant_(RootDatum,ratvec->bool):

\is_dominant
----------------------------------------------

``is_dominant: (RootDatum,ratvec->bool)``
Function defined at basic.at:607:4--608:33
(rd,v): >=@vec(*@(vec,mat)(numer@ratvec(v),simple_coroots@RootDatum(rd)))


.. _is_strictly_dominant_(RootDatum,ratvec->bool):

\is_strictly_dominant
----------------------------------------------

``is_strictly_dominant: (RootDatum,ratvec->bool)``
Function defined at basic.at:609:4--610:32
(rd,v): >@vec(*@(vec,mat)(numer@ratvec(v),simple_coroots@RootDatum(rd)))


.. _is_regular_(RootDatum,ratvec->bool):

\is_regular
----------------------------------------------

``is_regular: (RootDatum,ratvec->bool)``
Function defined at basic.at:611:4--612:49
(rd,v): all@[bool]( for x in *@(vec,mat)(numer@ratvec(v),poscoroots@RootDatum(rd)) do !=@int(x) od )


.. _is_regular_(Param->bool):

\is_regular
----------------------------------------------

``is_regular: (Param->bool)``
Function defined at basic.at:928:4--929:54
(p): is_regular@(RootDatum,ratvec)(root_datum@Param(p),infinitesimal_character@Param(p))


.. _is_integral_(RootDatum,ratvec->bool):

\is_integral
----------------------------------------------

``is_integral: (RootDatum,ratvec->bool)``
Function defined at basic.at:613:4--614:27
(rd,v): =@ratvec(%@(ratvec,int)(*@(ratvec,mat)(v,simple_coroots@RootDatum(rd)),1))


.. _radical_basis_(RootDatum->mat):

\radical_basis
----------------------------------------------

``radical_basis: (RootDatum->mat)``
Function defined at basic.at:617:4--618:44
(rd): matrix slicer@(int,mat,int,int,int,int)(36,coroot_radical@RootDatum(rd),0,0,semisimple_rank@RootDatum(rd),0)


.. _coradical_basis_(RootDatum->mat):

\coradical_basis
----------------------------------------------

``coradical_basis: (RootDatum->mat)``
Function defined at basic.at:619:4--620:44
(rd): matrix slicer@(int,mat,int,int,int,int)(36,root_coradical@RootDatum(rd),0,0,semisimple_rank@RootDatum(rd),0)


.. _is_semisimple_(RootDatum->bool):

\is_semisimple
----------------------------------------------

``is_semisimple: (RootDatum->bool)``
Function defined at basic.at:622:4-71
(rd): =@(int,int)(semisimple_rank@RootDatum(rd),rank@RootDatum(rd))


.. _derived_is_simply_connected_(RootDatum->bool):

\derived_is_simply_connected
----------------------------------------------

``derived_is_simply_connected: (RootDatum->bool)``
Function defined at basic.at:624:4--625:36
(rd): saturated_span@mat(simple_coroots@RootDatum(rd))


.. _has_connected_center_(RootDatum->bool):

\has_connected_center
----------------------------------------------

``has_connected_center: (RootDatum->bool)``
Function defined at basic.at:626:4--627:34
(rd): saturated_span@mat(simple_roots@RootDatum(rd))


.. _is_simply_connected_(RootDatum->bool):

\is_simply_connected
----------------------------------------------

``is_simply_connected: (RootDatum->bool)``
Function defined at basic.at:628:4--629:55
(rd):  if is_semisimple@RootDatum(rd) then derived_is_simply_connected@RootDatum(rd) else false fi


.. _is_adjoint_(RootDatum->bool):

\is_adjoint
----------------------------------------------

``is_adjoint: (RootDatum->bool)``
Function defined at basic.at:630:4--631:48
(rd):  if is_semisimple@RootDatum(rd) then has_connected_center@RootDatum(rd) else false fi


.. _derived_(RootDatum->RootDatum):

\derived
----------------------------------------------

``derived: (RootDatum->RootDatum)``
Function defined at basic.at:636:4-70
(rd):  let (d,)=derived_info@RootDatum(rd) in d


.. _mod_central_torus_(RootDatum->RootDatum):

\mod_central_torus
----------------------------------------------

``mod_central_torus: (RootDatum->RootDatum)``
Function defined at basic.at:637:4--638:42
(rd):  let (d,)=mod_central_torus_info@RootDatum(rd) in d


.. _is_simple_for_(vec->(vec->bool)):

\is_simple_for
----------------------------------------------

``is_simple_for: (vec->(vec->bool))``
Function defined at basic.at:643:4--644:35
(dual_two_rho): (alpha): =@(int,int)(*@(vec,vec)(dual_two_rho,alpha),2)


.. _simple_from_positive_(mat,mat->mat,mat):

\simple_from_positive
----------------------------------------------

``simple_from_positive: (mat,mat->mat,mat)``
Function defined at basic.at:647:4--650:3
(posroots,poscoroots): (columns_with@((vec->bool),mat)(is_simple_for@vec(sum@mat(poscoroots)),posroots),columns_with@((vec->bool),mat)(is_simple_for@vec(sum@mat(posroots)),poscoroots))


.. _fundamental_weights_(RootDatum->[ratvec]):

\fundamental_weights
----------------------------------------------

``fundamental_weights: (RootDatum->[ratvec])``
Function defined at basic.at:652:4--653:58
(rd):  for i: semisimple_rank@RootDatum(rd) do fundamental_weight@(RootDatum,int)(rd,i) od


.. _fundamental_coweights_(RootDatum->[ratvec]):

\fundamental_coweights
----------------------------------------------

``fundamental_coweights: (RootDatum->[ratvec])``
Function defined at basic.at:654:4--655:60
(rd):  for i: semisimple_rank@RootDatum(rd) do fundamental_coweight@(RootDatum,int)(rd,i) od


.. _dual_integral_(InnerClass,ratvec->InnerClass):

\dual_integral
----------------------------------------------

``dual_integral: (InnerClass,ratvec->InnerClass)``
Function defined at basic.at:664:4--665:79
(ic,gamma): inner_class@(RootDatum,mat)(dual@RootDatum(integrality_datum@(RootDatum,ratvec)(RdIc:ic,gamma)),-@mat(^@mat(distinguished_involution@InnerClass(ic))))


.. _Cartan_classes_(InnerClass->[CartanClass]):

\Cartan_classes
----------------------------------------------

``Cartan_classes: (InnerClass->[CartanClass])``
Function defined at basic.at:670:4--671:57
(ic):  for i: nr_of_Cartan_classes@InnerClass(ic) do Cartan_class@(InnerClass,int)(ic,i) od


.. _print_Cartan_info_(CartanClass->):

\print_Cartan_info
----------------------------------------------

``print_Cartan_info: (CartanClass->)``
Function defined at basic.at:673:4--690:5
(cc):  let (show,((cr,Cr,sr),ww,(orbit_size,fiber_size),(i_tp,r_tp,C_tp)))=((s):  if =@(string,string)(s,"") then "empty" else s fi ,Cartan_info@CartanClass(cc)) in prints@(string,int,string,int,string,int)("compact: ",cr,", complex: ",Cr,", split: ",sr); let str="canonical twisted involution: " in  if =@int(#@vec(ww)) then str:=+@(string,string)(str,"e") else voided: for s@i in ww do  if =@int(i) then str:=+@(string,int)(str,+@(int,int)(s,1)) else str:=+@(string,string)(str,+@(string,int)(",",+@(int,int)(s,1))) fi  od  fi ;prints@string(str);prints@(string,int,string,int,string,int)("twisted involution orbit size: ",orbit_size,"; fiber size: ",fiber_size,"; strong inv: ",*@(int,int)(orbit_size,fiber_size));prints@(string,string)("imaginary root system: ",show(str@LieType(i_tp)));prints@(string,string)("real root system: ",show(str@LieType(r_tp)));prints@(string,string)("complex factor: ",show(str@LieType(C_tp)))


.. _fundamental_Cartan_(InnerClass->CartanClass):

\fundamental_Cartan
----------------------------------------------

``fundamental_Cartan: (InnerClass->CartanClass)``
Function defined at basic.at:693:4-72
(ic): Cartan_class@(InnerClass,int)(ic,0)


.. _compact_rank_(CartanClass->int):

\compact_rank
----------------------------------------------

``compact_rank: (CartanClass->int)``
Function defined at basic.at:700:4--701:42
(cc):  let ((c,C,),,,)=Cartan_info@CartanClass(cc) in +@(int,int)(c,C)


.. _compact_rank_(InnerClass->int):

\compact_rank
----------------------------------------------

``compact_rank: (InnerClass->int)``
Function defined at basic.at:705:4-74
(G): compact_rank@CartanClass(fundamental_Cartan@InnerClass(G))


.. _split_rank_(CartanClass->int):

\split_rank
----------------------------------------------

``split_rank: (CartanClass->int)``
Function defined at basic.at:702:4--703:42
(cc):  let ((,C,s),,,)=Cartan_info@CartanClass(cc) in +@(int,int)(C,s)


.. _split_rank_(RealForm->int):

\split_rank
----------------------------------------------

``split_rank: (RealForm->int)``
Function defined at basic.at:706:4-71
(G): split_rank@CartanClass(most_split_Cartan@RealForm(G))


.. _number_(CartanClass,RealForm->int):

\number
----------------------------------------------

``number: (CartanClass,RealForm->int)``
Function defined at basic.at:714:4--715:65
(H,G): last@(int,(int->bool))(nr_of_Cartan_classes@InnerClass(IcRf:G),(i): =@(CartanClass,CartanClass)(Cartan_class@(RealForm,int)(G,i),H))


.. _form_name_(RealForm->string):

\form_name
----------------------------------------------

``form_name: (RealForm->string)``
Function defined at basic.at:721:4-66
(f): form_names@InnerClass(IcRf:f)[form_number@RealForm(f)]


.. _is_quasisplit_(RealForm->bool):

\is_quasisplit
----------------------------------------------

``is_quasisplit: (RealForm->bool)``
Function defined at basic.at:728:4-75
(G): =@(int,int)(form_number@RealForm(G),-@(int,int)(nr_of_real_forms@InnerClass(IcRf:G),1))


.. _is_quasicompact_(RealForm->bool):

\is_quasicompact
----------------------------------------------

``is_quasicompact: (RealForm->bool)``
Function defined at basic.at:729:4-57
(G): =@(int,int)(form_number@RealForm(G),0)


.. _split_form_(RootDatum->RealForm):

\split_form
----------------------------------------------

``split_form: (RootDatum->RealForm)``
Function defined at basic.at:731:4--732:50
(r): quasisplit_form@InnerClass(inner_class@(RootDatum,mat)(r,-@mat(id_mat@int(rank@RootDatum(r)))))


.. _split_form_(LieType->RealForm):

\split_form
----------------------------------------------

``split_form: (LieType->RealForm)``
Function defined at basic.at:735:4-70
(t): split_form@RootDatum(simply_connected@LieType(t))


.. _quasicompact_form_(InnerClass->RealForm):

\quasicompact_form
----------------------------------------------

``quasicompact_form: (InnerClass->RealForm)``
Function defined at basic.at:737:4-65
(ic): real_form@(InnerClass,int)(ic,0)


.. _is_compatible_(RealForm,RealForm->bool):

\is_compatible
----------------------------------------------

``is_compatible: (RealForm,RealForm->bool)``
Function defined at basic.at:740:4--743:68
(f,g):  let ic=inner_class@RealForm(f) in  let oc=*@(mat,mat)(occurrence_matrix@InnerClass(ic),^@mat(dual_occurrence_matrix@InnerClass(ic))) in  if =@(InnerClass,InnerClass)(inner_class@RealForm(g),dual@InnerClass(ic)) then >@(int,int)(oc[form_number@RealForm(f),form_number@RealForm(g)],0) else false fi


.. _is_compact_(RealForm->bool):

\is_compact
----------------------------------------------

``is_compact: (RealForm->bool)``
Function defined at basic.at:745:4--746:49
(G):  if =@(int,int)(KGB_size@RealForm(G),1) then =@(mat,int)(distinguished_involution@InnerClass(IcRf:G),1) else false fi


.. _is_compact_(int,KGBElt->bool):

\is_compact
----------------------------------------------

``is_compact: (int,KGBElt->bool)``
Function defined at basic.at:798:4-44
(p): =@(int,int)(status@(int,KGBElt)(p),1)


.. _is_compact_(KGBElt->(vec->bool)):

\is_compact
----------------------------------------------

``is_compact: (KGBElt->(vec->bool))``
Function defined at basic.at:840:4--842:64
(x):  let (coweight,is_im)=(+@(ratvec,ratvec)(rho_check_i@KGBElt(x),torus_factor@KGBElt(x)),is_imaginary@KGBElt(x)) in (alpha): assert@bool(is_im(alpha));=@rat(%@(rat,int)(*@(ratvec,ratvec)(coweight,QvV:alpha),2))


.. _KGB_status_text_(int->string):

\KGB_status_text
----------------------------------------------

``KGB_status_text: (int->string)``
Function defined at basic.at:787:4-67
(i): ["C-","ic","r ","nc","C+"][i]


.. _status_text_(int,KGBElt->string):

\status_text
----------------------------------------------

``status_text: (int,KGBElt->string)``
Function defined at basic.at:789:4-68
(p): KGB_status_text@int(status@(int,KGBElt)(p))


.. _status_text_(vec,KGBElt->string):

\status_text
----------------------------------------------

``status_text: (vec,KGBElt->string)``
Function defined at basic.at:790:4-68
(p): KGB_status_text@int(status@(vec,KGBElt)(p))


.. _status_text_(int,Param->string):

\status_text
----------------------------------------------

``status_text: (int,Param->string)``
Function defined at basic.at:988:4-72
(s,p): block_status_text@int(status@(int,Param)(s,p))


.. _status_text_(vec,Param->string):

\status_text
----------------------------------------------

``status_text: (vec,Param->string)``
Function defined at basic.at:992:4-72
(ap): block_status_text@int(status@(vec,Param)(ap))


.. _status_texts_(KGBElt->[string]):

\status_texts
----------------------------------------------

``status_texts: (KGBElt->[string])``
Function defined at basic.at:791:4--792:60
(x):  for s: semisimple_rank@RootDatum(RdRf:real_form@KGBElt(x)) do status_text@(int,KGBElt)(s,x) od


.. _status_texts_(Param->[string]):

\status_texts
----------------------------------------------

``status_texts: (Param->[string])``
Function defined at basic.at:989:4--990:60
(p):  for s: semisimple_rank@RootDatum(RdRf:real_form@Param(p)) do status_text@(int,Param)(s,p) od


.. _is_noncompact_(int,KGBElt->bool):

\is_noncompact
----------------------------------------------

``is_noncompact: (int,KGBElt->bool)``
Function defined at basic.at:797:4-47
(p): =@(int,int)(status@(int,KGBElt)(p),3)


.. _is_noncompact_(KGBElt->(vec->bool)):

\is_noncompact
----------------------------------------------

``is_noncompact: (KGBElt->(vec->bool))``
Function defined at basic.at:843:4--845:65
(x):  let (coweight,is_im)=(+@(ratvec,ratvec)(rho_check_i@KGBElt(x),torus_factor@KGBElt(x)),is_imaginary@KGBElt(x)) in (alpha): assert@bool(is_im(alpha));!=@rat(%@(rat,int)(*@(ratvec,ratvec)(coweight,QvV:alpha),2))


.. _is_descent_(int,KGBElt->bool):

\is_descent
----------------------------------------------

``is_descent: (int,KGBElt->bool)``
Function defined at basic.at:799:4-44
(p): <@(int,int)(status@(int,KGBElt)(p),3)


.. _is_descent_(int,Param->bool):

\is_descent
----------------------------------------------

``is_descent: (int,Param->bool)``
Function defined at basic.at:1001:4-52
(s,p): <@(int,int)(status@(int,Param)(s,p),4)


.. _is_descent_(vec,Param->bool):

\is_descent
----------------------------------------------

``is_descent: (vec,Param->bool)``
Function defined at basic.at:1008:4-52
(ap): <@(int,int)(status@(vec,Param)(ap),4)


.. _is_ascent_(int,KGBElt->bool):

\is_ascent
----------------------------------------------

``is_ascent: (int,KGBElt->bool)``
Function defined at basic.at:800:4-44
(p): >=@(int,int)(status@(int,KGBElt)(p),3)


.. _is_strict_descent_(int,KGBElt->bool):

\is_strict_descent
----------------------------------------------

``is_strict_descent: (int,KGBElt->bool)``
Function defined at basic.at:801:4-75
(p):  if is_descent@(int,KGBElt)(p) then not@bool(is_compact@(int,KGBElt)(p)) else false fi


.. _rho_i_(KGBElt->ratvec):

\rho_i
----------------------------------------------

``rho_i: (KGBElt->ratvec)``
Function defined at basic.at:825:4-59
(x): /@(vec,int)(sum@mat(imaginary_posroots@KGBElt(x)),2)


.. _rho_i_(RootDatum,mat->ratvec):

\rho_i
----------------------------------------------

``rho_i: (RootDatum,mat->ratvec)``
Function defined at basic.at:830:4--831:37
(rd_theta): /@(vec,int)(sum@mat(imaginary_posroots@(RootDatum,mat)(rd_theta)),2)


.. _rho_r_(KGBElt->ratvec):

\rho_r
----------------------------------------------

``rho_r: (KGBElt->ratvec)``
Function defined at basic.at:826:4-54
(x): /@(vec,int)(sum@mat(real_posroots@KGBElt(x)),2)


.. _rho_r_(RootDatum,mat->ratvec):

\rho_r
----------------------------------------------

``rho_r: (RootDatum,mat->ratvec)``
Function defined at basic.at:832:4--833:32
(rd_theta): /@(vec,int)(sum@mat(real_posroots@(RootDatum,mat)(rd_theta)),2)


.. _rho_check_i_(KGBElt->ratvec):

\rho_check_i
----------------------------------------------

``rho_check_i: (KGBElt->ratvec)``
Function defined at basic.at:827:4-67
(x): /@(vec,int)(sum@mat(imaginary_poscoroots@KGBElt(x)),2)


.. _rho_check_i_(RootDatum,mat->ratvec):

\rho_check_i
----------------------------------------------

``rho_check_i: (RootDatum,mat->ratvec)``
Function defined at basic.at:834:4--835:39
(rd_theta): /@(vec,int)(sum@mat(imaginary_poscoroots@(RootDatum,mat)(rd_theta)),2)


.. _rho_check_r_(KGBElt->ratvec):

\rho_check_r
----------------------------------------------

``rho_check_r: (KGBElt->ratvec)``
Function defined at basic.at:828:4-62
(x): /@(vec,int)(sum@mat(real_poscoroots@KGBElt(x)),2)


.. _rho_check_r_(RootDatum,mat->ratvec):

\rho_check_r
----------------------------------------------

``rho_check_r: (RootDatum,mat->ratvec)``
Function defined at basic.at:836:4--837:34
(rd_theta): /@(vec,int)(sum@mat(real_poscoroots@(RootDatum,mat)(rd_theta)),2)


.. _is_compact_imaginary_(KGBElt->(vec->bool)):

\is_compact_imaginary
----------------------------------------------

``is_compact_imaginary: (KGBElt->(vec->bool))``
Function defined at basic.at:848:4--850:44
(x):  let (p,q)=(is_imaginary@KGBElt(x),is_compact@KGBElt(x)) in (alpha):  if p(alpha) then q(alpha) else false fi


.. _is_compact_imaginary_(vec,KGBElt->bool):

\is_compact_imaginary
----------------------------------------------

``is_compact_imaginary: (vec,KGBElt->bool)``
Function defined at basic.at:866:4-76
(v,x): (is_compact_imaginary@KGBElt(x))(v)


.. _is_noncompact_imaginary_(KGBElt->(vec->bool)):

\is_noncompact_imaginary
----------------------------------------------

``is_noncompact_imaginary: (KGBElt->(vec->bool))``
Function defined at basic.at:851:4--853:44
(x):  let (p,q)=(is_imaginary@KGBElt(x),is_noncompact@KGBElt(x)) in (alpha):  if p(alpha) then q(alpha) else false fi


.. _is_noncompact_imaginary_(vec,KGBElt->bool):

\is_noncompact_imaginary
----------------------------------------------

``is_noncompact_imaginary: (vec,KGBElt->bool)``
Function defined at basic.at:867:4--868:31
(v,x): (is_noncompact_imaginary@KGBElt(x))(v)


.. _compact_posroots_(KGBElt->mat):

\compact_posroots
----------------------------------------------

``compact_posroots: (KGBElt->mat)``
Function defined at basic.at:855:4--856:51
(x): columns_with@((vec->bool),mat)(is_compact@KGBElt(x),imaginary_posroots@KGBElt(x))


.. _noncompact_posroots_(KGBElt->mat):

\noncompact_posroots
----------------------------------------------

``noncompact_posroots: (KGBElt->mat)``
Function defined at basic.at:857:4--858:54
(x): columns_with@((vec->bool),mat)(is_noncompact@KGBElt(x),imaginary_posroots@KGBElt(x))


.. _rho_ci_(KGBElt->ratvec):

\rho_ci
----------------------------------------------

``rho_ci: (KGBElt->ratvec)``
Function defined at basic.at:860:4-59
(x): /@(vec,int)(sum@mat(compact_posroots@KGBElt(x)),2)


.. _rho_nci_(KGBElt->ratvec):

\rho_nci
----------------------------------------------

``rho_nci: (KGBElt->ratvec)``
Function defined at basic.at:861:4-62
(x): /@(vec,int)(sum@mat(noncompact_posroots@KGBElt(x)),2)


.. _no_Cminus_roots_(KGBElt->bool):

\no_Cminus_roots
----------------------------------------------

``no_Cminus_roots: (KGBElt->bool)``
Function defined at basic.at:874:4--875:64
(x): none@(int,(int->bool))(semisimple_rank@RootDatum(RdRf:real_form@KGBElt(x)),(i): =@int(status@(int,KGBElt)(i,x)))


.. _no_Cplus_roots_(KGBElt->bool):

\no_Cplus_roots
----------------------------------------------

``no_Cplus_roots: (KGBElt->bool)``
Function defined at basic.at:876:4--877:65
(x): none@(int,(int->bool))(semisimple_rank@RootDatum(RdRf:real_form@KGBElt(x)),(i): =@(int,int)(status@(int,KGBElt)(i,x),4))


.. _blocks_(InnerClass->[Block]):

\blocks
----------------------------------------------

``blocks: (InnerClass->[Block])``
Function defined at basic.at:881:4--887:12
(ic):  let result=[] in voided: for rf in real_forms@InnerClass(ic) do voided: for drf in dual_real_forms@InnerClass(ic) do  if is_compatible@(RealForm,RealForm)(rf,drf) then result:=#@([T],T)(result,block@(RealForm,RealForm)(rf,drf)) else () fi  od  od ;result


.. _lambda_minus_rho_(Param->vec):

\lambda_minus_rho
----------------------------------------------

``lambda_minus_rho: (Param->vec)``
Function defined at basic.at:917:4-74
(p):  let (,lambda_rho,)=%@Param(p) in lambda_rho


.. _lambda_(Param->ratvec):

\lambda
----------------------------------------------

``lambda: (Param->ratvec)``
Function defined at basic.at:918:4-68
(p): +@(ratvec,ratvec)(QvV:lambda_minus_rho@Param(p),rho@RootDatum(RdRf:real_form@Param(p)))


.. _infinitesimal_character_(Param->ratvec):

\infinitesimal_character
----------------------------------------------

``infinitesimal_character: (Param->ratvec)``
Function defined at basic.at:919:4-74
(p):  let (,,gamma)=%@Param(p) in gamma


.. _infinitesimal_character_(ParamPol->ratvec):

\infinitesimal_character
----------------------------------------------

``infinitesimal_character: (ParamPol->ratvec)``
Function defined at basic.at:1046:4--1052:11
(P): assert@(bool,string)(!=@ParamPol(P),"empty polynomial has no infinitesimal character"); let (,,gamma)=%@Param(first_param@ParamPol(P)) in voided: for @p in P do assert@(bool,string)(=@(ratvec,ratvec)(infinitesimal_character@Param(p),gamma),"infinitesimal character not unique") od ;gamma


.. _nu_(Param->ratvec):

\nu
----------------------------------------------

``nu: (Param->ratvec)``
Function defined at basic.at:920:4-74
(p):  let (x,,gamma)=%@Param(p) in /@(ratvec,int)(*@(mat,ratvec)(-@(int,mat)(1,involution@KGBElt(x)),gamma),2)


.. _trivial_(RealForm->Param):

\trivial
----------------------------------------------

``trivial: (RealForm->Param)``
Function defined at basic.at:931:4--932:50
(G): param@(KGBElt,vec,ratvec)(KGB@(RealForm,int)(G,-@(int,int)(KGB_size@RealForm(G),1)),null@int(rank@RootDatum(RdRf:G)),rho@RootDatum(RdRf:G))


.. _parameter_(RealForm,int,ratvec,ratvec->Param):

\parameter
----------------------------------------------

``parameter: (RealForm,int,ratvec,ratvec->Param)``
Function defined at basic.at:937:4--938:49
(G,x,lambda,nu): param@(KGBElt,vec,ratvec)(KGB@(RealForm,int)(G,x),ratvec_as_vec@ratvec(-@(ratvec,ratvec)(lambda,rho@RootDatum(RdRf:G))),nu)


.. _parameter_(KGBElt,ratvec,ratvec->Param):

\parameter
----------------------------------------------

``parameter: (KGBElt,ratvec,ratvec->Param)``
Function defined at basic.at:939:4--940:53
(x,lambda,nu): param@(KGBElt,vec,ratvec)(x,ratvec_as_vec@ratvec(-@(ratvec,ratvec)(lambda,rho@RootDatum(RdRf:real_form@KGBElt(x)))),nu)


.. _parameter_gamma_(KGBElt,ratvec,ratvec->Param):

\parameter_gamma
----------------------------------------------

``parameter_gamma: (KGBElt,ratvec,ratvec->Param)``
Function defined at basic.at:943:4--946:57
(x,lambda,gamma):  let ((G,nx),theta)=(%@KGBElt(x),involution@KGBElt(x)) in parameter@(RealForm,int,ratvec,ratvec)(G,nx,+@(ratvec,ratvec)(/@(ratvec,int)(*@(mat,ratvec)(+@(int,mat)(1,theta),-@(ratvec,ratvec)(gamma,lambda)),2),lambda),gamma)


.. _block_of_(Param->[Param]):

\block_of
----------------------------------------------

``block_of: (Param->[Param])``
Function defined at basic.at:949:4-66
(p):  let (params,)=block@Param(p) in params


.. _imaginary_type_(int,Param->int):

\imaginary_type
----------------------------------------------

``imaginary_type: (int,Param->int)``
Function defined at basic.at:953:4-75
(s,p):  if =@(Param,Param)(cross@(int,Param)(s,p),p) then 2 else 1 fi


.. _imaginary_type_(vec,Param->int):

\imaginary_type
----------------------------------------------

``imaginary_type: (vec,Param->int)``
Function defined at basic.at:956:4--957:38
(alpha,p):  if =@(Param,Param)(cross@(vec,Param)(alpha,p),p) then 2 else 1 fi


.. _real_type_(int,Param->int):

\real_type
----------------------------------------------

``real_type: (int,Param->int)``
Function defined at basic.at:954:4-69
(s,p):  if =@(Param,Param)(cross@(int,Param)(s,p),p) then 1 else 2 fi


.. _real_type_(vec,Param->int):

\real_type
----------------------------------------------

``real_type: (vec,Param->int)``
Function defined at basic.at:958:4--959:38
(alpha,p):  if =@(Param,Param)(cross@(vec,Param)(alpha,p),p) then 1 else 2 fi


.. _is_nonparity_(int,Param->bool):

\is_nonparity
----------------------------------------------

``is_nonparity: (int,Param->bool)``
Function defined at basic.at:966:4-72
(s,p):  if is_real@(int,KGBElt)(s,x@Param(p)) then =@(Param,Param)(Cayley@(int,Param)(s,p),p) else false fi


.. _is_nonparity_(vec,Param->bool):

\is_nonparity
----------------------------------------------

``is_nonparity: (vec,Param->bool)``
Function defined at basic.at:969:4--970:43
(alpha,p):  if is_real@(vec,KGBElt)(alpha,x@Param(p)) then =@(Param,Param)(Cayley@(vec,Param)(alpha,p),p) else false fi


.. _is_parity_(int,Param->bool):

\is_parity
----------------------------------------------

``is_parity: (int,Param->bool)``
Function defined at basic.at:967:4-71
(s,p):  if is_real@(int,KGBElt)(s,x@Param(p)) then !=@(Param,Param)(Cayley@(int,Param)(s,p),p) else false fi


.. _is_parity_(vec,Param->bool):

\is_parity
----------------------------------------------

``is_parity: (vec,Param->bool)``
Function defined at basic.at:971:4--972:44
(alpha,p):  if is_real@(vec,KGBElt)(alpha,x@Param(p)) then !=@(Param,Param)(Cayley@(vec,Param)(alpha,p),p) else false fi


.. _block_status_text_(int->string):

\block_status_text
----------------------------------------------

``block_status_text: (int->string)``
Function defined at basic.at:985:4--986:56
(i):  case i in "C-", "ic", "r1", "r2", "C+", "rn", "i1", "i2" esac


.. _parity_poscoroots_(Param->mat):

\parity_poscoroots
----------------------------------------------

``parity_poscoroots: (Param->mat)``
Function defined at basic.at:994:4--996:64
(p):  let (alpha,real_poscoroots)=real_sys@KGBElt(x@Param(p)) in columns_with@((int->bool),mat)((i): !=@(int,int)(status@(vec,Param)(alpha[i],p),5),real_poscoroots)


.. _nonparity_poscoroots_(Param->mat):

\nonparity_poscoroots
----------------------------------------------

``nonparity_poscoroots: (Param->mat)``
Function defined at basic.at:997:4--999:63
(p):  let (alpha,real_poscoroots)=real_sys@KGBElt(x@Param(p)) in columns_with@((int->bool),mat)((i): =@(int,int)(status@(vec,Param)(alpha[i],p),5),real_poscoroots)


.. _tau_bitset_(Param->(int->bool),int):

\tau_bitset
----------------------------------------------

``tau_bitset: (Param->(int->bool),int)``
Function defined at basic.at:1002:4--1003:59
(p): ((s): is_descent@(int,Param)(s,p),semisimple_rank@RootDatum(RdRf:real_form@Param(p)))


.. _tau_(Param->[int]):

\tau
----------------------------------------------

``tau: (Param->[int])``
Function defined at basic.at:1005:4-57
(p): list@((int->bool),int)(tau_bitset@Param(p))


.. _tau_complement_(Param->[int]):

\tau_complement
----------------------------------------------

``tau_complement: (Param->[int])``
Function defined at basic.at:1006:4-63
(p): complement@((int->bool),int)(tau_bitset@Param(p))


.. _lookup_(Param,[Param]->int):

\lookup
----------------------------------------------

``lookup: (Param,[Param]->int)``
Function defined at basic.at:1010:4--1011:60
(p,block):  let i=-@(int,int)(#@[Param](block),1) in voided: while  if >=@int(i) then !=@(Param,Param)(block[i],p) else false fi  do i:=-@(int,int)(i,1) od ;i


.. _first_param_(ParamPol->Param):

\first_param
----------------------------------------------

``first_param: (ParamPol->Param)``
Function defined at basic.at:1020:4-65
(P):  let (,p)=first_term@ParamPol(P) in p


.. _last_param_(ParamPol->Param):

\last_param
----------------------------------------------

``last_param: (ParamPol->Param)``
Function defined at basic.at:1021:4-64
(P):  let (,p)=last_term@ParamPol(P) in p


.. _virtual_(Param->ParamPol):

\virtual
----------------------------------------------

``virtual: (Param->ParamPol)``
Function defined at basic.at:1035:4-35
(p): PolP:p


.. _virtual_(RealForm,[Param]->ParamPol):

\virtual
----------------------------------------------

``virtual: (RealForm,[Param]->ParamPol)``
Function defined at basic.at:1036:4--1037:65
(G,ps):  let one=Sp(I,I):(1,0) in +@(ParamPol,[(Split,Param)])(null_module@RealForm(G), for p in ps do (one,p) od )


.. _pol_format_(ParamPol->):

\pol_format
----------------------------------------------

``pol_format: (ParamPol->)``
Function defined at basic.at:1041:4--1043:74
(P): voided: for w@p in P do prints@(string,string,string,Param,string,ratvec)("(",split_format@Split(w),")*",p,", ",infinitesimal_character@Param(p)) od


.. _separate_by_infinitesimal_character_(ParamPol->[(ratvec,ParamPol)]):

\separate_by_infinitesimal_character
----------------------------------------------

``separate_by_infinitesimal_character: (ParamPol->[(ratvec,ParamPol)])``
Function defined at basic.at:1055:4--1063:38
(P):  let M=[] in  let insert=((,p):term):  let (inserted,gamma)=(false,infinitesimal_character@Param(p)) in voided: for (key,P)@i in M do  if =@(ratvec,ratvec)(key,gamma) then M[i]:=(key,+@(ParamPol,(Split,Param))(P,term));inserted:=true else () fi  od ; if inserted then () else M:=#@([T],T)(M,(gamma,PolP:p)) fi  in voided: for c@p in P do insert(c,p) od ;M


.. _in_string_list_(string,[string]->bool):

\in_string_list
----------------------------------------------

``in_string_list: (string,[string]->bool)``
Function defined at basic.at:1067:4--1068:54
(s,S):  let i=-@(int,int)(#@[string](S),1) in voided: while  if >=@int(i) then !=@(string,string)(S[i],s) else false fi  do i:=-@(int,int)(i,1) od ;>=@int(i)


.. _positive_imaginary_roots_and_coroots_(RootDatum,mat->mat,mat):

\positive_imaginary_roots_and_coroots
----------------------------------------------

``positive_imaginary_roots_and_coroots: (RootDatum,mat->mat,mat)``
Function defined at basic.at:601:4--602:49
(p): (imaginary_posroots@(RootDatum,mat)(p),imaginary_poscoroots@(RootDatum,mat)(p))


.. _positive_imaginary_roots_and_coroots_(KGBElt->mat,mat):

\positive_imaginary_roots_and_coroots
----------------------------------------------

``positive_imaginary_roots_and_coroots: (KGBElt->mat,mat)``
Function defined at basic.at:818:4--820:52
(x):  let p=(root_datum@KGBElt(x),involution@KGBElt(x)) in (imaginary_posroots@(RootDatum,mat)(p),imaginary_poscoroots@(RootDatum,mat)(p))


.. _imaginary_roots_and_coroots_(RootDatum,mat->mat,mat):

\imaginary_roots_and_coroots
----------------------------------------------

``imaginary_roots_and_coroots: (RootDatum,mat->mat,mat)``
Function defined at basic.at:1073:4--1074:78
(p):  let (a,b)=imaginary_sys@(RootDatum,mat)(p) in (##@(mat,mat)(negative_system@mat(a),a),##@(mat,mat)(negative_system@mat(b),b))


.. _imaginary_roots_and_coroots_(KGBElt->mat,mat):

\imaginary_roots_and_coroots
----------------------------------------------

``imaginary_roots_and_coroots: (KGBElt->mat,mat)``
Function defined at basic.at:1075:4--1076:70
(x): imaginary_roots_and_coroots@(RootDatum,mat)(root_datum@InnerClass(IcRf:real_form@KGBElt(x)),involution@KGBElt(x))


.. _positive_real_roots_and_coroots_(RootDatum,mat->mat,mat):

\positive_real_roots_and_coroots
----------------------------------------------

``positive_real_roots_and_coroots: (RootDatum,mat->mat,mat)``
Function defined at basic.at:603:4--604:39
(p): (real_posroots@(RootDatum,mat)(p),real_poscoroots@(RootDatum,mat)(p))


.. _positive_real_roots_and_coroots_(KGBElt->mat,mat):

\positive_real_roots_and_coroots
----------------------------------------------

``positive_real_roots_and_coroots: (KGBElt->mat,mat)``
Function defined at basic.at:821:4--823:42
(x):  let p=(root_datum@KGBElt(x),involution@KGBElt(x)) in (real_posroots@(RootDatum,mat)(p),real_poscoroots@(RootDatum,mat)(p))


.. _real_roots_and_coroots_(RootDatum,mat->mat,mat):

\real_roots_and_coroots
----------------------------------------------

``real_roots_and_coroots: (RootDatum,mat->mat,mat)``
Function defined at basic.at:1081:4--1082:73
(p):  let (a,b)=real_sys@(RootDatum,mat)(p) in (##@(mat,mat)(negative_system@mat(a),a),##@(mat,mat)(negative_system@mat(b),b))


.. _real_roots_and_coroots_(KGBElt->mat,mat):

\real_roots_and_coroots
----------------------------------------------

``real_roots_and_coroots: (KGBElt->mat,mat)``
Function defined at basic.at:1083:4--1084:65
(x): real_roots_and_coroots@(RootDatum,mat)(root_datum@InnerClass(IcRf:real_form@KGBElt(x)),involution@KGBElt(x))


.. _complex_posroots_(RootDatum,mat->mat):

\complex_posroots
----------------------------------------------

``complex_posroots: (RootDatum,mat->mat)``
Function defined at basic.at:1086:4--1087:46
(rd,theta): columns_with@((vec->bool),mat)(is_complex@mat(theta),posroots@RootDatum(rd))


.. _complex_posroots_(KGBElt->mat):

\complex_posroots
----------------------------------------------

``complex_posroots: (KGBElt->mat)``
Function defined at basic.at:1088:4--1089:47
(x): complex_posroots@(RootDatum,mat)(root_datum@KGBElt(x),involution@KGBElt(x))


.. _monomials_(ParamPol->[Param]):

\monomials
----------------------------------------------

``monomials: (ParamPol->[Param])``
Function defined at basic.at:1095:4-58
(P):  for c@p in P do p od


.. _monomial_(ParamPol,int->Param):

\monomial
----------------------------------------------

``monomial: (ParamPol,int->Param)``
Function defined at basic.at:1096:4-57
(P,i): monomials@ParamPol(P)[i]


.. _delete_([int],int->[int]):

\delete
----------------------------------------------

``delete: ([int],int->[int])``
Function defined at basic.at:1099:4-58
(v,k): ##@([T],[T])(v[0:k],v[+@(int,int)(k,1):0~])


.. _delete_([vec],int->[vec]):

\delete
----------------------------------------------

``delete: ([vec],int->[vec])``
Function defined at basic.at:1100:4-58
(v,k): ##@([T],[T])(v[0:k],v[+@(int,int)(k,1):0~])


.. _delete_([ratvec],int->[ratvec]):

\delete
----------------------------------------------

``delete: ([ratvec],int->[ratvec])``
Function defined at basic.at:1101:4-58
(v,k): ##@([T],[T])(v[0:k],v[+@(int,int)(k,1):0~])


.. _delete_([[vec]],int->[[vec]]):

\delete
----------------------------------------------

``delete: ([[vec]],int->[[vec]])``
Function defined at basic.at:1103:4-58
(v,k): ##@([T],[T])(v[0:k],v[+@(int,int)(k,1):0~])


.. _delete_([[ratvec]],int->[[ratvec]]):

\delete
----------------------------------------------

``delete: ([[ratvec]],int->[[ratvec]])``
Function defined at basic.at:1102:4-58
(v,k): ##@([T],[T])(v[0:k],v[+@(int,int)(k,1):0~])


.. _delete_([ParamPol],int->[ParamPol]):

\delete
----------------------------------------------

``delete: ([ParamPol],int->[ParamPol])``
Function defined at basic.at:1104:4-58
(P,k): ##@([T],[T])(P[0:k],P[+@(int,int)(k,1):0~])


.. _find_([int],int->int):

\find
----------------------------------------------

``find: ([int],int->int)``
Function defined at basic.at:1110:4-63
(v,k): first@(int,(int->bool))(#@[int](v),(i): =@(int,int)(v[i],k))


.. _find_([Param],Param->int):

\find
----------------------------------------------

``find: ([Param],Param->int)``
Function defined at basic.at:1111:4-63
(P,p): first@(int,(int->bool))(#@[Param](P),(i): =@(Param,Param)(P[i],p))


.. _find_([KGBElt],KGBElt->int):

\find
----------------------------------------------

``find: ([KGBElt],KGBElt->int)``
Function defined at basic.at:1112:4-63
(S,x): first@(int,(int->bool))(#@[KGBElt](S),(i): =@(KGBElt,KGBElt)(S[i],x))


.. _find_([[int]],[int]->int):

\find
----------------------------------------------

``find: ([[int]],[int]->int)``
Function defined at basic.at:1115:4-61
(S,v): first@(int,(int->bool))(#@[[int]](S),(i): =@(vec,vec)(V[I]:S[i],V[I]:v))


.. _find_vec_([vec],vec->int):

\find_vec
----------------------------------------------

``find_vec: ([vec],vec->int)``
Function defined at basic.at:1118:4-60
(S,v): first@(int,(int->bool))(#@[vec](S),(i): =@(vec,vec)(S[i],v))


.. _pad_(string,int->string):

\pad
----------------------------------------------

``pad: (string,int->string)``
Function defined at basic.at:1121:4-84
(s,padding):  let rv=s in voided: for i: -@(int,int)(padding,#@string(s)) do rv:=+@(string,string)(rv," ") od ;rv


