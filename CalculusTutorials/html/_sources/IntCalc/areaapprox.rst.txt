:index:`Approximating Areas`
============================

Discussion & Definitions
------------------------

From our discussion of the area problem we know that our goal is to calculate the area under a general curve.  We also know how we will be attacking this problem., by approximating the area with a sum of rectangle areas and then taking the limit as we use more and more rectangles.  At this point we need to formalize these approximations, introduce some notation and terminology, and examine the relationships between different approximations.

Although we will discuss the terms and develop the formulas in general we will use the function :math:`f(x) = x^2` as our pictorial and numeric example.  In the image below we are approximating the area under the curve on the interval :math:`[0, 1]` using 5 rectangles.

.. figure:: Images/Int/ApproxArea001.png
    :alt: y = x^2 on [0, 1] using 5 Rectangles

    :math:`f(x) = x^2` on :math:`[0, 1]` using 5 Rectangles


Note that the rectangles all have the same width, :math:`\frac{1}{5}.`  We will follow this convention, although we do not need to, since it will simplify the calculations.  So in general, if we have a function :math:`f(x)` and we want to find the area under the curve and over the interval :math:`[a,b]` we will divide the interval up into equal length segments (which will be the bases for the rectangles).  This is called a **regular partition** of :math:`[a,b].`

.. figure:: Images/Int/ApproxArea002.png
    :alt: y = x^2 on [0, 1] using 5 Rectangles

    :math:`f(x) = x^2` on :math:`[0, 1]` using 5 Rectangles

In our example, we have introduced :math:`x_0, x_1, x_2, x_3, x_4, x_5` with :math:`a = 0 = x_0`, :math:`b = 1 = x_5`, and each of the subintervals :math:`[x_0, x_1], [x_1, x_2], [x_2, x_3], [x_3, x_4], [x_4, x_5]` all have the same length of :math:`\frac{1}{5}.`

Now let's generalize this, if we create a regular partition of the interval :math:`[a,b]` using :math:`n` divisions (so :math:`n` rectangles) we would have values,  :math:`x_0, x_1, x_2, x_3, x_4, \ldots, x_n` with :math:`a = x_0`, :math:`b = x_n`, and each of the subintervals :math:`[x_0, x_1], [x_1, x_2], [x_2, x_3], [x_3, x_4], \ldots, [x_{n-1}, x_n]` all have the same length.  The length of each subinterval is called :math:`\Delta x` and is calculated by,

.. math::
    |[x_{i-1}, x_i]| = \frac{b-a}{n} = \Delta x

This will be the length of the base of each of our rectangles.

The next question is, what about the height of each of the rectangles?  The tops of the rectangles must intersect the curve or either the rectangles will be too tall or too short.  This means that the height of the rectangles must be :math:`f(x_i^*)` where :math:`x_i^*` is somewhere in the :math:`i^{th}` interval :math:`[x_{i-1}, x_i]`.  There are three common positions for :math:`x_i^*`, the left endpoint, the right endpoint, and the center.

We will start with the left endpoint,

.. figure:: Images/Int/ApproxArea003.png
    :alt: Left Endpoint Approximation

    Left Endpoint Approximation

In this case :math:`x_i^* = x_{i-1}`, this is called the **left-endpoint approximation**, the area of the rectangles is denoted :math:`L_n` and is calculated as,

.. admonition:: Definition: Left-Endpoint Approximation

    .. math::
        A \approx L_n = f(x_0) \Delta x + f(x_1) \Delta x + f(x_2) \Delta x + \cdots + f(x_{n-1}) \Delta x = \sum_{i = 1}^n f(x_{i-1}) \Delta x

If we use the right endpoint,

.. figure:: Images/Int/ApproxArea004.png
    :alt: Right Endpoint Approximation

    Right Endpoint Approximation

In this case :math:`x_i^* = x_{i}`, this is called the **right-endpoint approximation**, the area of the rectangles is denoted :math:`R_n` and is calculated as,

.. admonition:: Definition: Right-Endpoint Approximation

    .. math::
        A \approx R_n = f(x_1) \Delta x + f(x_2) \Delta x + f(x_3) \Delta x + \cdots + f(x_{n}) \Delta x = \sum_{i = 1}^n f(x_{i}) \Delta x


The third common position is at the midpoint of each interval,

.. figure:: Images/Int/ApproxArea005.png
    :alt: Midpoint Approximation

    Midpoint Approximation

In this case :math:`x_i^* = \bar{x}_i = \frac{x_{i-1} + x_{i}}{2}`, this is called the **midpoint approximation**, the area of the rectangles is denoted :math:`M_n` and is calculated as,

