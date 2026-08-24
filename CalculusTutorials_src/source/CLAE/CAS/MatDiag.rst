:index:`Diagonalization`
========================

:index:`Diagonalize Matrix`
---------------------------

Given a square matrix A, this option will return the diagonal matrix D and invertible matrix P such that :math:`A = PDP^{-1}` if D and P exist.  If A is not a diagonalizable matrix, and hence D and P do not exist, the program will return an error.  For example, say we have the matrix,

.. math::
    \left[\begin{array}{ccc}-7 & -16 & 4\\6 & 13 & -2\\12 & 16 & 1\end{array}\right]

If we select this option we get,

.. math::
    P = \left[\begin{array}{ccc}-2 & -4 & 1\\1 & 3 & 0\\2 & 0 & 3\end{array}\right]
    \qquad
    D = \left[\begin{array}{ccc}-3 & 0 & 0\\0 & 5 & 0\\0 & 0 & 5\end{array}\right]

and computing :math:`PDP^{-1}` gives the original matrix.

As another example, say we start with the matrix,

.. math::
    \left[\begin{array}{ccc}2 & 4 & 3\\-4 & -6 & -3\\3 & 3 & 1\end{array}\right]

Selecting this option will return an error since the matrix is not diagonalizable.  If we look at the eigenvalues and the eigenvectors of this matrix we see that there are two eigenvalues, 1 and :math:`-2`, the eigenvalue :math:`-2` has multiplicity 2 but its associated eigenspace is only one dimensional, so the matrix P does not exist.


:index:`Singular Value Decomposition`
-------------------------------------

This option returns a singular value decomposition of the matrix.  Specifically, it returns three matrices, U, S and V with :math:`A = USV^H`, where :math:`V^H` is the Hermite conjugation of V, which is a fancy way to say the conjugate transpose (or adjoint) of V.  The singular value decomposition of the matrix can be computationally intensive and hence take a while for the calculation to complete, even on relatively small matrices.

For example, say we start with

.. math::
    \left[\begin{array}{ccc}3 & 5 & 3\\-7 & -8 & 3\end{array}\right]

the singular value decomposition returns,

.. math::
    U = \left[\begin{array}{cc}\frac{\frac{79}{104} + \frac{\sqrt{17057}}{104}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} & \frac{\frac{79}{104} - \frac{\sqrt{17057}}{104}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}}\\\frac{1}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} & \frac{1}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}}\end{array}\right]

.. math::
    S = \left[\begin{array}{cc}\sqrt{\frac{165}{2} - \frac{\sqrt{17057}}{2}} & 0\\0 & \sqrt{\frac{\sqrt{17057}}{2} + \frac{165}{2}}\end{array}\right]

.. math::
    V = \left[\begin{array}{cc}\frac{- \frac{7}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} + \frac{\frac{237}{104} + \frac{3 \sqrt{17057}}{104}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}}}{\sqrt{\frac{165}{2} - \frac{\sqrt{17057}}{2}}} & \frac{- \frac{7}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{\frac{237}{104} - \frac{3 \sqrt{17057}}{104}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}}}{\sqrt{\frac{\sqrt{17057}}{2} + \frac{165}{2}}}\\\frac{- \frac{8}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} + \frac{\frac{395}{104} + \frac{5 \sqrt{17057}}{104}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}}}{\sqrt{\frac{165}{2} - \frac{\sqrt{17057}}{2}}} & \frac{- \frac{8}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{\frac{395}{104} - \frac{5 \sqrt{17057}}{104}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}}}{\sqrt{\frac{\sqrt{17057}}{2} + \frac{165}{2}}}\\\frac{\frac{3}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} + \frac{\frac{237}{104} + \frac{3 \sqrt{17057}}{104}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}}}{\sqrt{\frac{165}{2} - \frac{\sqrt{17057}}{2}}} & \frac{\frac{\frac{237}{104} - \frac{3 \sqrt{17057}}{104}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{3}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}}}{\sqrt{\frac{\sqrt{17057}}{2} + \frac{165}{2}}}\end{array}\right]

