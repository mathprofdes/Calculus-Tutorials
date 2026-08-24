:index:`Limits and Derivatives`
===============================

Limits, derivatives, and integration are at the heart of an introductory Calculus sequence.  Here we will look at limits and derivatives, integration is covered in the :doc:`CalIntegration` section.  These options allow the user to find limits of single variable expressions, take derivatives and higher-order derivatives (including partial derivatives), find derivatives and higher-order derivatives of implicitly defined relations, and a quick tangent line calculator that is helpful when examining these concepts graphically.

:index:`Limit`
--------------

This option will take the limit of a single variable function.  When invoked a dialog will appear asking the user to input the variable to take the limit with respect to,  the limit point for the limit, and what direction to take the limit (or two-sided).  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

The limit point can be any valid expression, including workspace entries (R1, R2, ...) as well as expressions that incorporate them.  Also remember that the infinities are denoted as ``oo`` and ``-oo``.  For a refresher on syntax look over the :doc:`../CLAE/syntax` materials.

We will go over a couple examples,

Say we have the expression, :math:`\displaystyle \frac{- x^{4} + \left(h + x\right)^{4}}{h}`, which is the difference quotient for :math:`f(x) = x^4`.  If we take the limit, use ``h`` for the variable, 0 for the limit point, and two-side, we get :math:`4 x^{3}`.

Along the same lines, say we have the expression, :math:`\displaystyle \frac{- \sin{\left(x \right)} + \sin{\left(h + x \right)}}{h}`, which is the difference quotient for :math:`f(x) = \sin(x)`.  If we take the limit, use ``h`` for the variable, 0 for the limit point, and two-side, we get :math:`\cos{\left(x \right)}`.  This tool may have its limitations but it does handle some fairly impressive algebraic manipulations.

Say we have the expression, :math:`\frac{1}{x}`,

.. figure:: Images/Limit001.png
    :alt: y = 1/x

    :math:`y = \frac{1}{x}`


the limit as :math:`x \to 0` from the left gives us :math:`-\infty`, from the right gives us :math:`\infty`, and if we try a two-sided limit we get :math:`\tilde{\infty}`, which displays as zoo.  From the SymPy documentation: `zoo represents complex infinity, i.e., the north pole of the Riemann sphere. The reason it is spelled this way is that it is “z-oo”, where “z” is the symbol commonly used for complex variables, and oo is the symbol SymPy uses for real positive infinity.`


Another interesting output you may get can be seen with :math:`\sin{\left(\frac{1}{x} \right)}`,

.. figure:: Images/Limit002.png
    :alt: y = sin(1/x)

    :math:`y = \sin{\left(\frac{1}{x}\right)}`


if we take the limit of this as :math:`x \to 0` we get the result, :math:`\left\langle -1, 1\right\rangle`, indicating the infinite oscillation between :math:`-1` and 1.

.. note::

    Do not try to find the limit of a sequence using this option, instead use the ``Sequence Limit`` option under the Calculus menu.  The algorithms are different between this and the sequence limit code since the sequence limit can assume that the domain is integers.

:index:`Derivative`
-------------------

This option will find the derivative or partial derivative of an expression with respect to the chosen variable and to the order specified.  When this option is selected a dialog box will appear asking the user for the variable (or list of variables) to take the derivative with respect to and the order of the derivative to calculate.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

For example, say we input the expression ``sin(x^3)^2``, that is, :math:`\sin^{2}{\left(x^{3} \right)}`.  If we take the first derivative with respect to ``x`` of this we get,

.. math::
    6 x^{2} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}

and if we take the third derivative of this we get,

.. math::
    - 216 x^{6} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)} - 108 x^{3} \sin^{2}{\left(x^{3} \right)} + 108 x^{3} \cos^{2}{\left(x^{3} \right)} + 12 \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}

Now lets say we have something a little more complicated,

.. math::
    \frac{y \sin^{2}{\left(x^{3} \right)}}{x^{2} + y^{2}}

If we take the derivative with respect to ``x``, that is, the partial derivative with respect to ``x`` we get,

.. math::
    \frac{6 x^{2} y \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{x^{2} + y^{2}} - \frac{2 x y \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}}

If we take the derivative with respect to ``y``, that is, the partial derivative with respect to ``y`` we get,

.. math::
    - \frac{2 y^{2} \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} + \frac{\sin^{2}{\left(x^{3} \right)}}{x^{2} + y^{2}}

With this tool we can take several partial derivatives at one time by listing the variables we wish to differentiate with respect to in order separated by commas.  So to take the partial derivative with respect to ``x`` first and then with respect to ``y`` we would enter ``x, y`` into the variables text box.  This will produce,

.. math::
    - \frac{12 x^{2} y^{2} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} + \frac{6 x^{2} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{x^{2} + y^{2}} + \frac{8 x y^{2} \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{3}} - \frac{2 x \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}}

