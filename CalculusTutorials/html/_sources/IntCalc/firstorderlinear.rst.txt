:index:`First-Order Linear Equations`
=====================================

Discussion & Definitions
------------------------

A first-order linear differential equation is one that can be put into the form,

.. math::
    y' + p(x)y = q(x)

The basic idea in solving a first-order linear differential equation is to turn the left hand side of the equation into a product rule.  This can be done by multiplying both sides by the **integrating factor**,

.. math::
    e^{\int p(x) \; dx}

This will turn the left hand side into the result of a product rule.  Reform the left hand side into the derivative of the product then integrate both sides and finally divide both sides by the integrating factor.

For example, solve the differential equation :math:`y' = 3x + xy`.  First write the equation in standard form,

.. math::
    y' -xy = 3x

Next calculate the integrating factor,

.. math::
    e^{\int p(x) \; dx} = e^{\int -x \; dx} = e^{-x^2/2}

Multiply both sides of the equation by the integrating factor,

.. math::
    y'e^{-x^2/2} -xe^{-x^2/2}y = 3xe^{-x^2/2}

Reform the left hand side into the derivative of the product,

.. math::
    \frac{d}{dx} \left( ye^{-x^2/2} \right) = 3xe^{-x^2/2}

Note that the left hand side is just the integrating factor times *y*.

Now integrate both sides,

.. math::
    ye^{-x^2/2} = - 3 e^{- \frac{x^{2}}{2}} + C

Finally, divide both sides by the integrating factor,

.. math::
    y = \frac{- 3 e^{- \frac{x^{2}}{2}} + C}{e^{-x^2/2}} = Ce^{x^2/2} - 3


Example: Solve :math:`y' = 3x + xy`
-----------------------------------

GeoGebra
^^^^^^^^

In general for GeoGebra we need to write the equation in the form :math:`y' = f(x, y)`. Our given differential equation is already in this form but for the general form :math:`y' + p(x)y = q(x)` we would rewrite it as :math:`y' = -p(x)y + q(x).`

Input the right hand side of the equation,

.. code-block:: console

    3x + xy

Assuming this came in as ``a(x, y)``, in a new cell input ``SolveODE(a)``.  The result is

.. math::
    f(x) = C_1 e^{x^2/2} - 3

where the :math:`C_1` comes in as a slider.

CLAE
^^^^

Input the differential equation,

.. code-block:: console

    3*x + x*f(x) - f(x).diff(x)

Then select ``Calculus > Solve ODE``, the result is,

.. math::
    f{\left(x \right)} = C_{1} e^{\frac{x^{2}}{2}} - 3

If you wish to graph this or work further with the solution you can extract the right hand side of the equation with ``Algebra > Equations > Right Hand Side``.


Maxima
^^^^^^

Input the differential equation,

.. code-block:: console

    de:3*x + x*y - 'diff(y, x);

Solve the ODE with,

.. code-block:: console

    sl:ode2(de, y, x);

the result of this is

.. math::
    y=\left( {\mathrm{\% c}}-3 {{\% e}^{-\frac{{{x}^{2}}}{2}}}\right)  {{\% e}^{\frac{{{x}^{2}}}{2}}}\mbox{}

which can obviously be simplified.  Doing

.. code-block:: console

    ratsimp(sl);

gives us

.. math::
    y={\mathrm{\% c}} {{\% e}^{\frac{{{x}^{2}}}{2}}}-3\mbox{}

