:index:`Maxima: Limits and Derivatives`
=======================================

Limit
-----

This will find the limit of a function.  When selected a dialog box will appear asking the use for the variable, limit point, the direction, and the Maxima running mode.  Remember that you are using CLAE syntax and not Maxima, so :math:`\pi` is ``pi``, :math:`e` is ``E``, :math:`\infty` is ``oo``, and :math:`-\infty` is ``-oo``.


Derivative
----------

This option finds the derivative (or partial derivative) of the function.  When selected a dialog box will appear asking the user for the variable to take the derivative with respect to and the order of the derivative.


Implicit Differentiation
------------------------

This option finds the implicit derivative of a function of two variables.  When selected a dialog box will appear asking the user for a dependent variable and an independent variable.  If the user selects *y* ad the dependent variable and *x* as the independent variable then the program will find :math:`\frac{dy}{dx}.`  For example, with the expression,

.. math::
    x y^{2} + \sin{\left(x - y \right)}

:math:`\frac{dy}{dx}` is

.. math::
    \frac{y^{2} + \cos{\left(x - y \right)}}{- 2 x y + \cos{\left(x - y \right)}}