If you then do the derivatives in reverse order, ``y, x``, you of course get the same result, which is a nice illustration of Clairaut’s Theorem.

Taking this s little further, if we list several variables and increase the order of the derivative it is the same as listing the variable list the order number of times.  For example, say we input a variable list ``x, y`` and changed the order to 3, then this is the same as a variable list of ``x, y, x, y, x, y``, a sixth order derivative.

.. math::
    \frac{\frac{144 x y^{2} \left(\frac{4 y^{2}}{x^{2} + y^{2}} - 1\right) \left(- \frac{12 x^{3} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{x^{2} + y^{2}} + \frac{4 x^{2} \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} - 3 x \left(\frac{4 x^{2}}{x^{2} + y^{2}} - 1\right) \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)} + 3 x \left(- 3 x^{3} \sin^{2}{\left(x^{3} \right)} + 3 x^{3} \cos^{2}{\left(x^{3} \right)} + 2 \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}\right) + \frac{\left(\frac{8 x^{2}}{x^{2} + y^{2}} - 4\right) \sin^{2}{\left(x^{3} \right)}}{x^{2} + y^{2}}\right)}{\left(x^{2} + y^{2}\right)^{2}} - \frac{288 x y^{2} \left(- \frac{12 x^{3} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{x^{2} + y^{2}} + \frac{4 x^{2} \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} - 3 x \left(\frac{4 x^{2}}{x^{2} + y^{2}} - 1\right) \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)} + 3 x \left(- 3 x^{3} \sin^{2}{\left(x^{3} \right)} + 3 x^{3} \cos^{2}{\left(x^{3} \right)} + 2 \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}\right) + \frac{\left(\frac{8 x^{2}}{x^{2} + y^{2}} - 4\right) \sin^{2}{\left(x^{3} \right)}}{x^{2} + y^{2}}\right)}{\left(x^{2} + y^{2}\right)^{2}} - \frac{288 x y^{2} \left(\frac{72 x^{3} y^{2} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} - \frac{24 x^{3} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{x^{2} + y^{2}} - \frac{48 x^{2} y^{2} \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{3}} + \frac{12 x^{2} \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} + \frac{6 x y^{2} \left(\frac{4 x^{2}}{x^{2} + y^{2}} - 1\right) \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{x^{2} + y^{2}} - \frac{6 x y^{2} \left(- 3 x^{3} \sin^{2}{\left(x^{3} \right)} + 3 x^{3} \cos^{2}{\left(x^{3} \right)} + 2 \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}\right)}{x^{2} + y^{2}} - 3 x \left(\frac{4 x^{2}}{x^{2} + y^{2}} - 1\right) \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)} + 3 x \left(- 3 x^{3} \sin^{2}{\left(x^{3} \right)} + 3 x^{3} \cos^{2}{\left(x^{3} \right)} + 2 \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}\right) - \frac{16 y^{2} \left(\frac{2 x^{2}}{x^{2} + y^{2}} - 1\right) \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} + \frac{\left(\frac{12 x^{2}}{x^{2} + y^{2}} - 6\right) \sin^{2}{\left(x^{3} \right)}}{x^{2} + y^{2}}\right)}{\left(x^{2} + y^{2}\right)^{2}} - \frac{144 x y^{2} \left(\frac{96 x^{3} y^{2} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} - \frac{12 x^{3} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{x^{2} + y^{2}} - \frac{48 x^{2} y^{2} \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{3}} + \frac{4 x^{2} \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} + \frac{12 x y^{2} \left(\frac{4 x^{2}}{x^{2} + y^{2}} - 1\right) \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{x^{2} + y^{2}} - \frac{12 x y^{2} \left(- 3 x^{3} \sin^{2}{\left(x^{3} \right)} + 3 x^{3} \cos^{2}{\left(x^{3} \right)} + 2 \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}\right)}{x^{2} + y^{2}} - 3 x \left(\frac{4 x^{2}}{x^{2} + y^{2}} - 1\right) \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)} + 3 x \left(- 3 x^{3} \sin^{2}{\left(x^{3} \right)} + 3 x^{3} \cos^{2}{\left(x^{3} \right)} + 2 \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}\right) - \frac{24 y^{2} \left(\frac{2 x^{2}}{x^{2} + y^{2}} - 1\right) \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} + \frac{\left(\frac{8 x^{2}}{x^{2} + y^{2}} - 4\right) \sin^{2}{\left(x^{3} \right)}}{x^{2} + y^{2}}\right)}{\left(x^{2} + y^{2}\right)^{2}} + \frac{72 x \left(\frac{96 x^{3} y^{2} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} - \frac{12 x^{3} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{x^{2} + y^{2}} - \frac{48 x^{2} y^{2} \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{3}} + \frac{4 x^{2} \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} + \frac{12 x y^{2} \left(\frac{4 x^{2}}{x^{2} + y^{2}} - 1\right) \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{x^{2} + y^{2}} - \frac{12 x y^{2} \left(- 3 x^{3} \sin^{2}{\left(x^{3} \right)} + 3 x^{3} \cos^{2}{\left(x^{3} \right)} + 2 \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}\right)}{x^{2} + y^{2}} - 3 x \left(\frac{4 x^{2}}{x^{2} + y^{2}} - 1\right) \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)} + 3 x \left(- 3 x^{3} \sin^{2}{\left(x^{3} \right)} + 3 x^{3} \cos^{2}{\left(x^{3} \right)} + 2 \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}\right) - \frac{24 y^{2} \left(\frac{2 x^{2}}{x^{2} + y^{2}} - 1\right) \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} + \frac{\left(\frac{8 x^{2}}{x^{2} + y^{2}} - 4\right) \sin^{2}{\left(x^{3} \right)}}{x^{2} + y^{2}}\right)}{x^{2} + y^{2}} + \frac{288 y^{2} \left(\frac{2 y^{2}}{x^{2} + y^{2}} - 1\right) \left(18 x^{6} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)} + 9 x^{3} \sin^{2}{\left(x^{3} \right)} - 9 x^{3} \cos^{2}{\left(x^{3} \right)} - \frac{3 x^{2} \left(\frac{4 x^{2}}{x^{2} + y^{2}} - 1\right) \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{x^{2} + y^{2}} + \frac{3 x^{2} \left(- 3 x^{3} \sin^{2}{\left(x^{3} \right)} + 3 x^{3} \cos^{2}{\left(x^{3} \right)} + 2 \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}\right)}{x^{2} + y^{2}} + \frac{2 x \left(\frac{2 x^{2}}{x^{2} + y^{2}} - 1\right) \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} - \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}\right)}{x^{2} + y^{2}} - \left(\frac{288 y^{2}}{x^{2} + y^{2}} - 72\right) \left(18 x^{6} \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)} + 9 x^{3} \sin^{2}{\left(x^{3} \right)} - 9 x^{3} \cos^{2}{\left(x^{3} \right)} - \frac{3 x^{2} \left(\frac{4 x^{2}}{x^{2} + y^{2}} - 1\right) \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}}{x^{2} + y^{2}} + \frac{3 x^{2} \left(- 3 x^{3} \sin^{2}{\left(x^{3} \right)} + 3 x^{3} \cos^{2}{\left(x^{3} \right)} + 2 \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}\right)}{x^{2} + y^{2}} + \frac{2 x \left(\frac{2 x^{2}}{x^{2} + y^{2}} - 1\right) \sin^{2}{\left(x^{3} \right)}}{\left(x^{2} + y^{2}\right)^{2}} - \sin{\left(x^{3} \right)} \cos{\left(x^{3} \right)}\right)}{\left(x^{2} + y^{2}\right)^{2}}