If we compute :math:`A = USV^H` we get the following which miraculously simplifies to the original matrix.

.. math::
    \left[\begin{array}{ccc}\frac{\left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right) \left(- \frac{7}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} + \frac{\frac{237}{104} + \frac{3 \sqrt{17057}}{104}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}}\right)}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} + \frac{\left(\frac{79}{104} - \frac{\sqrt{17057}}{104}\right) \left(- \frac{7}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{\frac{237}{104} - \frac{3 \sqrt{17057}}{104}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}}\right)}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} & \frac{\left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right) \left(- \frac{8}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} + \frac{\frac{395}{104} + \frac{5 \sqrt{17057}}{104}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}}\right)}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} + \frac{\left(\frac{79}{104} - \frac{\sqrt{17057}}{104}\right) \left(- \frac{8}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{\frac{395}{104} - \frac{5 \sqrt{17057}}{104}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}}\right)}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} & \frac{\left(\frac{79}{104} - \frac{\sqrt{17057}}{104}\right) \left(\frac{\frac{237}{104} - \frac{3 \sqrt{17057}}{104}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{3}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}}\right)}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{\left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right) \left(\frac{3}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} + \frac{\frac{237}{104} + \frac{3 \sqrt{17057}}{104}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}}\right)}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}}\\\frac{- \frac{7}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{\frac{237}{104} - \frac{3 \sqrt{17057}}{104}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{- \frac{7}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} + \frac{\frac{237}{104} + \frac{3 \sqrt{17057}}{104}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} & \frac{- \frac{8}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{\frac{395}{104} - \frac{5 \sqrt{17057}}{104}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{- \frac{8}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} + \frac{\frac{395}{104} + \frac{5 \sqrt{17057}}{104}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} & \frac{\frac{\frac{237}{104} - \frac{3 \sqrt{17057}}{104}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{3}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}}}{\sqrt{\left(- \frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2} + 1}} + \frac{\frac{3}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}} + \frac{\frac{237}{104} + \frac{3 \sqrt{17057}}{104}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}}}{\sqrt{1 + \left(\frac{79}{104} + \frac{\sqrt{17057}}{104}\right)^{2}}}\end{array}\right]

:index:`Singular Values`
------------------------

This option returns a singular values of the matrix.  The singular values of the matrix can be computationally intensive and hence take a while for the calculation to complete, even on relatively small matrices.

For example, the singular values of

.. math::
    \left[\begin{array}{ccc}3 & 5 & 3\\-7 & -8 & 3\end{array}\right]

are

.. math::
    \left[ \sqrt{\frac{\sqrt{17057}}{2} + \frac{165}{2}}, \  \sqrt{\frac{165}{2} - \frac{\sqrt{17057}}{2}}, \  0\right]

As another example, the singular values of

.. math::
    \left[\begin{array}{ccc}-8 & -1 & 10\\-8 & 9 & -10\\3 & 10 & 6\end{array}\right]

are

.. math::
    \left[ \sqrt{185 + \frac{5537}{3 \sqrt[3]{37560 + \frac{\sqrt{394995125859} i}{9}}} + \sqrt[3]{37560 + \frac{\sqrt{394995125859} i}{9}}}, \  \sqrt{185 + \frac{5537}{\left(- \frac{3}{2} + \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{37560 + \frac{\sqrt{394995125859} i}{9}}} + \left(- \frac{1}{2} + \frac{\sqrt{3} i}{2}\right) \sqrt[3]{37560 + \frac{\sqrt{394995125859} i}{9}}}, \  \sqrt{185 + \left(- \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \sqrt[3]{37560 + \frac{\sqrt{394995125859} i}{9}} + \frac{5537}{\left(- \frac{3}{2} - \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{37560 + \frac{\sqrt{394995125859} i}{9}}}}\right]
