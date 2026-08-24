:index:`Matrix Reduction and System Solving`
============================================

These options are for reducing matrices and obtaining parametric/vector form solutions to a linear system given as a matrix.

:index:`Echelon Form`
---------------------

This option returns an echelon form of the given matrix that is row equivalent to the original. This option will not divide entries by expressions containing variables, hence it avoids the possibility of division by 0.

For example, if we have the matrix,

.. math::
    \left[\begin{array}{cccc}1 & 2 & -6 & 9\\10 & 6 & -2 & -10\\8 & -6 & 0 & -5\end{array}\right]

this option will return the matrix,

.. math::
    \left[\begin{array}{cccc}1 & 2 & -6 & 9\\0 & -14 & 58 & -100\\0 & 0 & 604 & -1122\end{array}\right]

Also, if we have the matrix,

.. math::
    \left[\begin{array}{cccc}1 & 2 x & -6 & 9 x^{3}\\10 y & 6 \sin{\left(x \right)} & - 2 t & -10\\8 z & - 6 \cos{\left(y \right)} & 0 & - 5 t^{2}\end{array}\right]

this option will return the matrix,

.. math::
    \left[\begin{array}{cccc}1 & 2 x & -6 & 9 x^{3}\\0 & - 20 x y + 6 \sin{\left(x \right)} & - 2 t + 60 y & - 90 x^{3} y - 10\\0 & 0 & - 32 t x z - 12 t \cos{\left(y \right)} + 360 y \cos{\left(y \right)} + 288 z \sin{\left(x \right)} & 100 t^{2} x y - 30 t^{2} \sin{\left(x \right)} - 540 x^{3} y \cos{\left(y \right)} - 432 x^{3} z \sin{\left(x \right)} - 160 x z - 60 \cos{\left(y \right)}\end{array}\right]

:index:`Reduced Echelon Form`
-----------------------------

This option returns the reduced echelon form of the given matrix that is row equivalent to the original. This option will divide entries by expressions containing variables, hence it is assumed that these expressions are not 0.

For example, if we have the matrix,

.. math::
    \left[\begin{array}{cccc}1 & 2 & -6 & 9\\10 & 6 & -2 & -10\\8 & -6 & 0 & -5\end{array}\right]

this option will return the matrix,

.. math::
    \left[\begin{array}{cccc}1 & 0 & 0 & - \frac{157}{151}\\0 & 1 & 0 & - \frac{167}{302}\\0 & 0 & 1 & - \frac{561}{302}\end{array}\right]

Also, if we have the matrix,

.. math::
    \left[\begin{array}{cccc}1 & 2 x & -6 & 9 x^{3}\\10 y & 6 \sin{\left(x \right)} & - 2 t & -10\\8 z & - 6 \cos{\left(y \right)} & 0 & - 5 t^{2}\end{array}\right]

this option will return the matrix,

.. math::
    \left[\begin{array}{cccc}1 & 0 & 0 & \frac{- 5 t^{3} x + 45 t^{2} \sin{\left(x \right)} + 27 t x^{3} \cos{\left(y \right)} + 90 \cos{\left(y \right)}}{8 t x z + 3 t \cos{\left(y \right)} - 90 y \cos{\left(y \right)} - 72 z \sin{\left(x \right)}}\\0 & 1 & 0 & \frac{5 t^{3} - 150 t^{2} y + 72 t x^{3} z + 240 z}{16 t x z + 6 t \cos{\left(y \right)} - 180 y \cos{\left(y \right)} - 144 z \sin{\left(x \right)}}\\0 & 0 & 1 & \frac{- 50 t^{2} x y + 15 t^{2} \sin{\left(x \right)} + 270 x^{3} y \cos{\left(y \right)} + 216 x^{3} z \sin{\left(x \right)} + 80 x z + 30 \cos{\left(y \right)}}{16 t x z + 6 t \cos{\left(y \right)} - 180 y \cos{\left(y \right)} - 144 z \sin{\left(x \right)}}\end{array}\right]


:index:`Solve System`
---------------------

This will solve the system of equations given as an augmented matrix and output the solution in general solution vector form or sometimes as a set.

For example, if we have the matrix,

.. math::
    \left[\begin{array}{cccc}3 & -1 & -9 & -9\\-5 & 10 & -8 & 8\\-3 & 0 & 10 & 5\end{array}\right]

this option will return,

.. math::
    \left[\begin{array}{c}\frac{15}{2}\\\frac{27}{4}\\\frac{11}{4}\end{array}\right]


Also, if we have the matrix,

.. math::
    \left[\begin{array}{cccccc}8 & 2 & 6 & 1 & -3 & -9\\2 & 2 & -1 & -6 & 2 & -3\\-9 & -5 & 1 & -2 & -9 & -5\end{array}\right]

this option will return,

.. math::
    \left[\begin{array}{c}- \frac{217 x_{4}}{38} - \frac{71 x_{5}}{38} + \frac{193}{38}\\\frac{405 x_{4}}{38} + \frac{77 x_{5}}{38} - \frac{349}{38}\\\frac{74 x_{4}}{19} + \frac{44 x_{5}}{19} - \frac{99}{19}\\x_{4}\\x_{5}\end{array}\right]

