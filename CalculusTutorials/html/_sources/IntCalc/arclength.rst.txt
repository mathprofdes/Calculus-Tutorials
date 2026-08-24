:index:`Arc Length of a Curve`
==============================

Discussion & Definitions
------------------------

The Arc Length Formulas
^^^^^^^^^^^^^^^^^^^^^^^

.. admonition:: Theorem: Arc Length for :math:`y = f(x)`

    Let :math:`f(x)` be a smooth function over the interval :math:`[a, b]`. Then the arc length of the portion of the graph of :math:`f(x)` from the point :math:`(a, f (a))` to the point :math:`(b, f(b))` is given by

    .. math::
        L = \int_a^b \sqrt{1 + (f'(x))^2} \; dx

Note that the integrand of the arc-length integral can be fairly difficult to integrate.  Many times we must rely on approximation techniques.

The calculation of the arc length is completely symmetric, so the formula for a function defined in terms of *y* is identical.

.. admonition:: Theorem: Arc Length for :math:`x = f(y)`

    Let :math:`g(y)` be a smooth function over the *y*-interval :math:`[c, d]`. Then the arc length of the portion of the graph of :math:`g(y)` from the point :math:`(g(c), c)` to the point :math:`(g(d), d)` is given by

    .. math::
        L = \int_c^d \sqrt{1 + (g'(y))^2} \; dy

We can write these formulas fairly compactly in Leibniz notation.

.. math::
    L = \int_a^b \sqrt{1 + \left(\frac{dy}{dx}\right)^2} \; dx \qquad {\rm and} \qquad L = \int_c^d \sqrt{1 + \left(\frac{dx}{dy}\right)^2} \; dy

The Arc Length Function
^^^^^^^^^^^^^^^^^^^^^^^

We can take the Leibniz notation formulation a little further and create an arc length function that will come in handy when we extend this to surface area.

.. admonition:: Definition: The Arc Length Function

    Define

    .. math::
        s(x) = \int_a^x \sqrt{1 + (f'(t))^2} \; dt

Then by the Fundamental Theorem of Calculus Part 1 we get,

.. math::
    \frac{ds}{dx} = \sqrt{1 + (f'(x))^2} = \sqrt{1 + \left(\frac{dy}{dx}\right)^2}

Using the  Leibniz notation formulation and multiplying by :math:`dx` gives,

.. math::
    ds = \sqrt{1 + \left(\frac{dy}{dx}\right)^2} \; dx = \sqrt{dx^2 + dy^2}

and then squaring both sides gives a familiar formula,

.. math::
    ds^2 = dx^2 + dy^2

and from this we also get,

.. math::
    ds = \sqrt{1 + \left(\frac{dx}{dy}\right)^2} \; dy

A nice picture of the relationship between :math:`dx`, :math:`dy`, and :math:`ds` is below.

.. figure:: Images/Apps/ArcLength003.png
    :alt: Arc Length Function Visualization

    Arc Length Function Visualization

We can incorporate this into our arc length formula to get a vary concise statement.

.. admonition:: Theorem: Arc Length

    The arc length of a curve is

    .. math::
        L = \int_a^b ds

    where we can use either formulation for :math:`ds`

    .. math::
        ds = \sqrt{1 + \left(\frac{dy}{dx}\right)^2} \; dx = \sqrt{1 + \left(\frac{dx}{dy}\right)^2} \; dy

    The only thing you need to be careful with is that the bounds of integration need to match the variable of integration.  That is, if we use

    .. math::
        ds = \sqrt{1 + \left(\frac{dy}{dx}\right)^2} \; dx

    then the bounds must be in terms of *x*, and if we use

    .. math::
        ds = \sqrt{1 + \left(\frac{dx}{dy}\right)^2} \; dy

    then the bounds must be in terms of *y*.


Example: :math:`f(x) = \frac{\left(x^{2} + 2\right)^{\frac{3}{2}}}{3}` on :math:`[0, 2]`
----------------------------------------------------------------------------------------

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    (x^2 + 2)^(3/2)/3

Assume that the function came in as *f*, then form the arc-length integrand,

.. code-block:: console

    sqrt(1+(f'(x))^2)

Assume that came in as *g*, then integrate with ``Integral(g, 0, 2)`` and the result is 4.666667.  An image of the curve is below.

.. figure:: Images/Apps/ArcLength001.png
    :alt: y = (x^2 + 2)^(3/2)/3

    :math:`f(x) = \frac{\left(x^{2} + 2\right)^{\frac{3}{2}}}{3}`

CLAE
^^^^

Input the function,

.. code-block:: console

    (x^2 + 2)^(3/2)/3

Take its derivative with ``Calculus > Derivative``, variable *x* and order 1,  the result is :math:`x \sqrt{x^{2} + 2}`.  Assuming that the original expression came in as R1 and the derivative as R2, form the arc-length integrand,


.. code-block:: console

    sqrt(1+R2^2)

The result is, :math:`\sqrt{x^{2} \left(x^{2} + 2\right) + 1}`.

Now integrate with ``Calculus > Definite Integral``, lower bound 0 and upper bound 2.  Unfortunately the result is just,

.. math::
    \int\limits_{0}^{2} \sqrt{x^{2} \left(x^{2} + 2\right) + 1}\, dx

which is a little disappointing, but if we approximate this expression we get, 4.66666666666667.  We can get an exact answer if we help it along a little. Select the integrand expression then select ``Algebra > Factor`` this gives us :math:`\sqrt{\left(x^{2} + 1\right)^{2}}`.  We know this is :math:`x^{2} + 1` but since CLAE sees this as possibly complex it does not go that far.  Select ``Algebra > Special Simplifications`` leave the settings as they are and click OK.  This will result in  :math:`x^{2} + 1`.  Integrate this from 0 to 2 and we get an exact answer of :math:`\frac{14}{3}`.

An image of the curve is below.

.. figure:: Images/Apps/ArcLength002.png
    :alt: y = (x^2 + 2)^(3/2)/3

    :math:`f(x) = \frac{\left(x^{2} + 2\right)^{\frac{3}{2}}}{3}`

Maxima
^^^^^^

Input the function,

.. code-block:: console

    kill(all);
    f(x):=(x^2 + 2)^(3/2)/3

Then set up the integrand and do the integration,

.. code-block:: console

    al:sqrt(1+diff(f(x),x)^2);
    integrate(al, x, 0, 2);

The final result is 14/3.

Example: :math:`f(x) = \sin(x)` on :math:`[0, \pi]`
---------------------------------------------------

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    sin(x)

Assume that the function came in as *f*, then form the arc-length integrand,

.. code-block:: console

    sqrt(1+(f'(x))^2)

Assume that came in as *g*, then integrate with ``Integral(g, 0, pi)`` and the result is 3.8202.


CLAE
^^^^
Input the function,

.. code-block:: console

    sin(x)

Take its derivative with ``Calculus > Derivative``, variable *x* and order 1,  the result is :math:`\cos(x)`.  Assuming that the original expression came in as R1 and the derivative as R2, form the arc-length integrand,

.. code-block:: console

    sqrt(1+R2^2)

The result is, :math:`\sqrt{\cos^{2}{\left(x \right)} + 1}`.

Now integrate with ``Calculus > Definite Integral``, lower bound ``0`` and upper bound ``pi``.  The result is,

.. math::
    \int\limits_{0}^{\pi} \sqrt{\cos^{2}{\left(x \right)} + 1}\, dx

which is (this time) expected given the integrand.  If we approximate this expression we get, 3.82019778902771.


Maxima
^^^^^^

Input the function,

.. code-block:: console

    kill(all);
    f(x):=sin(x)

Then set up the integrand and do the integration,

.. code-block:: console

    al:sqrt(1+diff(f(x),x)^2);
    integrate(al, x, 0, %pi);

The result is,

.. math::
    \int_{0}^{{\pi} }{\left. \sqrt{{{\cos{(x)}}^{2}}+1}dx\right.}\mbox{}

Again this is expected, change ``integrate`` to ``romberg`` to approximate the integral.

.. code-block:: console

    romberg(f,x,0,%pi);

The approximation is 3.820197867551791.

