:index:`Special Matrices`
=========================

The Special Matrices options are a submenu under ``Edit > Special Matrices`` of the main program menu.


:index:`Identity`
-----------------

This option opens a dialog box allowing the user to input the size of the matrix.  In this case the matrix will be square.  The result loaded to the CAS is an identity matrix of the selected size.

:index:`Zero`
-------------

This option opens a dialog box allowing the user to input the size of the matrix.  The result loaded to the CAS is a zero matrix of the selected size.


:index:`Hilbert`
----------------

This option opens a dialog box allowing the user to input the size of the matrix.  In this case the matrix will be square.  The result loaded to the CAS is a Hilbert matrix of the selected size. That is, program will simply load each (i, j) cell with ``1/(i+j-1)``.

So a Hilbert matrix of size 7 is,

.. math::

    \left[\begin{array}{ccccccc}1 & \frac{1}{2} & \frac{1}{3} & \frac{1}{4} & \frac{1}{5} & \frac{1}{6} & \frac{1}{7}\\\frac{1}{2} & \frac{1}{3} & \frac{1}{4} & \frac{1}{5} & \frac{1}{6} & \frac{1}{7} & \frac{1}{8}\\\frac{1}{3} & \frac{1}{4} & \frac{1}{5} & \frac{1}{6} & \frac{1}{7} & \frac{1}{8} & \frac{1}{9}\\\frac{1}{4} & \frac{1}{5} & \frac{1}{6} & \frac{1}{7} & \frac{1}{8} & \frac{1}{9} & \frac{1}{10}\\\frac{1}{5} & \frac{1}{6} & \frac{1}{7} & \frac{1}{8} & \frac{1}{9} & \frac{1}{10} & \frac{1}{11}\\\frac{1}{6} & \frac{1}{7} & \frac{1}{8} & \frac{1}{9} & \frac{1}{10} & \frac{1}{11} & \frac{1}{12}\\\frac{1}{7} & \frac{1}{8} & \frac{1}{9} & \frac{1}{10} & \frac{1}{11} & \frac{1}{12} & \frac{1}{13}\end{array}\right]


:index:`Companion`
------------------

This option opens a dialog box allowing the user to input the polynomial for the companion matrix.  The input must be a monic polynomial or the output is undetermined, most of the time it will result in an error entry or possible be a 1 X 1 zero matrix.

For example, if we input :math:`x^4-5x^3+9x^2-4x+7` as ``x^4-5*x^3+9*x^2-4*x+7`` the resulting matrix is,

.. math::

    \left[\begin{array}{cccc}0 & 0 & 0 & -7\\1 & 0 & 0 & 4\\0 & 1 & 0 & -9\\0 & 0 & 1 & 5\end{array}\right]


:index:`Vandermonde`
--------------------

This option opens a dialog box allowing the user to input a list of expressions to be used in a Vandermonde matrix.  The input  must be a list of expressions separated by commas.

For example, if we input :math:`[x, y, z, w]` (or just :math:`x, y, z, w`) the resulting matrix is,

.. math::
    \left[\begin{array}{cccc}1 & x & x^{2} & x^{3}\\1 & y & y^{2} & y^{3}\\1 & z & z^{2} & z^{3}\\1 & w & w^{2} & w^{3}\end{array}\right]


:index:`Generate Matrix`
------------------------

The generate matrix option allows the user to generate a matrix where the contents of each cell are determined by a formula using the row and column indexes.  A Hilbert matrix is a special case of this where the formula is, ``1/(i+j-1)``.

When this option is selected a dialog box will appear allowing the user to input the size of the matrix, the formula to be used for each cell and the variables that are to be used for the row index and the column index.

For example, if we generate a 10 X 10 matrix with formula ``sin(i)/cos(j)`` where i is the row index and j is the column index the result would be,

