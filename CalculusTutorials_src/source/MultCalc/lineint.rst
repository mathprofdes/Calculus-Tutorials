:index:`Line Integrals`
=======================

A line integral gives us the ability to integrate multivariable functions and vector fields over arbitrary curves in a plane or in space. In this respect they are generalizations of the familiar definite integral. When we take a definite integral we integrate the function over the interval :math:`[a, b].` The interval :math:`[a, b]` can be regarded as a curve in the plane, the straight line from :math:`[a, 0]` to :math:`[b, 0].`  For a general line integral we take a curve *C* in the plane and integrate a multivariable function over this line.

There are two types of line integrals: scalar line integrals and vector line integrals. Scalar line integrals are integrals of a scalar function over a curve in a plane or in space. Vector line integrals are integrals of a vector field over a curve in a plane or in space.

Line Integrals in the Plane
---------------------------

The derivation of the line integral calculation below follows the same logic as the derivation for the arc-length of a curve.

.. admonition:: Definition: Line Integral

    Let :math:`C = \mathbf{r}(t) = (x(t), y(t))` be a smooth curve in the plane with :math:`\mathbf{r}(a)` being one endpoint to the curve and :math:`\mathbf{r}(b)` the other endpoint to the curve. Say :math:`f(x, y)` is a function of two variables whose domain contains the curve *C*, then the line integral of *f* over *C* with respect to arc-length is,

    .. math::
        \int_C f(x, y) \; ds = \int_a^b f(x(t), y(t)) \sqrt{\left( \frac{dx}{dt} \right)^2 + \left( \frac{dy}{dt} \right)^2} \; dt

Recall that with arc-length,

.. math::
    \frac{ds}{dt} = |\mathbf{r}'(t)| = \sqrt{\left( \frac{dx}{dt} \right)^2 + \left( \frac{dy}{dt} \right)^2}

so

.. math::
    ds = \sqrt{\left( \frac{dx}{dt} \right)^2 + \left( \frac{dy}{dt} \right)^2} \; dt = |\mathbf{r}'(t)| \; dt

With this we can make a more compact version of the line integral formula above,

.. math::
    \int_C f(x, y) \; ds  = \int_a^b f(\mathbf{r}(t))  |\mathbf{r}'(t)| \; dt

Line integrals have numerous applications which depend on what the function :math:`f(x, y)` represents.  Geometrically, it has a similar meaning as definite integrals of a single variable function over an interval, as one would expect.  If we graph the curve *C* on the *xy*-plane and then extend a "curtain" to the function, the line integral is the net area of that curtain.

.. figure:: Images/VecCalc/LineInt001.png
    :alt: Line Integral

    Line Integral


Example: Line Integral in the Plane
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In this example we will find the line integral of :math:`f(x, y) = x^2+y^2` where *C* is the portion of the parabola given by :math:`\mathbf{r}(t) = (t, 3 t^2)` for :math:`0 \leq t \leq 5.`  We will use,

.. math::
    \int_C f(x, y) \; ds  = \int_a^b f(\mathbf{r}(t))  |\mathbf{r}'(t)| \; dt

