:index:`Series`
===============

Discussion & Definitions
------------------------

In this section we will be taking a sequence :math:`\{ a_n \}` and adding up all the (infinite number of) terms in the sequence, that is,

.. math::
    \sum_{n = 1}^\infty a_n = a_1 + a_2  + a_3 + a_4 + \cdots

This is called an infinite series.  The first question is, how do we attack such a problem?  One approach is to change the series into a sequence and then use what we discussed in the previous section.  The way we will alter this series into a sequence is to take the sum of the first *n* terms for each *n*, these are called partial sums.  Specifically,

.. math::
    s_1 & = a_1 \\
    s_2 & = a_1 + a_2 \\
    s_3 & = a_1 + a_2 + a_3 \\
    s_4 & = a_1 + a_2 + a_3 + a_4 \\
    & \vdots \\
    s_n & = a_1 + a_2 + a_3 + a_4 + \cdots + a_n = \sum_{k = 1}^n a_k \\
    & \vdots \\

Then :math:`\{ s_n \}` is a sequence (of partial sums) and it seems reasonable that if this sequence converges it would converge to the same value as the series.  So if :math:`\{ s_n \}` converges to :math:`S` then we say,

.. math::
    \sum_{n = 1}^\infty a_n = a_1 + a_2  + a_3 + a_4 + \cdots = S

If the sequence :math:`\{ s_n \}` diverges then we say that the series :math:`\displaystyle \sum_{n = 1}^\infty a_n` diverges.

In general these can be difficult to calculate, the main problem is getting a closed form for the nth partial sum, :math:`s_n.`  If we can do that then the limit of the function should be relatively easy.  In many cases we simply need to know if the series converges or diverges.  If it does converge then sometimes just having a good estimate on the sum is sufficient.  Even if we cannot find the actual value of a convergent series we can use approximation techniques and algebraic manipulations to extract information about the series.

.. admonition:: Theorem: Algebraic Properties of Convergent Series

    If we have two convergent series :math:`\displaystyle \sum_{n = 1}^\infty a_n` and :math:`\displaystyle \sum_{n = 1}^\infty b_n`, then

    - :math:`\displaystyle \sum_{n = 1}^\infty a_n + b_n` converges to :math:`\displaystyle \sum_{n = 1}^\infty a_n + \sum_{n = 1}^\infty  b_n`.

    - :math:`\displaystyle \sum_{n = 1}^\infty a_n - b_n` converges to :math:`\displaystyle \sum_{n = 1}^\infty a_n - \sum_{n = 1}^\infty  b_n`.

    - For any real number :math:`c`, :math:`\displaystyle \sum_{n = 1}^\infty ca_n` converges to :math:`\displaystyle c \sum_{n = 1}^\infty a_n`.

Example: Geometric Series
-------------------------

A :index:`geometric series` is any series that we can write in the form

.. math::
    a + ar + ar^2 + ar^3 + \cdots = \sum_{n = 1}^\infty ar^{n-1}

These series are ones where we can find a nice expression for the nth partial sum.  We will not go through the derivation here, and leave it to your textbook for the details.

.. math::
    s_n = a + ar + ar^2 + ar^3 + \cdots ar^(n-1) = \frac{a \left(r^{n} - 1\right)}{r - 1} = \frac{a \left(1 - r^{n} \right)}{1 - r}

where :math:`r \neq 1`. Then

.. math::
    \lim_{n \to \infty} s_n = \lim_{n \to \infty} \frac{a \left(1 - r^{n} \right)}{1 - r} = \frac{a }{1 - r}

as long as :math:`-1 < r < 1`. The sequence (and hence series) diverges otherwise.

CLAE
^^^^

We will start out with the general solution, input the  expression for the nth term.  We will use :math:`ar^k` and then let *k* go from 0 to :math:`n-1`.

.. code-block:: console

    a*r^k

Now we will find both the nth partial sum and the infinite sum.  For the nth partial sum select ``Calculus > Sums > Sum``, the variable is *k*, the beginning index is 0 and the ending index is :math:`n-1`.  The result is,

.. math::
    a \left(\begin{cases} n & \text{for}\: r = 1 \\\frac{1 - r^{n}}{1 - r} & \text{otherwise} \end{cases}\right)

If we simplify this expression we get,

.. math::
    \begin{cases} a n & \text{for}\: r = 1 \\\frac{a \left(r^{n} - 1\right)}{r - 1} & \text{otherwise} \end{cases}

We know that for convergence we need :math:`|r| < 1`, so the second expression is what we would use.  Although we will not need to do this, if we wanted to extract this expression we could select ``Edit > Piecewise Conversions / Extractions > Extract Expression from Piecewise Function`` then set the number of the expression to 2 and the result will be :math:`\frac{a \left(r^{n} - 1\right)}{r - 1}`.

To find the sum of the first 10 terms of :math:`3 \cdot 0.5^n`, select the expression for the nth partial sum, then select ``Algebra > Evaluate``, the dialog box that appears should have the following in the variables box, ``[a, n, r]``.  Input the values for the variables in the same order they appear in the variables list, separated by commas and the brackets are optional, specifically ``3, 10, 0.5``, the result is 5.994140625.