Which simplifies to

.. math::
    \frac{648 x^{16} \sin{\left(2 x^{3} \right)} - 1944 x^{14} y^{2} \sin{\left(2 x^{3} \right)} + 648 x^{13} \cos{\left(2 x^{3} \right)} - 9072 x^{12} y^{4} \sin{\left(2 x^{3} \right)} - 8424 x^{11} y^{2} \cos{\left(2 x^{3} \right)} - 9072 x^{10} y^{6} \sin{\left(2 x^{3} \right)} - 684 x^{10} \sin{\left(2 x^{3} \right)} - 9072 x^{9} y^{4} \cos{\left(2 x^{3} \right)} - 1944 x^{8} y^{8} \sin{\left(2 x^{3} \right)} + 11772 x^{8} y^{2} \sin{\left(2 x^{3} \right)} + 9072 x^{7} y^{6} \cos{\left(2 x^{3} \right)} - 360 x^{7} \cos{\left(2 x^{3} \right)} + 360 x^{7} + 648 x^{6} y^{10} \sin{\left(2 x^{3} \right)} - 5544 x^{6} y^{4} \sin{\left(2 x^{3} \right)} + 8424 x^{5} y^{8} \cos{\left(2 x^{3} \right)} + 7560 x^{5} y^{2} \cos{\left(2 x^{3} \right)} - 7560 x^{5} y^{2} - 14616 x^{4} y^{6} \sin{\left(2 x^{3} \right)} - 648 x^{3} y^{10} \cos{\left(2 x^{3} \right)} - 12600 x^{3} y^{4} \cos{\left(2 x^{3} \right)} + 12600 x^{3} y^{4} + 3348 x^{2} y^{8} \sin{\left(2 x^{3} \right)} + 2520 x y^{6} \cos{\left(2 x^{3} \right)} - 2520 x y^{6} - 36 y^{10} \sin{\left(2 x^{3} \right)}}{x^{14} + 7 x^{12} y^{2} + 21 x^{10} y^{4} + 35 x^{8} y^{6} + 35 x^{6} y^{8} + 21 x^{4} y^{10} + 7 x^{2} y^{12} + y^{14}}