CLAE
""""

Input the function,

.. code-block:: console

    x^2+y^2

also input the curve,

.. code-block:: console

    [t, 3*t^2]

We will assume that these are in ``R1`` and ``R2`` respectively.  First we will create, :math:`f(\mathbf{r}(t))`, select ``R1``, then select ``Algebra > Evaluate``, leave the variables as ``[x, y]`` and input ``R2`` for the expressions.  The result is ``R3``, :math:`9 t^{4} + t^{2}.`  Now select ``R2`` and then ``Calculus > Derivative``, the result is ``R4``, :math:`\left[ 1, \  6 t\right].` Select ``R4`` and then select ``Vector > Length``, the result is ``R5``, :math:`\sqrt{36 t^{2} + 1}.`  Input ``R3*R5`` and this will be our integrand,

.. math::
    \sqrt{36 t^{2} + 1} \left(9 t^{4} + t^{2}\right)

Integrate this from 0 to 5, the final result is,

.. math::
    - \frac{7 \operatorname{asinh}{\left(30 \right)}}{13824} + \frac{10875035 \sqrt{901}}{2304} \approx 141680.66210366370327



Maxima
""""""

The command for the final integral is,

.. code-block:: console

    integrate(sqrt(36*t**2 + 1)*(9*t**4 + t**2), t, 0, 5);

The result is,

.. math::
    -\frac{7 \operatorname{asinh}(30)-65250210 \sqrt{901}}{13824}\mbox{}


One thing that we observed before is that a curve can have many different parameterizations, and depending on the calculation you are doing a different parameterization may produce a different result.  This is not the case with line integrals.

.. admonition:: Theorem: Line Integrals are Independent of Parameterization

    Given any two parameterizations of the curve *C*, ss long as the curve is traversed exactly once by the parameterization, then the line integral calculated from either parameterization is equal to the other.

One stipulation to our formula is that the curve *C* is smooth over the interval :math:`[a, b].` This means that :math:`\mathbf{r}'(t)` is continuous and nonzero on the interval :math:`[a, b].` If our curve *C* is not smooth but can be broken down into a finite sequence of smooth curves we can still take the line integral over this curve.

.. admonition:: Theorem: Line Integrals Over Piecewise Smooth Curves

    If the curve :math:`C` is piecewise-smooth meaning that it can be broken down into a sequence of smooth curves :math:`C_1, C_2, \ldots, C_n`, then,

    .. math::
        \int_C f(x, y) \; ds = \int_{C_1} f(x, y) \; ds  + \int_{C_2} f(x, y) \; ds  + \cdots + \int_{C_n} f(x, y) \; ds

Other line integrals that will prove useful are line integrals with respect to the coordinate axes.

.. admonition:: Definition: Line Integral With Respect to the Coordinate Axes

    Let :math:`C = \mathbf{r}(t) = (x(t), y(t))` be a smooth curve in the plane with :math:`\mathbf{r}(a)` being one endpoint to the curve and :math:`\mathbf{r}(b)` the other endpoint to the curve. Say :math:`f(x, y)` is a function of two variables whose domain contains the curve *C*, then,

    .. math::
        \int_C f(x, y) \; dx & = \int_a^b f(x(t), y(t)) x'(t) \; dt \\
        \int_C f(x, y) \; dy & = \int_a^b f(x(t), y(t)) y'(t) \; dt \\


Example: Line Integral With Respect to the Coordinate Axes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In this example we will calculate,

.. math::
    \int_C y^2 \sin(x) \; dx + xy \; dy

where *C* is the line segment from :math:`(3, -1)` to :math:`(2, 5).` To parameterize a line segment from point :math:`P` to point :math:`Q` we can use the simple formula, :math:`\mathbf{r}(t) = (1-t)P + tQ` for :math:`0 \leq t \leq 1.`  So for this line segment we have,

.. math::
    \mathbf{r}(t) = (1-t)P + tQ =  (1-t)(3, -1) + t(2, 5) = \left( 3 - t, \  6 t - 1\right)

So :math:`x'(t) = -1` and :math:`y'(t) = 6` and our integral is,

.. math::
    \int_C y^2 \sin(x) \; dx + xy \; dy & = \int_a^b f_1(x(t), y(t)) x'(t) + f_2(x(t), y(t)) y'(t) \; dt \\
    &= \int_0^1  (6 t - 1)^2 \sin(3 - t) (-1) + (3 - t)(6 t - 1) 6 \; dt \\

CLAE
""""

To do this integral first input the integrand,

.. code-block:: console

    (6*t - 1)^2 * sin(3 - t) * (-1) + (3 - t)*(6*t - 1)*6

Select ``Calculus > Definite Integral``, input the bounds of 0 and 1, the result is,

.. math::
    - 60 \sin{\left(2 \right)} + 47 \cos{\left(2 \right)} - 12 \sin{\left(3 \right)} + 27 - 71 \cos{\left(3 \right)} \approx 21.479280234656626888


Maxima
""""""

The Maxima command for the integral is,

.. code-block:: console

    integrate((18 - 6*t)*(6*t - 1) + (6*t - 1)**2*sin(t - 3), t, 0, 1);

and results in,

.. math::
    -12 \sin{(3)}-71 \cos{(3)}-60 \sin{(2)}+47 \cos{(2)}+27\mbox{}


