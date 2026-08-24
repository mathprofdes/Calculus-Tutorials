:index:`Logarithmic Differentiation`
====================================

Discussion & Definitions
------------------------

Logarithmic Differentiation has two main situations where it comes in handy, first if you have a function as an exponent, as with, :math:`f(x) = \left(2 x^{4} + 1\right)^{\tan{\left(x \right)}}`, and second, to simplify expressions that would require several applications of product, quotient, and chain rules, as with, :math:`f(x) = \frac{x \sqrt{2 x + 1}}{e^{x} \sin^{3}{\left(x \right)}}`.

In the first case Logarithmic Differentiation would be the universal approach. In the second case it is a technique that allows the person calculating the derivative to simplify multiple product and chain rules to make their job a bit easier.  Since a computer algebra system does not need to make expressions easier (they can just muscle through the calculation) sometimes they will incorporate this technique and sometimes not.

Below if the process of Logarithmic Differentiation. We will use our three computer algebra systems on both :math:`f(x) = \left(2 x^{4} + 1\right)^{\tan{\left(x \right)}}`, and :math:`f(x) = \frac{x \sqrt{2 x + 1}}{e^{x} \sin^{3}{\left(x \right)}}`.  From the output we will make a guess to what method was applied to the function to find its derivative.

.. admonition:: Problem Solving: Steps in Logarithmic Differentiation

    #. Write the function :math:`f(x)` as the equation :math:`y = f(x)`.
    #. Take natural logarithms of both sides of the above equation :math:`y = f(x)`, giving :math:`\ln(y) = \ln(f(x))`.
    #. Use the logarithm rules to expand the right hand side of the expression :math:`\ln(f(x))` as far as possible.
    #. Differentiate implicitly with respect to *x* on both sides, the left hand side will always be :math:`\displaystyle \frac{y'}{y}`, by the chain rule.
    #. Solve the resulting equation for :math:`y'` and replace *y* by :math:`f(x)`.


Example: :math:`f(x) = \left(2 x^{4} + 1\right)^{\tan{\left(x \right)}}`
------------------------------------------------------------------------

With the function :math:`f(x) = \left(2 x^{4} + 1\right)^{\tan{\left(x \right)}}` the method of Logarithmic Differentiation is natural to apply in order to turn the :math:`\tan(x)` exponent into a product rule.  When you take the derivative of this function using Logarithmic Differentiation the result will look like,

.. math::
    {{\left( 2 {{x}^{4}}+1\right) }^{\tan{(x)}}} \left( {{\sec{(x)}}^{2}} \log{\left( 2 {{x}^{4}}+1\right) }+\frac{8 {{x}^{3}} \tan{(x)}}{2 {{x}^{4}}+1}\right) \mbox{}

GeoGebra
^^^^^^^^

Input the expression,

.. code-block:: console

    (2 x^(4)+1)^(tan(x))

Now take the first derivative with ``f'``.

.. math::
    \ln(2x^4 + 1) (2x^4 + 1)^{\tan(x)} + \ln(2x^4 + 1) \tan^2(x) (2x^4 + 1)^{\tan(x)} + 8x^3 \tan(x) (2x^4 + 1)^{\tan(x) - 1}

Which appears to be a simplified version of the solution.

CLAE
^^^^

Input the expression,

.. code-block:: console

    (2*x^4 + 1)^tan(x)

Take the first derivative with ``Calculus > Derivative``, variable *x*, order 1.  The result is,

.. math::
    \left(2 x^{4} + 1\right)^{\tan{\left(x \right)}} \left(\frac{8 x^{3} \tan{\left(x \right)}}{2 x^{4} + 1} + \left(\tan^{2}{\left(x \right)} + 1\right) \ln{\left(2 x^{4} + 1 \right)}\right)

Which is nearly identical to the solution by Logarithmic Differentiation.  CLAE tends to turn :math:`\sec^2(x)` into :math:`\tan^2(x) + 1`.


Maxima
^^^^^^

Input the function,

.. code-block:: console

    kill(all);
    f(x):=(2*x^4 + 1)^tan(x)

Then the derivative,

.. code-block:: console

    diff(f(x), x)

The result is,

.. math::
    {{\left( 2 {{x}^{4}}+1\right) }^{\tan{(x)}}} \left( {{\sec{(x)}}^{2}} \log{\left( 2 {{x}^{4}}+1\right) }+\frac{8 {{x}^{3}} \tan{(x)}}{2 {{x}^{4}}+1}\right) \mbox{}

A direct result from Logarithmic Differentiation.

Example: :math:`f(x) = \frac{x \sqrt{2 x + 1}}{e^{x} \sin^{3}{\left(x \right)}}`
--------------------------------------------------------------------------------

With the function :math:`f(x) = \frac{x \sqrt{2 x + 1}}{e^{x} \sin^{3}{\left(x \right)}}`, Logarithmic Differentiation would not be necessary to pull out a difficult exponent but would significantly simplify this derivative. The derivative of this function using Logarithmic Differentiation the result will look like,

.. math::
    \frac{x \sqrt{2 x + 1}}{e^{x} \sin^{3}{\left(x \right)}} \left( \frac{1}{x} + \frac{1}{2x+1} - 1- 3\cot(x) \right)

GeoGebra
^^^^^^^^

Input the expression,

.. code-block:: console

    x sqrt(2 x+1) ((ℯ^(-x))/(sin^(3)(x)))

Now take the first derivative with ``f'``.  We will not display the result here but from the output it is clear that GeoGebra did not use this method for the derivative.

CLAE
^^^^

Input the expression,

.. code-block:: console

    (x*sqrt(2*x+1))/(E^x*sin(x)^3)

Take the first derivative with ``Calculus > Derivative``, variable *x*, order 1.  The result is,

.. math::
    - \frac{x \sqrt{2 x + 1} e^{- x}}{\sin^{3}{\left(x \right)}} - \frac{3 x \sqrt{2 x + 1} e^{- x} \cos{\left(x \right)}}{\sin^{4}{\left(x \right)}} + \frac{x e^{- x}}{\sqrt{2 x + 1} \sin^{3}{\left(x \right)}} + \frac{\sqrt{2 x + 1} e^{- x}}{\sin^{3}{\left(x \right)}}

It does look like CLAE may have used Logarithmic Differentiation to solve this.  The result is equivalent to the above solution simply distributing the first term through the quantity.  On the other hand, it could have applied the quotient rule and then split the result into four fractions.  CLAE does not tend to do this in general, it would leave a long numerator over the denominator.  This is, of course, just a guess based on the way CLAE tends to simplify its results.

Maxima
^^^^^^

Input the function,

.. code-block:: console

    kill(all);
    f(x):=(x*sqrt(2*x+1))/(%e^x*sin(x)^3)

Then the derivative,

.. code-block:: console

    diff(f(x), x)

The result is,

.. math::
    -\frac{x \sqrt{2 x+1} {{ e}^{-x}}}{{{\sin{(x)}}^{3}}}+\frac{\sqrt{2 x+1} {{ e}^{-x}}}{{{\sin{(x)}}^{3}}}+\frac{x {{ e}^{-x}}}{\sqrt{2 x+1} {{\sin{(x)}}^{3}}}-\frac{3 x \sqrt{2 x+1} {{ e}^{-x}} \cos{(x)}}{{{\sin{(x)}}^{4}}}\mbox{}

The same output as with CLAE.  As with CLAE this could have used either method but Maxima does tent to break up fractions more so than CLAE.  Hence it is probable that  Logarithmic Differentiation was not used here.  This is, of course, just a guess based on the way Maxima tends to simplify its results.


