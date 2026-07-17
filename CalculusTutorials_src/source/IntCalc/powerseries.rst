:index:`Power Series`
=====================

Discussion & Definitions
------------------------

From the previous sections we have been working with infinite series that either converge or diverge.  If they converge then it sums to a number.  In general, we are going to do now is turn these infinite series into functions by adding in a variable to each term.  Specifically,

.. admonition:: Definition: A Power Series

    A series of the form

    .. math::
        \sum_{n = 0}^\infty c_n x^n = c_0 + c_1 x + c_2 x^2 + c_3 x^3 + \cdots

    is a power series centered at :math:`x = 0`. A series of the form

    .. math::
        \sum_{n = 0}^\infty c_n (x - a)^n = c_0 + c_1 (x - a) + c_2 (x - a)^2 + c_3 (x - a)^3 + \cdots

    is a power series centered at :math:`x = a`.  The :math:`c_i` are all real number constants that are called coefficients.

A power series may converge for some values of *x* and may diverge for other values of *x*, or it is possible that a power series converges for all values of *x*.  One thing that is certain is that a power series always converges at :math:`x = a` (its center) since the sum is :math:`c_0`.  It turns out that there are only three cases for the convergence of a power series,

.. admonition:: Theorem: Convergence of a Power Series

    Given a power series centered at :math:`x = a`,

    .. math::
        \sum_{n = 0}^\infty c_n (x - a)^n = c_0 + c_1 (x - a) + c_2 (x - a)^2 + c_3 (x - a)^3 + \cdots

    The series satisfies exactly one of the following properties,

    1. The series converges at :math:`x = a` and diverges for all :math:`x \neq a`.
    2. The series converges for all real numbers :math:`x`.
    3. There exists a real number :math:`R > 0` such that the series converges if :math:`|x - a| < R` and diverges if :math:`|x - a| > R`. At the values :math:`x` where :math:`|x - a| = R`, the series may converge or diverge.

From the above theorem it shows that the set of all values of *x* where the series converges is an interval.  In the first case it is an interval of a single point :math:`[a, a]`, in the second case it is the entire real line :math:`(-\infty \infty)`, and in the third case it is one of the following four possibilities, :math:`(a-R, a+R)`, :math:`(a-R, a+R]`, :math:`[a-R, a+R)`, or :math:`[a-R, a+R]`.

The value :math:`R` is called the **radius of convergence**.  The **interval of convergence** is the interval of *x* values that the series converges.

The radius of convergence is usually found using the ratio test.  If the radius is 0 then we are in case 1, if the radius is :math:`\infty` we are in case 2, and if the radius is a finite positive number we are in case 3.  If we are in case 3 then to find the interval if convergence we need to check the two endpoints separately to determine if they are in the interval or not. The ratio and root tests will both fail at the endpoints so we need to use other methods to determine their inclusion.

We will use CLAE for the examples in this section.

Example: :math:`\sum_{n = 0}^\infty \frac{n^2 x^n}{2^n}`
--------------------------------------------------------

In this example we will find the radius and interval of convergence of the power series :math:`\displaystyle \sum_{n = 0}^\infty \frac{n^2 x^n}{2^n}`.

Input the nth term expression,

.. code-block:: console

    n^2*x^n/2^n

At this point we are going to set up the ratio test, select ``Algebra > Evaluate``, for the variable input *n* and for the expression input ``n + 1``.  This will give the result,

.. math::
    2^{- n - 1} x^{n + 1} \left(n + 1\right)^{2}

Assuming that the original expression came in as ``R1`` and the *n + 1* expression came in as ``R2`` form the ratio test expression by,

.. code-block:: console

    Abs(R2/R1)

The result is a little scary

.. math::
    \frac{2^{- \operatorname{re}{\left(n\right)} - 1} \cdot 2^{\operatorname{re}{\left(n\right)}} \left|{\frac{x^{n + 1} \left(n + 1\right)^{2}}{n^{2}}}\right|}{\left|{x^{n}}\right|}

but if we simplify it we get,

.. math::
    \frac{\left|{\frac{x \left(n + 1\right)^{2}}{n^{2}}}\right|}{2}

Select ``Calculus > Limit``, variable *n* and point is ``oo``, we get,

.. math::
    \frac{\left|{x}\right|}{2}

The ratio test says that the series converges if the result of that limit is less than 1, that is,

.. math::
    \frac{\left|{x}\right|}{2} < 1

which means,

.. math::
    \left|{x}\right| < 2

or equivalently,

.. math::
    -2 < x < 2

Note that we could also do this using the computer, assuming that :math:`\frac{\left|{x}\right|}{2}` was ``R5`` input ``R5 < 1`` into the CAS and then select ``Algebra > Solve``, variable *x*, and the result is,

.. math::
    -2 < x \wedge x < 2

where :math:`\wedge` means "and".  At this point we know we are in case 3 and we need to check the two endpoints, :math:`x = -2` and :math:`x = 2`.

First we substitute :math:`-2` for *x*. Select the original expression then select ``Algebra > Evaluate``, variable is *x* and expression is :math:`-2`.  The result is,

.. math::
    \left(-2\right)^{n} 2^{- n} n^{2}

simplify to

.. math::
    \left(-1\right)^{n} n^{2}

we certainly do not need the computer to tell us that :math:`\sum_{n = 0}^\infty \left(-1\right)^{n} n^{2}` diverges, just use the divergence test.  Do the same to substitute 2 for *x* and we get :math:`n^2`, again it is easy to deduce that :math:`\sum_{n = 0}^\infty n^{2}` also diverges.  So the interval of convergence is :math:`(-2, 2)`.


Example: :math:`\sum_{n = 0}^\infty \frac{x^n}{n!}`
---------------------------------------------------

Input the nth term expression,

.. code-block:: console

    x^n/n!

Evaluate *n* to *n + 1* to get,

.. math::
    \frac{x^{n + 1}}{\left(n + 1\right)!}

Form the ratio,

.. code-block:: console

    Abs(R2/R1)

to get,

.. math::
    \frac{\left|{\frac{x^{n + 1} n!}{\left(n + 1\right)!}}\right|}{\left|{x^{n}}\right|}

simplify

.. math::
    \left|{\frac{x}{n + 1}}\right|

Take the limit as :math:`n \to \infty` and the result is 0.  Since :math:`0 < 1` for any real number we put in for *x* we are in case 2 and the interval os convergence is :math:`(-\infty, \infty)`.

Example: :math:`\sum_{n = 0}^\infty n! x^n`
-------------------------------------------

Input the nth term expression,

.. code-block:: console

    n! * x^n

Evaluate *n* to *n + 1* to get,

.. math::
    x^{n + 1} \left(n + 1\right)!

Form the ratio,

.. code-block:: console

    Abs(R2/R1)

to get,

.. math::
    \frac{\left|{\frac{x^{n + 1} \left(n + 1\right)!}{n!}}\right|}{\left|{x^{n}}\right|}

simplify

.. math::
    \left|{x \left(n + 1\right)}\right|

Take the limit as :math:`n \to \infty` and the result is :math:`\infty \operatorname{sign}{\left(\left|{x}\right| \right)}`.  So the only value of *x* that produces a non infinite result id the center :math:`x = 0` os the interval of convergence is a single point :math:`\{ 0 \}`.