.. admonition:: Definition: Midpoint Approximation

    .. math::
        A \approx M_n = f(\bar{x}_1) \Delta x + f(\bar{x}_2) \Delta x + f(\bar{x}_3) \Delta x + \cdots + f(\bar{x}_{n}) \Delta x = \sum_{i = 1}^n f(\bar{x}_{i}) \Delta x

    where :math:`\bar{x}_i = \frac{x_{i-1} + x_{i}}{2}`.

.. note::

    We could take the position of :math:`x_i^*` anywhere in the subinterval, the approximations will be different but when we take the limit as the number of rectangles increases to infinity the results will be the same.  In fact, we could take :math:`x_i^*` at random in the interval.

There are two other sums we are interested in but they are not as easy to calculate, and do not have a nice compact formula as the ones above.  Note in our example of :math:`f(x) = x^2` with the left endpoint approximation.  All of the rectangles are completely below the curve.  So the approximation we get here will be an under estimate.  Likewise with the right endpoint approximation all of the rectangles contain the curve so the approximation we get here will be an over estimate.  Now this happens in our example since :math:`f(x) = x^2` is an increasing function on :math:`[0, 1]`.  In general, the left and right approximations will not be under and over estimates.  For example, looking at :math:`x^3-3 x^2+x+6` on :math:`[-1, 3]` we see that the left and right approximations are not over and under estimates since some rectangles are above the curve and some are below the curve.

.. figure:: Images/Int/ApproxArea006.png
    :alt: Left Endpoint Approximation

    Left Endpoint Approximation

.. figure:: Images/Int/ApproxArea007.png
    :alt: Right Endpoint Approximation

    Right Endpoint Approximation

We can, however, define two more approximations, the upper sum and the lower sum.  The **upper sum** (:math:`US_n`) is the approximation that uses the maximum of the function in each subinterval for the height of the rectangle.

.. figure:: Images/Int/ApproxArea008.png
    :alt: Upper Sum Approximation

    Upper Sum Approximation

The **lower sum** (:math:`LS_n`) is the approximation that uses the minimum of the function in each subinterval for the height of the rectangle.

.. figure:: Images/Int/ApproxArea009.png
    :alt: Lower Sum Approximation

    Lower Sum Approximation

These are not as easy to calculate since for some subintervals you might use the left endpoint, some the right endpoint, and some might use a point somewhere in between.  Basically, you need to fine the absolute maximum and absolute minimum of the function in each subinterval, which can be a significant amount of work.

.. figure:: Images/Int/ApproxArea010.png
    :alt: Lower Sum Approximation

    Lower Sum Approximation

Nonetheless, if you can calculate the upper and lower sums you are guaranteed that, :math:`LS_n \leq A \leq US_n`.

These approximations are special cases of a more general concept of the Riemann sum.

.. admonition:: Definition: Riemann Sum

    Let :math:`f(x)` be defined on a closed interval :math:`[a, b]` and let :math:`P` be a regular partition of :math:`[a, b].` Let :math:`\Delta x` be the width of each subinterval :math:`[x_{i − 1}, x_i]` and for each :math:`i`, let :math:`x_i^*` be any point in :math:`[x_{i − 1}, x_i]`. A **Riemann sum** is defined for :math:`f(x)`  as

    .. math::
        \sum_{i = 1}^n f(x^*_{i}) \Delta x

As we know from our area problem discussion, to define the area we let the number of rectangles increase without bound.  Formally,

.. admonition:: Definition: Area Under a Curve

    Let :math:`f(x)` be a continuous, nonnegative function on an interval :math:`[a, b]`, and let :math:`\sum_{i = 1}^n f(x^*_{i}) \Delta x` be a Riemann sum for :math:`f(x).` Then, the area under the curve :math:`y = f(x)` on :math:`[a, b]` is given by

    .. math::
        A = \lim_{n \to \infty} \sum_{i = 1}^n f(x^*_{i}) \Delta x


Example: :math:`f(x) = x^2` on :math:`[0, 1]`
---------------------------------------------

In this example we will analyze the approximations for the example we used for a visualizations of the concepts above, :math:`f(x) = x^2` on :math:`[0, 1].`

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    x^2

We will calculate and get a visualization for the left approximation, input the command,

.. code-block:: console

    RectangleSum(f,0,1,10,0)

The RectangleSum command takes in 5 arguments, the first is the function, then the lower bound for the interval, then the upper bound for the interval, the number of rectangles to use, and finally the position in the interval for the *x* values.  Here we are using 0 which designates the left endpoint.  The right endpoint would use a 1 here and the midpoint would use a 0.5 here.  You could also use 0.25 to take the *x* values 1/4 of the way from the left to right endpoints if you wanted.  The image you will get is below and notice that the approximation to the area is 0.285.

