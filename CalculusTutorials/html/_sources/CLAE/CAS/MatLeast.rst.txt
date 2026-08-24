:index:`Least Squares`
======================

The two options for the Least Squares process differ only in the form of the input.  The ``Ax = b`` form assumes that the matrix is a coefficient matrix and that there is another vector in the CAS that represents b.  The ``[A b]`` form assumes that the matrix is an augmented matrix.

:index:`Least Squares Ax = b Form`
----------------------------------

The ``Ax = b`` form assumes that the matrix is a coefficient matrix and that there is another vector in the CAS that represents b.  When this option is selected a dialog box will appear asking the user to select the CAS designation for the vector b.  For example, say we have the matrix and b vector in the CAS as,

.. math::
    A = \left[\begin{array}{ccc}1 & 1 & 2\\2 & 0 & -1\\-1 & 1 & 0\\0 & 2 & -1\end{array}\right]
    \qquad
    \mathbf{b} = \left[\begin{array}{c}3\\9\\9\\3\end{array}\right]

the result of the Least Squares process is,

.. math::
    \mathbf{x} = \left[\begin{array}{c}2\\3\\-1\end{array}\right]


:index:`Least Squares [A b] Form`
---------------------------------

The ``[A b]`` form assumes that the matrix is an augmented matrix. For example, say we have the matrix,

.. math::
    \left[\begin{array}{cccc}1 & 1 & 2 & 3\\2 & 0 & -1 & 9\\-1 & 1 & 0 & 9\\0 & 2 & -1 & 3\end{array}\right]

the result of the Least Squares process is,

.. math::
    \mathbf{x} = \left[\begin{array}{c}2\\3\\-1\end{array}\right]

