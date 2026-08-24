:index:`Parametric Equations (x, y) = (f(t), g(t))`
===================================================

Description
-----------

This type is for graphing the parametric equations

.. math::
    \begin{array}{rcl} x & = & f{\left(x \right)}\\ y & = & g{\left(x \right)}\end{array}

The independent variable in the expressions can be ``x`` or ``t`` but not both.  The variable ``y`` cannot be in the expressions either.  All other variables are considered constants.  In the CAS, the expressions can be input either as a list or as a :math:`2 \times 1` matrix with the first entry the expression for the x coordinate and the second entry the expression for the y coordinate.  For example, :math:`\left[ \sin{\left(x \right)}, \  \cos{\left(x \right)}\right]` or

.. math::
    \left[\begin{array}{c}\sin{\left(x \right)}\\\cos{\left(x \right)}\end{array}\right]

will give the parametric equations for

.. math::
    \begin{array}{rcl} x & = & \sin{\left(t \right)}\\ y & = &  \cos{\left(t \right)}\end{array}

Insert/Edit Dialog
------------------

The Insert/Edit Dialog for parametric equations is pictured below.

.. figure:: Images/para_rect_dialog.png
    :alt: Parametric Equation Properties Dialog

    Parametric Equation Properties Dialog

The first inputs are the x and y coordinate expressions, then the lower and upper bounds on the parameter values, and finally the number of points and the line width options.

Options
-------

Parameter Minimum and Maximum
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Lower and upper bounds for the parameter can be any legitimate expression that evaluates to a real number.  For example, ``1.234``, ``3*pi``, ``1/E``, etc.  For example, if we graph,

.. math::
    \begin{array}{rcl} x & = & \sin{\left(t \right)}\\ y & = & \cos{\left(t \right)}\end{array}

on the default range of :math:`[-10, 10]` we get,

.. figure:: Images/para_rect001.png
    :alt: Parameter Minimum and Maximum Example

    Parameter Minimum and Maximum Example

and if we change the bounds to :math:`[\pi/4, 5\pi/3]` we get,

.. figure:: Images/para_rect002.png
    :alt: Parameter Minimum and Maximum Example

    Parameter Minimum and Maximum Example

Points
^^^^^^

.. include:: points.md

Line Width
^^^^^^^^^^

.. include:: linewidth.md
