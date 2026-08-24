:index:`Extract from Matrix`
============================

Once an entry is entered you can edit the entry by double-clicking it.  To reduce the amount of editing you need to do, the program offers numerous facilities for extracting and manipulating an expression.  These are primarily things you would normally do as part of calculations in Calculus or Linear Algebra.  This set of manipulations deal primarily with extracting information from matrices.


Entry
-----

This option extracts a single entry from a matrix.  When selected a dialog box will appear asking for the row and column of the entry you wish to extract.  When you click OK the selected entry will be a new expression item in the CAS workspace.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

and we extract the entry from row 3 and column 2 the value 6 would be loaded into the CAS.


Row
---

This option extracts a single row from a matrix, the result is a 1 X n matrix.  When selected a dialog box will appear asking for the row you wish to extract.  When you click OK the selected entry will be a new matrix item in the CAS workspace.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

and we extract row 2, the following matrix is added to the CAS,

.. math::

    \left[\begin{array}{ccc}2 & 5 & 8\end{array}\right]


Column
------

This option extracts a single column from a matrix, the result is an n X 1 matrix.  When selected a dialog box will appear asking for the column you wish to extract.  When you click OK the selected entry will be a new matrix item in the CAS workspace.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

and we extract column 2, the following matrix is added to the CAS,

.. math::

    \left[\begin{array}{c}4\\5\\6\end{array}\right]


Row Range
---------

This option extracts a range of rows from a matrix, the result is a matrix.  When selected a dialog box will appear asking for the beginning and ending rows you wish to extract.  When you click OK the selected entry will be a new matrix item in the CAS workspace.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

and we extract rows 2 to 3, the following matrix is added to the CAS,

.. math::

    \left[\begin{array}{ccc}2 & 5 & 8\\3 & 6 & 9\end{array}\right]


Column Range
------------

This option extracts a range of columns from a matrix, the result is a matrix.  When selected a dialog box will appear asking for the beginning and ending columns you wish to extract.  When you click OK the selected entry will be a new matrix item in the CAS workspace.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

and we extract columns 2 to 3, the following matrix is added to the CAS,

.. math::

    \left[\begin{array}{cc}4 & 7\\5 & 8\\6 & 9\end{array}\right]


Row Pattern
-----------

This option extracts rows from a matrix according to a pattern of row numbers, the result is a matrix.  When selected a dialog box will appear asking for the row pattern.  The pattern is simply a list of row numbers separated by at least one space. For example, the pattern ``1 3 5 2`` will extract rows 1, 3, 5, and 2 in that order and create a new matrix with those 4 rows.  This has the added bonus of being able to rearrange and to duplicate the rows of a matrix.  For example, if the matrix has 3 rows then ``1 3 2`` will interchange rows 2 and 3.  Also, ``1 3 3 2 1`` will duplicate row 3 for the new rows 2 and 3 and put a duplicate of row 1 at the bottom.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

a pattern of ``3 1`` will produce,

.. math::

    \left[\begin{array}{ccc}3 & 6 & 9\\1 & 4 & 7\end{array}\right]


a pattern of ``2 2 1 3`` will produce,

.. math::

    \left[\begin{array}{ccc}2 & 5 & 8\\2 & 5 & 8\\1 & 4 & 7\\3 & 6 & 9\end{array}\right]


Column Pattern
--------------

This option extracts columns from a matrix according to a pattern of column numbers, the result is a matrix.  When selected a dialog box will appear asking for the column pattern.  The pattern is simply a list of column numbers separated by at least one space. For example, the pattern ``1 3 5 2`` will extract columns 1, 3, 5, and 2 in that order and create a new matrix with those 4 columns.  This has the added bonus of being able to rearrange and to duplicate the columns of a matrix.  For example, if the matrix has 3 columns then ``1 3 2`` will interchange columns 2 and 3.  Also, ``1 3 3 2 1`` will duplicate column 3 for the new columns 2 and 3 and put a duplicate of column 1 at the end.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

a pattern of ``3 1`` will produce,

.. math::

    \left[\begin{array}{cc}7 & 1\\8 & 2\\9 & 3\end{array}\right]


a pattern of ``2 2 1 3`` will produce,

.. math::

    \left[\begin{array}{cccc}4 & 4 & 1 & 7\\5 & 5 & 2 & 8\\6 & 6 & 3 & 9\end{array}\right]


Row and Column Pattern
----------------------

