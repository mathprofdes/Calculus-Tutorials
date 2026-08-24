:index:`Extreme Values`
=======================

Discussion & Definitions
------------------------

Finding the largest and smallest values of a function is critical to solving optimization problems, such as, minimizing the materials in construction or maximizing profit.

We will start with absolute extremum.

.. admonition:: Definition: Absolute Extremes

    Let :math:`f` be a function defined over an interval :math:`I` and let :math:`c \in I`. We say :math:`f` has an **absolute maximum** on :math:`I` at :math:`c` if :math:`f(c) \geq f(x)` for all :math:`x \in I`. We say :math:`f` has an **absolute minimum** on :math:`I` at :math:`c` if :math:`f(c) \leq f(x)` for all :math:`x \in I`. If :math:`f` has an absolute maximum on :math:`I` at :math:`c` or an absolute minimum on :math:`I` at :math:`c`, we say :math:`f` has an **absolute extremum** on :math:`I` at :math:`c`.

A couple things to note before we proceed,

- A quick note about the language here.  If a function :math:`f` has an absolute extremum over an interval :math:`I` at :math:`c`, the absolute extremum is :math:`f(c)`. The real number :math:`c` is a point in the domain at which the absolute extremum occurs.
- Another thing to note is that an absolute extremum not only relies on the function but also the interval :math:`I`.  So a function could have an absolute extremum on one interval but not on another.
- There could be several places where the function attains an absolute maximum and/or its absolute minimum.

Let's look at a few examples to get a feel for the possibilities.

Take the function, :math:`f(x) = \frac{x}{x^{2} + 1}`, graph is below.

.. figure:: Images/Apps/ExtVal001.png
    :alt: y = x/(x^2+1)

    :math:`f(x) = \frac{x}{x^{2} + 1}`

- On the interval :math:`(-\infty, \infty)`, the function has an absolute maximum of :math:`1/2` at :math:`x = 1` and an absolute minimum of :math:`-1/2` at :math:`x = -1`.
- On the interval :math:`[-10, 10]`, the function has an absolute maximum of :math:`1/2` at :math:`x = 1` and an absolute minimum of :math:`-1/2` at :math:`x = -1`.
- On the interval :math:`[0, \infty)`, the function has an absolute maximum of :math:`1/2` at :math:`x = 1` and an absolute minimum of :math:`0` at :math:`x = 0`.
- On the interval :math:`(0, \infty)`, the function has an absolute maximum of :math:`1/2` at :math:`x = 1` and no absolute minimum.
- On the interval :math:`[1, 5]`, the function has an absolute maximum of :math:`1/2` at :math:`x = 1` and an absolute minimum of :math:`5/26` at :math:`x = 5`.
- On the interval :math:`(1, 5]`, the function has no absolute maximum and an absolute minimum of :math:`5/26` at :math:`x = 5`.
- On the interval :math:`(1, 5)`, the function has no absolute maximum and no absolute minimum.

Take the function, :math:`f(x) = x^3`, graph is below.

.. figure:: Images/Apps/ExtVal002.png
    :alt: y = x^3

    :math:`f(x) = x^3`

- On the interval :math:`(-\infty, \infty)`, the function has no absolute maximum and no absolute minimum.
- On the interval :math:`(0, \infty)`, the function has no absolute maximum and no absolute minimum.
- On the interval :math:`[0, \infty)`, the function has no absolute maximum and an absolute minimum of 0 at :math:`x = 0`.

Take the function, :math:`f(x) = \sin(x)`, graph is below.

.. figure:: Images/Apps/ExtVal003.png
    :alt: y = sin(x)

    :math:`f(x) = \sin(x)`

- On the interval :math:`(-\infty, \infty)`, the function has an absolute maximum of 1 at :math:`\frac{\pi}{2} + 2\pi k` and an absolute minimum of :math:`-1` at :math:`\frac{3\pi}{2} + 2\pi k`.  So there are an infinite number of places where the function attains its absolute maximum and its absolute minimum.
- On the interval :math:`[0, 4\pi]`, the function has an absolute maximum of 1 at :math:`\frac{\pi}{2}` and :math:`\frac{5\pi}{2}` and an absolute minimum of :math:`-1` at :math:`\frac{3\pi}{2}` and :math:`\frac{7\pi}{2}`.

With all of these possibilities it is nice to have some general results that guarantee the existence of an absolute maximum and minimum, the **Extreme Value Theorem** does just that.

.. admonition:: Theorem: Extreme Value Theorem

    If :math:`f` is a continuous function over the closed, bounded interval :math:`[a, b]`, then there is a point in :math:`[a, b]` at which :math:`f` has an absolute maximum over :math:`[a, b]` and there is a point in :math:`[a, b]` at which :math:`f` has an absolute minimum over :math:`[a, b]`.

For example, with :math:`f(x) = \frac{x}{x^{2} + 1}`,

- On the interval :math:`[-10, 10]`, the function has an absolute maximum of :math:`1/2` at :math:`x = 1` and an absolute minimum of :math:`-1/2` at :math:`x = -1`.
- On the interval :math:`[1, 5]`, the function has an absolute maximum of :math:`1/2` at :math:`x = 1` and an absolute minimum of :math:`5/26` at :math:`x = 5`.

.. admonition:: Definition: Local Extremes

    A function :math:`f` has a **local maximum** at :math:`c` if there exists an open interval :math:`I` containing :math:`c` such that :math:`I` is contained in the domain of :math:`f` and :math:`f(c) \geq f(x)` for all :math:`x \in I`. A function :math:`f` has a **local minimum** at :math:`c` if there exists an open interval :math:`I` containing :math:`c` such that :math:`I` is contained in the domain of :math:`f` and :math:`f(c) \leq f(x)` for all :math:`x \in I`. A function :math:`f` has a **local extremum** at :math:`c` if :math:`f` has a local maximum at :math:`c` or :math:`f` has a local minimum at :math:`c`.

