:index:`Taylor Series`
======================

Discussion & Definitions
------------------------

The Taylor and Maclaurin series derivations give us a method for starting with a function and then calculating the coefficients of the power series representation for that function. Unlike the previous section, we will not need to rely on the geometric series and series manipulations to represent functions with series.  Here is how it goes.

Derivation
^^^^^^^^^^

Say we wish to represent a function :math:`f(x)` as a series,

.. math::
    f(x) = \sum_{n = 0}^\infty c_n (x - a)^n = c_0 + c_1 (x - a) + c_2 (x - a)^2 + c_3 (x - a)^3 + \cdots

Finding :math:`c_0` is easy, evaluate both sides of the equation at :math:`x = a`,

.. math::
    f(a) = \sum_{n = 0}^\infty c_n (a - a)^n = c_0 + c_1 (a - a) + c_2 (a - a)^2 + c_3 (a - a)^3 + \cdots = c_0

so :math:`c_0 = f(a)`.  Now to get :math:`c_1`, take the derivative of both sides,

.. math::
    f'(x) = c_1  + 2c_2 (x - a) + 3c_3 (x - a)^2 + 4c_4 (x - a)^3 + \cdots

evaluating at :math:`x = a` gives :math:`c_1 = f'(a)`.  Taking the second derivative,

.. math::
    f''(x) = 2c_2 + 3 \cdot 2 \cdot c_3 (x - a) + 4 \cdot 3 \cdot c_4 (x - a)^2 + \cdots

evaluating at :math:`x = a` gives :math:`c_2 = \frac{f''(a)}{2}`.  Taking the third derivative,

