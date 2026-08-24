:index:`Indeterminate Forms`
============================

Discussion & Definitions
------------------------

Indeterminate Forms are where most textbooks discuss l'Hospital’s Rule.  This is a nice technique for finding limits that are difficult and have a certain form to them.  It is also an application of the derivative, which is why it is here and not in the material on limits.

As with derivative techniques this is primarily a by hand technique but is also incorporated into many computer algebra systems in the code for calculating limits.  Since these tutorials are focused on using computer algebra system technology we will not go into how to apply the rule in your by hand calculations.  Instead we will give a quick summary of the rule, the forms it can be used for, and then do some examples using our software systems.

.. admonition:: Theorem: l'Hospital’s Rule (0/0 Case)

    Suppose :math:`f` and :math:`g` are differentiable functions over an open interval containing :math:`a`, except possibly at :math:`a`. If :math:`\lim_{x \to a} f(x) = 0` and :math:`\lim_{x \to a} g(x) = 0`, then

    .. math::
        \lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}

    assuming the limit on the right exists or is :math:`\infty` or :math:`-\infty`. This result also holds if we are considering one-sided limits, or if :math:`a` is :math:`-\infty` or :math:`\infty`.

Here is why it is called an indeterminate form.  From the language it implies that limits of this form cannot be determined.  In other words, if all we know is that we have a 0/0 form the limit could be anything.  As some examples, where each of the limit is of the form 0/0.

.. math::
    \lim_{x \to 0} \frac{\sin(x)}{x} = 1

.. math::
    \lim_{x \to 0} \frac{3\sin(x)}{x} = 3

.. math::
    \lim_{x \to 0^+} \frac{- x^{2} + \tan{\left(x \right)}}{x^{2} \tan{\left(x \right)}} = \infty

.. admonition:: Theorem: l'Hospital’s Rule (:math:`\infty/\infty` Case)

    Suppose :math:`f` and :math:`g` are differentiable functions over an open interval containing :math:`a`, except possibly at :math:`a`. If :math:`\lim_{x \to a} f(x) = \pm \infty` and :math:`\lim_{x \to a} g(x) = \pm \infty`, then

    .. math::
        \lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}

    assuming the limit on the right exists or is :math:`\infty` or :math:`-\infty`. This result also holds if we are considering one-sided limits, or if :math:`a` is :math:`-\infty` or :math:`\infty`.

For other indeterminate forms are as follows, in each case the goal to calculate the limit is to manipulate the form into one of the two above and then complete the calculation.

.. admonition:: Other Indeterminate Forms

    - :math:`f(x) \cdot g(x) \to 0 \cdot \infty` form, invert one of the functions to, :math:`\frac{f(x)}{1/g(x)}` or :math:`\frac{g(x)}{1/f(x)}` to obtain one of the above forms.

    - :math:`f(x) - g(x) \to \infty - \infty` form, no set process here, algebraically manipulate to obtain one of the above forms.

    - :math:`f(x)^{g(x)} \to 1^\infty {\; \rm or \; } \infty^0 {\; \rm or \; } 0^0` form, to solve these try the following procedure,

        i. Take the natural logarithm of the expression, :math:`\ln\left(f(x)^{g(x)}\right) = g(x) \cdot \ln\left(f(x)\right)`.

        ii. :math:`g(x) \cdot \ln\left(f(x)\right)` will be of the :math:`0 \cdot \infty` form.  Then use the technique from above to finish this limit.

        iii. If the limit exists raise it as a power of :math:`e` to obtain the limit of the original expression.

Example: :math:`\lim_{x \to 0^+} x \ln{\left(x \right)}`
--------------------------------------------------------

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    x*ln(x)

In a new cell input ``LimitAbove``, function is ``f`` and value is 0.  Result is 0.

CLAE
^^^^

Input the function,

.. code-block:: console

    x*ln(x)

Select ``Calculus > Limit``, variable is *x*, limit point is 0, the direction is right. Result is 0.


Maxima
^^^^^^

Input the function,

.. code-block:: console

    kill(all);
    f(x):=x*log(x)

Then find the limit,

.. code-block:: console

    limit(f(x),x,0,plus)

Result is 0.

Example: :math:`\lim_{x \to 0^+} \frac{1}{x^2} - \frac{1}{\tan(x)}`
-------------------------------------------------------------------

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    1/x^2 - 1/tan(x)

