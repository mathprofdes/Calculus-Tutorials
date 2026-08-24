:index:`Remove from Matrix`
===========================

As with all the editing options, when you make a change to an entry, such as removing rows or columns, the original entry is unaltered and a new entry is created.

Row
---

This option removes a single row from a matrix.  When selected a dialog box will appear asking for the row you wish to remove.  When you click OK the program will remove the row and create a new matrix item in the CAS workspace.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccccccc}3 & -10 & 6 & 7 & -2 & -7 & -7\\9 & -8 & 3 & -4 & 10 & -10 & -5\\-8 & -3 & -2 & 9 & -9 & 0 & 7\\5 & 5 & 8 & 3 & 1 & 0 & 2\\-4 & 7 & 2 & 8 & 7 & 1 & -7\end{array}\right]


and we remove row 4, the following matrix is added to the CAS,

.. math::

    \left[\begin{array}{ccccccc}3 & -10 & 6 & 7 & -2 & -7 & -7\\9 & -8 & 3 & -4 & 10 & -10 & -5\\-8 & -3 & -2 & 9 & -9 & 0 & 7\\-4 & 7 & 2 & 8 & 7 & 1 & -7\end{array}\right]


Column
------

This option removes a single column from a matrix.  When selected a dialog box will appear asking for the column you wish to remove.  When you click OK the program will remove the column and create a new matrix item in the CAS workspace.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccccccc}3 & -10 & 6 & 7 & -2 & -7 & -7\\9 & -8 & 3 & -4 & 10 & -10 & -5\\-8 & -3 & -2 & 9 & -9 & 0 & 7\\5 & 5 & 8 & 3 & 1 & 0 & 2\\-4 & 7 & 2 & 8 & 7 & 1 & -7\end{array}\right]


and we remove column 5, the following matrix is added to the CAS,

.. math::

    \left[\begin{array}{cccccc}3 & -10 & 6 & 7 & -7 & -7\\9 & -8 & 3 & -4 & -10 & -5\\-8 & -3 & -2 & 9 & 0 & 7\\5 & 5 & 8 & 3 & 0 & 2\\-4 & 7 & 2 & 8 & 1 & -7\end{array}\right]


Row Range
---------

This option removes a range of rows from a matrix, the result is a matrix.  When selected a dialog box will appear asking for the beginning and ending rows you wish to remove.  When you click OK the altered entry will be a new matrix item in the CAS workspace.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccccccc}3 & -10 & 6 & 7 & -2 & -7 & -7\\9 & -8 & 3 & -4 & 10 & -10 & -5\\-8 & -3 & -2 & 9 & -9 & 0 & 7\\5 & 5 & 8 & 3 & 1 & 0 & 2\\-4 & 7 & 2 & 8 & 7 & 1 & -7\end{array}\right]

and we remove rows 2 to 4, the following matrix is added to the CAS,

.. math::

    \left[\begin{array}{ccccccc}3 & -10 & 6 & 7 & -2 & -7 & -7\\-4 & 7 & 2 & 8 & 7 & 1 & -7\end{array}\right]


Column Range
------------

This option removes a range of columns from a matrix, the result is a matrix.  When selected a dialog box will appear asking for the beginning and ending columns you wish to remove.  When you click OK the altered entry will be a new matrix item in the CAS workspace.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccccccc}3 & -10 & 6 & 7 & -2 & -7 & -7\\9 & -8 & 3 & -4 & 10 & -10 & -5\\-8 & -3 & -2 & 9 & -9 & 0 & 7\\5 & 5 & 8 & 3 & 1 & 0 & 2\\-4 & 7 & 2 & 8 & 7 & 1 & -7\end{array}\right]

and we remove columns 4 to 6, the following matrix is added to the CAS,

.. math::

    \left[\begin{array}{cccc}3 & -10 & 6 & -7\\9 & -8 & 3 & -5\\-8 & -3 & -2 & 7\\5 & 5 & 8 & 2\\-4 & 7 & 2 & -7\end{array}\right]