:index:`Implicit Differentiation`
---------------------------------

This option will calculate an implicit derivative to the specified order.  When invoked a dialog box will appear asking the user for the dependent and independent variables, and the order of the derivative.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

If our dependent variable is ``y`` and our independent variable is ``x`` then the derivative would be :math:`\frac{dy}{dx}`.  If we instead our dependent variable is ``x`` and our independent variable is ``y`` then the derivative would be :math:`\frac{dx}{dy}`.

For example, say we input the expression ``(x^2-1)*(x^2-4)*(x^2-9)-(y^2*(y^2-4)*(y^2-9))``, that is,

.. math::
    - y^{2} \left(y^{2} - 9\right) \left(y^{2} - 4\right) + \left(x^{2} - 9\right) \left(x^{2} - 4\right) \left(x^{2} - 1\right)

As an implicitly defined expression we assume (as with solving) that this expression is equal to 0, specifically,

.. math::
    - y^{2} \left(y^{2} - 9\right) \left(y^{2} - 4\right) + \left(x^{2} - 9\right) \left(x^{2} - 4\right) \left(x^{2} - 1\right) = 0

.. figure:: Images/Der001.png
    :alt: Implicit Expression

    :math:`- y^{2} \left(y^{2} - 9\right) \left(y^{2} - 4\right) + \left(x^{2} - 9\right) \left(x^{2} - 4\right) \left(x^{2} - 1\right) = 0`

If we find :math:`\frac{dy}{dx}` with ``y`` and ``x`` we get,

.. math::
    \frac{x \left(3 x^{4} - 28 x^{2} + 49\right)}{y \left(3 y^{4} - 26 y^{2} + 36\right)}

and :math:`\frac{dx}{dy}` with ``x`` and  ``y`` we get,

.. math::
    \frac{y \left(3 y^{4} - 26 y^{2} + 36\right)}{x \left(3 x^{4} - 28 x^{2} + 49\right)}

We can find higher order derivatives here as well, if we find :math:`\frac{d^2y}{dx^2}` with ``y`` and  ``x`` and an order of 2 we get,

.. math::
    \frac{- 135 x^{10} y + \frac{702 x^{10}}{y} - \frac{324 x^{10}}{y^{3}} + 2520 x^{8} y - \frac{13104 x^{8}}{y} + \frac{6048 x^{8}}{y^{3}} - 16170 x^{6} y + \frac{84084 x^{6}}{y} - \frac{38808 x^{6}}{y^{3}} + 135 x^{4} y^{7} - 2340 x^{4} y^{5} + 13380 x^{4} y^{3} + 13080 x^{4} y - \frac{194592 x^{4}}{y} + \frac{98784 x^{4}}{y^{3}} - 756 x^{2} y^{7} + 13104 x^{2} y^{5} - 74928 x^{2} y^{3} + 121233 x^{2} y + \frac{78414 x^{2}}{y} - \frac{86436 x^{2}}{y^{3}} + 441 y^{7} - 7644 y^{5} + 43708 y^{3} - 91728 y + \frac{63504}{y}}{27 y^{12} - 702 y^{10} + 7056 y^{8} - 34424 y^{6} + 84672 y^{4} - 101088 y^{2} + 46656}

which simplifies to

.. math::
    \frac{x^{2} \left(- 324 x^{8} + 6048 x^{6} - 38808 x^{4} + 98784 x^{2} - 86436\right) + y^{4} \left(- 135 x^{10} + 2520 x^{8} - 16170 x^{6} + 135 x^{4} y^{6} - 2340 x^{4} y^{4} + 13380 x^{4} y^{2} + 13080 x^{4} - 756 x^{2} y^{6} + 13104 x^{2} y^{4} - 74928 x^{2} y^{2} + 121233 x^{2} + 441 y^{6} - 7644 y^{4} + 43708 y^{2} - 91728\right) + y^{2} \left(702 x^{10} - 13104 x^{8} + 84084 x^{6} - 194592 x^{4} + 78414 x^{2} + 63504\right)}{y^{3} \left(27 y^{12} - 702 y^{10} + 7056 y^{8} - 34424 y^{6} + 84672 y^{4} - 101088 y^{2} + 46656\right)}

Taking this example a little further, if we evaluate the original expression at :math:`x = 1` we get

.. math::
    - y^{2} \left(y^{2} - 9\right) \left(y^{2} - 4\right) = 0

which gives the solutions :math:`\left[ -3, \  -2, \  0, \  2, \  3\right]`, then evaluating :math:`\frac{dy}{dx}` at the point :math:`(1, -2)` gives us :math:`3/5`.  Hence the slope of the tangent line to this implicit curve at the point :math:`(1, -2)` is :math:`3/5`.  Hence the tangent line equation is :math:`y = \frac{3 x}{5} - \frac{13}{5}` and if we graph this with the curve we see,

