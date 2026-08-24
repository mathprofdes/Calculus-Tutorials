:index:`3-D Transformations`
============================

The 3-D Transformation Matrices options are a submenu under ``Edit > 3-D Transformations`` of the main program menu.


:index:`Scaling Matrix`
-----------------------

When this item is selected a dialog box will appear allowing the user to input the x, y, and z scaling factors for the matrix.  For example, if the user inputs a, b, and c for these respectively the result is,

.. math::

    \left[\begin{array}{ccc}a & 0 & 0\\0 & b & 0\\0 & 0 & c\end{array}\right]

:index:`Rotation Matrix About the X-Axis`
-----------------------------------------

When this item is selected a dialog box will appear allowing the user to input the rotation angle for the matrix.  For example, if the user inputs a for this the result is,

.. math::

    \left[\begin{array}{ccc}1 & 0 & 0\\0 & \cos{\left(a \right)} & - \sin{\left(a \right)}\\0 & \sin{\left(a \right)} & \cos{\left(a \right)}\end{array}\right]


:index:`Rotation Matrix About the Y-Axis`
-----------------------------------------

When this item is selected a dialog box will appear allowing the user to input the rotation angle for the matrix.  For example, if the user inputs a for this the result is,

.. math::

    \left[\begin{array}{ccc}\cos{\left(a \right)} & 0 & \sin{\left(a \right)}\\0 & 1 & 0\\- \sin{\left(a \right)} & 0 & \cos{\left(a \right)}\end{array}\right]

:index:`Rotation Matrix About the Z-Axis`
-----------------------------------------

When this item is selected a dialog box will appear allowing the user to input the rotation angle for the matrix.  For example, if the user inputs a for this the result is,

.. math::

    \left[\begin{array}{ccc}\cos{\left(a \right)} & - \sin{\left(a \right)} & 0\\\sin{\left(a \right)} & \cos{\left(a \right)} & 0\\0 & 0 & 1\end{array}\right]

:index:`Rotation Matrix About (x, y, z)`
----------------------------------------

When this item is selected a dialog box will appear allowing the user to input the vector to rotate about and the rotation angle for the matrix.  For example, if the user inputs x, y, z for the vector and a for the angle the result is,

.. math::

    \left[\begin{array}{ccc}x^{2} \left(1 - \cos{\left(a \right)}\right) + \cos{\left(a \right)} & x y \left(1 - \cos{\left(a \right)}\right) - z \sin{\left(a \right)} & x z \left(1 - \cos{\left(a \right)}\right) + y \sin{\left(a \right)}\\x y \left(1 - \cos{\left(a \right)}\right) + z \sin{\left(a \right)} & y^{2} \left(1 - \cos{\left(a \right)}\right) + \cos{\left(a \right)} & - x \sin{\left(a \right)} + y z \left(1 - \cos{\left(a \right)}\right)\\x z \left(1 - \cos{\left(a \right)}\right) - y \sin{\left(a \right)} & x \sin{\left(a \right)} + y z \left(1 - \cos{\left(a \right)}\right) & z^{2} \left(1 - \cos{\left(a \right)}\right) + \cos{\left(a \right)}\end{array}\right]

:index:`Reflection over the xy-Plane`
-------------------------------------

The result of this is the 3-dimensional xy-plane reflection matrix.

.. math::

    \left[\begin{array}{ccc}1 & 0 & 0\\0 & 1 & 0\\0 & 0 & -1\end{array}\right]


:index:`Reflection over the xz-Plane`
-------------------------------------

The result of this is the 3-dimensional xz-plane reflection matrix.

.. math::

    \left[\begin{array}{ccc}1 & 0 & 0\\0 & -1 & 0\\0 & 0 & 1\end{array}\right]


:index:`Reflection over the yz-Plane`
-------------------------------------

The result of this is the 3-dimensional yz-plane reflection matrix.

.. math::

    \left[\begin{array}{ccc}-1 & 0 & 0\\0 & 1 & 0\\0 & 0 & 1\end{array}\right]


:index:`Reflection over the Origin`
-----------------------------------

The result of this is the 3-dimensional reflection over the origin matrix.

.. math::

    \left[\begin{array}{ccc}-1 & 0 & 0\\0 & -1 & 0\\0 & 0 & -1\end{array}\right]

