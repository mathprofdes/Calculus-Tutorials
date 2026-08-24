:index:`Separation and Collection of Variables`
===============================================

These tools will collect and separate variables as well as do a partial fraction decomposition of rational functions.

:index:`Separate Variables`
---------------------------

This option separates variables in an expression, if possible. It separates with respect to all variables in an expression and collects constant coefficients that are independent of the variables.

For example, :math:`\left(x y\right)^{a}` separates into :math:`x^{a} y^{a}`.

Another example, :math:`2 x^{2} z \sin{\left(y \right)} + 2 x^{2} z` separates into :math:`2 x^{2} z \left(\sin{\left(y \right)} + 1\right)`.

.. note::

    With this tool the bases of powers will be separated regardless of assumptions on the variables. So the user needs to be aware that when applying this tool that the domains of the variables allow the operations.  For example, with :math:`\left(x y\right)^{a}` separating into :math:`x^{a} y^{a}`, we are making the assumption that not both ``x`` and ``y`` are negative since in that case we would have,

    .. math::

        1 = \left( (-1) (-1) \right)^{1/2} = (-1)^{1/2} (-1)^{1/2} = i \cdot i = -1


:index:`Collect`
----------------

This tool collects additive terms of an expression. When this option is invoked a dialog box will appear asking which variable to collect.

For example, if we have the expression :math:`a x^{2} + a x + b x^{2} - b x + c` and collect (with ``x``) to :math:`c + x^{2} \left(a + b\right) + x \left(a - b\right)`.

:index:`Partial Fractions`
--------------------------

Does a partial fraction decomposition of the given rational function.  When selected, a dialog box will appear asking the user for the variable to decompose with respect to and the number system to factor the denominator over.  If the rational function is of a single variable, that variable will automatically be loaded into the variable text area.  Since partial fraction decomposition requires the factorization of the denominator polynomial this process can be lengthy, especially over the real numbers. Here are a couple examples.

Say we want to do a partial fraction decomposition of :math:`\displaystyle \frac{1}{x^{3} - 1}`.  Over the rationals and reals we get,

.. math::
    \frac{- x - 2}{3 x^{2} + 3 x + 3} + \frac{1}{3 x - 3}

and over the complex numbers we get,

.. math::
    \frac{- \frac{1}{2} - \frac{\sqrt{3} i}{2}}{3 x + \frac{3}{2} + \frac{3 \sqrt{3} i}{2}} + \frac{- \frac{1}{2} + \frac{\sqrt{3} i}{2}}{3 x + \frac{3}{2} - \frac{3 \sqrt{3} i}{2}} + \frac{1}{3 x - 3}

As another example, take :math:`\displaystyle \frac{1}{x^{4} + 1}`. Over the reals we get,

.. math::
    \frac{- \sqrt{2} x + 2}{4 x^{2} - 4 \sqrt{2} x + 4} + \frac{\sqrt{2} x + 2}{4 x^{2} + 4 \sqrt{2} x + 4}

and over the complex numbers we get,

.. math::
    \frac{\frac{\sqrt{2}}{2} + \frac{\sqrt{2} i}{2}}{4 x + 2 \sqrt{2} + 2 \sqrt{2} i} - \frac{- \frac{\sqrt{2}}{2} + \frac{\sqrt{2} i}{2}}{4 x + 2 \sqrt{2} - 2 \sqrt{2} i} - \frac{\frac{\sqrt{2}}{2} - \frac{\sqrt{2} i}{2}}{4 x - 2 \sqrt{2} + 2 \sqrt{2} i} - \frac{\frac{\sqrt{2}}{2} + \frac{\sqrt{2} i}{2}}{4 x - 2 \sqrt{2} - 2 \sqrt{2} i}

.. note::

    The partial fraction decomposition relies on the factorization of the denominator of the rational function.  The SymPy CAS uses two different algorithms to do the decomposition so the selection of a number system works a little differently depending on what you are factoring over.  The main difference is with the inclusion of other variables.  For example, when decomposing over the rationals or the complexes you can include other variables, but over the reals the rational expression must be of a single variable.  For example, say we wanted to decompose the expression :math:`\displaystyle \frac{1}{a x^{4} + 1}` over the complex number system, we would get,

    .. math::
        \frac{i \sqrt[4]{- \frac{1}{a}}}{4 x + 4 i \sqrt[4]{- \frac{1}{a}}} - \frac{i \sqrt[4]{- \frac{1}{a}}}{4 x - 4 i \sqrt[4]{- \frac{1}{a}}} + \frac{\sqrt[4]{- \frac{1}{a}}}{4 x + 4 \sqrt[4]{- \frac{1}{a}}} - \frac{\sqrt[4]{- \frac{1}{a}}}{4 x - 4 \sqrt[4]{- \frac{1}{a}}}

    Over the real number system the program would simply return the original rational expression.  In addition, decomposing over the reals can take substantially longer to complete.