This option extracts both rows and columns from a matrix according to a pattern of row and column numbers, the result is a matrix.  When selected a dialog box will appear asking for the row and column patterns.  The pattern is simply a list of numbers separated by at least one space.  The extraction is the intersection of the row pattern selection and the column pattern selection.  This has the added bonus of being able to rearrange and to duplicate the the rows and columns of a matrix.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

a row pattern of ``1 2`` and column pattern of ``2 3`` will produce,

.. math::
    \left[\begin{array}{cc}4 & 7\\5 & 8\end{array}\right]

and a row pattern of ``1 3 1`` and column pattern of ``1 3`` will produce,

.. math::
    \left[\begin{array}{cc}1 & 7\\3 & 9\\1 & 7\end{array}\right]


Submatrix
---------

This option will open a dialog box asking the user for a row range and column range.  The result is a new matrix with the row and column ranges from the original.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

extracting rows 1 to 2 and columns 2 to 3 produces the following matrix,

.. math::

    \left[\begin{array}{cc}4 & 7\\5 & 8\end{array}\right]



Rows to List of Vectors
-----------------------

This option creates a list of row vectors, one for each row in the matrix.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

this option will produce,

.. math::

    \left[ \left[\begin{array}{ccc}1 & 4 & 7\end{array}\right], \  \left[\begin{array}{ccc}2 & 5 & 8\end{array}\right], \  \left[\begin{array}{ccc}3 & 6 & 9\end{array}\right]\right]

Columns to List of Vectors
--------------------------

This option creates a list of column vectors, one for each column in the matrix.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

this option will produce,

.. math::

    \left[ \left[\begin{array}{c}1\\2\\3\end{array}\right], \  \left[\begin{array}{c}4\\5\\6\end{array}\right], \  \left[\begin{array}{c}7\\8\\9\end{array}\right]\right]

All Rows
--------

This will extract each row of the matrix and load it into the CAS workspace in separate entries.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

this option will produce three new entries in the CAS,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\end{array}\right]

.. math::

    \left[\begin{array}{ccc}2 & 5 & 8\end{array}\right]

.. math::

    \left[\begin{array}{ccc}3 & 6 & 9\end{array}\right]



All Columns
-----------

This will extract each column of the matrix and load it into the CAS workspace in separate entries.

For example, if the matrix is,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

this option will produce three new entries in the CAS,

.. math::

    \left[\begin{array}{c}1\\2\\3\end{array}\right]

.. math::

    \left[\begin{array}{c}4\\5\\6\end{array}\right]

.. math::

    \left[\begin{array}{c}7\\8\\9\end{array}\right]


Separate by Variables
---------------------

This is a fairly specialized operation.  It comes in handy if you have a solution vector to a linear system or matrix and you wish to write it as a set of vectors separated by the free variables.

For example, if the matrix is,

.. math::
    \left[\begin{array}{cccccccc}1 & -6 & 31 & 15 & 36 & 10 & -40 & 145\\-100 & 561 & -2866 & -1383 & -3327 & 568 & -2272 & 12039\\-13 & 73 & -373 & -180 & -433 & 71 & -284 & 1517\\-81 & 486 & -2511 & -1215 & -2916 & 5 & -19 & 2106\\9 & -54 & 279 & 135 & 324 & 0 & 0 & -225\end{array}\right]

Then we select ``Matrix > Solve System``, we get,

.. math::
    \left[\begin{array}{c}5 x_{3} + 3 x_{4} + 6 x_{5} - 7\\6 x_{3} + 3 x_{4} + 7 x_{5} + 3\\x_{3}\\x_{4}\\x_{5}\\1\\-4\end{array}\right]

This is a vector form for the solution set.  If we now apply the Separate by Variables option with ``Edit > Extract from Matrix > Separate by Variables`` the result is,

.. math::
    \left[ \left[\begin{array}{c}5\\6\\1\\0\\0\\0\\0\end{array}\right], \  \left[\begin{array}{c}3\\3\\0\\1\\0\\0\\0\end{array}\right], \  \left[\begin{array}{c}6\\7\\0\\0\\1\\0\\0\end{array}\right], \  \left[\begin{array}{c}-7\\3\\0\\0\\0\\1\\-4\end{array}\right]\right]

The first three vectors are the free variable vectors and the last one is the vector of constants (that is, the translation).  The description of the object tells the user the order of the vectors, ``Separation by Variables of R4 [x3, x4, x5, 'Constants']``.

Note that you probably do not want to use this option if the entries of the matrix have variables that are in addition to the free variables.  This option will split the matrix over all symbols, free variables as well as entry variables.