.. math::

    \left[\begin{array}{cccccccccc}\frac{\sin{\left(1 \right)}}{\cos{\left(1 \right)}} & \frac{\sin{\left(1 \right)}}{\cos{\left(2 \right)}} & \frac{\sin{\left(1 \right)}}{\cos{\left(3 \right)}} & \frac{\sin{\left(1 \right)}}{\cos{\left(4 \right)}} & \frac{\sin{\left(1 \right)}}{\cos{\left(5 \right)}} & \frac{\sin{\left(1 \right)}}{\cos{\left(6 \right)}} & \frac{\sin{\left(1 \right)}}{\cos{\left(7 \right)}} & \frac{\sin{\left(1 \right)}}{\cos{\left(8 \right)}} & \frac{\sin{\left(1 \right)}}{\cos{\left(9 \right)}} & \frac{\sin{\left(1 \right)}}{\cos{\left(10 \right)}}\\\frac{\sin{\left(2 \right)}}{\cos{\left(1 \right)}} & \frac{\sin{\left(2 \right)}}{\cos{\left(2 \right)}} & \frac{\sin{\left(2 \right)}}{\cos{\left(3 \right)}} & \frac{\sin{\left(2 \right)}}{\cos{\left(4 \right)}} & \frac{\sin{\left(2 \right)}}{\cos{\left(5 \right)}} & \frac{\sin{\left(2 \right)}}{\cos{\left(6 \right)}} & \frac{\sin{\left(2 \right)}}{\cos{\left(7 \right)}} & \frac{\sin{\left(2 \right)}}{\cos{\left(8 \right)}} & \frac{\sin{\left(2 \right)}}{\cos{\left(9 \right)}} & \frac{\sin{\left(2 \right)}}{\cos{\left(10 \right)}}\\\frac{\sin{\left(3 \right)}}{\cos{\left(1 \right)}} & \frac{\sin{\left(3 \right)}}{\cos{\left(2 \right)}} & \frac{\sin{\left(3 \right)}}{\cos{\left(3 \right)}} & \frac{\sin{\left(3 \right)}}{\cos{\left(4 \right)}} & \frac{\sin{\left(3 \right)}}{\cos{\left(5 \right)}} & \frac{\sin{\left(3 \right)}}{\cos{\left(6 \right)}} & \frac{\sin{\left(3 \right)}}{\cos{\left(7 \right)}} & \frac{\sin{\left(3 \right)}}{\cos{\left(8 \right)}} & \frac{\sin{\left(3 \right)}}{\cos{\left(9 \right)}} & \frac{\sin{\left(3 \right)}}{\cos{\left(10 \right)}}\\\frac{\sin{\left(4 \right)}}{\cos{\left(1 \right)}} & \frac{\sin{\left(4 \right)}}{\cos{\left(2 \right)}} & \frac{\sin{\left(4 \right)}}{\cos{\left(3 \right)}} & \frac{\sin{\left(4 \right)}}{\cos{\left(4 \right)}} & \frac{\sin{\left(4 \right)}}{\cos{\left(5 \right)}} & \frac{\sin{\left(4 \right)}}{\cos{\left(6 \right)}} & \frac{\sin{\left(4 \right)}}{\cos{\left(7 \right)}} & \frac{\sin{\left(4 \right)}}{\cos{\left(8 \right)}} & \frac{\sin{\left(4 \right)}}{\cos{\left(9 \right)}} & \frac{\sin{\left(4 \right)}}{\cos{\left(10 \right)}}\\\frac{\sin{\left(5 \right)}}{\cos{\left(1 \right)}} & \frac{\sin{\left(5 \right)}}{\cos{\left(2 \right)}} & \frac{\sin{\left(5 \right)}}{\cos{\left(3 \right)}} & \frac{\sin{\left(5 \right)}}{\cos{\left(4 \right)}} & \frac{\sin{\left(5 \right)}}{\cos{\left(5 \right)}} & \frac{\sin{\left(5 \right)}}{\cos{\left(6 \right)}} & \frac{\sin{\left(5 \right)}}{\cos{\left(7 \right)}} & \frac{\sin{\left(5 \right)}}{\cos{\left(8 \right)}} & \frac{\sin{\left(5 \right)}}{\cos{\left(9 \right)}} & \frac{\sin{\left(5 \right)}}{\cos{\left(10 \right)}}\\\frac{\sin{\left(6 \right)}}{\cos{\left(1 \right)}} & \frac{\sin{\left(6 \right)}}{\cos{\left(2 \right)}} & \frac{\sin{\left(6 \right)}}{\cos{\left(3 \right)}} & \frac{\sin{\left(6 \right)}}{\cos{\left(4 \right)}} & \frac{\sin{\left(6 \right)}}{\cos{\left(5 \right)}} & \frac{\sin{\left(6 \right)}}{\cos{\left(6 \right)}} & \frac{\sin{\left(6 \right)}}{\cos{\left(7 \right)}} & \frac{\sin{\left(6 \right)}}{\cos{\left(8 \right)}} & \frac{\sin{\left(6 \right)}}{\cos{\left(9 \right)}} & \frac{\sin{\left(6 \right)}}{\cos{\left(10 \right)}}\\\frac{\sin{\left(7 \right)}}{\cos{\left(1 \right)}} & \frac{\sin{\left(7 \right)}}{\cos{\left(2 \right)}} & \frac{\sin{\left(7 \right)}}{\cos{\left(3 \right)}} & \frac{\sin{\left(7 \right)}}{\cos{\left(4 \right)}} & \frac{\sin{\left(7 \right)}}{\cos{\left(5 \right)}} & \frac{\sin{\left(7 \right)}}{\cos{\left(6 \right)}} & \frac{\sin{\left(7 \right)}}{\cos{\left(7 \right)}} & \frac{\sin{\left(7 \right)}}{\cos{\left(8 \right)}} & \frac{\sin{\left(7 \right)}}{\cos{\left(9 \right)}} & \frac{\sin{\left(7 \right)}}{\cos{\left(10 \right)}}\\\frac{\sin{\left(8 \right)}}{\cos{\left(1 \right)}} & \frac{\sin{\left(8 \right)}}{\cos{\left(2 \right)}} & \frac{\sin{\left(8 \right)}}{\cos{\left(3 \right)}} & \frac{\sin{\left(8 \right)}}{\cos{\left(4 \right)}} & \frac{\sin{\left(8 \right)}}{\cos{\left(5 \right)}} & \frac{\sin{\left(8 \right)}}{\cos{\left(6 \right)}} & \frac{\sin{\left(8 \right)}}{\cos{\left(7 \right)}} & \frac{\sin{\left(8 \right)}}{\cos{\left(8 \right)}} & \frac{\sin{\left(8 \right)}}{\cos{\left(9 \right)}} & \frac{\sin{\left(8 \right)}}{\cos{\left(10 \right)}}\\\frac{\sin{\left(9 \right)}}{\cos{\left(1 \right)}} & \frac{\sin{\left(9 \right)}}{\cos{\left(2 \right)}} & \frac{\sin{\left(9 \right)}}{\cos{\left(3 \right)}} & \frac{\sin{\left(9 \right)}}{\cos{\left(4 \right)}} & \frac{\sin{\left(9 \right)}}{\cos{\left(5 \right)}} & \frac{\sin{\left(9 \right)}}{\cos{\left(6 \right)}} & \frac{\sin{\left(9 \right)}}{\cos{\left(7 \right)}} & \frac{\sin{\left(9 \right)}}{\cos{\left(8 \right)}} & \frac{\sin{\left(9 \right)}}{\cos{\left(9 \right)}} & \frac{\sin{\left(9 \right)}}{\cos{\left(10 \right)}}\\\frac{\sin{\left(10 \right)}}{\cos{\left(1 \right)}} & \frac{\sin{\left(10 \right)}}{\cos{\left(2 \right)}} & \frac{\sin{\left(10 \right)}}{\cos{\left(3 \right)}} & \frac{\sin{\left(10 \right)}}{\cos{\left(4 \right)}} & \frac{\sin{\left(10 \right)}}{\cos{\left(5 \right)}} & \frac{\sin{\left(10 \right)}}{\cos{\left(6 \right)}} & \frac{\sin{\left(10 \right)}}{\cos{\left(7 \right)}} & \frac{\sin{\left(10 \right)}}{\cos{\left(8 \right)}} & \frac{\sin{\left(10 \right)}}{\cos{\left(9 \right)}} & \frac{\sin{\left(10 \right)}}{\cos{\left(10 \right)}}\end{array}\right]

Note that it simply substitutes in values and does not do some obvious simplifications.