For example, take :math:`f(x) = x^3-x`, graph below,

.. figure:: Images/Apps/ExtVal004.png
    :alt: y = x^3 - x

    :math:`f(x) = x^3 - x`

On :math:`(-\infty, \infty)` the function has no absolute maximum and no absolute minimum.  But it does have a local maximum of :math:`\frac{2 \sqrt{3}}{9}` at :math:`x = - \frac{\sqrt{3}}{3}` and a local minimum of :math:`-\frac{2 \sqrt{3}}{9}` at :math:`x = \frac{\sqrt{3}}{3}`.  Although we can simply see this, if we follow the definition to the letter we need to come up with a couple intervals.  For the local maximum we can use :math:`(-1, 0)` (or :math:`(-0.75, -0.25)` or :math:`(-0.6, -0.5)`).  For the local minimum we can use :math:`(0, 1)`, amongst others.


As another example, :math:`f(x) = x^{5} - 3 x^{3} + x`, graph below,

.. figure:: Images/Apps/ExtVal005.png
    :alt: y = x^5 - x^3 + x

    :math:`f(x) = x^{5} - 3 x^{3} + x`

This function has two local maximums and two local minimums.  The local maximums are

.. math::
    \frac{\left(7 \sqrt{10} + 3 \sqrt{610}\right) \sqrt{\sqrt{61} + 9}}{250} \approx 1.57819155662093 \quad {\rm at} \quad x = - \sqrt{\frac{\sqrt{61}}{10} + \frac{9}{10}} \approx -1.29654346922526

and

.. math::
    \frac{\sqrt{9 - \sqrt{61}} \left(- 7 \sqrt{10} + 3 \sqrt{610}\right)}{250} \approx 0.226696737096979 \quad {\rm at} \quad x = \sqrt{\frac{9}{10} - \frac{\sqrt{61}}{10}} \approx 0.344927575600059

The local minimums are

.. math::
    \frac{\sqrt{9 - \sqrt{61}} \left(- 3 \sqrt{610} + 7 \sqrt{10}\right)}{250} \approx -0.226696737096979 \quad {\rm at} \quad x = - \sqrt{\frac{9}{10} - \frac{\sqrt{61}}{10}} \approx -0.344927575600059

and

.. math::
    \frac{\sqrt{\sqrt{61} + 9} \left(- 3 \sqrt{610} - 7 \sqrt{10}\right)}{250} \approx -1.57819155662093  \quad {\rm at} \quad x = \sqrt{\frac{\sqrt{61}}{10} + \frac{9}{10}} \approx 1.29654346922526

One more example, consider the following function,

.. figure:: Images/Apps/ExtVal006.png
    :alt: Critical Point Example

    Critical Point Example

It has a local maximum of about 1.4 around :math:`x = -0.6`, a local minimum of about 0.6 around  :math:`x = 0.6`, and another local maximum of 3 at :math:`x = 2`.

It should be fairly clear that we are gearing up to find these local maximums and local minimums and of course it will relate to the derivative of the function.  Take the above example, informally speaking, the local maximums and minimums occur at spots where the function "turns around".  There are essentially two ways that a continuous function can turn around, either smoothly were the derivative will exist or at a sharp corner where the derivative will not exist. If the derivative exists at the turnaround point the transition is smooth and if we think about tangent lines to the curve at that point the slope must be 0.  Hence the derivative is 0.  This observation gives us the following definition of a **critical point** or **critical number** as well as Fermat's Theorem.

.. admonition:: Definition: Critical Point

    Let :math:`c` be an interior point in the domain of :math:`f`. We say that :math:`c` is a **critical point** or **critical number** of :math:`f` if :math:`f'(c) = 0` or :math:`f'(c)` is undefined.

.. admonition:: Theorem: Fermat's Theorem

    If :math:`f` has a local extremum at :math:`c` and :math:`f` is differentiable at :math:`c`, then :math:`f'(c) = 0`.

As we have seen before with theorems, we need to be a little careful about how we read them.  This is saying that if we have a local extreme then it must be at a critical number.  It does not say that we must have an extreme at every critical number.  Two very quick examples to illustrate this, first :math:`f(x) = x^3`, there is a critical value at :math:`x = 0`, since :math:`f'(x) = 3x^2`, and hence :math:`f'(0) = 0`, but there is no local maximum or minimum at :math:`x = 0`.

.. figure:: Images/Apps/ExtVal007.png
    :alt: y = x^3

    :math:`f(x) = x^3`

Another example is  :math:`f(x) = \sqrt[3]{x}`, there is a critical value at :math:`x = 0`, since :math:`f'(x)` does not exist there. :math:`f'(x) = \frac{1}{3 x^{\frac{2}{3}}}` and hence :math:`f'(0)` is undefined, but there is no local maximum or minimum at :math:`x = 0`.

.. figure:: Images/Apps/ExtVal008.png
    :alt: y = x^(1/3)

    :math:`f(x) = \sqrt[3]{x}`

Putting all of this together we have the following theorem about absolute extrema.

.. admonition:: Theorem: Location of Absolute Extrema

    Let :math:`f` be a continuous function over a closed, bounded interval :math:`I`. The absolute maximum of :math:`f` over :math:`I` and the absolute minimum of :math:`f` over :math:`I` must occur at endpoints of :math:`I` or at critical points of :math:`f` in :math:`I`.

This theorem can be rewritten into an algorithm for finding absolute extrema.