.. figure:: Images/Der002.png
    :alt: Implicit Expression and Tangent Line

    :math:`- y^{2} \left(y^{2} - 9\right) \left(y^{2} - 4\right) + \left(x^{2} - 9\right) \left(x^{2} - 4\right) \left(x^{2} - 1\right) = 0` and :math:`y = \frac{3 x}{5} - \frac{13}{5}`


:index:`Tangent Line`
---------------------

This option will allow you to create a tangent line equation to an explicitly defined curve quickly.  When this option is invoked a dialog box will appear asking the user to input the variable that will be differentiated with respect to, the point of tangency, if we are working in rectangular or polar coordinates and the form of the output of the tangent line.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

The output type has three options,

- Function ``y = mx + b``:  This will give the tangent line as ``mx + b``.
- General ``ax + by + c = 0``:  This will give the tangent line as ``ax + by + c``.
- Matrix/Linear System:  This will give the tangent line as the 1 X 3 matrix ``[a b c]`` which represents the expression ``ax + by = c``.

The form of the output is up to you.  Some pros and cons.  If you are graphing these then either function or matrix form would be best.  The general form uses the implicit expression graphing system which requires many more calculations.  If the curve has several places where there are vertical tangents then either the general or matrix forms would be better since at these spots the slope is undefined and hence the m in mx + b is undefined.  So for graphing the matrix form is probably the best but it is the least human readable of the three.

We will look at a couple examples.

Input the expression, ``x^3 - 5*x^2 + 4*x + 1``, that is, :math:`x^{3} - 5 x^{2} + 4 x + 1`.  Click and drag it over to the 2-D graph and we get (with a little zooming and moving),

.. figure:: Images/Der003.png
    :alt: x^3 - 5*x^2 + 4*x + 1

    :math:`y = x^{3} - 5 x^{2} + 4 x + 1`

Select ``Calculus > Tangent Line``, use 1 for the point of tangency, rectangular coordinates, and Function ``y = mx + b`` for the output type.  This gives us :math:`4 - 3 x`, graph this as well by clicking and dragging it to the graph and   see.

.. figure:: Images/Der004.png
    :alt: x^3 - 5*x^2 + 4*x + 1 and y = 4 - 3*x

    :math:`y = x^{3} - 5 x^{2} + 4 x + 1` and :math:`y = 4 - 3 x`

I we had selected the general form output we would have gotten, :math:`3 x + y - 4` and if we would have selected the matrix form output we would have gotten, :math:`\left[\begin{array}{ccc}-3 & -1 & -4\end{array}\right]`.  As you can see these are all equivalent.  Furthermore, you can click and drag them to the 2-D graphics view and you will get the same lines.

Lets take this a little further.  Do another tangent line but this time put in ``a`` for the point of tangency.  If we use function output we get, :math:`a^{3} - 5 a^{2} + 4 a + \left(- a + x\right) \left(3 a^{2} - 10 a + 4\right) + 1`. If we click and drag this over to the graph we get the tangent line and we get a slider attached to the constant ``a``.

.. figure:: Images/Der005.png
    :alt: x^3 - 5*x^2 + 4*x + 1 and general tangent line

    :math:`y = x^{3} - 5 x^{2} + 4 x + 1` and General Tangent Line

If you move the slider you will see the tangent line moving along the curve.

We will do an example of a tangent line to a polar coordinate curve.  Input the expression :math:`\sin{\left(3 t \right)}`, graph it and change the graph type to polar coordinates. Now select tangent line, put the point of tangency as 2 and change to polar coordinates.  The result is,

.. math::
    \frac{\left(t - \sin{\left(6 \right)} \cos{\left(2 \right)}\right) \left(\sin{\left(6 \right)} \cos{\left(2 \right)} + 3 \sin{\left(2 \right)} \cos{\left(6 \right)}\right)}{3 \cos{\left(2 \right)} \cos{\left(6 \right)} - \sin{\left(2 \right)} \sin{\left(6 \right)}} + \sin{\left(2 \right)} \sin{\left(6 \right)}

Graphing this along with the curve gives,

.. figure:: Images/Der006.png
    :alt: Polar Coordinate Curve and Tangent Line

    Polar Coordinate Curve and Tangent Line

Doing the same but using ``a`` as the point of tangency we get an equation that will link to the ``a`` slider and give a tangent line on the polar curve at the position of the ``a`` slider.

.. math::
    \frac{\left(t - \sin{\left(3 a \right)} \cos{\left(a \right)}\right) \left(3 \sin{\left(a \right)} \cos{\left(3 a \right)} + \sin{\left(3 a \right)} \cos{\left(a \right)}\right)}{- \sin{\left(a \right)} \sin{\left(3 a \right)} + 3 \cos{\left(a \right)} \cos{\left(3 a \right)}} + \sin{\left(a \right)} \sin{\left(3 a \right)}