.. figure:: Images/Int/ApproxArea011.png
    :alt: Rectangle Sum Approximation

    Rectangle Sum Approximation

Now increase the number of rectangles to 50, the approximation is now 0.3234 and the image is,

.. figure:: Images/Int/ApproxArea012.png
    :alt: Rectangle Sum Approximation

    Rectangle Sum Approximation

Now increase the number of rectangles to 500, the approximation is now 0.33233 and the image is,

.. figure:: Images/Int/ApproxArea013.png
    :alt: Rectangle Sum Approximation

    Rectangle Sum Approximation

From our discussion above we know that these are all upper sums.  Let's move over to the right endpoint. Change the number of rectangles back to 10 and change the last entry from 0 to 1.  The image should change to the one below and the approximation is 0.385.

.. figure:: Images/Int/ApproxArea014.png
    :alt: Rectangle Sum Approximation

    Rectangle Sum Approximation

Now increase the number of rectangles to 50, the approximation is now 0.3434 and the image is,

.. figure:: Images/Int/ApproxArea015.png
    :alt: Rectangle Sum Approximation

    Rectangle Sum Approximation

Now increase the number of rectangles to 500, the approximation is now 0.33433 and the image is,

.. figure:: Images/Int/ApproxArea016.png
    :alt: Rectangle Sum Approximation

    Rectangle Sum Approximation

It appears that the approximations are getting closer to 0.33333... We also know that :math:`0.33233 \leq A \leq 0.33433`.


CLAE
^^^^

CLAE does not have the nice rectangle visualization but it does have an option for calculating Riemann sums with a very large number of rectangles.

Input the function,

.. code-block:: console

    x^2

You can graph this if you would like but we will stick with the computations.  Select the function, then select ``Calculus > Integral Approximation Techniques > Riemann Sum``.  In the dialog box that appears put in 0 for the lower bound, 1 for the upper bound, change the test point position to 0 (for the left endpoint), and keep the number of rectangles at 10.  The result is, 0.285.  Now repeat this with 50 rectangles and keep the other settings as above, we get 0.3234. Now do 500 rectangles, for 0.3323339999999999.  Let's go a bit further, do the same approximations with 1000, 1,000,000, and 10,000,000 rectangles, we will get 0.33283350000000034, 0.3333328333334962, and 0.33333328333333545.

The test point position of 0 designates the left endpoint.  The right endpoint would use a 1 here and the midpoint would use a 0.5 here.  You could also use 0.25 to take the *x* values 1/4 of the way from the left to right endpoints if you wanted.

Do the above calculations with the right endpoint (test point position set to 1), the results are as follows.

.. math::

    \begin{array}{l|l}
    n & R_n  \\ \hline
    10 & 0.3850000000000001 \\
    50 & 0.34340000000000004 \\
    500 & 0.3343339999999999 \\
    1000 & 0.33383350000000034 \\
    1000000 & 0.3333338333334962 \\
    10000000 & 0.33333338333333545 \\
    \end{array}

It appears that the approximations are getting closer to 0.33333...

Do the above calculations with the midpoint (test point position set to 0.5), the results are as follows.

.. math::

    \begin{array}{l|l}
    n & M_n  \\ \hline
    10 & 0.3325 \\
    50 & 0.33330000000000004 \\
    500 & 0.3333330000000001 \\
    1000 & 0.3333332499999999 \\
    1000000 & 0.3333333333332426 \\
    10000000 & 0.3333333333333564 \\
    \end{array}

It appears that the approximations here are getting closer to 0.33333... as well.

Maxima
^^^^^^

Maxima does not have a built-in function for Riemann sums but it does have a sum command that we can use to get the job done.  We will start with the left endpoint using 10 rectangles.

Input the function,

.. code-block:: console

    f(x):=x^2

define :math:`\Delta x`,

.. code-block:: console

    dx:(1-0)/10

Now we can calculate the sum,

.. code-block:: console

    s:sum(f((i-1)*dx)*dx,i,1,10)

The result is :math:`\frac{57}{200}`, and finally we can get an approximation to the value with,

.. code-block:: console

    float(s), numer

with a result of 0.285.  Now we can change the number of rectangles by changing the value of *dx* and altering the sum command to match.  We could also change the interval in a similar manner.  This is doable but can be a little cumbersome.  While we do not want to digress into programming in Maxima we can create a Maxima function to simplify the process.  The following will define a left Riemann sum function. Copy and paste it into Maxima and hit Shift+Enter to load it into the workspace.

