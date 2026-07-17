:index:`Minors and Cofactors`
=============================

The Minors and Cofactors submenu has options for quick calculations of minors, cofactors, adjugates, adjoints, and conjugates.

:index:`(i, j) Minor`
---------------------

The (i, j)-minor of a matrix A is defined to be :math:`M_{ij} = \det(A_{i,j})`, where :math:`A_{ij}` is the submatrix formed by deleting the `i` th row and the `j` th column of `A` .  For example, say we have the following matrix,

.. math::
    \left[\begin{array}{ccc}-8 & -6 & -8\\7 & 7 & 1\\-4 & 8 & -9\end{array}\right]

The (3, 2)-minor is 48 and the (1, 2)-minor is :math:`-59`.

:index:`(i, j) Minor Submatrix`
-------------------------------

The (i, j)-minor submatrix :math:`A_{i,j}`, where :math:`A_{ij}` is the submatrix formed by deleting the `i` th row and the `j` th column of `A` .  For example, say we have the following matrix,

.. math::
    \left[\begin{array}{ccc}-8 & -6 & -8\\7 & 7 & 1\\-4 & 8 & -9\end{array}\right]

The (3, 2)-minor matrix is

.. math::
    \left[\begin{array}{cc}-8 & -8\\7 & 1\end{array}\right]

and the (1, 2)-minor matrix is

.. math::
    \left[\begin{array}{cc}7 & 1\\-4 & -9\end{array}\right]

:index:`(i, j) Cofactor`
------------------------

The (i, j)-cofactor of a matrix A is defined to be :math:`C_{ij} = (-1)^{i+j} \det(A_{i,j})`, where :math:`A_{ij}` is the submatrix formed by deleting the `i` th row and the `j` th column of `A` .  For example, say we have the following matrix,

.. math::
    \left[\begin{array}{ccc}-8 & -6 & -8\\7 & 7 & 1\\-4 & 8 & -9\end{array}\right]

The (3, 2)-cofactor is :math:`-48` and the (1, 2)-cofactor is :math:`59`.

:index:`Cofactor Matrix`
------------------------

The Cofactor Matrix is defined to be

.. math::
    \left[\begin{array}{cccc}C_{11} & C_{12} & \cdots & C_{1n}\\C_{21} & C_{22} & \cdots & C_{2n}\\ \vdots & \vdots & \ddots & \vdots  \\ C_{n1} & C_{n2} & \cdots & C_{nn}\end{array}\right]

where :math:`C_{i,j}` is the (i, j)-cofactor of a matrix A.  For example, say we have the following matrix,

.. math::
    \left[\begin{array}{ccc}-8 & -6 & -8\\7 & 7 & 1\\-4 & 8 & -9\end{array}\right]

The cofactor matrix is

.. math::
    \left[\begin{array}{ccc}-71 & 59 & 84\\-118 & 40 & 88\\50 & -48 & -14\end{array}\right]

:index:`Adjugate`
-----------------

The Adjugate, also known as the Classical Adjoint is the transpose of the cofactor matrix.

.. math::
    \left[\begin{array}{cccc}C_{11} & C_{12} & \cdots & C_{1n}\\C_{21} & C_{22} & \cdots & C_{2n}\\ \vdots & \vdots & \ddots & \vdots  \\ C_{n1} & C_{n2} & \cdots & C_{nn}\end{array}\right]^T =
    \left[\begin{array}{cccc}C_{11} & C_{21} & \cdots & C_{n1}\\C_{12} & C_{22} & \cdots & C_{n2}\\ \vdots & \vdots & \ddots & \vdots  \\ C_{1n} & C_{2n} & \cdots & C_{nn}\end{array}\right]

For example, say we have the following matrix,

.. math::
    \left[\begin{array}{ccc}-8 & -6 & -8\\7 & 7 & 1\\-4 & 8 & -9\end{array}\right]

The adjugate matrix is

.. math::
    \left[\begin{array}{ccc}-71 & -118 & 50\\59 & 40 & -48\\84 & 88 & -14\end{array}\right]


:index:`Adjoint`
----------------

The Adjoint of a matrix `A` is defined to be the conjugate transpose of A. For example, say we have the matrix,

.. math::
    \left[\begin{array}{ccc}-8 + 3 i & -6 - 10 i & -8 - 6 i\\7 + 6 i & 7 + 3 i & 1 - 10 i\\-4 + 2 i & 8 - 10 i & -9 - 7 i\end{array}\right]

then the adjoint is

.. math::
    \left[\begin{array}{ccc}-8 - 3 i & 7 - 6 i & -4 - 2 i\\-6 + 10 i & 7 - 3 i & 8 + 10 i\\-8 + 6 i & 1 + 10 i & -9 + 7 i\end{array}\right]


:index:`Conjugate`
------------------

The Conjugate of a matrix `A` is defined to be the matrix formed by taking the complex conjugate of each entry of A. For example, say we have the matrix,

.. math::
    \left[\begin{array}{ccc}-8 + 3 i & -6 - 10 i & -8 - 6 i\\7 + 6 i & 7 + 3 i & 1 - 10 i\\-4 + 2 i & 8 - 10 i & -9 - 7 i\end{array}\right]

then the conjugate is

.. math::
    \left[\begin{array}{ccc}-8 - 3 i & -6 + 10 i & -8 + 6 i\\7 - 6 i & 7 - 3 i & 1 + 10 i\\-4 - 2 i & 8 + 10 i & -9 + 7 i\end{array}\right]