To find the sum of the infinite series we can select the original expression :math:`a r^{k}`, then select ``Calculus > Sums > Sum``,  The variable is *k*, beginning index is 0 and the ending index is ``oo`` (our symbol for :math:`\infty`).  The result is

.. math::
    a \left(\begin{cases} \frac{1}{1 - r} & \text{for}\: \left|{r}\right| < 1 \\\sum_{k=0}^{\infty} r^{k} & \text{otherwise} \end{cases}\right)

simplified becomes,

.. math::
    \begin{cases} - \frac{a}{r - 1} & \text{for}\: r > -1 \wedge r < 1 \\a \sum_{k=0}^{\infty} r^{k} & \text{otherwise} \end{cases}

Again we could extract the first expression since this one corresponds to the convergence criteria.  Or we can simply select the above expression, select ``Algebra > Evaluate``, use 3 for *a*, 1/2 for *r*, and 1 for *k* (which is simply needed for input but is not used in the evaluation), the result is 6.

Maxima
^^^^^^

For the general nth partial sum, input

.. code-block::

    ps:sum(a*r^k, k, 0, n-1), simpsum;

.. math::
    \frac{a\, \left( {{r}^{n}}-1\right) }{r-1}\mbox{}

We can change this into a function with

.. code-block::

    f(a, r, n):=''ps;

Then we can find the sum of the first 10 terms of :math:`3 \cdot 0.5^n` with,

.. code-block::

    f(3, 0.5, 10);

The result is 5.994140625.

For the infinite sum we can evaluate,

.. code-block::

    sm:sum(a*r^k, k, 0, inf), simpsum;

Maxima will ask you if :math:`|r| - 1` is positive, negative, or zero, input *n* and then Shift+Enter.

.. math::
    \frac{a}{1-r}\mbox{}

Change this into a function with

.. code-block:: console

    g(a, r):=''sm;

Then the infinite sum for the example above is,

.. code-block:: console

    g(3, 1/2);

which returns 6.


Example: Harmonic Series
------------------------

.. admonition:: Definition: The Harmonic Series

    A series that comes up frequently both in theory and practice is the :index:`harmonic series`. The harmonic series is defined as

    .. math::
        \sum_{n = 1}^\infty \frac{1}{n} = 1 + \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \frac{1}{5} + \cdots

As we will see below, the harmonic series diverges.

CLAE
^^^^

Input the expression for the nth term,

.. code-block:: console

    1/n

Then select ``Calculus > Sums > Sum``, for the variable use *n*, beginning index is 1 and the ending index is ``oo`` (our symbol for :math:`\infty`).  The result is :math:`\infty`.

One interesting fact about this series is that is grows very slowly.  To see this select the ``1/n`` expression, then select ``Calculus > Sums > Approximate Sum``, *n* is the variable, beginning index is 1 and set the ending index to 1000000.  The result is only 14.392726722864989, and the sum of the first 10,000,000 terms is only 16.695311365857272.


Maxima
^^^^^^

To show the divergence of the harmonic series input,

.. code-block:: console

    sum(1/n, n, 0, inf), simpsum;

The result is an error that tells you that the series diverges.  To see the slow convergence we can change the infinity to *k*

.. code-block:: console

    hs:sum(1.0/n, n, 1, k), simpsum;

then turn this into a function,

.. code-block:: console

    hsf(k):=''hs;

then find the sum of the first 100,000 entries,

.. code-block:: console

    hsf(100000), simpsum;

The result is 12.09014612986343.

Example: Telescoping Series
---------------------------

Another series of interest is a telescoping series. This is a series where the majority of the middle terms of a partial sum cancel each other out.  For example,

.. math::
    \sum_{n = 1}^\infty \frac{1}{n(n+1)}

If we use partial fractions on the nth tern expression we get,

.. math::
    \sum_{n = 1}^\infty \frac{1}{n(n+1)} = \sum_{n = 1}^\infty \frac{1}{n} - \frac{1}{n + 1}

so the nth partial sum is

.. math::
    s_n = 1 - \frac{1}{2} + \frac{1}{2} - \frac{1}{3} + \frac{1}{2} - \frac{1}{3} + \cdots + \frac{1}{n} - \frac{1}{n+1} = 1 - \frac{1}{n+1}

so

.. math::
    \sum_{n = 1}^\infty \frac{1}{n(n+1)} = \lim_{n \to \infty} s_n = \lim_{n \to \infty} 1 - \frac{1}{n+1} = 1

Although we are primarily interested in how to use the computer algebra systems to investigate these concepts this is a nice method for some by-hand calculations.  In addition, this is built into some computer systems when evaluating infinite sums.

CLAE
^^^^

Input the expression,

.. code-block:: console

    1/(n*(n + 1))

then select ``Calculus > Sums > Sum``, the variable is *n*, beginning index is 1 and ending index is ``oo``.  The result is 1 as expected.

