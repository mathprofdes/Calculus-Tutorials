:index:`Euler's Method Curve`
=============================

Description
-----------

**Euler's Method** is a way to approximate the solution to the initial-value problem, :math:`y' = f(x, y)` where the initial value is :math:`(x_0, y_0) = (x_0, y(x_0))`, the step size is :math:`h`, :math:`x_n = x_{n-1} + h` and :math:`y_n = y_{n-1} + hf(x_{n-1}, y_{n-1})`.  Another way to view this is as a flow curve through a vector field that is defined as a direction field or slope field for the function, :math:`f(x, y)`.

Like the direction field, the input for this type is the function :math:`f(x, y)` or :math:`f(t, y)`.


Insert/Edit Dialog
------------------

The Insert/Edit Dialog for the Euler's Method curve is shown below.

.. figure:: Images/EMC_dialog.png
    :alt: Euler's Method Curve Properties Dialog

    Euler's Method Curve Properties Dialog


The first input is the function :math:`f(x, y)`, after that are options for the initial point, delta x, number of steps, direction, line width, points to include, and the point size.

Options
-------

Initial Point
^^^^^^^^^^^^^

This is the point of origin for the curve, in the language above, it is the point :math:`(x_0, y_0) = (x_0, y(x_0))`.  This is a list of two expressions that must evaluate to a real number but can include constants, so any valid expression that does not include the variables ``x``, ``t``, and ``y``.  It is common to set this to ``[a, b]``, then two sliders will be created (one for ``a`` and one for ``b``) then the user can move the sliders to change the initial point and see the change in the curve in real time.

Delta X
^^^^^^^

This is the step size, :math:`h` in the above definition.  This can be any valid expression that does not include the variables ``x``, ``t``, and ``y`` but can include constants. The smaller this is the better the approximation but also the more steps needed to cover the same range.

Number of Steps
^^^^^^^^^^^^^^^

This is the number of steps that are done in the method.  If the curve ends prematurely simply increase this value to extend the curve.  This is the number of steps that are taken in each direction from the initial point.

Direction
^^^^^^^^^

There are three options for the direction.

- **Forward:** Only plots the curve in the forward direction, that is, :math:`h > 0`.
- **Backward:** Only plots the curve in the backward direction, that is, :math:`h < 0`.
- **Both Forward and Backward:** Plots both directions.

Line Width
^^^^^^^^^^

.. include:: linewidth.md

Include Points
^^^^^^^^^^^^^^

This determines which points to include in the plot.

- **No Points:** Does not plot any points, just the line.
- **Initial Point:** Plots just the initial point for the curve.
- **All Points:** Plots all points used in the approximation of the curve.

Point Size
^^^^^^^^^^

The size of the points that are plotted, if any are selected.

Example
-------

Say we use the example above of :math:`f(x, y) = x^{2} + y^{2} - 1`.  If we graph the Euler's Method curve with initial point :math:`(0, 0)` we get,

.. figure:: Images/EMC001.png
    :alt: Euler's Method Curve

    Euler's Method Curve

If we also include the direction field for this function we see the image,

.. figure:: Images/EMC002.png
    :alt: Euler's Method Curve with Direction Field

    Euler's Method Curve with Direction Field

Changing the initial point to :math:`(a, b)`, include the initial point in the plot, and move the sliders to :math:`(0.2, 0.6)` we get,

.. figure:: Images/EMC003.png
    :alt: Euler's Method Curve with Direction Field and Initial Point

    Euler's Method Curve with Direction Field and Initial Point

If we then include all points we see,

.. figure:: Images/EMC004.png
    :alt: Euler's Method Curve with Direction Field and All Points

    Euler's Method Curve with Direction Field and All Points

Finally, if we just plot the forward direction, include only the initial point, and move the sliders a bit we see,

.. figure:: Images/EMC005.png
    :alt: Euler's Method Curve, Forward Direction Only

    Euler's Method Curve, Forward Direction Only