In a new cell input ``LimitAbove``, function is ``f`` and value is 0.  Result is :math:`\infty`.

CLAE
^^^^

Input the function,

.. code-block:: console

    1/x^2 - 1/tan(x)

Select ``Calculus > Limit``, variable is *x*, limit point is 0, the direction is right. Result is :math:`\infty`.


Maxima
^^^^^^

Input the function,

.. code-block:: console

    kill(all);
    f(x):=1/x^2 - 1/tan(x)

Then find the limit,

.. code-block:: console

    limit(f(x),x,0,plus)

Result is :math:`\infty`.





Example: :math:`\lim_{x \to a} \frac{\sqrt{2a^3x-x^4} - a \sqrt[3]{a^2x} }{a - \sqrt[4]{ax^3}}` with :math:`a > 0`
------------------------------------------------------------------------------------------------------------------

Another classic example is in the study of l’Hospital’s Rule.  Marquis de l’Hospital published the very first Calculus textbook in 1696, where l’Hospital’s Rule is first seen in print. l’Hospital did not discover this rule, the Swiss mathematician John Bernoulli (1667–1748) is the one who discovered the method.  l’Hospital and Bernoulli had an interesting business relationship where l’Hospital purchased the rights to this method, which is why it is named after him and not Bernoulli.  In his book l’Hospital wanted to calculate,

.. math::

    \lim_{x \to a} \frac{\sqrt{2a^3x-x^4} - a \sqrt[3]{a^2x} }{a - \sqrt[4]{ax^3}}

which is a :math:`\frac{0}{0}` indeterminate form and hence can be attacked using l’Hospital’s Rule (really Bernoulli's Rule).  This expression also assumed that :math:`a > 0`.

GeoGebra
^^^^^^^^

With GeoGebra if we try to input the expression,

.. code-block:: console

    (-a*(a^2*x)^(1/3) + sqrt(2*a^3*x - x^4))/(a - (a*x^3)^(1/4))

GeoGebra will not see *a* as an undefined variable, it will automatically create a slider for it and substitute the slider value into the expression.  This makes it difficult to establish the limit in general so we will not use GeoGebra for this example.

CLAE
^^^^

Input the function,

.. code-block:: console

    (-a*(a^2*x)^(1/3) + sqrt(2*a^3*x - x^4))/(a - (a*x^3)^(1/4))

Select ``Calculus > Limit``, variable is *x*, limit point is 0, the direction is Two Sided.  Now before clicking OK we have additional information that CLAE needs to know about, that is :math:`a > 0`.  Select ``Edit Variable Properties``, in the dialog box that comes up select the *a* entry in the left and then select positive on the right, clisk OK then click OK on the limit dialog.  The result is :math:`\frac{16 a}{9}`.


.. note::
    If we had not told CLAE that *a* was positive, the result would have been,

    .. math::

        \frac{- a^{\frac{4}{3}} \left|{a}\right|^{\frac{2}{3}} + a^{2}}{a - \left|{a}\right|}

    It should be fairly obvious that this does not work for ``a`` being a positive real number since the denominator is clearly 0 in this case.  By telling CLAE that *a* was positive it could use different simplification routines to result in a better answer.

Maxima
^^^^^^

Input the function,

.. code-block:: console

    kill(all);
    f(x):=(-a*(a^2*x)^(1/3) + sqrt(2*a^3*x - x^4))/(a - (a*x^3)^(1/4))

Then find the limit,

.. code-block:: console

    limit(f(x),x,a)

When you run the limit command Maxima is smart enough to realize that the answer is dependent on the value of *a*.  Since we do not set this in advance, as in CLAE, Maxima comes back with a question, "Is "a" positive or negative?".  The user then types in the response followed by Shift+Enter.  You can type in the words positive or negative or just the first letter is sufficient.  Here we typed in p for positive and hit Shift+Enter. Maxima then finished out the calculation. The result is :math:`\frac{16 a}{9}`.

.. code-block:: maxima

    (%i1)   kill(all);
            f(x):=(-a*(a^2*x)^(1/3) + sqrt(2*a^3*x - x^4))/(a - (a*x^3)^(1/4));
    (%o0)   done
    (%o1)   f(x):=((-a)*(a^2*x)^(1/3)+sqrt(2*a^3*x-x^4))/(a-(a*x^3)^(1/4))

    (%i2)   limit(f(x),x,a);
            "Is "a" positive or negative?"p;
    (%o2)   (16*a)/9

