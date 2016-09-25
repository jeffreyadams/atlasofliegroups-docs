Change of Coordinates 
======================

For this and following sessions you want to download the files ``basic.at``, ``groups.at`` and ``lietypes.at``.

To change atlas' coordinates for roots and other weights to your
prefered coordinate system you can also download the file ``coordinates.at`` (included in the all.at file) and do the following::


     atlas> set rd=simply_connected(C2)
     Identifier rd: RootDatum 
     atlas> simple_roots(rd) 
     Value: 
     | 2, -2 | 
     | -1, 2 | 
     
     atlas> set A=mat:[[1,-1],[0,2]] 
     Identifier A: mat atlas> A
     Value: 
     | 1, 0 | 
     | -1, 2 | 
     
     atlas> set C=change_basis_integral (rd,A) 
       Identifier C: mat (hiding previous one of type string (constant))
     atlas> C 
     Value: 
     | 1, 1 | 
     | 0, 1 | 
     
     atlas> set sr=simple_roots (rd) 
     Identifier sr: mat 
     atlas> sr 
     Value: 
     | 2, -2 | 
     |-1, 2 |
     
     atlas> C*sr 
     Value: 
     | 1, 0 | 
     | -1, 2 | 
     
     atlas> C*sr=A 
     Value:true 
     atlas> rho(rd) 
     Value: 
     [ 1, 1 ]/1 
       
     atlas> C*rho(rd) 
     Value: 
     [ 2, 1]/1 
     
     atlas> 

So, ``C`` is the change of basis matrix and you can change any vector
written in the original basis like ``rho``into one expressed in terms of the basis you want in the ususal way using the matrix ``C``.

Now, for this example this was not so necessary since we can use the real form expression of the group::

    atlas> simple_roots(Sp(4,R)) 
    Value: 
    | 1, 0 | 
    | -1, 2 | 
    atlas> 

However, this matrix is needed for example for G=SL(3,R). However, in this case we do not get integral matrices. So we need a more general command::
	 atlas> set G=SL(3,R) 
	 Identifier G: RealForm (hiding previous one of type RealForm)
	 atlas> sr:=simple_roots (G) 
	 Value: 
	 | 1, 1 | 
	 | -1, 2 | 

	 atlas> A:=[[1,-1,0],[0,1,-1]] 
	 Value: 
	 | 1, 0 | 
	 | -1, 1 | 
	 | 0, -1 | 

	 atlas> set C=change_basis (G,A) 
	 Identifier C: [ratvec] (hiding previous one of type mat) 
	 atlas> C 
	 Value: 
	 [[ 2, -1, -1 ]/3,[ -1, 2, -1 ]/3] 
	 atlas> C*sr 
	 Value: 
	 [[ 1, -1, 0 ]/1,[ 0, 1, -1 ]/1] 
	 atlas> make_integral(C*sr)
	 Value: 
	 | 1, 0 | 
	 | -1, 1 | 
	 | 0, -1 | 
	 
	 atlas> C*rho(G) 
	 Value: 
	 [ 1, 0, -1]/1 

	 atlas> 

Note the use of the new command:``make_integral``. Since the end result is an integral matrix, ``atlas`` can re-write it as such.  

Now to translate things back to atlas' coordinates we use the inverse change of coordinates matrix::

    atlas> set D=inverse_change_basis(SL(3,R),A) 
    Identifier D:[ratvec] 
    atlas> D 
    Value: 
    [[ 1, 0 ]/1,[ 0, 1 ]/1,[ -1, -1 ]/1] 
    
    atlas> D*C 
    Value: 
    [[ 1, 0 ]/1,[ 0, 1 ]/1] 
    
    atlas> make_integral(D*C) 
    Value: 
    | 1, 0 | 
    | 0, 1 | 
    
    atlas> 

For more information about this look at the coordinates.at file and watch the supplemental video on coordinates on the atlas website.  