.. code-block:: maxima

    left_sum(RSfct,lb,ub,n):=block([dx,s,a],local(RSfct,lb,ub,n,dx,s,a),
    dx:(ub-lb)/n,
    s:sum(RSfct(lb+(i-1)*dx)*dx,i,1,n),
    a:float(s), numer,
    a)$

Now to take the left sum approximation with 10 rectangles we would run

.. code-block:: console

    left_sum(f,0,1,10)

The result will be 0.285.  Now change the 10 to 50 and rerun for 0.3234.  Then 500, 1000, and 1,000,000 for 0.332334, 0.3328335, 0.3333328333335. Note that we just use the function name and not ``f(x)``.  A right approximation function is very similar.  Copy the code below, paste into Maxima and hit Shift+Enter.

.. code-block:: maxima

    right_sum(RSfct,lb,ub,n):=block([dx,s,a],local(RSfct,lb,ub,n,dx,s,a),
    dx:(ub-lb)/n,
    s:sum(RSfct(lb+i*dx)*dx,i,1,n),
    a:float(s), numer,
    a)$

Now to take the right sum approximation with 10 rectangles we would run

.. code-block:: console

    right_sum(f,0,1,10)

The result will be 0.385.  Now change the 10 to 50 and rerun for 0.3434.  Then 500, 1000, and 1,000,000 for 0.334334, 0.3338335, 0.3333338333335.

It appears that the approximations are getting closer to 0.33333...

A midpoint sum is similar and given below.

.. code-block:: maxima

    mid_sum(RSfct,lb,ub,n):=block([dx,s,xp,a],local(RSfct,lb,ub,n,dx,s,xp,a),
    dx:(ub-lb)/n,
    xp:lb+i*dx - dx/2,
    s:sum(RSfct(xp)*dx,i,1,n),
    a:float(s), numer,
    a)$

It can be run with the same syntax,

.. code-block:: console

    right_sum(f,0,1,10)

The result will be 0.3325.  Now change the 10 to 50 and rerun for 0.3333.  Then 500, 1000, and 1,000,000 for 0.333333, 0.33333325, 0.33333333333325.  These too appear to be getting closer to 0.33333...

.. note::

    With the three functions we created ``left_sum``, ``right_sum``, and ``mid_sum`` we use ``RSfct`` as the input function.  With the way these functions are written and the way Maxima handles variables you do not want to define your function that you are taking the sums of to be named ``RSfct``, it is unlikely that you would but should be mentioned nonetheless.


Example: :math:`f(x) = e^{\sin(x)}` on :math:`[1, 3]`
-----------------------------------------------------

In this example we will analyze the approximations for :math:`f(x) = e^{\sin(x)}` on :math:`[1, 3].` A graph of the function and the area we are interested in is below.

.. figure:: Images/Int/ApproxArea017.png
    :alt: y = e^sin(x) on [1, 3]

    :math:`f(x) = e^{\sin(x)}` on :math:`[1, 3]`

GeoGebra
^^^^^^^^

Follow the rectangle sum procedure in the first example to approximate the area under the curve using the midpoint.  With 20 rectangles we get 4.4258.

.. figure:: Images/Int/ApproxArea018.png
    :alt: y = e^sin(x) on [1, 3] with 20 Rectangles

    :math:`f(x) = e^{\sin(x)}` on :math:`[1, 3]` with 20 Rectangles

If we increase this to 100 rectangles we get 4.42484. With 1000 rectangles we get 4.4248.

CLAE
^^^^

Follow the rectangle sum procedure in the first example to approximate the area under the curve using the midpoint.  You can input the function as either,

.. code-block:: console

    exp(sin(x))

or

.. code-block:: console

    E^sin(x)

With 20 rectangles we get 4.42579773949299. If we increase this to 100 rectangles we get 4.424839818343443. With 1000 rectangles we get 4.424800326038407 and with 1,000,000 rectangles we get 4.424799927135514.

Maxima
^^^^^^

Follow the rectangle sum procedure in the first example using our midpoint sum function to approximate the area under the curve using the midpoint.

Input the function,

.. code-block:: console

    f(x):=exp(sin(x))

then input the following to use 20 rectangles,

.. code-block:: console

    mid_sum(f, 1, 3, 20)

With 20 rectangles we get 4.42579773949299. If we increase this to 100 rectangles we get 4.424839818343443. With 1000 rectangles we get 4.424800326038407 and with 10,000 rectangles we get 4.424799931124128.

Example: Finding the exact value of the area.
---------------------------------------------

At the end of this section we defined the area under the curve as the limit of a Riemann sum.

