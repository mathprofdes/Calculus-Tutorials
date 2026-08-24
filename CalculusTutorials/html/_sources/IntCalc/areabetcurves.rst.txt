:index:`Areas Between Curves`
=============================

Discussion & Definitions
------------------------

In most Calculus books the area between curves section is mainly an introductory exercise in going through the process of representing a quantity as the limit of a Riemann sum and hence establishing that it is a definite integral.  This is a good exercise to do since many quantities in the physical sciences and economics (among others) can be represented this way, but we will leave the details to the textbook you are using.

.. admonition:: Theorem: Finding the Area between Two Curves

    Let :math:`f(x)` and :math:`g(x)` be continuous functions such that :math:`f(x) \geq g(x)` over an interval :math:`[a, b]`. Let :math:`R` denote the region bounded above by the graph of :math:`f(x)`, below by the graph of :math:`g(x)`, and on the left and right by the lines :math:`x = a` and :math:`x = b`, respectively. Then, the area of :math:`R` is given by

    .. math::
        A = \int_a^b f(x) - g(x) \; dx

For example, if we take the curves :math:`f(x) = 2-x^2` and :math:`g(x) = x^2` then the area between these two curves on the interval :math:`[0, 1/2]` is

.. math::
    \int_0^{1/2} (2-x^2) - (x^2) \; dx = \frac{11}{12} \approx 0.916666666666667

.. figure:: Images/Apps/AreaBetCurves001.png
    :alt: Area Between y = 2-x^2 and y = x^2 on [0, 1/2]

    Area Between  :math:`f(x) = 2-x^2` and :math:`g(x) = x^2` on :math:`[0, 1/2]`

If the two curves intersect so that over the interval one is no longer larger than the other, that is, they cross, then to find the area of the region bounded by the curves we need to either integrate the absolute value of the difference or break the integral up into separate integrals each of which has one function always over the other.

.. admonition:: Theorem: Finding the Area of a Region between Curves That Cross

    Let :math:`f(x)` and :math:`g(x)` be continuous functions over an interval :math:`[a, b]`. Let :math:`R` denote the region between the graphs of :math:`f(x)` and :math:`g(x)`, and be bounded on the left and right by the lines :math:`x = a` and :math:`x = b`, respectively. Then, the area of :math:`R` is given by

    .. math::
        A = \int_a^b \left| f(x) - g(x) \right| \; dx

Absolute values are notoriously difficult for most computer algebra systems to deal with since they require the system to break up the integral between the positive and negative regions of the integrand, which require the system to solve the integrand for 0, think about combinations of trigonometric functions. In most cases, it is better to do this yourself by finding where the functions cross and then do an integral for each separate section.

For example, if we take the curves :math:`f(x) = 2-x^2` and :math:`g(x) = x^2` and wish to find the area between these two curves on the interval :math:`[0, 2]`, first we would graph the curves and look at the enclosed region.

.. figure:: Images/Apps/AreaBetCurves002.png
    :alt: Area Between y = 2-x^2 and y = x^2 on [0, 2]

    Area Between  :math:`f(x) = 2-x^2` and :math:`g(x) = x^2` on :math:`[0, 2]`

Clearly the curves intersect.  Solving for the intersection points gives two solutions, :math:`-1` and 1 so we have,

.. math::
    \int_0^{2} |(2-x^2) - (x^2)| \; dx = \int_0^{1} (2-x^2) - (x^2) \; dx  + \int_1^{2} (x^2) - (2-x^2) \; dx = \frac{4}{3} + \frac{8}{3} = 4

Of course, if the curves intersect more than once over the interval of interest we would break the integral up into more segments.  We can also switch the roles of *x* and *y* around to find the areas of regions bounded by functions in *y*, for example, :math:`x = y^2` and :math:`x = \sin(y)`.

.. figure:: Images/Apps/AreaBetCurves003.png
    :alt: Area Between x = y^2 and x = sin(y)

    Area Between :math:`x = y^2` and :math:`x = \sin(y)`

.. admonition:: Theorem: Finding the Area between Two Curves, Integrating along the y-axis

    Let :math:`u(y)` and :math:`v(y)` be continuous functions such that :math:`u(y) \geq v(y)` for all :math:`y \in [c, d].` Let :math:`R` denote the region bounded on the right by the graph of :math:`u(y),` on the left by the graph of :math:`v(y),` and above and below by the lines :math:`y = d` and :math:`y = c`, respectively. Then, the area of :math:`R` is given by

    .. math::
        A = \int_c^d u(y) - v(y) \; dy


Example: Area bounded by :math:`f(x) = \sqrt{1 - x^{2}}` and :math:`g(x) = x^{2} + 2 x + 1`
-------------------------------------------------------------------------------------------

If we graph these two functions we get the following image (with the region we want shaded).

.. figure:: Images/Apps/AreaBetCurves004.png
    :alt: Area bounded by f(x) = \sqrt{1 - x^{2}} and :g(x) = x^{2} + 2 x + 1

    Area bounded by :math:`f(x) = \sqrt{1 - x^{2}}` and :math:`g(x) = x^{2} + 2 x + 1`

Solving :math:`\sqrt{1 - x^{2}} = x^{2} + 2 x + 1` gives us two solutions :math:`-1` and 0. So our area is

