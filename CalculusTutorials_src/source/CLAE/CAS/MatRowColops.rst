:index:`Row and Column Operations`
==================================

This submenu contains user interface options to do elementary row and column operations to a matrix.  These options are some of the few that are given shortcuts.  While there are facilities in this program to do reduction to echelon and reduced echelon forms, these operations will help the user learn the reduction process.  When any row or column operation is done on a matrix the result is added to the CAS workspace and the original matrix is unaltered.  This also allows the user to look back over the reduction process and all matrices created during the process.

:index:`Scale a Row`
--------------------

This option simply scales a row of a matrix.  When selected a dialog box will appear asking the user for row number and scaling factor.  The scale factor can be any legitimate expression, including CAS workspace entries.  Note that the program does allow the user to do invalid row operations, such as scaling a row by a factor of 0.

For example, say we have the following matrix,

.. math::
    \left[\begin{array}{cccc}1 & 2 & -6 & 9\\10 & 6 & -2 & -10\\8 & -6 & 0 & -5\end{array}\right]

If we scale row 2 by 1/10 we get,

.. math::
    \left[\begin{array}{cccc}1 & 2 & -6 & 9\\1 & \frac{3}{5} & - \frac{1}{5} & -1\\8 & -6 & 0 & -5\end{array}\right]

Note that the arithmetic is exact, as expected.

:index:`Interchange Two Rows`
-----------------------------

This simply interchanges two rows.  When selected a dialog box will appear asking for the two rows to interchange. In this case, if the user tries to interchange a row with itself the result is an error.

For example, say we have the following matrix,

.. math::
    \left[\begin{array}{cccc}1 & 2 & -6 & 9\\10 & 6 & -2 & -10\\8 & -6 & 0 & -5\end{array}\right]

If we interchange rows 1 and 2 we get,

.. math::
    \left[\begin{array}{cccc}10 & 6 & -2 & -10\\1 & 2 & -6 & 9\\8 & -6 & 0 & -5\end{array}\right]


:index:`Add a Multiple of a Row to Another`
-------------------------------------------

This option adds a multiple of a row to another a row of a matrix.  When selected a dialog box will appear asking the user for the row number of the row that will be multiplied, the multiplication factor, and the number of the row to add this result to.  The multiplication factor can be any legitimate expression, including CAS workspace entries.  If the user tries to use the same row as the multiplier row and the add to row the result will be an error.

For example, say we have the following matrix,

.. math::
    \left[\begin{array}{cccc}1 & 2 & -6 & 9\\10 & 6 & -2 & -10\\8 & -6 & 0 & -5\end{array}\right]

If we multiply row 1 by :math:`-10` and add to row 2 we get,

.. math::
    \left[\begin{array}{cccc}1 & 2 & -6 & 9\\0 & -14 & 58 & -100\\8 & -6 & 0 & -5\end{array}\right]


:index:`Scale a Column`
-----------------------

This option simply scales a column of a matrix.  When selected a dialog box will appear asking the user for column number and scaling factor.  The scale factor can be any legitimate expression, including CAS workspace entries.  Note that the program does allow the user to do invalid column operations, such as scaling a row by a factor of 0.

For example, say we have the following matrix,

.. math::
    \left[\begin{array}{cccc}1 & 2 & -6 & 9\\10 & 6 & -2 & -10\\8 & -6 & 0 & -5\end{array}\right]

If we scale column 2 by 1/6 we get,

.. math::
    \left[\begin{array}{cccc}1 & \frac{1}{3} & -6 & 9\\10 & 1 & -2 & -10\\8 & -1 & 0 & -5\end{array}\right]


:index:`Interchange Two Columns`
--------------------------------

This simply interchanges two columns.  When selected a dialog box will appear asking for the two columns to interchange. In this case, if the user tries to interchange a column with itself the result is an error.

For example, say we have the following matrix,

.. math::
    \left[\begin{array}{cccc}1 & 2 & -6 & 9\\10 & 6 & -2 & -10\\8 & -6 & 0 & -5\end{array}\right]

If we interchange columns 1 and 2 we get,

.. math::
    \left[\begin{array}{cccc}2 & 1 & -6 & 9\\6 & 10 & -2 & -10\\-6 & 8 & 0 & -5\end{array}\right]


:index:`Add a Multiple of a Column to Another`
----------------------------------------------

This option adds a multiple of a column to another a column of a matrix.  When selected a dialog box will appear asking the user for the column number of the column that will be multiplied, the multiplication factor, and the number of the column to add this result to.  The multiplication factor can be any legitimate expression, including CAS workspace entries.  If the user tries to use the same column as the multiplier column and the add to column the result will be an error.

For example, say we have the following matrix,

.. math::
    \left[\begin{array}{cccc}1 & 2 & -6 & 9\\10 & 6 & -2 & -10\\8 & -6 & 0 & -5\end{array}\right]

If we multiply column 1 by :math:`-2` and add to column 2 we get,

.. math::
    \left[\begin{array}{cccc}1 & 0 & -6 & 9\\10 & -14 & -2 & -10\\8 & -22 & 0 & -5\end{array}\right]


