:index:`Polar Function r = f(t)`
================================

Description
-----------

This type will graph the expression in polar coordinates, that is, the polar function :math:`r = f(t) = f(\theta)`.  The independent variable in the expression can be ``x`` or ``t`` but not both.  The variable ``y`` cannot be in the expression either.  All other variables are considered constants.


Insert/Edit Dialog
------------------

The Insert/Edit Dialog for the polar functions is shown below.

.. figure:: Images/Polar_dialog.png
    :alt: Polar Function Properties Dialog

    Polar Function Properties Dialog


The first input box is for the expression, following that are options for the parameter minimum and maximum, the number of points, and the line width.

Options
-------

Parameter Minimum and Maximum
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Lower and upper bounds for the parameter can be any legitimate expression that evaluates to a real number.  For example, ``1.234``, ``3*pi``, ``1/E``, etc.  For example, if we graph,

.. math::
    r = \sin{\left(3 t \right)}

on the default range of :math:`[0, 2\pi]` we get,

.. figure:: Images/Polar001.png
    :alt: Polar Parameter Minimum and Maximum Example

    Polar Parameter Minimum and Maximum Example

and if we change the bounds to :math:`[\pi/4, 3\pi/4]` we get,

.. figure:: Images/Polar002.png
    :alt: Polar Parameter Minimum and Maximum Example

    Polar Parameter Minimum and Maximum Example

Points
^^^^^^

.. include:: points.md

Line Width
^^^^^^^^^^

.. include:: linewidth.md

Example
-------

As another quick example, input ``t/10``, graph this as a polar function and set the parameter range to :math:`[0, 20]` and you get the following image.

.. figure:: Images/Polar003.png
    :alt: Polar Function Example

    Polar Function Example

