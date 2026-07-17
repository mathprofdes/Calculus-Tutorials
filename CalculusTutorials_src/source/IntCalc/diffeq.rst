:index:`Differential Equations`
===============================

Discussion & Definitions
------------------------

Differential Equations and Verifying Solutions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A **differential equation** is simply an equation that has derivatives in it, for example, :math:`xy' = \sin(x)+y` or  :math:`y'' -3y'= x^3y-7x+3`.  Solving a differential equation means finding a function :math:`y = f(x)` so that when the function is substituted into the equation we have both sides equal to each other.

For example, say we have the following differential equation,

.. math::
    - f{\left(x \right)} + \frac{d}{d x} f{\left(x \right)} = x^{2} - 3

One solution to this equation is :math:`f(x) = e^{x} - x^{2} - 2 x + 1`, to verify this we simply put the function into the equation, take the derivatives and simplify to see if we get a true statement, and here we do.

.. math::
    x^{2} + 2 x - e^{x} + \frac{d}{d x} \left(- x^{2} - 2 x + e^{x} + 1\right) - 1 = x^{2} - 3

Along the same lines we can also verify if a function is not a solution by the same method. For example :math:`x^{2}` is not a solution since,

.. math::
    - x^{2} + \frac{d}{d x} x^{2} = - x^{2} + 2 x \neq x^{2} - 3

There are many ways to solve a differential equation, some methods with produce an exact solution and others a numerical or graphical solution.  A detailed discussion of solving methods is best for a course in differential equations but we will look at some of them here.

The **order** of a differential equation is the highest order of any of the derivatives in the equation.  For example, :math:`xy' = \sin(x)+y` has order 1 and :math:`y'' -3y'= x^3y-7x+3` has order 2.  Usually, in an integral Calculus class we study first order equations.

General and Particular Solutions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In our above differential equation

.. math::
    - f{\left(x \right)} + \frac{d}{d x} f{\left(x \right)} = x^{2} - 3

we looked at the solution :math:`f(x) = e^{x} - x^{2} - 2 x + 1`.  Another solution to this equation is :math:`f(x) = 7e^{x} - x^{2} - 2 x + 1`, and another is :math:`f(x) = -4e^{x} - x^{2} - 2 x + 1`.  In general, any function of the form :math:`f(x) = c e^{x} - x^{2} - 2 x + 1`, where :math:`c` is any real number is a solution to this differential equation.  This is called the **general solution** to the differential equation and represents an entire family fol solutions.

.. figure:: Images/DE/DEDef001.png
    :alt: Family of Solutions to the Differential Equation

    Family of Solutions to the Differential Equation

The solution :math:`f(x) = e^{x} - x^{2} - 2 x + 1` is one particular member of that family and is called a particular solution to the differential equation.  In some cases, such as with initial-value problems below, if we have a little more information (such as a particular point on the graph) we can find a particular solution from the general solution.

Initial-Value Problems
^^^^^^^^^^^^^^^^^^^^^^

Usually a given differential equation has an infinite number of solutions.  If we have some more information about a particular curve or the physical situation we can find a particular solution that satisfies the conditions.  In many cases this is a point on the curve :math:`(a, b)` which tells us that :math:`f(a) = b` and would give us an equation that we might be able to solve for the general constants in the general solution.  This point or the equation :math:`f(a) = b` is called an **initial value**. A differential equation together with one or more initial values is called an **initial-value problem**. The general rule is that the number of initial values needed for an initial-value problem is equal to the order of the differential equation. For example, :math:`xy' = \sin(x)+y` would require one initial value and  :math:`y'' -3y'= x^3y-7x+3` would require two.

For example, solve the initial value problem :math:`y' = 3e^x+x^2-4` with the initial value :math:`y(0) = 5`, that is the point :math:`(0, 5)` is on the curve.

This is a fairly nice differential equation since we can take the integral of both sides,

.. math::
    y' & = 3e^x+x^2-4 \\
    \int y' \; dx & = \int 3e^x+x^2-4 ; dx \\
    y + C_1 & = 3e^x+\frac{x^3}{3}-4x + C_2 \\
    y & = 3e^x+\frac{x^3}{3}-4x + C_2 - C_1  \\
    y & = 3e^x+\frac{x^3}{3}-4x + C  \\

Now using our initial value information that :math:`y(0) = 5`,

.. math::
    5 = 3e^0+\frac{0^3}{3}-4 \cdot 0 + C = 3 + C  \\

So :math:`C = 2` and our particular solution is :math:`y = 3e^x+\frac{x^3}{3}-4x + 2`.


