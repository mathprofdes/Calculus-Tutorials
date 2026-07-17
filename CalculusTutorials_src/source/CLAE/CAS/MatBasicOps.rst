:index:`Basic Operations on Matrices`
=====================================

:index:`Arithmetic Operations`
------------------------------

Arithmetic operations of ``+``, ``-``, ``*``, and ``^`` can be done on matrices as long as the operation is defined on the matrices in the expression.  To do these, first input the matrices into the CAS workspace and then use their designations (R1, R2, ...) to input the arithmetic expression into the CAS input bar.

For example, say we have the following matrices in the CAS workspace.

- R1 is the matrix

.. math::
    \left[\begin{array}{ccc}-10 & 7 & 2\\1 & 7 & 10\\0 & 7 & -5\end{array}\right]


- R2 is the matrix

.. math::
    \left[\begin{array}{ccc}5 & -6 & 2\\3 & -9 & -6\\3 & 7 & -8\end{array}\right]


- R3 is the matrix

.. math::
    \left[\begin{array}{ccc}-6 & -2 & -9\\5 & 4 & 1\\-4 & -8 & -7\\-2 & 4 & -5\\-9 & 6 & 6\end{array}\right]

The expression ``R1 + R2`` returns

.. math::
    \left[\begin{array}{ccc}-5 & 1 & 4\\4 & -2 & 4\\3 & 14 & -13\end{array}\right]

The expression ``R1 - R2`` returns

.. math::
    \left[\begin{array}{ccc}-15 & 13 & 0\\-2 & 16 & 16\\-3 & 0 & 3\end{array}\right]

The expression ``R1 * R2`` returns

.. math::
    \left[\begin{array}{ccc}-23 & 11 & -78\\56 & 1 & -120\\6 & -98 & -2\end{array}\right]

The expression ``R1^3`` returns

.. math::
    \left[\begin{array}{ccc}-1077 & 980 & -56\\156 & 1015 & 1144\\-56 & 812 & -321\end{array}\right]

The expression ``R1^-1`` returns

.. math::
    \left[\begin{array}{ccc}- \frac{15}{157} & \frac{7}{157} & \frac{8}{157}\\\frac{5}{1099} & \frac{50}{1099} & \frac{102}{1099}\\\frac{1}{157} & \frac{10}{157} & - \frac{11}{157}\end{array}\right]

The expression ``R3 * R2`` returns

.. math::
    \left[\begin{array}{ccc}-63 & -9 & 72\\40 & -59 & -22\\-65 & 47 & 96\\-13 & -59 & 12\\-9 & 42 & -102\end{array}\right]

The expression ``R2 * R3`` returns an error.

:index:`Transpose`
------------------

The transpose option returns the transpose of the selected matrix. For example, the transpose of

.. math::
    \left[\begin{array}{ccc}-6 & -2 & -9\\5 & 4 & 1\\-4 & -8 & -7\\-2 & 4 & -5\\-9 & 6 & 6\end{array}\right]

returns

.. math::
    \left[\begin{array}{ccccc}-6 & 5 & -4 & -2 & -9\\-2 & 4 & -8 & 4 & 6\\-9 & 1 & -7 & -5 & 6\end{array}\right]


:index:`Determinant`
--------------------

This option returns the determinant of a square matrix.  If the matrix is not square then an error is returned.  For example, the determinant of

.. math::
    \left[\begin{array}{ccc}5 & -6 & 2\\3 & -9 & -6\\3 & 7 & -8\end{array}\right]

returns 640. Also the determinant of

.. math::
    \left[\begin{array}{ccc}x + 10 & -7 & -2\\-1 & x - 7 & -10\\0 & -7 & x + 5\end{array}\right]

returns :math:`x^{3} + 8 x^{2} - 132 x - 1099`.

:index:`Inverse`
----------------

This option returns the inverse of a square matrix if the inverse exists, that is, if the determinant is not 0.  If the matrix does not have an inverse an error is returned.  For example, the inverse of

.. math::
    \left[\begin{array}{ccc}5 & -6 & 2\\3 & -9 & -6\\3 & 7 & -8\end{array}\right]

is

.. math::
    \left[\begin{array}{ccc}\frac{19}{105} & - \frac{17}{315} & \frac{3}{35}\\\frac{1}{105} & - \frac{23}{315} & \frac{2}{35}\\\frac{8}{105} & - \frac{53}{630} & - \frac{3}{70}\end{array}\right]
