:index:`Surface of Revolution`
==============================

Description
-----------

This is really a convince type since a surface of revolution can be created parametrically.  Since surfaces of revolution tend to be studied in an integral calculus class before parametric surfaces we included this type to make the plotting easier for the user.

This will take a single variable function in either ``x``, ``y``, or ``z`` and create a surface by rotating it around an axis of rotation that is parallel to a coordinate axis and in a coordinate plane.  That is, axes of the form :math:`x = a`, :math:`y = a`, or :math:`z = a`.

To create a surface of revolution, input a function in a single variable, either ``x``, ``y``, or ``z`` and not contain any other variables in the set of 3D variables (``x``, ``y``, ``z``, ``p``, ``t``, ``u``, and ``v``). All other variables outside this set are considered constants.

Insert/Edit Dialog
------------------

The Insert/Edit Dialog for this type is shown below.

.. figure:: Images/SRev_dialog.png
    :alt: Surface of Revolution Dialog Box

    Surface of Revolution Dialog Box


This type has a lot of options mainly due to the scope of surfaces that can be created. The first input is for the expression then there are options for, the independent variable, dependent variable, axis of revolution, start and end values along the function, start and end values of the rotation angle, the number of divisions along the function and over the rotation, clipping, plot object, mesh color, shading mode and smooth shading.

Options
-------

Independent Variable
^^^^^^^^^^^^^^^^^^^^

This is the independent variable for the function.  This option is only used if the function is a constant function and the independent variable cannot be determined from the expression.  If the independent variable can be determined from the expression then that variable is used and overrides any setting of this option.  For example, if the expression is ``sin(x)`` then ``x`` is taken as the independent variable.  On the other hand, if the expression is ``3`` then the setting of this option will be takes as the independent variable.

Dependent Variable
^^^^^^^^^^^^^^^^^^

This is the dependent variable for the function.  Since we could view :math:`\sin(x)` as :math:`y = \sin(x)` or :math:`z = \sin(x)` we need to know the dependent variable.

Axis of Revolution
^^^^^^^^^^^^^^^^^^

This is the equation of the line that the curve is rotated about.  It can have the form :math:`x = a`, :math:`y = a`, or :math:`z = a`.  The value ``a`` can be any legitimate expression that evaluates to a real number.  For example, ``y = 0`` is the x-axis.

Function Start Value
^^^^^^^^^^^^^^^^^^^^

This is the starting value along the function for the surface.

Function End Value
^^^^^^^^^^^^^^^^^^

This is the ending value along the function for the surface.

Rotation Start Value
^^^^^^^^^^^^^^^^^^^^

This is the starting angular value of rotation for the surface.  This allows the user to only graph a portion of the rotation if they wish.

Rotation End Value
^^^^^^^^^^^^^^^^^^

This is the ending angular value of rotation for the surface. This allows the user to only graph a portion of the rotation if they wish.

Function Range Divisions
^^^^^^^^^^^^^^^^^^^^^^^^

This is the number of divisions of the range along the function.

Rotation Divisions
^^^^^^^^^^^^^^^^^^

This is the number of divisions of the angular range.

Clip Values to View
^^^^^^^^^^^^^^^^^^^^

.. include:: clipping3d.md

Plot
^^^^

.. include:: plotObjects3d.md

Surface Mesh Color
^^^^^^^^^^^^^^^^^^

.. include:: meshcolor.md

Surface Shading
^^^^^^^^^^^^^^^

.. include:: shading3d.md

Smooth Shading
^^^^^^^^^^^^^^

.. include:: smoothshading3d.md


Examples
--------

:math:`y = \sin(x)` About the X-Axis
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The the function was graphed on :math:`[0, \pi]`.

.. figure:: Images/SRev001.png
    :alt: y = sin(x) About the X-Axis

    :math:`y = \sin(x)` About the X-Axis


:math:`y = \sin(x)` About the Axis :math:`y = 2`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The the function was graphed on :math:`[0, \pi]`.

.. figure:: Images/SRev002.png
    :alt: y = sin(x) About y = 2

    :math:`y = \sin(x)` About the Axis :math:`y = 2`


:math:`z = \sin(x)` About the Axis :math:`z = 2`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The the function was graphed on :math:`[0, \pi]`.

.. figure:: Images/SRev003.png
    :alt: y = sin(x) About z = 2

    :math:`y = \sin(x)` About the Axis :math:`z = 2`