When we define a curve :math:`C = \mathbf{r}(t)` for :math:`a \leq t \leq b` we are traversing the curve in a particular direction, the direction of increasing :math:`t.` We can also traverse the curve in the negative direction, that is backwards along the curve, denoted by :math:`-C.`  For definite integrals of a single variable we know that reversing the bounds gives us a :math:`-1` factor for the integral.  A similar thing happens with coordinate line integrals but not with integrals with respect to arc-length.

.. admonition:: Theorem: Line Integrals and Orientation

    Let :math:`C` be a curve defined by :math:`\mathbf{r}(t)` for :math:`a \leq t \leq b` and let :math:`-C` represent the curve with the same points but opposite orientation. Then,

    .. math::
        \int_{-C} f(x, y) \; dx & = -\int_{C} f(x, y) \; dx \\
        \int_{-C} f(x, y) \; dy & = -\int_{C} f(x, y) \; dy \\
        \int_{-C} f(x, y) \; ds & = \int_{C} f(x, y) \; ds \\


Line Integrals in Space
-----------------------

Line integrals for space curves are identical to those in the plane, we simply add on another dimension.


.. admonition:: Definition: Line Integrals for Space Curves

    Let :math:`C = \mathbf{r}(t) = (x(t), y(t), z(t))` be a smooth curve in space with :math:`\mathbf{r}(a)` being one endpoint to the curve and :math:`\mathbf{r}(b)` the other endpoint to the curve. Say :math:`f(x, y, z)` is a function of three variables whose domain contains the curve *C*, then the line integral of *f* over *C* with respect to arc-length is,

    .. math::
        \int_C f(x, y, z) \; ds & = \int_a^b f(\mathbf{r}(t))  |\mathbf{r}'(t)| \; dt \\
        & = \int_a^b f(x(t), y(t), z(t)) \sqrt{\left( \frac{dx}{dt} \right)^2 + \left( \frac{dy}{dt} \right)^2 + \left( \frac{dz}{dt} \right)^2 } \; dt

.. admonition:: Theorem: Line Integrals Over Piecewise Smooth Curves

    If the curve :math:`C` is piecewise-smooth meaning that it can be broken down into a sequence of smooth curves :math:`C_1, C_2, \ldots, C_n`, then,

    .. math::
        \int_C f(x, y, z) \; ds = \int_{C_1} f(x, y, z) \; ds  + \int_{C_2} f(x, y, z) \; ds  + \cdots + \int_{C_n} f(x, y, z) \; ds


.. admonition:: Definition: Line Integral With Respect to the Coordinate Axes

    Let :math:`C = \mathbf{r}(t) = (x(t), y(t), z(t))` be a smooth curve in space with :math:`\mathbf{r}(a)` being one endpoint to the curve and :math:`\mathbf{r}(b)` the other endpoint to the curve. Say :math:`f(x, y, z)` is a function of three variables whose domain contains the curve *C*, then,

    .. math::
        \int_C f(x, y, z) \; dx & = \int_a^b f(x(t), y(t), z(t)) x'(t) \; dt \\
        \int_C f(x, y, z) \; dy & = \int_a^b f(x(t), y(t), z(t)) y'(t) \; dt \\
        \int_C f(x, y, z) \; dz & = \int_a^b f(x(t), y(t), z(t)) z'(t) \; dt \\


.. admonition:: Theorem: Line Integrals and Orientation

    Let :math:`C` be a curve defined by :math:`\mathbf{r}(t)` for :math:`a \leq t \leq b` and let :math:`-C` represent the curve with the same points but opposite orientation. Then,

    .. math::
        \int_{-C} f(x, y, z) \; dx & = -\int_{C} f(x, y, z) \; dx \\
        \int_{-C} f(x, y, z) \; dy & = -\int_{C} f(x, y, z) \; dy \\
        \int_{-C} f(x, y, z) \; dz & = -\int_{C} f(x, y, z) \; dz \\
        \int_{-C} f(x, y, z) \; ds & = \int_{C} f(x, y, z) \; ds \\

Example: Line Integral
^^^^^^^^^^^^^^^^^^^^^^

In this example we will find the line integral of :math:`f(x, y, z) = x^2+y^2+z` where *C* is one turn of the helix given by :math:`\mathbf{r}(t) = (\cos(t), \sin(t), t)` for :math:`0 \leq t \leq 2\pi.`  We will again use the formula,

