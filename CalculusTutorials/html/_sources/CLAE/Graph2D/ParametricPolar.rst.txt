:index:`Polar Parametric Equations (r, theta) = (f(t), g(t))`
=============================================================

Description
-----------

This type is for graphing parametric equations in polar coordinates,

.. math::
    \begin{array}{rcl} r & = & f{\left(t \right)}\\ \theta & = & g{\left(t \right)}\end{array}

The independent variable in the expressions can be ``x`` or ``t`` but not both.  The variable ``y`` cannot be in the expressions either.  All other variables are considered constants.  In the CAS, the expressions can be input either as a list or as a :math:`2 \times 1` matrix with the first entry the expression for the :math:`r` coordinate and the second entry the expression for the :math:`\theta` coordinate.  For example, :math:`\left[ \sin{\left(x \right)}, \  \cos{\left(x \right)}\right]` or

.. math::
    \left[\begin{array}{c}\sin{\left(x \right)}\\\cos{\left(x \right)}\end{array}\right]

will give the parametric equations for

.. math::
    \begin{array}{rcl} r & = & \sin{\left(t \right)}\\ \theta & = &  \cos{\left(t \right)}\end{array}

Insert/Edit Dialog
------------------

The Insert/Edit Dialog for parametric equations is pictured below.

.. figure:: Images/PolarPara_dialog.png
    :alt: Polar Parametric Equation Properties Dialog

    Polar Parametric Equation Properties Dialog

The first inputs are the :math:`r` and :math:`\theta` coordinate expressions, then the lower and upper bounds on the parameter values, and finally the number of points and the line width options.

Options
-------

Parameter Minimum and Maximum
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Lower and upper bounds for the parameter can be any legitimate expression that evaluates to a real number.  For example, ``1.234``, ``3*pi``, ``1/E``, etc.  For example, if we graph,

Points
^^^^^^

.. include:: points.md

Line Width
^^^^^^^^^^

.. include:: linewidth.md


Example
-------

If we use the above example of,

.. math::
    \begin{array}{rcl} r & = & \sin{\left(t \right)}\\ \theta & = &  \cos{\left(t \right)}\end{array}

on :math:`[-10, 10]` we get,

.. figure:: Images/PolarPara001.png
    :alt: Polar Parametric Equation Example

    Polar Parametric Equation Example

As another quick example, say we plot,

.. math::
    \begin{array}{rcl} r & = & \sin{\left(t \right)}\\ \theta & = &  t\end{array}

on :math:`[-10, 10]` we get,

.. figure:: Images/PolarPara002.png
    :alt: Polar Parametric Equation Example

    Polar Parametric Equation Example

and if we interchange the roles of :math:`r` and :math:`\theta`  to

.. math::
    \begin{array}{rcl} r & = & t \\ \theta & = &  \sin{\left(t \right)}\end{array}

on :math:`[-10, 10]` we get,

.. figure:: Images/PolarPara003.png
    :alt: Polar Parametric Equation Example

    Polar Parametric Equation Example

