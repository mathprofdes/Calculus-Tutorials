:index:`Join Matrices`
======================

These operations are essentially the reverse of the extraction operations.  Joins are when you take 2 or more matrices and concatenate them either vertically or horizontally.

Row Join
--------

A row join joins two matrices horizontally, that is, it lines up the two by their rows and concatenates them.  Thus you can only row join two matrices if they have the same number of rows.  If you want to join two matrices with different numbers of rows you need to use the matrix editor on the smaller one and add in the needed rows, then you can do the row join.

When this is selected a dialog box will appear listing the names of all the entries in the CAS workspace.  Select a matrix from the list and click OK.  If the two matrices have the same number of rows it will join them with the currently selected matrix on the left and the one selected from the dialog box on the right.

For example, if you currently have

.. math::

    \left[\begin{array}{cc}1 & 4\\2 & 5\\3 & 6\end{array}\right]

selected and in the dialog box you select

.. math::

    \left[\begin{array}{c}7\\8\\9\end{array}\right]

the result will be

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]


Column Join
-----------

A column join joins two matrices vertically, that is, it lines up the two by their columns and concatenates them.  Thus you can only column join two matrices if they have the same number of columns.  If you want to join two matrices with different numbers of columns you need to use the matrix editor on the smaller one and add in the needed columns, then you can do the column join.

When this is selected a dialog box will appear listing the names of all the entries in the CAS workspace.  Select a matrix from the list and click OK.  If the two matrices have the same number of columns it will join them with the currently selected matrix on the top and the one selected from the dialog box on the bottom.

For example, if you currently have

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

selected and in the dialog box you select

.. math::

    \left[\begin{array}{ccc}3 & 6 & 9\\1 & 4 & 7\end{array}\right]

the result will be

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\\3 & 6 & 9\\1 & 4 & 7\end{array}\right]



Multiple Row Join
-----------------

The Multiple Row Join allows you to join more than two matrices at one time. When selected a dialog box will appear asking for the row join pattern.  List the matrices using their description name in the order to join with at least one space between each entry. For example, ``R2 R3 R1`` will join the matrices in R2, R3, and R1 in that order if the matrices all have the same number of rows.  This also allows you to duplicate matrices, for example ``R1 R1`` will row join R1 with itself.

For example, say R1 is the following matrix,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

and R2 is the matrix,

.. math::

    \left[\begin{array}{ccc}1 & 2 & 3\\4 & 5 & 6\\7 & 8 & 9\end{array}\right]

Then a pattern of ``R1 R2`` would produce,

.. math::

    \left[\begin{array}{cccccc}1 & 4 & 7 & 1 & 2 & 3\\2 & 5 & 8 & 4 & 5 & 6\\3 & 6 & 9 & 7 & 8 & 9\end{array}\right]

and a pattern of ``R2 R1 R2`` would produce,

.. math::

    \left[\begin{array}{ccccccccc}1 & 2 & 3 & 1 & 4 & 7 & 1 & 2 & 3\\4 & 5 & 6 & 2 & 5 & 8 & 4 & 5 & 6\\7 & 8 & 9 & 3 & 6 & 9 & 7 & 8 & 9\end{array}\right]

Multiple Column Join
--------------------

The Multiple Column Join allows you to join more than two matrices at one time. When selected a dialog box will appear asking for the column join pattern.  List the matrices using their description name in the order to join with at least one space between each entry. For example, ``R2 R3 R1`` will join the matrices in R2, R3, and R1 in that order if the matrices all have the same number of columns.  This also allows you to duplicate matrices, for example ``R1 R1`` will row join R1 with itself.

For example, say R1 is the following matrix,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

and R2 is the matrix,

.. math::

    \left[\begin{array}{ccc}1 & 2 & 3\\4 & 5 & 6\\7 & 8 & 9\end{array}\right]

Then a pattern of ``R1 R2`` would produce,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\\1 & 2 & 3\\4 & 5 & 6\\7 & 8 & 9\end{array}\right]

and a pattern of ``R2 R1 R2`` would produce,

.. math::

    \left[\begin{array}{ccc}1 & 2 & 3\\4 & 5 & 6\\7 & 8 & 9\\1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\\1 & 2 & 3\\4 & 5 & 6\\7 & 8 & 9\end{array}\right]


Row Join List
-------------

This will take a list of matrices that all have the same number of rows and join them in the order they are in the list.

For example, say we have the following list of matrices,

.. math::

    \left[ \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right], \  \left[\begin{array}{cc}a & b\\c & d\\e & f\end{array}\right], \  \left[\begin{array}{ccc}1 & 2 & 3\\4 & 5 & 6\\7 & 8 & 9\end{array}\right]\right]

if we row join this list we obtain,

.. math::

    \left[\begin{array}{cccccccc}1 & 4 & 7 & a & b & 1 & 2 & 3\\2 & 5 & 8 & c & d & 4 & 5 & 6\\3 & 6 & 9 & e & f & 7 & 8 & 9\end{array}\right]


Column Join List
----------------

This will take a list of matrices that all have the same number of columns and join them in the order they are in the list.

For example, say we have the following list of matrices,

.. math::

    \left[ \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right], \  \left[\begin{array}{ccc}a & c & e\\b & d & f\end{array}\right], \  \left[\begin{array}{ccc}1 & 2 & 3\\4 & 5 & 6\\7 & 8 & 9\end{array}\right]\right]


if we column join this list we obtain,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\\a & c & e\\b & d & f\\1 & 2 & 3\\4 & 5 & 6\\7 & 8 & 9\end{array}\right]
