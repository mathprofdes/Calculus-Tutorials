:index:`General Vector Operations`
==================================

For most operations, *except arithmetic*, a vector can be represented by either a column vector or a list.  For example, the following would be seen as the vector :math:`(1, 2, 3)`.

.. math::
    \left[ 1, \  2, \  3\right] \qquad \left[\begin{array}{c}1\\2\\3\end{array}\right]

:index:`Vector Arithmetic`
--------------------------

For vector arithmetic the vectors must be represented by column vectors (that is, n X 1 matrices).  Since vectors are just special sized matrices any operation valid for n X 1 matrices is valid for vectors.

Arithmetic operations of ``+``, ``-``, and ``*`` can be done on vectors as long as the operation is defined on the vectors in the expression.  To do these, first input the vectors into the CAS workspace and then use their designations (R1, R2, ...) to input the arithmetic expression into the CAS input bar.

For example, say we have the two vectors,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{c}4\\5\\6\end{array}\right]

in the CAS workspace as ``R1`` and ``R2`` respectively.

Then ``R1+R2`` returns,

.. math::
    \left[\begin{array}{c}5\\7\\9\end{array}\right]

``R1-R2`` returns,

.. math::
    \left[\begin{array}{c}-3\\-3\\-3\end{array}\right]

``5*R1`` returns,

.. math::
    \left[\begin{array}{c}5\\10\\15\end{array}\right]

``5*R1 - 7*R2`` returns,

.. math::
    \left[\begin{array}{c}-23\\-25\\-27\end{array}\right]

:index:`Length`
---------------

This finds the 2-norm of the selected vector. For example, say we have the following vector,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]

its real 2-norm is, :math:`\sqrt{14}`.

Say we have the following vector,

.. math::
    \left[\begin{array}{c}x\\y\\z\end{array}\right]

its real 2-norm is, :math:`\sqrt{x^{2} + y^{2} + z^{2}}`.

:index:`Normalize`
------------------

This normalizes the selected vector using the real 2-norm.  For example, say we have the following vector,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]

its 2-norm normalization is, :math:`\sqrt{14}`.

.. math::
    \left[\begin{array}{c}\frac{\sqrt{14}}{14}\\\frac{\sqrt{14}}{7}\\\frac{3 \sqrt{14}}{14}\end{array}\right]

Say we have the following vector,

.. math::
    \left[\begin{array}{c}x\\y\\z\end{array}\right]

its 2-norm normalization is,

.. math::
    \left[\begin{array}{c}\frac{x}{\sqrt{x^{2} + y^{2} + z^{2}}}\\\frac{y}{\sqrt{x^{2} + y^{2} + z^{2}}}\\\frac{z}{\sqrt{x^{2} + y^{2} + z^{2}}}\end{array}\right]


:index:`Dot Product`
--------------------

To calculate a dot (or scalar) product of two vectors, select one of the vectors, then select this option, a dialog box will appear asking the user to select the second vector using its CAS designation.  Once that is selected the program will return the dot product of the two vectors. For example, say we have the two vectors,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{c}4\\5\\6\end{array}\right]

The dot product of these returns 32.

:index:`Cross Product`
----------------------

To calculate a dot (or vector) product of two three-dimensional vectors :math:`u \times v`, select the first vector :math:`u`, then select this option, a dialog box will appear asking the user to select the second vector using its CAS designation, select the vector :math:`v` from this list.  Once that is selected the program will return the cross product of the two vectors. For example, say we have the two vectors,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{c}4\\5\\6\end{array}\right]

The cross product of these (in the order given) returns,

.. math::
    \left[\begin{array}{c}-3\\6\\-3\end{array}\right]


:index:`Distance`
-----------------

To calculate the distance between two vectors as points, select one of the vectors, then select this option, a dialog box will appear asking the user to select the second vector using its CAS designation.  Once that is selected the program will return the distance between the two vectors. For example, say we have the two vectors,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{c}4\\5\\6\end{array}\right]

The distance between these returns :math:`3 \sqrt{3}`.


:index:`Angle`
--------------

To calculate the angle between two vectors in radians, select one of the vectors, then select this option, a dialog box will appear asking the user to select the second vector using its CAS designation.  Once that is selected the program will return the angle between the two vectors. For example, say we have the two vectors,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{c}4\\5\\6\end{array}\right]

The angle between these returns :math:`\operatorname{acos}{\left(\frac{16 \sqrt{22}}{77} \right)} \approx 0.225726128552734`.
