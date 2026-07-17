:index:`Other Matrix Operations`
================================

This set of matrix operations are ones that may be of interest depending on what areas of linear algebra are being studied.

:index:`Permanent`
------------------

This option returns the permanent of a matrix. Unlike determinant, permanent is defined for both square and non-square matrices.  For an :math:`m \times n` matrix, with :math:`m` less than or equal to :math:`n`, it is given as the sum over the permutations :math:`s` of size less than or equal to :math:`m` on :math:`[1, 2, \ldots, n]` of the product from :math:`i = 1` to :math:`m` of :math:`M[i, s[i]]`. Taking the transpose will not affect the value of the permanent.  In the case of a square matrix, this is the same as the permutation definition of the determinant, but it does not take the sign of the permutation into account.  For example, the permanent of

.. math::
    \left[\begin{array}{ccc}-8 & -1 & 10\\-8 & 9 & -10\\3 & 10 & 6\end{array}\right]

is :math:`-84`, and the permanent of

.. math::
    \left[\begin{array}{ccccc}6 & -9 & -1 & 10 & 6\\9 & -3 & -7 & 5 & -7\\4 & -1 & 7 & -4 & 4\end{array}\right]

is :math:`-854`, which is the same as the permanent of

.. math::
    \left[\begin{array}{ccc}6 & 9 & 4\\-9 & -3 & -1\\-1 & -7 & 7\\10 & 5 & -4\\6 & -7 & 4\end{array}\right]


:index:`Pseudo-Inverse`
-----------------------

The pseudo-inverse, sometimes called a one-sided inverse, of a non-square matrix :math:`A` is a matrix :math:`B` such that either :math:`BA = I` or :math:`BA = I`.  If the matrix is square and invertible, the pseudo-inverse is the same as the inverse. If the matrix is square but not invertible the pseudo-inverse operation will return a result but the familiar properties will not hold. For example, the pseudo-inverse of

.. math::
    \left[\begin{array}{ccccc}6 & -9 & -1 & 10 & 6\\9 & -3 & -7 & 5 & -7\\4 & -1 & 7 & -4 & 4\end{array}\right]

is

.. math::
    \left[\begin{array}{ccc}- \frac{1953}{426464} & \frac{14123}{213232} & \frac{34323}{426464}\\- \frac{14991}{426464} & - \frac{11}{213232} & - \frac{2835}{426464}\\- \frac{185}{426464} & - \frac{3357}{213232} & \frac{26507}{426464}\\\frac{9747}{213232} & - \frac{1209}{106616} & - \frac{11129}{213232}\\\frac{18023}{426464} & - \frac{10669}{213232} & \frac{2939}{426464}\end{array}\right]

Note that

.. math::
    \left[\begin{array}{ccccc}6 & -9 & -1 & 10 & 6\\9 & -3 & -7 & 5 & -7\\4 & -1 & 7 & -4 & 4\end{array}\right]     \left[\begin{array}{ccc}- \frac{1953}{426464} & \frac{14123}{213232} & \frac{34323}{426464}\\- \frac{14991}{426464} & - \frac{11}{213232} & - \frac{2835}{426464}\\- \frac{185}{426464} & - \frac{3357}{213232} & \frac{26507}{426464}\\\frac{9747}{213232} & - \frac{1209}{106616} & - \frac{11129}{213232}\\\frac{18023}{426464} & - \frac{10669}{213232} & \frac{2939}{426464}\end{array}\right] = \left[\begin{array}{ccc}1 & 0 & 0\\0 & 1 & 0\\0 & 0 & 1\end{array}\right]


:index:`Trace`
--------------

The trace of a square matrix is simply the sum of entries on the main diagonal.  In general, this is easy to calculate but if you have a matrix that is complicated this option may be useful. For example, the trace of,

.. math::
    \left[\begin{array}{ccc}-8 & -1 & 10\\-8 & 9 & -10\\3 & 10 & 6\end{array}\right]

is 7.


:index:`Iterate`
----------------

This option is for examining repeated applications of a matrix transformation.  Specifically, if the user selects a square matrix :math:`A` and inputs a vector :math:`\mathbf{x}` this option will return the list,

.. math::
    \left[ \mathbf{x}, A\mathbf{x}, A^2\mathbf{x}, A^3\mathbf{x}, \ldots, A^n\mathbf{x} \right]

When this option is selected a dialog box will appear asking the user to input an initial vector or matrix and the number of iterations to do.  The initial vector can be input as a list of entries or as a CAS workspace designation.  The input can be either a column vector or a matrix as long as the number of rows of the initial vector or matrix matches the number of columns of the matrix :math:`A.`

For example, if the selected matrix is

.. math::
    \left[\begin{array}{cc}1 & 3\\2 & 4\end{array}\right]

and the initial vector is

.. math::
    \left[\begin{array}{c}1\\-1\end{array}\right]

then 10 iterations returns,

.. math::
    \left[ \left[\begin{array}{c}1\\-1\end{array}\right], \  \left[\begin{array}{c}-2\\-2\end{array}\right], \  \left[\begin{array}{c}-8\\-12\end{array}\right], \  \left[\begin{array}{c}-44\\-64\end{array}\right], \  \left[\begin{array}{c}-236\\-344\end{array}\right], \  \left[\begin{array}{c}-1268\\-1848\end{array}\right], \  \left[\begin{array}{c}-6812\\-9928\end{array}\right], \  \left[\begin{array}{c}-36596\\-53336\end{array}\right], \  \left[\begin{array}{c}-196604\\-286536\end{array}\right], \  \left[\begin{array}{c}-1056212\\-1539352\end{array}\right], \  \left[\begin{array}{c}-5674268\\-8269832\end{array}\right]\right]

In addition, if we use the same matrix and the initial matrix is,

.. math::
    \left[\begin{array}{ccc}1 & 3 & 5\\2 & 4 & 6\end{array}\right]

then 5 iterations returns,

.. math::
    \left[ \left[\begin{array}{ccc}1 & 3 & 5\\2 & 4 & 6\end{array}\right], \  \left[\begin{array}{ccc}7 & 15 & 23\\10 & 22 & 34\end{array}\right], \  \left[\begin{array}{ccc}37 & 81 & 125\\54 & 118 & 182\end{array}\right], \  \left[\begin{array}{ccc}199 & 435 & 671\\290 & 634 & 978\end{array}\right], \  \left[\begin{array}{ccc}1069 & 2337 & 3605\\1558 & 3406 & 5254\end{array}\right], \  \left[\begin{array}{ccc}5743 & 12555 & 19367\\8370 & 18298 & 28226\end{array}\right]\right]