**Definition:** Let :math:`f(x)` be a continuous, nonnegative function on an interval :math:`[a, b]`, and let :math:`\sum_{i = 1}^n f(x^*_{i}) \Delta x` be a Riemann sum for :math:`f(x).` Then, the area under the curve :math:`y = f(x)` on :math:`[a, b]` is given by

.. math::
    A = \lim_{n \to \infty} \sum_{i = 1}^n f(x^*_{i}) \Delta x

In subsequent sections we will see that there are alternative ways to make this calculation that are in general much easier.  Doing these calculations by hand is restricted to the simplest of functions, usually polynomials of degree 3 or less.  Even with the power of a computer algebra system this calculation is difficult.

CLAE: :math:`f(x) = x^2` on :math:`[0, 1]`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We will take the example we were using above and follow it through to an exact value, from our approximations we would assume the exact value is :math:`\frac{1}{3}`.  We will use the right endpoint formula for the Riemann sum, any can be used so we simply chose one.  Our function is :math:`f(x) = x^2`, the interval :math:`[a, b] = [0, 1]`, :math:`\Delta x = \frac{b-a}{n} = \frac{1}{n}`, and :math:`x_i = a + i \Delta x = \frac{i}{n}.`  So our area is

.. math::
    A = \lim_{n \to \infty} \sum_{i = 1}^n f(x^*_{i}) \Delta x = \lim_{n \to \infty} \sum_{i = 1}^n \left( \frac{i}{n} \right)^2  \frac{1}{n}

There are a number of ways we can do this in CLAE, here is one of them,

Input the function,

.. code-block:: console

    x^2

Now evaluate this at :math:`\frac{i}{n}` with ``Algebra > Evaluate``, variable is *x*, expression is ``i/n``.  The result will be

.. math::

    \frac{i^{2}}{n^{2}}

If we assume that this is in ``R2`` we can input ``R2*1/n`` into the CAS and get the expression for :math:`f(x^*_{i}) \Delta x`, which is

.. math::

    \frac{i^{2}}{n^{3}}

Now we take the sum, ``Calculus > Sum > Sum``, variable *i*, beginning index 1, ending index ``n``.  The result is,

.. math::
    \frac{\frac{n^{3}}{3} + \frac{n^{2}}{2} + \frac{n}{6}}{n^{3}}

which simplifies to

.. math::
    \frac{2 n^{2} + 3 n + 1}{6 n^{2}}

Now take the limit of this expression as :math:`n \to \infty` with ``Calculus > Limit``, variable *n*, limit point ``oo``, and the result is, as expected, :math:`\frac{1}{3}.`


CLAE: :math:`f(x) = e^{\sin(x)}` on :math:`[1, 3]`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We will follow the same procedure with :math:`f(x) = e^{\sin(x)}` on :math:`[1, 3].`

Again we will use the right endpoint formula for the Riemann sum.  Our function is :math:`f(x) = e^{\sin(x)}`, the interval :math:`[a, b] = [1, 3]`, :math:`\Delta x = \frac{b-a}{n} = \frac{2}{n}`, and :math:`x_i = a + i \Delta x = 1 + \frac{2i}{n}.`  So our area is

.. math::
    A = \lim_{n \to \infty} \sum_{i = 1}^n f(x^*_{i}) \Delta x = \lim_{n \to \infty} \sum_{i = 1}^n e^{\sin\left( 1+\frac{2i}{n} \right)} \frac{2}{n}

Input the function,

.. code-block:: console

    exp(sin(x))

Now evaluate this at :math:`1 + \frac{2i}{n}` with ``Algebra > Evaluate``, variable is *x*, expression is ``1 + 2*i/n``.  The result will be

.. math::
    e^{\sin{\left(\frac{2 i}{n} + 1 \right)}}

If we assume that this is in ``R2`` we can input ``R2*2/n`` into the CAS and get the expression for :math:`f(x^*_{i}) \Delta x`, which is

.. math::
    \frac{2 e^{\sin{\left(\frac{2 i}{n} + 1 \right)}}}{n}

Now we take the sum, ``Calculus > Sum > Sum``, variable *i*, beginning index 1, ending index ``n``.  The result is,

.. math::
    \sum_{i=1}^{n} \frac{2 e^{\sin{\left(\frac{2 i}{n} + 1 \right)}}}{n}

This is a bad sign that it cannot simplify the sum and usually means that going further will not result in anything of interest.  If we do push forward and take the limit of this expression as :math:`n \to \infty` with ``Calculus > Limit``, variable *n*, limit point ``oo``, and the result is an error message, which simply means that the CAS could not do the calculation.