.. math::
    \int_{-1}^0 \sqrt{1 - x^{2}} - (x^{2} + 2 x + 1) \; dx = \left. - \frac{x^{3}}{3} - x^{2} + \frac{x \sqrt{1 - x^{2}}}{2} - x + \frac{\operatorname{asin}{\left(x \right)}}{2} \right|_{-1}^0 = - \frac{1}{3} + \frac{\pi}{4}

GeoGebra
^^^^^^^^

Input the two functions,

.. code-block:: console

    sqrt(1 - x^2)

and

.. code-block:: console

    x^2 + 2 x + 1

Assume they came in as *f* and *g* respectively.  Find the intersection points with ``Solve(f=g)``, giving :math:`-1` and 0, then find the area with, ``Integral(f(x)-g(x),-1,0)``.  The result is 0.45206.

CLAE
^^^^

Input the two functions,

.. code-block:: console

    sqrt(1 - x^2)

and

.. code-block:: console

    x^2 + 2*x + 1

Assume they came in as ``R1`` and ``R2`` respectively.  Find the intersection points first by taking the difference ``R1-R2`` and then selecting ``Algebra > Solve``, giving :math:`-1` and 0, then find the area with, ``Calculus > Definite Integral``, using the bounds of :math:`-1` and 0.  The result is,

.. math::
    - \frac{1}{3} + \frac{\pi}{4} \approx 0.452064830064115

Maxima
^^^^^^

Input the two functions,

.. code-block:: console

    kill(all);
    f(x):=sqrt(1 - x^2);
    g(x):=x^2 + 2*x + 1;

The solve command does not work well with these equations but from the graph it appears that the solutions are :math:`-1` and 0.  Finding the integral with,

.. code-block:: console

    integrate(f(x)-g(x),x,-1,0);

gives,

.. math::
    \frac{3 {\pi} -4}{12}


Example: Area bounded by :math:`f(x) = 2-x^2` and :math:`g(x) = x^2` on :math:`[0, 2]`
--------------------------------------------------------------------------------------

We did this example above but here we will look at the processes in our computer algebra systems.

.. figure:: Images/Apps/AreaBetCurves002.png
    :alt: Area bounded by f(x) = 2-x^2 and g(x) = x^2` on [0, 2]

    Area bounded by :math:`f(x) = 2-x^2` and :math:`g(x) = x^2` on :math:`[0, 2]`

GeoGebra
^^^^^^^^

Input the two functions,

.. code-block:: console

    2-x^2

.. code-block:: console

    x^2

Assume they came in as *f* and *g* respectively.  Find the intersection points with ``Solve(f=g)``, giving :math:`-1` and 1, then find the area of the first region with, ``Integral(f(x)-g(x),0, 1)`` and then the second region with ``Integral(g(x)-f(x),1, 2)``.  The results are 1.33333 and 2.66667 respectively. Adding these gives us the expected result of 4.

Note that if we tried the absolute value definition and input ``Integral(|f(x)-g(x)|,0,2)`` GeoGebra returns 4.  Under the hood, an approximation technique was used on the function.

CLAE
^^^^

Input the two functions,

.. code-block:: console

    2-x^2

.. code-block:: console

    x^2

Assume they came in as ``R1`` and ``R2`` respectively.  Find the intersection points first by taking the difference ``R1-R2`` and then selecting ``Algebra > Solve``, giving :math:`-1` and 1. Select the ``R1-R2`` expression, then find the first area with, ``Calculus > Definite Integral``, using the bounds of 0 and 1.  The result is, :math:`\frac{4}{3}`.  Now input ``R2-R1``, select it , then find the second area with, ``Calculus > Definite Integral``, using the bounds of 1 and 2.  The result is, :math:`\frac{8}{3}`. Add these together to obtain the final answer of 4.

If we tried the absolute value approach.  Input ``abs(R1-R2)``, select this and then select ``Calculus > Definite Integral``, using the bounds of 0 and 2. The result is,

.. math::
    \int\limits_{0}^{2} \begin{cases} 2 x^{2} - 2 & \text{for}\: x^{2} \geq 1 \\2 - 2 x^{2} & \text{otherwise} \end{cases}\, dx

Clearly, CLAE did not want to do the integral.  If we select this and then select ``Algebra > Approximate`` we will get the solution of 4, although it took several seconds for this to evaluate.  On the other hand, we could have selected ``Calculus > Definite Integral Approximation`` with the bounds 0 and 2 and the result would be 4 again, but quicker this way.

Maxima
^^^^^^

Input the two functions,

.. code-block:: console

    kill(all);
    f(x):=2-x^2;
    g(x):=x^2;

Find the intersection points with

.. code-block:: console

    solve(f(x)=g(x));

giving :math:`-1` and 1.  Then find the integral with,

.. code-block:: console

    integrate(f(x)-g(x),x,0,1)+ integrate(g(x)-f(x),x,1,2);

the result being 4, as expected.

If we tried the absolute value approach.  Input,

.. code-block:: console

    h(x):=abs(f(x)-g(x))

then take the integral with,

.. code-block:: console

    integrate(h(x),x,0,2);

the result will be,

.. math::
    \int_{0}^{2}{\left. \left| 2 {{x}^{2}}-2\right| dx\right.}\mbox{}

Clearly, Maxima did not want to do the integral.  If we instead use an integral approximation command,

.. code-block:: console

    romberg(h(x),x,0,2);

we will get the solution of 4.0.