Since this curve has several places where there are vertical tangent lines using the matrix form would be better for the graph.  This option gives us,

.. math::
    \left[\begin{array}{ccc}\sin{\left(2 a \right)} - 2 \sin{\left(4 a \right)} & \cos{\left(2 a \right)} + 2 \cos{\left(4 a \right)} & - \sin^{2}{\left(3 a \right)}\end{array}\right]


The tangent line calculation also works with parametrically defined curves in both rectangular and polar coordinates.

Input the parametric expression :math:`\left[ \sin{\left(x \right)}, \  \cos{\left(3 x \right)}\right]`, with the syntax, ``[sin(x), cos(3*x)]``.  Graph this in rectangular coordinates and you will see,

.. figure:: Images/Der007.png
    :alt: Parametric Curve

    Parametric Curve

If we create the rectangular coordinate tangent line at 3 we get,

.. math::
    \frac{\left(- 3 x + 3 \sin{\left(3 \right)}\right) \sin{\left(9 \right)}}{\cos{\left(3 \right)}} + \cos{\left(9 \right)}

and a visualization of,

.. figure:: Images/Der008.png
    :alt: Parametric Curve and Tangent Line

    Parametric Curve and Tangent Line

To do an example of polar coordinate parametric equations we will use the same parametric equations and simply shift to polar coordinates.  On the graph hide the tangent line and for the curve select parametric equations in polar coordinates and the graph should change to this,

.. figure:: Images/Der009.png
    :alt: Polar Parametric Curve

    Polar Parametric Curve

Do a tangent line at 3 again but select polar coordinates this time.  The formula will be,

.. math::
    \frac{\left(x - \sin{\left(3 \right)} \cos{\left(\cos{\left(9 \right)} \right)}\right) \left(- 3 \sin{\left(3 \right)} \sin{\left(9 \right)} \cos{\left(\cos{\left(9 \right)} \right)} + \sin{\left(\cos{\left(9 \right)} \right)} \cos{\left(3 \right)}\right)}{\cos{\left(3 \right)} \cos{\left(\cos{\left(9 \right)} \right)} + 3 \sin{\left(3 \right)} \sin{\left(9 \right)} \sin{\left(\cos{\left(9 \right)} \right)}} + \sin{\left(3 \right)} \sin{\left(\cos{\left(9 \right)} \right)}

and graphing it with the curve gives us,

.. figure:: Images/Der010.png
    :alt: Polar Parametric Curve and Tangent Line

    Polar Parametric Curve and Tangent Line

We can, of course, do the same with a variable point of tangency, like ``a``, to get a tangent line that will follow the curve as the slider is moved.


:index:`Maximums and Minimums`
------------------------------

This option will allow you to find absolute or local maximums and minimums of a single variable function on a finite interval.  When this option is invoked the following dialog box will appear.

.. figure:: Images/Der011.png
    :alt: Maximums and Minimums Dialog Box

    Maximums and Minimums Dialog Box

The program will automatically find the independent variable and if you try to invoke this on a multi-variable function you will get an error.

- The first two inputs are for the lower and upper bounds of the interval of interest.  This must be a finite interval and the values must evaluate to real numbers.  They can be expressions, such as ``pi/3`` but must evaluate to a number.
- The Type is simply absolute or local.
- The Extremes allow you to select minimums, maximums, or both.
- The Result is a selector between values and points.  If values are selected then the output is either a single value or list of values for the extremes that are requested.  If points are selected, the output will be a list of lists where each of the inner lists is an (x, y) point specifying where the extremes occur.
- Numerics is a selection between calculating exact values or approximate values.  If the approximate option is selected the test points and tolerance options will be enabled. If exact mode is being used the test points and tolerance are not needed nor are they used.
- The Test Points is the number of points the interval is broken up into in order to approximate where the derivative of the function is 0.  Hence to find some of the critical points.
- The Tolerance is the minimal amount of space between the critical numbers.  So if two critical numbers are found that are within the tolerance of each other they are considered the same point.  The selector here is the exponent, so an input of 8 means the tolerance is :math:`10^{-8}`.

There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.  The methods that are involved in calculating maximums and minimums make an overarching assumption that you are working with real numbers in the interval you specified.

For example, say we have the function, :math:`f(x) = x + 2 \sin{\left(x \right)}`.

.. figure:: Images/Der012.png
    :alt: x 2 sin(x)

    :math:`f(x) = x + 2 \sin{\left(x \right)}`

