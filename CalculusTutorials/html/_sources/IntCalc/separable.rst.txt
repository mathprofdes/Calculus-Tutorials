:index:`Separable Equations`
============================

Discussion & Definitions
------------------------

As discussed in previous sections, solving differential equation exactly can be difficult and sometimes impossible to do.  There are some special forms of differential equations that in many cases can be solved exactly.  One very nice form is a separable equation.  Essentially these are when the derivative is equal to a product of two functions, one in terms of *x* and the other in terms of *y*.

.. admonition:: Definition: Separable Differential Equation

    A separable differential equation is any equation that can be written in the form

    .. math::
        y' = f(x)g(y)

If you were solving the differential equation by hand you would use the following procedure that is called separation of variables.

.. admonition:: Problem-Solving: Separation of Variables

    1. Check for any values of *y* that make :math:`g(y) = 0`. These correspond to constant solutions.

    2. Rewrite the differential equation in the form,

    .. math::
        y' & = f(x)g(y) \\
        \frac{dy}{dx} & = f(x)g(y) \\
        \frac{dy}{g(y)} & = f(x) \; dx \\

    3. Integrate both sides of the equation.

    .. math::
        \int \frac{dy}{g(y)} & = \int f(x) \; dx \\

    4. Solve the resulting equation for *y* if possible. It is not always possible to obtain *y* as an explicit function of *x*. Quite often we have to write *y* as an implicit function of *x*.

    5. If an initial condition exists, substitute the appropriate values for *x* and *y* into the equation and solve for the constant.


For example, we will solve the differential equation, :math:`\frac{dy}{dx} = y^{2} e^{x} \sin{\left(3 x \right)}.`

.. math::
    \frac{dy}{dx} & = y^{2} e^{x} \sin{\left(3 x \right)} \\
    y^{-2} \; dy & = e^{x} \sin{\left(3 x \right)} \; dx \\
    \int y^{-2} \; dy & = \int e^{x} \sin{\left(3 x \right)} \; dx \\
    - \frac{1}{y} + C_1 & = \frac{\left(\sin{\left(3 x \right)} - 3 \cos{\left(3 x \right)}\right) e^{x}}{10} + C_2 \\
    - \frac{1}{y} & = \frac{\left(\sin{\left(3 x \right)} - 3 \cos{\left(3 x \right)}\right) e^{x}}{10} + C \\
    \frac{1}{y} & = - \frac{\left(\sin{\left(3 x \right)} - 3 \cos{\left(3 x \right)}\right) e^{x}}{10} + C \\
    y & = \frac{10}{10 C - \left(\sin{\left(3 x \right)} - 3 \cos{\left(3 x \right)}\right) e^{x}}

Example: :math:`\frac{dy}{d x} = \left(x^{2} - 4\right) \left(3 y + 2\right)`
-----------------------------------------------------------------------------

GeoGebra
^^^^^^^^

Input the right hand side of the equation,

.. code-block:: console

    (x^2 - 4)(3y + 2)

Assuming that this came in as ``a(x, y)``, in a new cell input ``SolveODE(a)`` and the solution may take a couple moments bur we get,

.. math::
    f{\left(x \right)} = 1 \cdot e^{x \left(x^{2} - 12\right)} - \frac{2}{3}

Note that the first 1 is really a constant that is linked up to the :math:`C_1` slider.  Since GeoGebra does not allow variables outside the independent variables of the graphics system these constants will come in as slider. So the general solution would really be.

.. math::
    f{\left(x \right)} = C_{1} e^{x \left(x^{2} - 12\right)} - \frac{2}{3}

CLAE
^^^^

Input the expression with derivatives, also note that we use ``f(x)`` in place of ``y``,

.. code-block:: console

    (x^2 - 4)*(3*f(x) + 2) - f(x).diff(x)

Now select ``Calculus > Solve ODE``, the dialog box should have everything filled in as needed. The result is,

.. math::
    f{\left(x \right)} = C_{1} e^{x \left(x^{2} - 12\right)} - \frac{2}{3}

If you wish to graph this or work further with the solution you can extract the right hand side of the equation with ``Algebra > Equations > Right Hand Side``.

Maxima
^^^^^^

Input the expression with derivatives,

.. code-block:: console

    kill(all);
    de:(x^2-4)*(3*y + 2) - 'diff(y, x);

Then solve the ODE with

.. code-block:: console

    sl:ode2(de,y,x);

The result is,

.. math::
    y=\left( {\mathrm{\% c}}-\frac{2 {{\% e}^{12 x-{{x}^{3}}}}}{3}\right)  {{\% e}^{{{x}^{3}}-12 x}}\mbox{}



Example: :math:`\frac{dy}{d x} = y^{2} e^{x} \sin{\left(3 x \right)}`
---------------------------------------------------------------------

GeoGebra
^^^^^^^^

Input the right hand side of the equation,

.. code-block:: console

    y^(2) e^(x) sin(3x)

Assuming that this came in as ``a(x, y)``, in a new cell input ``SolveODE(a)`` and the solution may take a couple moments bur we get,

.. math::
    f{\left(x \right)} =  \frac{10}{10 \cdot 1 - e^{x} \sin{\left(3 x \right)} + 3 e^{x} \cos{\left(3 x \right)}}

Note that the :math:`10 \cdot 1` is really :math:`10 \cdot C_1`, the 1 is linked up to the :math:`C_1` slider.  Since GeoGebra does not allow variables outside the independent variables of the graphics system these constants will come in as slider. So the general solution would really be.

.. math::
    f{\left(x \right)} =  \frac{10}{10 \cdot C_1 - e^{x} \sin{\left(3 x \right)} + 3 e^{x} \cos{\left(3 x \right)}}

CLAE
^^^^

Input the expression with derivatives, also note that we use ``f(x)`` in place of ``y``,

.. code-block:: console

    y^2*exp(x)*sin(3*x) - f(x).diff(x)

Now select ``Calculus > Solve ODE``, the dialog box should have everything filled in as needed. The result is,

.. math::
    f{\left(x \right)} = - \frac{10}{C_{1} + e^{x} \sin{\left(3 x \right)} - 3 e^{x} \cos{\left(3 x \right)}}

If you wish to graph this or work further with the solution you can extract the right hand side of the equation with ``Algebra > Equations > Right Hand Side``.

Maxima
^^^^^^

Input the expression with derivatives,

.. code-block::

    kill(all);
    de:y^2*%e^x*sin(3*x) - 'diff(y, x);

Then solve the ODE with

.. code-block:: console

    sl:ode2(de,y,x);

The result is,

.. math::
    -\frac{1}{y}=\frac{{{\% e}^{x}} \sin{\left( 3 x\right) }-3 {{\% e}^{x}} \cos{\left( 3 x\right) }}{10}+{\mathrm{\% c}}\mbox{}

Note that the solution is implicitly given, which is common in Maxima, we can solve this for ``y`` with,

.. code-block:: console

    solve(sl,y);

which gives,

.. math::
    \left[ y=-\frac{10}{{{\% e}^{x}} \sin{\left( 3 x\right) }-3 {{\% e}^{x}} \cos{\left( 3 x\right) }+10 {\mathrm{\% c}}}\right] \mbox{}
