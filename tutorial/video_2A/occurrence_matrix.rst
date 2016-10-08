Occurrence Matrices
====================

We mentionned before that a Cartan may appear in differend real forms
of an inner class. More precisely for a given inner class there
is a fixed set of Cartans which may ar may not appear in the different
real forms associated to this inner class. If we ask for the number
of Cartan classes of real form we get the same number regardless of
the real form we are using. This can be misleading unless we
understand what the software is doing. This is because ``atlas`` is
implicitly assuming that you are asking for the number of Cartans in
the inner class of these real forms. For example,::

   atlas> set G=SO(5,4)
   Identifier G: RealForm
   atlas> nr_of_Cartan_classes (G)
   Value: 9
   atlas> G:=SO(9,0)
   Value: compact connected real group with Lie algebra 'so(9)'
   atlas> nr_of_Cartan_classes (G)
   Value: 9
   atlas>

So, to find out which Cartans appear in each individual real form there is an ``occurrence matrix``::

    atlas> occurrence_matrix (G)
    Value: 
    | 1, 0, 0, 0, 0, 0, 0, 0, 0 |
    | 1, 0, 1, 0, 0, 0, 0, 0, 0 |
    | 1, 1, 1, 1, 0, 0, 0, 0, 0 |
    | 1, 1, 1, 1, 0, 1, 0, 1, 0 |
    | 1, 1, 1, 1, 1, 1, 1, 1, 1 |
    
This matrix has 9 columns for the Cartan classes and 5 rows for the real forms of the group of type B4. Recall that the real forms for this inner class can be listed as follows::

    atlas> for H in real_forms (G) do prints(H) od
    compact connected real group with Lie algebra 'so(9)'
    disconnected real group with Lie algebra 'so(8,1)'
    disconnected real group with Lie algebra 'so(7,2)'
    disconnected real group with Lie algebra 'so(6,3)'
    disconnected split real group with Lie algebra 'so(5,4)'
    Value: [(),(),(),(),()]
    atlas>

And remember that to avoid getting the empty values we do::

    atlas> void: for H in real_forms (G) do prints(H) od 
    compact connected real group with Lie algebra 'so(9)'
    disconnected real group with Lie algebra 'so(8,1)'
    disconnected real group with Lie algebra 'so(7,2)'
    disconnected real group with Lie algebra 'so(6,3)'
    disconnected split real group with Lie algebra 'so(5,4)'
    atlas> 

So, the occurrence matrix says that all 9 Cartans appear in the split
form SO(5,4), that only the compact Cartan appears in the compact real
form SO(9,0), that SO(6,3) has only 6 Cartans,etc. Also note that the
Compact Cartan appears in all real forms but the split Cartan only
appears in the split real form.