And we find the value of the absolute maximum of this function on :math:`[-10, 10]`.  The lower bound is :math:`-10`, the upper bound is 10, the type is Absolute, Extremes is Maximum, Result is Value, and Numerics is Exact.  The result is :math:`\sqrt{3} + \frac{8 \pi}{3}` and if we graph this value it comes in as a horizontal line,

.. figure:: Images/Der013.png
    :alt: x 2 sin(x) and Absolute Maximum

    :math:`f(x) = x + 2 \sin{\left(x \right)}`  and Absolute Maximum

If we instead find the points of the absolute maximum and minimum of this function on :math:`[-10, 10]`.  The lower bound is :math:`-10`, the upper bound is 10, the type is Absolute, Extremes are Both, Result is Point, and Numerics is Exact.  The result is

.. math::
    \left[ \left[ - \frac{8 \pi}{3}, \  - \frac{8 \pi}{3} - \sqrt{3}\right], \  \left[ \frac{8 \pi}{3}, \  \sqrt{3} + \frac{8 \pi}{3}\right]\right]

and if we graph these points we get,

.. figure:: Images/Der014.png
    :alt: x 2 sin(x) and Absolute Maximum Point

    :math:`f(x) = x + 2 \sin{\left(x \right)}`  and Absolute Maximum Point


If we instead find the points of the local maximums and minimums of this function on :math:`[-10, 10]`.  The lower bound is :math:`-10`, the upper bound is 10, the type is Local, Extremes are Both, Result is Point, and Numerics is Exact.  The result is

.. math::
    \left[ \left[ - \frac{8 \pi}{3}, \  - \frac{8 \pi}{3} - \sqrt{3}\right], \  \left[ - \frac{4 \pi}{3}, \  - \frac{4 \pi}{3} + \sqrt{3}\right], \  \left[ - \frac{2 \pi}{3}, \  - \frac{2 \pi}{3} - \sqrt{3}\right], \  \left[ \frac{2 \pi}{3}, \  \sqrt{3} + \frac{2 \pi}{3}\right], \  \left[ \frac{4 \pi}{3}, \  - \sqrt{3} + \frac{4 \pi}{3}\right], \  \left[ \frac{8 \pi}{3}, \  \sqrt{3} + \frac{8 \pi}{3}\right]\right]

and if we graph these points we get,

.. figure:: Images/Der015.png
    :alt: x 2 sin(x) and Local Extremes

    :math:`f(x) = x + 2 \sin{\left(x \right)}`  and Local Extremes

If you each of the above examples using approximate mode you will get the same solutions except in approximate form.

Let's do another example that is a little more complex. Consider the function, :math:`f(x) = x^{2} + 5 x \sin{\left(x \right)}`.

.. figure:: Images/Der016.png
    :alt: x^2 + 5x sin(x)

    :math:`f(x) = x^{2} + 5 x \sin{\left(x \right)}`

If we try to find all the local maximums and minimums on the interval :math:`[-12, 12]` we will get an error, which simply means that the program could not find the exact solutions.  In the process it would need to find exact solutions to :math:`5 x \cos{\left(x \right)} + 2 x + 5 \sin{\left(x \right)} = 0` and as you know, when polynomials and trigonometric functions are combined it is in general a difficult equation to solve exactly.  So in these cases you can switch to approximation mode for numerical approximations to the extremes.

As for the settings, the lower bound is :math:`-12`, the upper bound is 12, the type is Local, Extremes are Both, Result is Point, and Numerics is Approximate.  The result is

.. math::
    \left[ \left[ -10.6793241824911, \  63.2993715288081\right], \  \left[ -8.38118028622317, \  106.460095169846\right], \  \left[ -4.52845452339979, \  -1.75343549817341\right], \  \left[ -2.35003646166806, \  13.8823119041911\right], \  \left[ 0, \  0\right], \  \left[ 2.35003646166806, \  13.8823119041911\right], \  \left[ 4.52845452339979, \  -1.75343549817341\right], \  \left[ 8.38118028622317, \  106.460095169846\right], \  \left[ 10.6793241824911, \  63.2993715288081\right]\right]

Graphing these along with the curve gives,

.. figure:: Images/Der017.png
    :alt: x^2 + 5x sin(x) and Local Extremes

    :math:`f(x) = x^{2} + 5 x \sin{\left(x \right)}` and Local Extremes

