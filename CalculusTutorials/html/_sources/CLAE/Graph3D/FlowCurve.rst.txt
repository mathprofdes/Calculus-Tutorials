:index:`Flow Curve`
===================

Description
-----------

A flow curve through a vector field :math:`F = (f(x, y, z), g(x, y, z), h(x, y, z))` is an approximation of how a particle would move through a vector field (or force field), much like an Euler's Method curve through a direction field in 2D.  Specifically, the flow curve is defined to be a set of points with initial point :math:`(x_0, y_0, z_0)` and all subsequence points

.. math::
    (x_n, y_n, z_n) = (x_{n-1}, y_{n-1}, z_{n-1}) + h(f(x_{n-1}, y_{n-1}, z_{n-1}), g(x_{n-1}, y_{n-1}, z_{n-1}), h(x_{n-1}, y_{n-1}, z_{n-1}))

where :math:`h` is the step factor.

There are two ways to input a vector field into this application, either a list with three expressions or a :math:`3 \times 1` matrix.  For example, the field :math:`F = (y, z, x)` could be input as either, ``[y,z,x]`` or as

.. math::
    \left[\begin{array}{c}y\\z\\x\end{array}\right]


Insert/Edit Dialog
------------------

The Insert/Edit Dialog for the flow curve is shown below.

.. figure:: Images/FC_dialog.png
    :alt: Flow Curve Dialog Box

    Flow Curve Dialog Box


The first three inputs are the functions for the x, y, and z components to the vectors in the field, after that are options for the initial point, step factor, number of steps, direction, line width, points to include, the point size, and clipping.

Options
-------

Initial Point
^^^^^^^^^^^^^

This is the point of origin for the curve, in the language above, it is the point :math:`(x_0, y_0, z_0)`.  This is a list of two expressions that must evaluate to real numbers but can include constants, so any valid expression that does not include the set of 3D variables (``x``, ``y``, ``z``, ``p``, ``t``, ``u``, and ``v``).  They may contain constants that will link with a slider.  It is common to set this to ``[a, b, c]``, then three sliders will be created (one for ``a``, one for ``b``, and one for ``c``) then the user can move the sliders to change the initial point and see the change in the curve in real time.

Step factor
^^^^^^^^^^^

This is the step factor, :math:`h` in the above definition.  This can be any valid expression that does not include the set of 3D variables (``x``, ``y``, ``z``, ``p``, ``t``, ``u``, and ``v``) but can include constants. The smaller this is the better the approximation but also the more steps needed to cover the same range.

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

Clip to View
^^^^^^^^^^^^

.. include:: clipping3d.md


Example
-------

Say we use the example above of the field :math:`F = (y, z, x)`, set the initial point to :math:`(a, b, c)`, move the sliders, reposition, plot the initial point along with the vector field we would see,

.. figure:: Images/FC001.png
    :alt: Flow Curve Example with Vector Field

    Flow Curve Example with Vector Field

change :math:`(a, b, c)` and reposition,

.. figure:: Images/FC002.png
    :alt: Flow Curve Example with Vector Field

    Flow Curve Example with Vector Field

remove the vector field and reposition,

.. figure:: Images/FC003.png
    :alt: Flow Curve Example

    Flow Curve Example