.. math::
    \int_C f(x, y, z) \; ds  = \int_a^b f(\mathbf{r}(t))  |\mathbf{r}'(t)| \; dt

CLAE
""""

Input the function,

.. code-block:: console

    x^2+y^2+z

also input the curve,

.. code-block:: console

    [cos(t), sin(t), t]

We will assume that these are in ``R1`` and ``R2`` respectively.  First we will create, :math:`f(\mathbf{r}(t))`, select ``R1``, then select ``Algebra > Evaluate``, leave the variables as ``[x, y, z]`` and input ``R2`` for the expressions.  The result is ``R3`` and ``R4`` (simplified), :math:`t + \sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} = t+1.`  Now select ``R2`` and then ``Calculus > Derivative``, the result is ``R5``, :math:`\left[ - \sin{\left(t \right)}, \  \cos{\left(t \right)}, \  1\right].` Select ``R5`` and then select ``Vector > Length``, the result is ``R6`` and ``R7`` (simplified), :math:`\sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} = \sqrt{2}.`  Input ``R4*R7`` and this will be our integrand,

.. math::
    \sqrt{2} \left(t + 1\right)

Integrate this from 0 to :math:`2\pi`, the final result is,

.. math::
    2 \sqrt{2} \pi + 2 \sqrt{2} \pi^{2} \approx 36.801222674872250631


Line Integrals of Vector Fields
-------------------------------

The second type of line integrals are vector line integrals, in which we integrate along a curve through a vector field.  This is often motivated by the concept of Work.  One question would be is if this vector field was a force field that described the force on a particle at each point in space and we have an object that is moving along this curve, hoe much work is done by the object to traverse the curve?  Line integrals through a vector field have many more applications then this but it is a good illustration of what we are doing.

.. figure:: Images/VecCalc/LineInt002.png
    :alt: Line Integral Through a Vector Field

    Line Integral Through a Vector Field


.. admonition:: Definition: Line Integrals of Vector Fields

    Let :math:`\mathbf{F}` be a continuous vector field and let :math:`C = \mathbf{r}(t)` for :math:`a \leq t \leq b` be a smooth curve contained in the vector field. Then the line integral of *F* along *C* is

    .. math::
        \int_C \mathbf{F} \cdot d\mathbf{r} = \int_a^b \mathbf{F}(\mathbf{r}(t)) \cdot \mathbf{r}'(t) \; dt = \int_C \mathbf{F} \cdot \mathbf{T} \; ds

The above formulas apply to both two and three dimensions.  If the field and curve are in two dimensions, specifically, :math:`\mathbf{F}(x, y) = P \; \mathbf{i} + Q \; \mathbf{j}` and :math:`C = \mathbf{r}(t) = (x(t), y(t)),` then

.. math::
    \int_C \mathbf{F} \cdot d\mathbf{r} = \int_a^b P \; dx + Q \; dy

If the field and curve are in three dimensions, specifically, :math:`\mathbf{F}(x, y, z) = P \; \mathbf{i} + Q \; \mathbf{j}  + R \; \mathbf{k}` and :math:`C = \mathbf{r}(t) = (x(t), y(t), z(t)),` then

.. math::
    \int_C \mathbf{F} \cdot d\mathbf{r} = \int_a^b P \; dx + Q \; dy  + R \; dz


.. admonition:: Theorem: Properties of Vector Line Integrals

    If :math:`\mathbf{F}` and :math:`\mathbf{G}` be continuous vector fields that contain a smooth curve C. Then

    1. :math:`\displaystyle \int_C (\mathbf{F} + \mathbf{G}) \cdot d\mathbf{r} = \int_C \mathbf{F} \cdot d\mathbf{r} + \int_C \mathbf{G} \cdot d\mathbf{r}`

    2. :math:`\displaystyle \int_C k \mathbf{F} \cdot d\mathbf{r} = k \int_C \mathbf{F} \cdot d\mathbf{r}` for a constant :math:`k.`

    3. :math:`\displaystyle \int_{-C} \mathbf{F} \cdot d\mathbf{r} = - \int_C \mathbf{F} \cdot d\mathbf{r}`

    4. If the curve :math:`C` is piecewise-smooth meaning that it can be broken down into a sequence of smooth curves :math:`C_1, C_2, \ldots, C_n`, then,

    .. math::
        \int_C \mathbf{F} \cdot d\mathbf{r} = \int_{C_1} \mathbf{F} \cdot d\mathbf{r} + \int_{C_2} \mathbf{F} \cdot d\mathbf{r} + \cdots + \int_{C_n} \mathbf{F} \cdot d\mathbf{r}


Example: Line Integrals of a Vector Field
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In this example we will take the vector field :math:`\mathbf{F}(x, y, z) = \left( \sin{\left(y \right)}, \  \cos{\left(z \right)}, \  \sin{\left(x + y \right)}\right)` and the twisted cubic :math:`\mathbf{r}(t) = \left( t, \  t^{2}, \  t^{3}\right)` for :math:`-2 \leq t \leq 2` and find

.. math::
    \int_C \mathbf{F} \cdot d\mathbf{r} = \int_a^b \mathbf{F}(\mathbf{r}(t)) \cdot \mathbf{r}'(t) \; dt

CLAE
""""