Example: Verifying a Solution to a Differential Equation
--------------------------------------------------------

In this example we will verify that :math:`f(x) = e^{x} - x^{2} - 2 x + 1` and the general solution :math:`f(x) = ce^{x} - x^{2} - 2 x + 1` are solutions to the differential equation,

.. math::
    - f{\left(x \right)} + \frac{d}{d x} f{\left(x \right)} = x^{2} - 3

GeoGebra
^^^^^^^^

Input the solution function,

.. code-block:: console

    e^x - x^2 - 2 x + 1

Assuming this came in as ``f(x)`` we can input the derivative portion into a new cell,

.. code-block:: console

    f'-f

you may need to simplify this with,

.. code-block:: console

    Simplify(g)

but the result should be the right hand side of our equation.

We can do the same process with

.. code-block:: console

    c e^x - x^2 - 2 x + 1

the only difference is that ``c`` will be replaced with a slider.  The rest of the steps are the same and you can move the slider around to see that the final simplification remains the same.

CLAE
^^^^

Input the solution function,

.. code-block:: console

    E^x - x^2 - 2*x + 1

Assume this came in as ``R1``. Now input the differential equation, as with all equations in CLAE we need to make this an equation equal to 0.  So the equation we want is,

.. math::
    - x^{2} - f{\left(x \right)} + \frac{d}{d x} f{\left(x \right)} + 3

In CLAE (really SymPy) y is considered a variable so we need to use the notation of ``f(x)`` (or ``g(x)``, ``h(x)``, ``g(t)``, etc) for it to realize that we are dealing with an unknown function.  Also, CLAE does not recognize the prime notation since it was built to also handle multivariable expressions and partial derivatives.  So the derivative notation is a little lengthy.  The notation ``f(x).diff(x)`` would represent :math:`f'(x)`.  Similarly, we can do higher order derivatives, ``f(x).diff(x, 2)`` would represent :math:`f''(x)`, ``f(x).diff(x, 3)`` would represent :math:`f'''(x)`, ``f(x).diff(x, 7)`` would represent :math:`f^{(7)}(x)`, and so on. So our differential equation would be,

.. code-block:: console

    -x^2 - f(x) + f(x).diff(x) +3

Assume this came in as ``R2``.  To verify the solution select ``R2``, then select ``Algebra > Evaluate``, for the variable input ``f(x)`` and for the expression input ``R1``, the result will be,

.. math::
    2 x - e^{x} + \frac{d}{d x} \left(- x^{2} - 2 x + e^{x} + 1\right) + 2

Now select ``Algebra > Simplify`` to simplify the above expression and the result is 0, verifying the solution.

To verify the general solution input the expression,

.. code-block:: console

    c*E^x - x^2 - 2*x + 1

Assume this came in as ``R5``.  To verify the solution select ``R2`` (the differential equation), then select ``Algebra > Evaluate``, for the variable input ``f(x)`` and for the expression input ``R5``, the result will be,

.. math::
    - c e^{x} + 2 x + \frac{\partial}{\partial x} \left(c e^{x} - x^{2} - 2 x + 1\right) + 2

Now select ``Algebra > Simplify`` to simplify the above expression and the result is 0, verifying the solution.

.. note::

    Sometimes when using the simplify option to verify a differential equation the simplify might not return 0 immediately.  In some cases you need to simplify twice.  If you do simplify several times then it is possible that the simplify is not seeing a relationship it cn exploit or the intended solution is not a solution.  In these cases you can sometimes take a graphical approach and graph the simplified result, if the graph is the *x*-axis then you probably do have a viable solution.

    There is also an ODE solution checker in CLAE that s a little more powerful and easier to use for checking solutions to differential equations.  This option is discussed in the solving ODE section below and the user's guide for CLAE.

Maxima
^^^^^^

Input the solution function,

.. code-block:: console

    kill(all);
    f(x):=%e^x - x^2 - 2*x + 1

.. code-block:: console

    diff(f(x),x)-f(x);

The result should be the right hand side.  The same will work for the general solution,

.. code-block:: console

    f(x):=c*%e^x - x^2 - 2*x + 1

Note that we could also define the differential equation as a function,

.. code-block:: console

    de(fct):=diff(fct,x)-fct;

Then to verify the solution we could simply input,

.. code-block:: console

    de(f(x));


Example: Initial-Value Problem
------------------------------

We will solve the initial-value problem we looked at above.  Solve the initial value problem :math:`y' = 3e^x+x^2-4` with the initial value :math:`y(0) = 5`, that is the point :math:`(0, 5)` is on the curve.