.. admonition:: Problem Solving: Locating Absolute Extrema over a Closed Interval

    Consider a continuous function :math:`f` defined over the closed interval :math:`[a, b]`.

    #. Evaluate :math:`f` at the endpoints :math:`x = a` and :math:`x = b`.
    #. Find all critical points of :math:`f` that are in the interval :math:`(a, b)` and evaluate :math:`f` at those critical points.
    #. Compare all the functional values found in the previous steps, the largest is the absolute maximum of :math:`f` and the smallest is the absolute minimum of :math:`f`.


Example: :math:`f(x) = x^3-x`
-----------------------------

In this example we are going to find all the local maximums and minimums of the function :math:`f(x) = x^3-x`.

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    x^3-x

The quick way to get approximations to the local maximums and minimums, as well as roots and the y intercept, is to select Special Points from the objects menu.

.. figure:: Images/Apps/ExtVal009.png
    :alt: GeoGebra Special Points

    GeoGebra Special Points

You will note that the option ran three functions, Root, Extremum, and Intersect.  You could have run these separately as well.  One downside to this is that the displayed values are approximations.  If you want exact values you can find the roots of the derivative, that is, solve :math:`f'(x) = 0`.  To do so, in a new cell type in ``Solve``, select ``Solve``, the solve function asks for an equation you can input just ``f'`` or ``f'(x)`` or ``f'(x) = 0``.  The output will be the exact answers, if they can be calculated.  You may also have noted that there is a Solutions function.  This is the same as the Solve command but returns approximate values.  Also, from the solve command the resulting cell has a button that will toggle between exact and approximate mode.  This also shows you that the ``NSolve`` command could have been used in place of ``Solve`` which would start in approximate mode and toggle to exact mode.

Another note here is that the Solve command will return the solutions but will not graph them.  The solutions are in list form, lets say they are ``l1``.  In a new cell input ``l1`` and it will approximate the solutions as well as graph these as vertical lines.  If you had use the Solutions command instead of the Solve command you would not need to do the approximation step.

.. figure:: Images/Apps/ExtVal010.png
    :alt: GeoGebra using Solve

    GeoGebra using Solve

One advantage ot using Solutions in stead of Solve is that you can find the corresponding y-values from the list result of Solutions but not from the list solutions from Solve.  Had you used Solutions and say the list name was ``l2`` then the y-values could be calculated using ``f(l2)``.

CLAE
^^^^

Input and graph the function,

.. code-block:: console

    x^3-x

.. figure:: Images/Apps/ExtVal011.png
    :alt: y = x^3-x

    :math:`f(x) = x^3-x`

To find the critical numbers first find the derivative, select the expression, select ``Calculus > Derivative``, variable *x*, order 1.  The result is :math:`3 x^{2} - 1`.  Then solve the equation :math:`f'(x) = 3 x^{2} - 1 = 0` by selecting ``Algebra > Solve``, variable *x* and the result will be,

.. math::
    \left[ - \frac{\sqrt{3}}{3}, \  \frac{\sqrt{3}}{3}\right]

Click and drag these over to the graph and change the type to vertical lines.

.. figure:: Images/Apps/ExtVal012.png
    :alt: y = x^3-x with Critical Values

    :math:`f(x) = x^3-x` with Critical Values

To get the corresponding y-values there are two options,

**Option 1:** Select the original function, select ``Algebra > Evaluate``, the variable is *x*, for the expression input ``R3[0]``.  This assumes that the solutions to the derivative equaling 0 are in the ``R3`` result.  What ``R3[0]`` will do is extract the first entry of the list stored in R3.  Hence it will evaluate the function at the first solution.  Then do the same thing again but this time use ``R3[1]`` to evaluate the second solution.  Your results will be :math:`\frac{2 \sqrt{3}}{9}` and :math:`-\frac{2 \sqrt{3}}{9}` respectively.

**Option 2:** First extract all the solutions to their own output cells by selecting the solution list output, then select ``Edit > Extract from List > Extract All List Entries``.  Now evaluate each one by selecting the original function, then select ``Algebra > Evaluate``, the variable is *x*, for the expression input ``R4`` (assuming that the first entry went into R4).  Then do the same but use ``R5`` instead of ``R4``.  Your results will be :math:`\frac{2 \sqrt{3}}{9}` and :math:`-\frac{2 \sqrt{3}}{9}` respectively.

CLAE does have a feature to find both absolute and local maximums and minimums on finite intervals.  Although this is quicker to a solution, the above methods help you understand the process a bit better.  Nonetheless, once you understand the process and can do these calculations by hand, the machine can help you out with more difficult situations.

Select the function, then select ``Calculus > Maximums and Minimums``, a dialog box will appear with numerous options.  From the graph it looks like all of our local extrema are between :math:`-1` and 1.  So input :math:`-1` and 1 for the lower and upper bounds.  For this exercise we want local extrema so select Local.  We also want both the maximums and minimums, so select Both.  For the next option we could have the program just output the y-values of the extremes or the points, we will want the points here so select Point.  The options below this are to choose between exact numeric output or approximations.  We will leave it as exact but if the program cannot produce exact solutions we will redo it with approximations.  Click OK and we get,

.. math::
    \left[ \left[ - \frac{\sqrt{3}}{3}, \  \frac{2 \sqrt{3}}{9}\right], \  \left[ \frac{\sqrt{3}}{3}, \  - \frac{2 \sqrt{3}}{9}\right]\right]

If we click and drag this over to the graph it will come in as a point set and along with the curve we see,

.. figure:: Images/Apps/ExtVal024.png
    :alt: y = x^3-x with Extreme Points

    :math:`f(x) = x^3-x` with Extreme Points


Maxima
^^^^^^

Input and graph the function,

.. code-block:: console

    kill(all);
    f(x):=x^3-x