.. math::
    f'''(x) = 3 \cdot 2 \cdot c_3 + 4 \cdot 3 \cdot 2 \cdot c_4 (x - a) + \cdots

evaluating at :math:`x = a` gives :math:`c_3 = \frac{f'''(a)}{2 \cdot 3}`.  Taking the fourth derivative,

.. math::
    f^{(4)}(x) = 4 \cdot 3 \cdot 2 \cdot c_4  + 5 \cdot 4 \cdot 3 \cdot 2 \cdot c_5  (x - a) + \cdots

evaluating at :math:`x = a` gives :math:`c_4 = \frac{f^{(4)}(a)}{2 \cdot 3 \cdot 4}`.  A this point we can see the pattern.  In general,

.. math::
    c_n = \frac{f^{(n)}(a)}{n!}

One thing this implies is that the function :math:`f(x)` has derivatives of all orders.  Also, as in the last section, the series expansion may not converge to the function on the entire domain of the function.

.. admonition:: Definition: Taylor Series

    If :math:`f` has derivatives of all orders at :math:`x = a`, then the **Taylor Series** for the function :math:`f` at :math:`a` is

    .. math::
        \sum_{n=0}^\infty \frac{f^{(n)}(a)}{n!} (x-a)^n = f(a) + f'(a)(x-a) + \frac{f''(a)}{2} (x-a)^2 + \cdots + \frac{f^{(n)}(a)}{n!} (x-a)^n + \cdots

    The Taylor series for :math:`f` at 0 is known as the **Maclaurin Series** for :math:`f.`

Frequently we need to work with the first several terms of the series so we give them a name as well.

.. admonition:: Definition: Taylor Polynomial

    If :math:`f` has *n* derivatives at :math:`x = a`, then the nth **Taylor Polynomial** for the function :math:`f` at :math:`a` is

    .. math::
        p_n(x) = f(a) + f'(a)(x-a) + \frac{f''(a)}{2} (x-a)^2 + \cdots + \frac{f^{(n)}(a)}{n!} (x-a)^n

    The nth Taylor polynomial for :math:`f` at 0 is known as the nth **Maclaurin Polynomial** for :math:`f.`

If you are finding Taylor series by hand you would take several derivatives and evaluate them at :math:`x = a` to find a pattern for :math:`f^{(n)}(a)`, then divide by :math:`n!` to get the general nth coefficient.  For example, let :math:`f(x) = e^x` and we will use :math:`a = 0`.

.. math::
    f(0) & = e^0 = 1 \\
    f'(0) & = e^0 = 1 \\
    f''(0) & = e^0 = 1 \\
    f'''(0) & = e^0 = 1 \\
    f^{(4)}(0) & = e^0 = 1 \\

So the pattern here is easy, 1, and our Taylor series is,

.. math::
    e^x = \sum_{n=0}^\infty \frac{x^n}{n!}

As another example take :math:`f(x) = \sin(x)` and we will again use :math:`a = 0`.

.. math::
    f(0) & = \sin(0) = 0 \\
    f'(0) & = \cos(0) = 1 \\
    f''(0) & = -\sin(0) = 0 \\
    f'''(0) & = -\cos(0) = -1 \\
    f^{(4)}(0) & = \sin(0) = 0 \\
    f^{(5)}(0) & = \cos(0) = 1 \\
    f^{(6)}(0) & = -\sin(0) = 0 \\
    f^{(7)}(0) & = -\cos(0) = -1 \\
    f^{(8)}(0) & = \sin(0) = 0 \\
    & \vdots

Obviously we get repetition every fourth derivative.  As for a pattern, all even derivatives are 0 and for all the odd derivatives we get 1 or :math:`-1`.  It is easy to see that :math:`f^{(2m+1)}(0) = (-1)^m`, so our series is,

.. math::
    \sin(x) = \sum_{n=0}^\infty (-1)^n \frac{x^{2n+1}}{(2n+1)!}

We did not discuss the intervals of convergence for either of these examples.  You can find that interval of convergence the same way as with a general power series, use the ratio test (or the root test).  For example, with

.. math::
    e^x = \sum_{n=0}^\infty \frac{x^n}{n!}

.. math::
    \lim_{n \to \infty} \left| \frac{\frac{x^{n+1}}{(n+1)!}}{\frac{x^n}{n!}} \right| = \lim_{n \to \infty} \frac{1}{n+1}|x| = 0

Hence the radius of convergence is infinite and the interval of convergence is :math:`(-\infty, \infty).`  The same is true for :math:`\sin(x)` but this does not happen for all functions.  The following is a list of some of the most used functions, their Taylor series (really Maclaurin series) expansions, and the radius of convergence of the series, we derived most of these in this section or the previous section.

.. math::
    \begin{array}{lc}
    \displaystyle \frac{1}{1-x} = \sum_{n = 0}^\infty x^n = 1 + x + x^2 + x^3 + \cdots & R = 1 \\
    \displaystyle e^x = \sum_{n = 0}^\infty \frac{x^n}{n!} = 1 + x + \frac{x^2}{2} + \frac{x^3}{3!} + \frac{x^4}{4!} + \cdots & R = \infty \\
    \displaystyle \sin(x) = \sum_{n=0}^\infty (-1)^n \frac{x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots & R = \infty \\
    \displaystyle \cos(x) = \sum_{n=0}^\infty (-1)^n \frac{x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots & R = \infty \\
    \displaystyle \tan^{-1}(x) = \sum_{n=0}^\infty (-1)^n \frac{x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots & R = 1 \\
    \displaystyle \ln(1+x) = \sum_{n = 1}^\infty (-1)^{n+1} \frac{x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots & R = 1 \\
    \end{array}


Convergence
^^^^^^^^^^^

One concept we glossed over is that of convergence.  We simply did a few derivatives and some algebra to obtain expressions for the coefficients of the series.  We did not verify that the series approaches the function on its interval of convergence.  Algebraically, this can get a bit complex and we will not go into much detail here but we will outline the theory.  Your textbook should have more details on this.  We will visualize this convergence graphically to get a feel for the concept.

.. admonition:: Theorem: Taylor Polynomial Remainder

    Let :math:`f` be a function that can be differentiated :math:`n + 1` times on an interval :math:`I` containing the real number :math:`a`. Let :math:`p_n(x)` be the nth Taylor polynomial of :math:`f` at :math:`a` and let

    .. math::
        R_n(x) = f(x) − p_n(x)

    be the nth remainder. Then for each :math:`x` in the interval :math:`I`. If there exists a real number :math:`M` such that :math:`\left| f^{(n+1)}(x) \right| \leq M`, for all :math:`x \in I` then,

    .. math::
        \left| R_n(x) \right| \leq \frac{M}{(n+1)!} |x-a|^{n+1}

    for all :math:`x \in I.`

.. admonition:: Theorem: Convergence of Taylor Series

    If :math:`f` has derivatives of all orders on an interval :math:`I` containing :math:`a`. Then the Taylor series

    .. math::
        \sum_{n=0}^\infty \frac{f^{(n)}(a)}{n!} (x-a)^n

    converges to :math:`f(x)` for all :math:`x \in I` if and only if

    .. math::
        \lim_{n \to \infty} R_n(x) = 0

    for all :math:`x \in I.`

So if we were verifying this algebraically we would need to take the remainder inequality and show that this expression goes to 0 as :math:`n \to \infty.`  Since the bound :math:`M` could change when *n* changes this can be a little tricky.

Example: Visualizing the Convergence of the Series for :math:`\sin(x)`
----------------------------------------------------------------------

We will approach this in a similar manner as we did with :math:`\frac{1}{1-x}` in the last section, except that we will use functions from the CAS to calculate the Taylor polynomials.

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    sin(x)

Now we will graph the degree 10, 20, and 30 Taylor polynomials along with the graph. To create the degree 10 Taylor polynomial use the following syntax, we assume that the function is :math:`f(x).`

.. code-block:: console

    TaylorPolynomial(f,0,10)

Repeat with ``TaylorPolynomial(f,0,20)`` and ``TaylorPolynomial(f,0,30)``.  You should see the following image.

.. figure:: Images/Series/series006.png
    :alt: Convergence of Taylor polynomials to the function sin(x).

    Convergence of Taylor polynomials to the function :math:`\sin(x)`

Note how the higher degree polynomials hug the graph for a longer interval.  Although this is far from an algebraic proof it does give you the feel that as the degree increases the polynomials will get closer to the function on the entire real line.  It also shows that we can do some interesting things with polynomials.

CLAE
^^^^

Input the function,

.. code-block:: console

    sin(x)

Now we will graph the degree 10, 20, and 30 Taylor polynomials along with the graph. To create the degree 10 Taylor polynomial, select the function, then select ``Calculus > Taylor Series``, variable is *x*, point is 0, and the order is 10.  The result is,

.. math::
    \frac{x^{9}}{362880} - \frac{x^{7}}{5040} + \frac{x^{5}}{120} - \frac{x^{3}}{6} + x

Do the same with order 20 and 30, the results are,

.. math::
    - \frac{x^{19}}{121645100408832000} + \frac{x^{17}}{355687428096000} - \frac{x^{15}}{1307674368000} + \frac{x^{13}}{6227020800} - \frac{x^{11}}{39916800} + \frac{x^{9}}{362880} - \frac{x^{7}}{5040} + \frac{x^{5}}{120} - \frac{x^{3}}{6} + x

and

.. math::
    \frac{x^{29}}{8841761993739701954543616000000} - \frac{x^{27}}{10888869450418352160768000000} + \frac{x^{25}}{15511210043330985984000000} - \frac{x^{23}}{25852016738884976640000} + \frac{x^{21}}{51090942171709440000} - \frac{x^{19}}{121645100408832000} + \frac{x^{17}}{355687428096000} - \frac{x^{15}}{1307674368000} + \frac{x^{13}}{6227020800} - \frac{x^{11}}{39916800} + \frac{x^{9}}{362880} - \frac{x^{7}}{5040} + \frac{x^{5}}{120} - \frac{x^{3}}{6} + x

Graph the three polynomials along with the function and you should have the following image.

.. figure:: Images/Series/series007.png
    :alt: Convergence of Taylor polynomials to the function sin(x).

    Convergence of Taylor polynomials to the function :math:`\sin(x)`

Note how the higher degree polynomials hug the graph for a longer interval.  Although this is far from an algebraic proof it does give you the feel that as the degree increases the polynomials will get closer to the function on the entire real line.  It also shows that we can do some interesting things with polynomials.

Maxima
^^^^^^

Input the function,

.. code-block:: console

    kill(all);
    f(x):=sin(x)

To create the Taylor polynomials we can use the ``taylor`` function,

.. code-block:: console

    t10:taylor(f(x),x,0,10);
    t20:taylor(f(x),x,0,20);
    t30:taylor(f(x),x,0,30);

Then we can plot these along with the function by,

.. code-block:: console

    wxplot2d([f(x), t10, t20, t30],[x,-15,15],[y,-10,10]);

The image should look something like the following,

.. figure:: Images/Series/series008.png
    :alt: Convergence of Taylor polynomials to the function sin(x).

    Convergence of Taylor polynomials to the function :math:`\sin(x)`

Note how the higher degree polynomials hug the graph for a longer interval.  Although this is far from an algebraic proof it does give you the feel that as the degree increases the polynomials will get closer to the function on the entire real line.  It also shows that we can do some interesting things with polynomials.


Example: Visualizing the Convergence of the Series for :math:`\sin(x)` about :math:`x = \pi`
--------------------------------------------------------------------------------------------

We will do the same process here as we did in the last example except that we will center the series at :math:`x = \pi` instead of :math:`x = 0.`

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    sin(x)

Now we will graph the degree 10, 20, and 30 Taylor polynomials along with the graph. To create the degree 10 Taylor polynomial use the following syntax, we assume that the function is :math:`f(x).`

.. code-block:: console

    TaylorPolynomial(f,pi,10)

Repeat with ``TaylorPolynomial(f,pi,20)`` and ``TaylorPolynomial(f,pi,30)``.  You should see the following image.

.. figure:: Images/Series/series009.png
    :alt: Convergence of Taylor polynomials to the function sin(x).

    Convergence of Taylor polynomials to the function :math:`\sin(x)`

CLAE
^^^^

Input the function,

.. code-block:: console

    sin(x)

Now we will graph the degree 10, 20, and 30 Taylor polynomials along with the graph. To create the degree 10 Taylor polynomial, select the function, then select ``Calculus > Taylor Series``, variable is *x*, point is ``pi``, and the order is 10.  The result is,

.. math::
    - x - \frac{\left(x - \pi\right)^{9}}{362880} + \frac{\left(x - \pi\right)^{7}}{5040} - \frac{\left(x - \pi\right)^{5}}{120} + \frac{\left(x - \pi\right)^{3}}{6} + \pi

Do the same with order 20 and 30, the results are,

.. math::
    - x + \frac{\left(x - \pi\right)^{19}}{121645100408832000} - \frac{\left(x - \pi\right)^{17}}{355687428096000} + \frac{\left(x - \pi\right)^{15}}{1307674368000} - \frac{\left(x - \pi\right)^{13}}{6227020800} + \frac{\left(x - \pi\right)^{11}}{39916800} - \frac{\left(x - \pi\right)^{9}}{362880} + \frac{\left(x - \pi\right)^{7}}{5040} - \frac{\left(x - \pi\right)^{5}}{120} + \frac{\left(x - \pi\right)^{3}}{6} + \pi

and

.. math::
    - x - \frac{\left(x - \pi\right)^{29}}{8841761993739701954543616000000} + \frac{\left(x - \pi\right)^{27}}{10888869450418352160768000000} - \frac{\left(x - \pi\right)^{25}}{15511210043330985984000000} + \frac{\left(x - \pi\right)^{23}}{25852016738884976640000} - \frac{\left(x - \pi\right)^{21}}{51090942171709440000} + \frac{\left(x - \pi\right)^{19}}{121645100408832000} - \frac{\left(x - \pi\right)^{17}}{355687428096000} + \frac{\left(x - \pi\right)^{15}}{1307674368000} - \frac{\left(x - \pi\right)^{13}}{6227020800} + \frac{\left(x - \pi\right)^{11}}{39916800} - \frac{\left(x - \pi\right)^{9}}{362880} + \frac{\left(x - \pi\right)^{7}}{5040} - \frac{\left(x - \pi\right)^{5}}{120} + \frac{\left(x - \pi\right)^{3}}{6} + \pi

Graph the three polynomials along with the function and you should have the following image.

.. figure:: Images/Series/series010.png
    :alt: Convergence of Taylor polynomials to the function sin(x).

    Convergence of Taylor polynomials to the function :math:`\sin(x)`

Maxima
^^^^^^

Input the function,

.. code-block:: console

    kill(all);
    f(x):=sin(x)

To create the Taylor polynomials we can use the ``taylor`` function,

.. code-block:: console

    t10:taylor(f(x),x,%pi,10);
    t20:taylor(f(x),x,%pi,20);
    t30:taylor(f(x),x,%pi,30);

Then we can plot these along with the function by,

.. code-block:: console

    wxplot2d([f(x), t10, t20, t30],[x,-10,20],[y,-10,10]);

The image should look something like the following,

.. figure:: Images/Series/series011.png
    :alt: Convergence of Taylor polynomials to the function sin(x).

    Convergence of Taylor polynomials to the function :math:`\sin(x)`