Input the vector field,

.. code-block:: console

    [sin(y),cos(z),sin(x + y)]

and the curve,

.. code-block:: console

    [t,t^2,t^3]

We will assume that these come in as ``R1`` and ``R2`` respectively.  Click and drag both of these to the 3D graphics window, the first should come in as a vector field and the second as a space curve.  Change the bounds on the space curve to :math:`-2` and :math:`2.`  The image should look like the following.  Move the graph around to get a feel for the curve and field.

.. figure:: Images/VecCalc/LineInt003.png
    :alt: Line Integral Through a Vector Field

    Line Integral Through a Vector Field

To continue the calculation, select ``R1`` then select ``Algebra > Evaluate``, input ``R2`` as the expressions, the result is ``R3``,

.. math::
    \left[ \sin{\left(t^{2} \right)}, \  \cos{\left(t^{3} \right)}, \  \sin{\left(t^{2} + t \right)}\right]

Now select ``R2`` and take its derivative, the result is ``R4``,

.. math::
    \left[ 1, \  2 t, \  3 t^{2}\right]

Now take the dot product of ``R3`` and ``R4``, you can do this by selecting ``R3``, then select ``Vector > Dot Product``, in the dialog that appears select ``R4`` and click OK.  The result will be,

.. math::
    \sin{\left(t^{2} \right)} + 3 \sin{\left(t^{2} + t \right)} \overline{t}^{2} + 2 \cos{\left(t^{3} \right)} \overline{t}

Note that there is a line over some of the *t* terms.  This is the complex conjugate of *t*.  Select ``Algebra > Simplify Assuming Real Variables`` and the result is,

.. math::
    3 t^{2} \sin{\left(t \left(t + 1\right) \right)} + 2 t \cos{\left(t^{3} \right)} + \sin{\left(t^{2} \right)}

Now integrate this between :math:`-2` and :math:`2.`  The result is,

.. math::
    \int\limits_{-2}^{2} \left(3 t^{2} \sin{\left(t \left(t + 1\right) \right)} + 2 t \cos{\left(t^{3} \right)} + \sin{\left(t^{2} \right)}\right)\, dt

which means that CLAE (SymPy) could not evaluate the integral exactly.  Select this output and then select ``Algebra > Approximate`` and we get the approximate result of, 4.2440999323061119222.

Maxima
""""""

The command for the integral is,

.. code-block:: console

    integrate(3*t**2*sin(t*(t + 1)) + 2*t*cos(t**3) + sin(t**2), t, -2, 2);

The output is fairly lengthy with several special functions, the approximate value from CLAE is probably more informative.

