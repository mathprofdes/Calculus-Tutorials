
Assumptions about variables are essentially what type of number does the variable represent.  In most cases in an introductory Calculus sequence you simply assume that all variables represent real numbers, and sometimes complex numbers.  The default setting for variables is as a real number except for solving equations where we use complex numbers.

As a classic example, say we input ``sqrt(x^2)`` into the CAS, the entry would be displayed as,

.. math::

    \sqrt{x^{2}}

If we select ``Algebra > Simplify``, a simplification that makes no assumptions about the variables, the result is still, 

.. math::

    \sqrt{x^{2}}

But if we use ``Algebra > Special Simplifications``, leave the settings as is, and click OK the result is,

.. math::
    
    \left|{x}\right|

The difference is that the default domain for ``x`` in the Special Simplifications dialog was a real number.  In the real number system, :math:`\sqrt{x^{2}} = \left|{x}\right|` but in the complex number system it is not.  For example, :math:`\sqrt{i^{2}} = -1 \neq \left|{i}\right| = 1`.

Another classic example is in the study of l’Hospital’s Rule.  Marquis de l’Hospital published the very first Calculus textbook in 1696, where l’Hospital’s Rule is first seen in print. l’Hospital did not discover this rule, the Swiss mathematician John Bernoulli (1667–1748) is the one who discovered the method.  l’Hospital and Bernoulli had an interesting business relationship where l’Hospital purchased the rights to this method, which is why it is named after him and not Bernoulli.  In his book l’Hospital wanted to calculate,

.. math::

    \lim_{x \to a} \frac{\sqrt{2a^3x-x^4} - a \sqrt[3]{a^2x} }{a - \sqrt[4]{ax^3}}

which is a :math:`\frac{0}{0}` indeterminate form and hence can be attacked using l’Hospital’s Rule.  This expression also assumed that :math:`a > 0`.  

If we put this expression into our CAS ``(-a*(a^2*x)^(1/3) + sqrt(2*a^3*x - x^4))/(a - (a*x^3)^(1/4))``, then select ``Calculus > Limit``, when the limit dialog comes up input ``x`` for the variable and ``a`` for the limit point, and click OK.  The result will be, 

.. math::

    \frac{- a^{\frac{4}{3}} \left|{a}\right|^{\frac{2}{3}} + a^{2}}{a - \left|{a}\right|}

It should be fairly obvious that this does not work for ``a`` being a positive real number since the denominator is clearly 0 in this case.  This time when we select ``Calculus > Limit`` we will change the data type of ``a`` to be a positive real, and leave ``x`` alone.  This time the result is the correct answer for these assumptions of,

.. math::

    \frac{16 a}{9}

In the vast majority of cases you will not need to do anything with variable assumptions. The reason we incorporated the ability to specify assumptions about the variable data type is that in a few instances (like in the above examples) you may need to tell the program that variable belongs to a more restrictive domain.  