.. code-block:: console

    wxplot2d(f(x),[x,-1.5,1.5])

.. figure:: Images/Apps/ExtVal013.png
    :alt: y = x^3-x

    :math:`f(x) = x^3-x`

Take the derivative,

.. code-block:: console

    df:diff(f(x),x)

Solve :math:`f'(x) = 0`,

.. code-block:: console

    sl:solve(df=0,x)

The result will be,

.. math::
    \left[ x=-\frac{1}{\sqrt{3}}\operatorname{,}x=\frac{1}{\sqrt{3}}\right] \mbox{}

To get the corresponding y-values we can evaluate each of the two solutions by extracting the values from the list of solutions.  To evaluate the function at the first solution can be done with,

.. code-block:: console

    f(rhs(sl[1]))

and the second can be done with,

.. code-block:: console

    f(rhs(sl[2]))

What is happening here is that the solution list was stored in ``sl`` from our solve command.  Then ``sl[1]`` is the first entry, ``sl[2]`` is the second entry, and so on if the list was longer.  Each entry is an equation and we want the right hand side of the equation, which is what the ``rhs`` function extracts.  Once extracted we simple evaluate the function at that number. Your results should be the following, respectively.

.. math::
    \frac{2}{{{3}^{\frac{3}{2}}}}\mbox{}  \quad {\rm and } \quad -\frac{2}{{{3}^{\frac{3}{2}}}}\mbox{}


Example: :math:`f(x) = x^3-x` on :math:`[-1, 2]`
------------------------------------------------

In this example we are going to find the absolute maximums and minimums of the function :math:`f(x) = x^3-x` on the interval :math:`[-1, 2]`.

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    x^3-x

The quick way to get approximations to the local maximums and minimums, as well as roots and the y intercept, is to select Special Points from the objects menu.

.. figure:: Images/Apps/ExtVal009.png
    :alt: y = x^3-x with Special Points

    :math:`f(x) = x^3-x` with Special Points

You will note that the option ran three functions, Root, Extremum, and Intersect.  You could have run these separately as well.  One downside to this is that the displayed values are approximations.  If you want exact values you can find the roots of the derivative, that is, solve :math:`f'(x) = 0`.  To do so, in a new cell type in ``Solve``, select ``Solve``, the solve function asks for an equation you can input just ``f'`` or ``f'(x)`` or ``f'(x) = 0``.  The output will be the exact answers, if they can be calculated.  You may also have noted that there is a Solutions function.  This is the same as the Solve command but returns approximate values.  Also, from the solve command the resulting cell has a button that will toggle between exact and approximate mode.  This also shows you that the ``NSolve`` command could have been used in place of ``Solve`` which would start in approximate mode and toggle to exact mode.

Another note here is that the Solve command will return the solutions but will not graph them.  The solutions are in list form, lets say they are ``l1``.  In a new cell input ``l1`` and it will approximate the solutions as well as graph these as vertical lines.  If you had use the Solutions command instead of the Solve command you would not need to do the approximation step.

.. figure:: Images/Apps/ExtVal010.png
    :alt: y = x^3-x using Solve

    :math:`f(x) = x^3-x` using Solve

One advantage ot using Solutions in stead of Solve is that you can find the corresponding y-values from the list result of Solutions but not from the list solutions from Solve.  Had you used Solutions and say the list name was ``l2`` then the y-values could be calculated using ``f(l2)``.

Continuing with the determination of the absolute maximums and minimums we first take all the critical numbers in our interval of interest, :math:`[-1, 2]`.  The approximate critical numbers are :math:`\{-0.57735, 0.57735\}` both are in the interval and have functional values :math:`\{0.3849, -0.3849\}` respectively.  Also, check the endpoints by evaluating the function at :math:`-1` and 2, which are 0 and 6 respectively.

So the function has an absolute minimum of :math:`-0.3849` at :math:`x = \frac{\sqrt{3}}{3} \approx 0.57735` and an absolute maximum of 6 at :math:`x = 2`.

.. figure:: Images/Apps/ExtVal016.png
    :alt: y = x^3-x Restricted to [-1, 2]

    :math:`f(x) = x^3-x` Restricted to :math:`[-1, 2]`

If you want to restrict the domain of the function to :math:`[-1, 2]` for a better visualization (as above) you can do it by first inputting the region and then attaching the region to the function.  In a new cell, input

.. code-block:: console

    -1 <= x <= 2

This will graph the region and assign it to a variable, we will assume that the variable is ``a``.  Then you can attach it to the function with ``f,a``.  This will make an automatic if statement.  Deselect the original function and the graph of the domain and you will get an image like the one above.


CLAE
^^^^

Input and graph the function,

.. code-block:: console

    x^3-x

.. figure:: Images/Apps/ExtVal011.png
    :alt: y = x^3-x

    :math:`f(x) = x^3-x`

To find the critical numbers first find the derivative, select the expression, select ``Calculus > Derivative``, variable *x*, order 1.  The result is :math:`3 x^{2} - 1`.  Then solve the equation :math:`f'(x) = 3 x^{2} - 1 = 0` by selecting ``Algebra > Solve``, variable *x* and the result will be,

.. math::
    \left[ - \frac{\sqrt{3}}{3}, \  \frac{\sqrt{3}}{3}\right]

Click and drag these over to the graph and change the type to vertical lines.

.. figure:: Images/Apps/ExtVal012.png
    :alt: y = x^3-x with Critical Numbers

    :math:`f(x) = x^3-x` with Critical Numbers

To get the corresponding y-values there are two options,

