:index:`2-D Transformations`
============================

The 2-D Transformation Matrices options are a submenu under ``Edit > 2-D Transformations`` of the main program menu.


:index:`Scaling Matrix`
-----------------------

When this item is selected a dialog box will appear allowing the user to input the x and y scaling factors for the matrix.  For example, if the user inputs a and b for these respectively the result is,

.. math::

    \left[\begin{array}{cc}a & 0\\0 & b\end{array}\right]


:index:`Rotation Matrix`
------------------------

When this item is selected a dialog box will appear allowing the user to input the rotation angle for the matrix.  For example, if the user inputs a for this the result is,

.. math::

    \left[\begin{array}{cc}\cos{\left(a \right)} & - \sin{\left(a \right)}\\\sin{\left(a \right)} & \cos{\left(a \right)}\end{array}\right]


:index:`Reflection over the x-Axis`
-----------------------------------

The result of this is the 2-dimensional x-axis reflection matrix.

.. math::

    \left[\begin{array}{cc}1 & 0\\0 & -1\end{array}\right]


:index:`Reflection over the y-Axis`
-----------------------------------

The result of this is the 2-dimensional y-axis reflection matrix.

.. math::

    \left[\begin{array}{cc}-1 & 0\\0 & 1\end{array}\right]


:index:`Reflection over y = x`
------------------------------

The result of this is the 2-dimensional y = x reflection matrix.

.. math::

    \left[\begin{array}{cc}0 & 1\\1 & 0\end{array}\right]


:index:`Reflection over y = -x`
-------------------------------

The result of this is the 2-dimensional y = -x reflection matrix.

.. math::

    \left[\begin{array}{cc}0 & -1\\-1 & 0\end{array}\right]


:index:`Reflection over the Origin`
-----------------------------------

The result of this is the 2-dimensional reflection over the origin matrix.

.. math::

    \left[\begin{array}{cc}-1 & 0\\0 & -1\end{array}\right]

:index:`Horizontal Shear`
-------------------------

When this item is selected a dialog box will appear allowing the user to input the shear factor.  For example, if the user inputs a for this the result is,

.. math::

    \left[\begin{array}{cc}1 & a\\0 & 1\end{array}\right]


:index:`Vertical Shear`
-----------------------

When this item is selected a dialog box will appear allowing the user to input the shear factor.  For example, if the user inputs a for this the result is,

.. math::

    \left[\begin{array}{cc}1 & 0\\a & 1\end{array}\right]