GeoGebra
^^^^^^^^

Input the right hand side of the differential equation,

.. code-block:: console

    3e^x+x^2-4

Assume this came in as ``f(x)``.  We could integrate this but GeoGebra would not return the integral with the constant of integration ``c``, it makes ``c`` a slider, so we cannot solve for ``c``.  On the other hand, GeoGebra has functions for solving differential equations of the form :math:`y' = f(x, y)`, which this one is.

In a new cell input,

.. code-block:: console

    SolveODE(f, (0, 5))

This will solve the differential equation :math:`y' = 3e^x+x^2-4` and find the particular solution that passes through the point :math:`(0, 5)`.  In other words, our initial value problem.  The result is,

.. math::
    y = 3e^x+\frac{x^3}{3}-4x + 2

CLAE
^^^^

Input the right hand side of the differential equation,

.. code-block:: console

    3*E^x+x^2-4

Assume this came in as ``R1``.  Now select ``Calculus > Indefinite Integral``, variable *x*, and include the constant.  The result is,

.. math::
    C_{1} + \frac{x^{3}}{3} - 4 x + 3 e^{x}

With this selected we evaluate it at :math:`x = 0`.  Select ``Algebra > Evaluate``, variable *x* and expression 0.  The result is, :math:`C_{1} + 3`.

We hardly need the CAS to solve this equal to 5 but just for practice when we get something more difficult.  Assume the last expression came in as ``R4``, input ``R4 - 5`` and then do ``Algebra > Solve`` on the result, variable now is ``C1``, this returns our expected 2.

Maxima
^^^^^^

Input the right hand side of the differential equation,

.. code-block:: console

    kill(all);
    f(x):=3*%e^x+x^2-4

Integrate with,

.. code-block:: console

    intf:integrate(f(x),x);

This will return the indefinite integral without a constant, to add the constant and turn this into a function do the following,

.. code-block:: console

    intfc(x):=''(intf+c);

Now solve the initial value problem with,

.. code-block:: console

    solve(intfc(0)=5,c);

Which gives the result of :math:`c  = 2`.

Example: Solving Differential Equations
---------------------------------------

As noted above, the techniques involved in finding solutions to differential equations are best left to a course in differential equations. Below are some examples in using our technologies to solve differential equations.  Not every differential equation is solvable exactly, just like not every integral has an elementary solution.  We will concentrate here on exact solutions to differential equations.  Some numeric and graphical solutions will be discussed in the subsequent sections.

GeoGebra
^^^^^^^^

GeoGebra has functions for solving differential equations and initial-value problems of the form :math:`y' = f(x, y)`.  Higher-order differential equations and those involving more difficult expressions need other computer algebra systems.  The function for these is ``SolveODE``, which comes in several forms.

- ``SolveODE(f(x, y))`` solves a differential equation exactly and returns the general solution with constants implemented as sliders.
- ``SolveODE(f(x, y), (a, b))`` solves the initial-value problem :math:`y' = f(x, y)` and :math:`y(a) = b`.  Note that the point :math:`(a, b)` can be a geometric point that is on the plot.