**Option 1:** Select the original function, select ``Algebra > Evaluate``, the variable is *x*, for the expression input ``R3[0]``.  This assumes that the solutions to the derivative equaling 0 are in the ``R3`` result.  What ``R3[0]`` will do is extract the first entry of the list stored in R3.  Hence it will evaluate the function at the first solution.  Then do the same thing again but this time use ``R3[1]`` to evaluate the second solution.  Your results will be :math:`\frac{2 \sqrt{3}}{9} \approx 0.384900179459751` and :math:`-\frac{2 \sqrt{3}}{9} \approx -0.384900179459751` respectively.

**Option 2:** First extract all the solutions to their own output cells by selecting the solution list output, then select ``Edit > Extract from List > Extract All List Entries``.  Now evaluate each one by selecting the original function, then select ``Algebra > Evaluate``, the variable is *x*, for the expression input ``R4`` (assuming that the first entry went into R4).  Then do the same but use ``R5`` instead of ``R4``.  Your results will be :math:`\frac{2 \sqrt{3}}{9} \approx 0.384900179459751` and :math:`-\frac{2 \sqrt{3}}{9} \approx -0.384900179459751` respectively.

Now evaluate the expression at the endpoints by select the original function, then select ``Algebra > Evaluate``, the variable is *x*, and :math:`-1` for the expression, then do the same with 2.  The results should be 0 and 6 respectively.

So the function has an absolute minimum of :math:`-\frac{2 \sqrt{3}}{9} \approx -0.384900179459751` at :math:`x = \frac{\sqrt{3}}{3} \approx 0.577350269189626` and an absolute maximum of 6 at :math:`x = 2`.

.. figure:: Images/Apps/ExtVal015.png
    :alt: y = x^3-x Restricted to [-1, 2]

    :math:`f(x) = x^3-x` Restricted to :math:`[-1, 2]`

If you want to restrict the domain to :math:`[-1, 2]` for better visualization you can do it with a piecewise defined function.  If we assume that the original function is in the R1 result then all you need to do is select ``Edit > Input Piecewise Defined Function`` or the corresponding toolbar button. Change the expressions to 1, in the expression cell input ``R1`` and in the domain cell input ``(x >= -1) & (x <= 2)``.  Select OK and the restricted domain function will be loaded into the CAS,

.. math::
    \begin{cases} x^{3} - x & \text{for}\: x \geq -1 \wedge x \leq 2 \\\text{NaN} & \text{for}\: x > 2 \vee x < -1 \end{cases}

Click and drag this over to the graph and deselect the original expression.

Again, we could use the maximum and minimum finder in CLAE to do this.  Select the function, then select ``Calculus >> Maximums and Minimums``, the bounds are :math:`-1` and 2, we want Absolute, Both, Point, and Exact.  Click OK and we get,

.. math::
    \left[ \left[ 2, \  6\right], \  \left[ \frac{\sqrt{3}}{3}, \  - \frac{2 \sqrt{3}}{9}\right]\right]

Plotting these and the original function gives us the image,

.. figure:: Images/Apps/ExtVal025.png
    :alt: y = x^3-x with Maximum and Minimum

    :math:`f(x) = x^3-x` with Maximum and Minimum

Maxima
^^^^^^

Input and graph the function,

.. code-block:: console

    kill(all);
    f(x):=x^3-x

.. code-block:: console

    wxplot2d(f(x),[x,-1,2])

.. figure:: Images/Apps/ExtVal017.png
    :alt: y = x^3-x

    :math:`f(x) = x^3-x`

Take the derivative,

.. code-block:: console

    df:diff(f(x),x)

Solve :math:`f'(x) = 0`,

.. code-block:: console

    sl:solve(df=0,x)

The result will be,

.. math::
    \left[ x=-\frac{1}{\sqrt{3}}\operatorname{,}x=\frac{1}{\sqrt{3}}\right] \mbox{}

To get the corresponding y-values we can evaluate each of the two solutions by extracting the values from the list of solutions.  To evaluate the function at the first solution can be done with,

.. code-block:: console

    f(rhs(sl[1]))

and the second can be done with,

.. code-block:: console

    f(rhs(sl[2]))

What is happening here is that the solution list was stored in ``sl`` from our solve command.  Then ``sl[1]`` is the first entry, ``sl[2]`` is the second entry, and so on if the list was longer.  Each entry is an equation and we want the right hand side of the equation, which is what the ``rhs`` function extracts.  Once extracted we simple evaluate the function at that number. Your results should be the following, respectively.

.. math::
    \frac{2}{{{3}^{\frac{3}{2}}}}\mbox{}  \quad {\rm and } \quad -\frac{2}{{{3}^{\frac{3}{2}}}}\mbox{}

To finish this up we evaluate the function at the endpoints,

.. code-block:: console

    f(-1);
    f(2)

getting 0 and 6 respectively.  So the function has an absolute minimum of :math:`-\frac{2 \sqrt{3}}{9} \approx -0.384900179459751` at :math:`x = \frac{\sqrt{3}}{3} \approx 0.577350269189626` and an absolute maximum of 6 at :math:`x = 2`.



Example: :math:`f(x) = x^5-3 x^3+x`
-----------------------------------

In this example we are going to find all the local maximums and minimums of the function :math:`f(x) = x^5-3x^3+x`.

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    x^5 - 3 x^3 + x

Use the methods from the first example to find the local maximums and minimums.

.. figure:: Images/Apps/ExtVal018.png
    :alt: y = x^5 - 3 x^3 + x

    :math:`f(x) = x^5-3 x^3+x`


CLAE
^^^^

Input and graph the function,

.. code-block:: console

    x^5 - 3*x^3 + x

.. figure:: Images/Apps/ExtVal019.png
    :alt: y = x^5 - 3 x^3 + x

    :math:`f(x) = x^5-3 x^3+x`

Follow the procedures in the first example to find the local maximums and minimums, the critical numbers are,

