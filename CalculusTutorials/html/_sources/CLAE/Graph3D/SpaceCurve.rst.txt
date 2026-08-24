:index:`Space Curve (x, y, z) = (f(t), g(t), h(t))`
===================================================

Description
-----------

This type graphs parametrically defined curves of the form :math:`(x, y, z) = (f(t), g(t), h(t))`.  The independent variable in the expressions must be ``t``.  All other variables outside the set of 3D variables (``x``, ``y``, ``z``, ``p``, ``t``, ``u``, and ``v``) are considered constants.  The curve can be input either as a list with three entries representing the x, y, and z expressions or as a :math:`3 \times 1` matrix where the rows are the x, y, and z expressions.  For example, either as :math:`\left[ 7 \cos{\left(t \right)}, \  7 \sin{\left(t \right)}, \  t\right]` or as

.. math::
    \left[\begin{array}{c}7 \cos{\left(t \right)}\\7 \sin{\left(t \right)}\\t\end{array}\right]

Insert/Edit Dialog
------------------

The Insert/Edit Dialog for this type is shown below.

.. figure:: Images/SpaceCurve_dialog.png
    :alt: Space Curve Dialog Box

    Space Curve Dialog Box

The first three inputs are for the x, y, and z expressions, below that are options for the minimum and maximum t values, the number of points to use for the plot, the line width, and clipping.

Options
-------

Minimum t Value
^^^^^^^^^^^^^^^

The beginning value for the range of t.

Maximum t Value
^^^^^^^^^^^^^^^

The ending value for the range of t.

Points
^^^^^^

.. include:: points.md

Line Width
^^^^^^^^^^

.. include:: linewidth.md

Clip Values to View
^^^^^^^^^^^^^^^^^^^^

.. include:: clipping3d.md

Example
-------

If we plot

.. math::
    \left[\begin{array}{c}7 \cos{\left(t \right)}\\7 \sin{\left(t \right)}\\t\end{array}\right]

on the default interval of :math:`[-10, 10]` we get,

.. figure:: Images/SpaceCurve001.png
    :alt: Space Curve Example

    Space Curve Example