.. math::
    \operatorname{(}\sqrt{{\pi} } \operatorname{(}\left( 4 \% i+4\right)  \operatorname{erf}\left( \sqrt{2} \% i+\sqrt{2}\right) +\left( 4 \% i-4\right)  \operatorname{erf}\left( \sqrt{2} \% i-\sqrt{2}\right) +\left( 4-4 \% i\right)  \operatorname{erf}\left( 2 \sqrt{-\% i}\right) +\left( 4 \% i+4\right)  \operatorname{erf}\left( 2 {{\left( -1\right) }^{\frac{1}{4}}}\right) +12 \sin{\left( \frac{1}{4}\right) }+36 \cos{\left( \frac{1}{4}\right) }\operatorname{)}+ \left( \left( -12 \% i-12\right)  \sin{\left( \frac{1}{4}\right) }+\left( 12 \% i-12\right)  \cos{\left( \frac{1}{4}\right) }\right)  \operatorname{gamma\_ incomplete}\left( \frac{3}{2}\operatorname{,}\frac{25 \% i}{4}\right) +\left( \left( -12 \% i-12\right)  \sin{\left( \frac{1}{4}\right) }+\left( 12 \% i-12\right)  \cos{\left( \frac{1}{4}\right) }\right) \operatorname{gamma\_ incomplete}\left( \frac{3}{2}\operatorname{,}\frac{9 \% i}{4}\right) +\left( \left( 12 \% i-12\right)  \sin{\left( \frac{1}{4}\right) }+\left( -12 \% i-12\right)  \cos{\left( \frac{1}{4}\right) }\right)  \operatorname{gamma\_ incomplete}\left( \frac{3}{2}\operatorname{,}-\frac{9 \% i}{4}\right) + \left( \left( 12 \% i-12\right)  \sin{\left( \frac{1}{4}\right) }+\left( -12 \% i-12\right)  \cos{\left( \frac{1}{4}\right) }\right)  \operatorname{gamma\_ incomplete}\left( \frac{3}{2}\operatorname{,}-\frac{25 \% i}{4}\right) +\left( 3 {{2}^{\frac{5}{2}}} \% i \sin{\left( \frac{1}{4}\right) }+3 {{2}^{\frac{5}{2}}} \cos{\left( \frac{1}{4}\right) }\right) \operatorname{gamma\_ incomplete}\left( 1\operatorname{,}\frac{25 \% i}{4}\right) +\left( -3 {{2}^{\frac{5}{2}}} \% i \sin{\left( \frac{1}{4}\right) }-3 {{2}^{\frac{5}{2}}} \cos{\left( \frac{1}{4}\right) }\right)  \operatorname{gamma\_ incomplete}\left( 1\operatorname{,}\frac{9 \% i}{4}\right) +\left( 3 {{2}^{\frac{5}{2}}} \% i \sin{\left( \frac{1}{4}\right) }-3 {{2}^{\frac{5}{2}}} \cos{\left( \frac{1}{4}\right) }\right) \operatorname{gamma\_ incomplete}\left( 1\operatorname{,}-\frac{9 \% i}{4}\right) +\left( 3 {{2}^{\frac{5}{2}}} \cos{\left( \frac{1}{4}\right) }-3 {{2}^{\frac{5}{2}}} \% i \sin{\left( \frac{1}{4}\right) }\right)  \operatorname{gamma\_ incomplete}\left( 1\operatorname{,}-\frac{25 \% i}{4}\right) +\left( \left( 3-3 \% i\right)  \sin{\left( \frac{1}{4}\right) }+\left( -3 \% i-3\right)  \cos{\left( \frac{1}{4}\right) }\right) \operatorname{gamma\_ incomplete}\left( \frac{1}{2}\operatorname{,}\frac{25 \% i}{4}\right) +\left( \left( 3-3 \% i\right)  \sin{\left( \frac{1}{4}\right) }+\left( -3 \% i-3\right)  \cos{\left( \frac{1}{4}\right) }\right)  \operatorname{gamma\_ incomplete}\left( \frac{1}{2}\operatorname{,}\frac{9 \% i}{4}\right) +\left( \left( 3 \% i+3\right)  \sin{\left( \frac{1}{4}\right) }+\left( 3 \% i-3\right)  \cos{\left( \frac{1}{4}\right) }\right) \operatorname{gamma\_ incomplete}\left( \frac{1}{2}\operatorname{,}-\frac{9 \% i}{4}\right) +\left( \left( 3 \% i+3\right)  \sin{\left( \frac{1}{4}\right) }+\left( 3 \% i-3\right)  \cos{\left( \frac{1}{4}\right) }\right)  \operatorname{gamma\_ incomplete}\left( \frac{1}{2}\operatorname{,}-\frac{25 \% i}{4}\right) \operatorname{)}/{{2}^{\frac{9}{2}}}\mbox{}