.. math::
    \left[ - \sqrt{\frac{9}{10} - \frac{\sqrt{61}}{10}}, \  \sqrt{\frac{9}{10} - \frac{\sqrt{61}}{10}}, \  - \sqrt{\frac{\sqrt{61}}{10} + \frac{9}{10}}, \  \sqrt{\frac{\sqrt{61}}{10} + \frac{9}{10}}\right]

Evaluating the function at each of these we see that this function has two local maximums and two local minimums.  The local maximums are

.. math::
    \frac{\left(7 \sqrt{10} + 3 \sqrt{610}\right) \sqrt{\sqrt{61} + 9}}{250} \approx 1.57819155662093 \quad {\rm at} \quad x = - \sqrt{\frac{\sqrt{61}}{10} + \frac{9}{10}} \approx -1.29654346922526

and

.. math::
    \frac{\sqrt{9 - \sqrt{61}} \left(- 7 \sqrt{10} + 3 \sqrt{610}\right)}{250} \approx 0.226696737096979 \quad {\rm at} \quad x = \sqrt{\frac{9}{10} - \frac{\sqrt{61}}{10}} \approx 0.344927575600059

The local minimums are

.. math::
    \frac{\sqrt{9 - \sqrt{61}} \left(- 3 \sqrt{610} + 7 \sqrt{10}\right)}{250} \approx -0.226696737096979 \quad {\rm at} \quad x = - \sqrt{\frac{9}{10} - \frac{\sqrt{61}}{10}} \approx -0.344927575600059

and

.. math::
    \frac{\sqrt{\sqrt{61} + 9} \left(- 3 \sqrt{610} - 7 \sqrt{10}\right)}{250} \approx -1.57819155662093  \quad {\rm at} \quad x = \sqrt{\frac{\sqrt{61}}{10} + \frac{9}{10}} \approx 1.29654346922526

Using CLAEs maximum and minimum finder, select the function, then select ``Calculus > Maximums and Minimums``, Local, Both, Point, Exact, will return,

.. math::
    \left[ \left[ - \sqrt{\frac{\sqrt{61}}{10} + \frac{9}{10}}, \  - \left(\frac{\sqrt{61}}{10} + \frac{9}{10}\right)^{\frac{5}{2}} - \sqrt{\frac{\sqrt{61}}{10} + \frac{9}{10}} + 3 \left(\frac{\sqrt{61}}{10} + \frac{9}{10}\right)^{\frac{3}{2}}\right], \  \left[ - \sqrt{\frac{9}{10} - \frac{\sqrt{61}}{10}}, \  - \sqrt{\frac{9}{10} - \frac{\sqrt{61}}{10}} - \left(\frac{9}{10} - \frac{\sqrt{61}}{10}\right)^{\frac{5}{2}} + 3 \left(\frac{9}{10} - \frac{\sqrt{61}}{10}\right)^{\frac{3}{2}}\right], \  \left[ \sqrt{\frac{9}{10} - \frac{\sqrt{61}}{10}}, \  - 3 \left(\frac{9}{10} - \frac{\sqrt{61}}{10}\right)^{\frac{3}{2}} + \left(\frac{9}{10} - \frac{\sqrt{61}}{10}\right)^{\frac{5}{2}} + \sqrt{\frac{9}{10} - \frac{\sqrt{61}}{10}}\right], \  \left[ \sqrt{\frac{\sqrt{61}}{10} + \frac{9}{10}}, \  - 3 \left(\frac{\sqrt{61}}{10} + \frac{9}{10}\right)^{\frac{3}{2}} + \sqrt{\frac{\sqrt{61}}{10} + \frac{9}{10}} + \left(\frac{\sqrt{61}}{10} + \frac{9}{10}\right)^{\frac{5}{2}}\right]\right]

which simplifies to

.. math::
    \left[ \left[ - \frac{\sqrt{10 \sqrt{61} + 90}}{10}, \  \frac{\left(7 \sqrt{10} + 3 \sqrt{610}\right) \sqrt{\sqrt{61} + 9}}{250}\right], \  \left[ - \frac{\sqrt{90 - 10 \sqrt{61}}}{10}, \  \frac{\sqrt{9 - \sqrt{61}} \left(- 3 \sqrt{610} + 7 \sqrt{10}\right)}{250}\right], \  \left[ \frac{\sqrt{90 - 10 \sqrt{61}}}{10}, \  \frac{\sqrt{9 - \sqrt{61}} \left(- 7 \sqrt{10} + 3 \sqrt{610}\right)}{250}\right], \  \left[ \frac{\sqrt{10 \sqrt{61} + 90}}{10}, \  \frac{\sqrt{\sqrt{61} + 9} \left(- 3 \sqrt{610} - 7 \sqrt{10}\right)}{250}\right]\right]

and approximates to

.. math::
    \left[ \left[ -1.29654346922526, \  1.57819155662093\right], \  \left[ -0.344927575600059, \  -0.226696737096979\right], \  \left[ 0.344927575600059, \  0.226696737096979\right], \  \left[ 1.29654346922526, \  -1.57819155662093\right]\right]

Plotting gives us,

.. figure:: Images/Apps/ExtVal026.png
    :alt: y = x^5 - 3 x^3 + x with Extreme Points

    :math:`f(x) = x^5-3 x^3+x` with Extreme Points

Maxima
^^^^^^

Input and graph the function,

.. code-block:: console

    kill(all);
    f(x):=x^5-3*x^3+x

.. code-block:: console

    wxplot2d(f(x),[x,-2,2])

.. figure:: Images/Apps/ExtVal020.png
    :alt: y = x^5 - 3 x^3 + x

    :math:`f(x) = x^5-3 x^3+x`