For example, let's solve the differential equation, :math:`y' = 2 x y \left(2 y + 1\right)`.  Input the right hand side,

.. code-block:: console

    2 x y (2 y + 1)

Assuming this came in as ``a(x, y)`` in a new cell input

.. code-block:: console

    SolveODE(a)

and it returns the result along with a slider for the constant.  If we check this by, assuming that the solution equation is ``g``,

.. code-block:: console

    g' - a(x,g)

we see that the expression is not 0 as expected but if we look over to the graph the plot is the *x*-axis, telling us that the solution does check but the expression did not simplify to 0.  If we further did the command ``Simplify(h)`` (assuming the last expression was *h*) it does return 0.


CLAE
^^^^

Input the differential equation,

.. code-block:: console

    2*x*f(x)*(2*f(x) + 1) - f(x).diff(x)

Then select this and then select ``Calculus > Solve ODE``, the function should automatically load as ``f(x)``, if not input it, then hit OK.  The result is,

.. math::
    f{\left(x \right)} = \frac{e^{C_{1} + x^{2}}}{2 - 2 e^{C_{1} + x^{2}}}

Note that it returns the result as an equation.  If we assume that the differential equation came in as ``R1`` and the above solution was ``R2``, to check the solution, select ``R1`` and in the expression input of the checking dialog box input ``R2`` the result is, :math:`\left( \text{True}, \  0\right)`.  The first entry is true or false, true meaning that the solution checks and if it were false that would have meant that the solution did not check.  The second entry in the tuple is the result of the expression after the function has been substituted into the differential equation and simplified.

We could have also just input the expression on the right hand side of the solution equation.  If we select the solution equation then select ``Algebra > Equations > Right Hand Side`` it will extract the right hand side expression, assume it came in as ``R4``.  If we select the differential equation and then ``Calculus > Check ODE Solution``, and then input ``R4`` into the expression input we get the same result.

You do not need to use a CAS result in this option, you can also simply input the expression.  For example,  if we gave the same differential equation to GeoGebra the result would be,

.. math::
    \frac{e^{x^{2}}}{C_{1} - 2 e^{x^{2}}}

If we wished to check this solution we could select the differential equation and then select ``Calculus > Check ODE Solution``, and then input ``exp(x^2)/(C1 - 2*exp(x^2))``, we get the same result :math:`\left( \text{True}, \  0\right)`.


.. note::

    Several notes about the ODE solution checker.

    - First, it may return false even if the solution is a solution to the ODE, it depends if the simplification is powerful enough to return exactly 0 for the check.  In these cases you can also check the solution graphically.  Extract the second expression using options from the Edit manu, and graph it, if it is equivalently 0, that is, graphs as the *x*-axis then the expression should have reduced to 0 and returned true.

    - We could have checked the solution using the evaluation option from the Algebra menu.  Select the differential equation, then select ``Algebra > Evaluate``, input the function ``f(x)`` and the expression for the solution.  Note here we cannot use the equation.  We can still use CAS results.  Then select ``Algebra > Simplify`` to simplify the expression.  You may need to simplify the expression several times.  If the result is 0 then the solution checks.  As with the checker it is possible that the solution is valid but the simplification does not return 0 bt an expression that is equivalently 0.  The above example is a good example of this.  If we use the evaluation if the Algebra menu for this equation and solution we get,

    .. math::
        \frac{2 x \left(1 + \frac{2 e^{C_{1} + x^{2}}}{2 - 2 e^{C_{1} + x^{2}}}\right) e^{C_{1} + x^{2}}}{2 - 2 e^{C_{1} + x^{2}}} - \frac{\partial}{\partial x} \frac{e^{C_{1} + x^{2}}}{2 - 2 e^{C_{1} + x^{2}}}

    which simplifies to

    .. math::
        \frac{x}{4 \sinh^{2}{\left(\frac{C_{1}}{2} + \frac{x^{2}}{2} \right)}} + \frac{x e^{C_{1} + x^{2}}}{e^{C_{1} + x^{2}} - 1} - \frac{x e^{2 C_{1} + 2 x^{2}}}{\left(e^{C_{1} + x^{2}} - 1\right)^{2}}

    and then

    .. math::
        - \frac{x \left(4 e^{C_{1} + x^{2}} \sinh^{2}{\left(\frac{C_{1}}{2} + \frac{x^{2}}{2} \right)} + 2 e^{C_{1} + x^{2}} - e^{2 C_{1} + 2 x^{2}} - 1\right)}{\left(2 \cosh{\left(C_{1} + x^{2} \right)} - 2\right) \left(- 2 e^{C_{1} + x^{2}} + e^{2 C_{1} + 2 x^{2}} + 1\right)}

    if we graph this we get,

    .. figure:: Images/DE/DE003.png
        :alt: Graphical Verification of the Solution to the Differential Equation

        Graphical Verification of the Solution to the Differential Equation

    Which appears to be equivalently 0 (for any value of :math:`C_1`) so we would graphically conclude that we have a solution.

    Clearly the algebraic methods in the solution checker are stronger than those of the simplify methods.

Maxima
^^^^^^

Maxima has an ODE solver command, in fact several.  The downside is that the result may be returned implicitly.  If we use the above example, input the differential equation,

.. code-block:: console

    kill(all);
    de:2*x*(2*y + 1)*y - 'diff(y, x)

Note the single quote before the diff command.  If we forget it the program will evaluate the derivative of *y* with respect to *x* and get 0. Then we can find the solution with,

.. code-block:: console

    sl:ode2(de,y,x)

The result is

.. math::
    -\frac{\log{\left( 2 y+1\right) }-\log{(y)}}{2}=\frac{{{x}^{2}}}{2}+{\mathrm{\% c}}\mbox{}

Note that the solution is implicit.  In some cases the solve command will produce an explicit expression but here we still get an implicit result.