.. note::

    A few notes about the maximum and minimum calculations.

    - Exact mode will, of course, produce exact solutions but the methods involved are more difficult and will take more time.  In addition, if the program cannot produce exact solutions it will return an error.
    - If exact mode does fail there is a good chance that the approximate mode will be successful.
    - Approximate mode does use numeric approximations and, in any case, when using numeric methods there is a possibility that solutions may be missed.
    - This option works fairly well at skipping isolated singularities.  For example, with

    .. math::
        f(x) = \frac{x^{4} + 1}{x^{2} - 1}

    on the interval :math:`[-3, 3]`, looking for exact local extrema, it handles :math:`x = -1` and :math:`x = 1` as it should and returns,

    .. math::
        \left[ \left[ - \sqrt{1 + \sqrt{2}}, \  \frac{\sqrt{2} \left(1 + \left(1 + \sqrt{2}\right)^{2}\right)}{2}\right], \  \left[ 0, \  -1\right], \  \left[ \sqrt{1 + \sqrt{2}}, \  \frac{\sqrt{2} \left(1 + \left(1 + \sqrt{2}\right)^{2}\right)}{2}\right]\right]

    .. figure:: Images/Der018.png
        :alt: Exact Local Extremes

        Exact Local Extremes


    - For functions that do not have isolated singularities, for example, :math:`f(x) = \ln(\sin(x))` it is better to restrict the intervals to sections that are continuous.
    - In exact mode there are times that the output may look a bit messy, in many cases you can select ``Algebra > Approximate`` to get an approximation to the values and not need to redo the maximum/minimum process in approximate mode.  For example, with the function,

    .. math::
        f(x) = \frac{x^{4} + x + 1}{x^{2} - 1}

    on the interval :math:`[-3, 3]`, looking for exact local extrema, we get,

    .. math::
        \left[ \left[ \operatorname{CRootOf} {\left(2 x^{5} - 4 x^{3} - x^{2} - 2 x - 1, 0\right)}, \  \frac{\operatorname{CRootOf} {\left(2 x^{5} - 4 x^{3} - x^{2} - 2 x - 1, 0\right)} + 1 + \operatorname{CRootOf} {\left(2 x^{5} - 4 x^{3} - x^{2} - 2 x - 1, 0\right)}^{4}}{-1 + \operatorname{CRootOf} {\left(2 x^{5} - 4 x^{3} - x^{2} - 2 x - 1, 0\right)}^{2}}\right], \  \left[ \operatorname{CRootOf} {\left(2 x^{5} - 4 x^{3} - x^{2} - 2 x - 1, 1\right)}, \  \frac{\operatorname{CRootOf} {\left(2 x^{5} - 4 x^{3} - x^{2} - 2 x - 1, 1\right)} + \operatorname{CRootOf} {\left(2 x^{5} - 4 x^{3} - x^{2} - 2 x - 1, 1\right)}^{4} + 1}{-1 + \operatorname{CRootOf} {\left(2 x^{5} - 4 x^{3} - x^{2} - 2 x - 1, 1\right)}^{2}}\right], \  \left[ \operatorname{CRootOf} {\left(2 x^{5} - 4 x^{3} - x^{2} - 2 x - 1, 2\right)}, \  \frac{1 + \operatorname{CRootOf} {\left(2 x^{5} - 4 x^{3} - x^{2} - 2 x - 1, 2\right)} + \operatorname{CRootOf} {\left(2 x^{5} - 4 x^{3} - x^{2} - 2 x - 1, 2\right)}^{4}}{-1 + \operatorname{CRootOf} {\left(2 x^{5} - 4 x^{3} - x^{2} - 2 x - 1, 2\right)}^{2}}\right]\right]

    which approximates to

    .. math::
        \left[ \left[ -1.4037567900355, \  3.58487919398945\right], \  \left[ -0.441902599484908, \  -0.740915239126713\right], \  \left[ 1.66430437054306, \  5.84024389246302\right]\right]

    .. figure:: Images/Der019.png
        :alt: Approximate Local Extremes

        Approximate Local Extremes


:index:`Continuous Domain`
--------------------------

This option will open a dialog box asking for the independent variable to use, if the program is to use the entire real line or an interval as the encompassing domain and the bounds for the interval if that is selected.  The result is a union of intervals inside the encompassing domain where the function is continuous.  While this is not technically the domain of the function, with most functions studied in Calculus the domain and the continuous domain are the same.

For example, if we take the function :math:`\tan(x)` on the entire real line the result is,

.. math::
    \mathbb{R} \setminus \left(\left\{2 \pi k + \frac{\pi}{2}\; \middle|\; k \in \mathbb{Z}\right\} \cup \left\{2 \pi k + \frac{3 \pi}{2}\; \middle|\; k \in \mathbb{Z}\right\}\right)

which is :math:`\mathbb{R}` minus the singularities. If we used the same function on the interval :math:`[0, 10]` we get,

.. math::
    \left[0, \frac{\pi}{2}\right) \cup \left(\frac{\pi}{2}, \frac{3 \pi}{2}\right) \cup \left(\frac{3 \pi}{2}, \frac{5 \pi}{2}\right) \cup \left(\frac{5 \pi}{2}, 10\right]

.. note::

    In cases where there are a lot of singularities, such as :math:`\tan(x)`, it is better to use the entire real line and not a large interval.  If there are a lot of intervals in the union the process can be lengthy.


Variable Assumptions
--------------------

.. include:: ../CLAE/VariableAssumptions.md