Take the derivative,

.. code-block:: console

    df:diff(f(x),x)

Solve :math:`f'(x) = 0`,

.. code-block:: console

    sl:solve(df=0,x)

The result will be,

.. math::
    \left[ x=-\frac{\sqrt{\sqrt{61}+9}}{\sqrt{10}}\operatorname{,}x=\frac{\sqrt{\sqrt{61}+9}}{\sqrt{10}}\operatorname{,}x=-\frac{\sqrt{9-\sqrt{61}}}{\sqrt{10}}\operatorname{,}x=\frac{\sqrt{9-\sqrt{61}}}{\sqrt{10}}\right] \mbox{}

approximately

.. math::
    \operatorname{[}x=-1.296543469225257\operatorname{,}x=1.296543469225257\operatorname{,}x=-0.3449275756000593\operatorname{,}x=0.3449275756000593\operatorname{]}\mbox{}

Evaluating the original function at these points gives, respectively,

.. math::
    -\frac{{{\left( \sqrt{61}+9\right) }^{\frac{5}{2}}}}{{{10}^{\frac{5}{2}}}}+\frac{3 {{\left( \sqrt{61}+9\right) }^{\frac{3}{2}}}}{{{10}^{\frac{3}{2}}}}-\frac{\sqrt{\sqrt{61}+9}}{\sqrt{10}}\mbox{} \approx 1.578191556620925

.. math::
    \frac{{{\left( \sqrt{61}+9\right) }^{\frac{5}{2}}}}{{{10}^{\frac{5}{2}}}}-\frac{3 {{\left( \sqrt{61}+9\right) }^{\frac{3}{2}}}}{{{10}^{\frac{3}{2}}}}+\frac{\sqrt{\sqrt{61}+9}}{\sqrt{10}}\mbox{} \approx -1.578191556620925

.. math::
    -\frac{{{\left( 9-\sqrt{61}\right) }^{\frac{5}{2}}}}{{{10}^{\frac{5}{2}}}}+\frac{3 {{\left( 9-\sqrt{61}\right) }^{\frac{3}{2}}}}{{{10}^{\frac{3}{2}}}}-\frac{\sqrt{9-\sqrt{61}}}{\sqrt{10}}\mbox{} \approx -0.2266967370969792

.. math::
    \frac{{{\left( 9-\sqrt{61}\right) }^{\frac{5}{2}}}}{{{10}^{\frac{5}{2}}}}-\frac{3 {{\left( 9-\sqrt{61}\right) }^{\frac{3}{2}}}}{{{10}^{\frac{3}{2}}}}+\frac{\sqrt{9-\sqrt{61}}}{\sqrt{10}}\mbox{} \approx 0.2266967370969792


Example: :math:`f(x) = \frac{x^{3} - 3 x^{2} + x - 1}{x^{2} - 4}`
-----------------------------------------------------------------

For this example we will just find the critical numbers to :math:`f(x) = \frac{x^{3} - 3 x^{2} + x - 1}{x^{2} - 4}`.

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    (x^3 - 3 x^2 + x - 1)/(x^2 - 4)

.. figure:: Images/Apps/ExtVal021.png
    :alt: y = (x^3-3x^2+x-1)/(x^2-4)

    :math:`f(x) = \frac{x^{3} - 3 x^{2} + x - 1}{x^{2} - 4}`

Following the procedures from the first example, solving :math:`f'(x) = 0`, the Solve command reverts to approximation mode giving :math:`x = -4.3761` and :math:`x = 0.16791`.  In the previous examples we never needed to worry about the critical numbers from the derivative not existing.  Since the derivative is,

.. math::
    \frac{x^{4} - 13 x^{2} + 26 x - 4}{x^{4} - 8 x^{2} + 16}

there is the possibility of division by 0.  To extract the denominator go to a new cell, type in and select ``Denominator``, then type in ``f'``.  It will extract, :math:`x^{4} - 8 x^{2} + 16`.  Now use the Solve command and the results are :math:`-2` and 2.  These are where the derivative does not exist but we would not consider then critical numbers since the original function does not exist at these points either.


CLAE
^^^^

Input the function,

.. code-block:: console

    (x^3 - 3*x^2 + x - 1)/(x^2 - 4)

.. figure:: Images/Apps/ExtVal022.png
    :alt: y = (x^3-3x^2+x-1)/(x^2-4)

    :math:`f(x) = \frac{x^{3} - 3 x^{2} + x - 1}{x^{2} - 4}`

Following the procedures from the first example, the derivative is,

.. math::
    - \frac{2 x \left(x^{3} - 3 x^{2} + x - 1\right)}{\left(x^{2} - 4\right)^{2}} + \frac{3 x^{2} - 6 x + 1}{x^{2} - 4} = \frac{x^{4} - 13 x^{2} + 26 x - 4}{x^{4} - 8 x^{2} + 16}

Selecting ``Algebra > Solve`` returns the following solutions.

.. math::
    \left[ - \frac{\sqrt{\frac{121}{18 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}}} + 2 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}} + \frac{26}{3}}}{2} + \frac{\sqrt{- 2 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}} - \frac{121}{18 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}}} + \frac{52}{\sqrt{\frac{121}{18 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}}} + 2 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}} + \frac{26}{3}}} + \frac{52}{3}}}{2}, \  \frac{\sqrt{\frac{121}{18 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}}} + 2 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}} + \frac{26}{3}}}{2} - \frac{\sqrt{- \frac{52}{\sqrt{\frac{121}{18 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}}} + 2 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}} + \frac{26}{3}}} - 2 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}} - \frac{121}{18 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}}} + \frac{52}{3}}}{2}, \  \frac{\sqrt{\frac{121}{18 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}}} + 2 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}} + \frac{26}{3}}}{2} + \frac{\sqrt{- \frac{52}{\sqrt{\frac{121}{18 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}}} + 2 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}} + \frac{26}{3}}} - 2 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}} - \frac{121}{18 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}}} + \frac{52}{3}}}{2}, \  - \frac{\sqrt{- 2 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}} - \frac{121}{18 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}}} + \frac{52}{\sqrt{\frac{121}{18 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}}} + 2 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}} + \frac{26}{3}}} + \frac{52}{3}}}{2} - \frac{\sqrt{\frac{121}{18 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}}} + 2 \sqrt[3]{\frac{\sqrt{73462}}{12} + \frac{5057}{216}} + \frac{26}{3}}}{2}\right]

