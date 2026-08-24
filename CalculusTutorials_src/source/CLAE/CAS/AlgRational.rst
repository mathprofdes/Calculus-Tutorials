:index:`Rational Expressions`
=============================

These options will help decompose rational expressions.

:index:`Numerator`
------------------

This will extract the numerator of the rational expression.  If the expression is not a single rational expression the program will attempt to combine the expression into a single rational expression before returning the numerator.  For example, say we get the numerator from the partial fraction decomposition of :math:`\displaystyle \frac{1}{x^{3} - 1}`,

.. math::
    \frac{- x - 2}{3 x^{2} + 3 x + 3} + \frac{1}{3 x - 3}

the program will return :math:`3 x^{2} + 3 x + \left(- x - 2\right) \left(3 x - 3\right) + 3` which simplifies to 9.  As you can see it simply simplified the expression to a common denominator.

:index:`Denominator`
--------------------

This will extract the denominator of the rational expression.  If the expression is not a single rational expression the program will attempt to combine the expression into a single rational expression before returning the denominator.  For example, say we get the numerator from the partial fraction decomposition of :math:`\displaystyle \frac{1}{x^{3} - 1}`,

.. math::
    \frac{- x - 2}{3 x^{2} + 3 x + 3} + \frac{1}{3 x - 3}

the program will return :math:`\left(3 x - 3\right) \left(3 x^{2} + 3 x + 3\right)` which simplifies to :math:`9 x^{3} - 9`.  As you can see it simply simplified the expression to a common denominator.


:index:`Numerator and Denominator`
----------------------------------

This will extract the numerator and denominator of the rational expression, as discussed above.  It will return the results in a list, the first entry is the numerator and the second entry is the denominator.  The example above gives the output of,

.. math::

    \left[ 3 x^{2} + 3 x + \left(- x - 2\right) \left(3 x - 3\right) + 3, \  \left(3 x - 3\right) \left(3 x^{2} + 3 x + 3\right)\right]