Approximating these gives,

.. math::
    \left[ 0.167912960145734, \  2.10409286580631 - 1.00817857993217 i, \  2.10409286580631 + 1.00817857993217 i, \  -4.37609869175835\right]

So the first and last are real and the middle two are complex.  In the previous examples we never needed to worry about the critical numbers from the derivative not existing.  Since the derivative is,

.. math::
    \frac{x^{4} - 13 x^{2} + 26 x - 4}{x^{4} - 8 x^{2} + 16}

there is the possibility of division by 0.  To extract the denominator select the derivative expression, then select ``Algebra > Rational Expressions > Denominator``.  If you selected the simplified version then the result is :math:`x^{4} - 8 x^{2} + 16` and if you had selected the unsimplified version the result would be :math:`\left(x^{2} - 4\right)^{3}`.  If you apply ``Algebra > Solve`` to either of these the results are :math:`-2` and 2.  These are where the derivative does not exist but we would not consider then critical numbers since the original function does not exist at these points either.

Maxima
^^^^^^

Input and graph the function,

.. code-block:: console

    kill(all);
    f(x):=(x^3 - 3*x^2 + x - 1)/(x^2 - 4)

.. code-block:: console

    wxplot2d(f(x),[x,-5,5],[y,-15,15])


.. figure:: Images/Apps/ExtVal023.png
    :alt: y = (x^3-3x^2+x-1)/(x^2-4)

    :math:`f(x) = \frac{x^{3} - 3 x^{2} + x - 1}{x^{2} - 4}`

Following the procedures from the first example, the derivative is,

.. code-block:: console

    df:diff(f(x),x)
    dfs:ratsimp(df)

.. math::
    \frac{3 {{x}^{2}}-6 x+1}{{{x}^{2}}-4}-\frac{2 x\, \left( {{x}^{3}}-3 {{x}^{2}}+x-1\right) }{{{\left( {{x}^{2}}-4\right) }^{2}}}\mbox{} = \frac{{{x}^{4}}-13 {{x}^{2}}+26 x-4}{{{x}^{4}}-8 {{x}^{2}}+16}\mbox{}

The solutions to :math:`f'(x) = 0` give,

.. code-block:: console

    sl:solve(df=0,x)

.. math::
    \operatorname{[}x=-\frac{\sqrt{9 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{2}{3}}}+78 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}+121}}{6 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{6}}}}-\operatorname{sqrt(}-{{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}+
    \frac{156 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{6}}}}{\sqrt{9 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{2}{3}}}+78 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}+121}}-\frac{121}{9 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}}+\frac{52}{3}\operatorname{)}/2\operatorname{,}x=\operatorname{sqrt(}-
    {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}+\frac{156 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{6}}}}{\sqrt{9 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{2}{3}}}+78 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}+121}}-\frac{121}{9 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}}+\frac{52}{3}\operatorname{)}/2-
    \frac{\sqrt{9 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{2}{3}}}+78 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}+121}}{6 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{6}}}}\operatorname{,}x=\frac{\sqrt{9 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{2}{3}}}+78 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}+121}}{6 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{6}}}}-\operatorname{sqrt(}-{{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}-\frac{156 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{6}}}}{\sqrt{9 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{2}{3}}}+78 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}+121}}-\frac{121}{9 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}}+\frac{52}{3}\operatorname{)}/2\operatorname{,}x=\frac{\sqrt{9 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{2}{3}}}+78 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}+121}}{6 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{6}}}}+\operatorname{sqrt(}-{{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}-
    \frac{156 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{6}}}}{\sqrt{9 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{2}{3}}}+78 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}+121}}-\frac{121}{9 {{\left( \frac{2 \sqrt{73462}}{3}+\frac{5057}{27}\right) }^{\frac{1}{3}}}}+\frac{52}{3}\operatorname{)}/2\operatorname{]}\mbox{}

which approximates to

.. code-block:: console

    float(sl), numer;

.. math::
    \operatorname{[}x=-4.376098691758354\operatorname{,}x=0.1679129601457334\operatorname{,}x=2.104092865806311-1.008178579932175 {{\left( -1\right) }^{0.5}}\operatorname{,}x=1.008178579932175 {{\left( -1\right) }^{0.5}}+2.104092865806311\operatorname{]}\mbox{}

In the previous examples we never needed to worry about the critical numbers from the derivative not existing.  Since the derivative is,

.. math::
    \frac{x^{4} - 13 x^{2} + 26 x - 4}{x^{4} - 8 x^{2} + 16}

there is the possibility of division by 0.  To extract the denominator,

.. code-block:: console

    dfsd:denom(dfs)

which returns :math:`x^{4} - 8 x^{2} + 16`.  Note we are using the simplified version that already simplified the rational expression.  Note, do not use the unsimplified version, the denom function just returns 1.  Solving this expression for 0,

.. code-block:: console

    solve(dfsd)

the results are :math:`-2` and 2.  These are where the derivative does not exist but we would not consider then critical numbers since the original function does not exist at these points either.
