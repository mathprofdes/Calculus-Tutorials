:index:`Solving Equations`
==========================

In this software package all expressions are solved for 0.  So invoking any of the solving options on an expression on the CAS solves that expression for 0.  The underlying SymPy CAS that we are using can create and solve equations but this just introduces more unnecessary syntax for the user.  So if you need to solve an equation just put all the terms on one side and select the solver you wish to use.  This program offers several different solvers including some advanced ones.

:index:`Solve`
--------------

This is the most general solver that will produce an acceptable answer the majority of the time.  When you select this option a dialog box will appear asking for the variable or variables you wish to solve for.  Input the desired variable or list of variables and click OK.  The output is usually a list of solutions if the program can solve the equation.  If the program cannot find an algebraic solution to the equation it will produce an error.  We will do several examples of this tool.

- Say we have the following in the CAS, ``-x^2 + (x^2 + 3*x + 2)^2 + 1``, that is, :math:`- x^{2} + \left(x^{2} + 3 x + 2\right)^{2} + 1`.  If we select ``Algebra > Solve`` and put in ``x`` as the variable we get

.. math::

    \left[ -1, \  - \frac{5}{3} - \frac{4}{\left(- \frac{3}{2} - \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{3 \sqrt{129} + 35}} - \frac{\left(- \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \sqrt[3]{3 \sqrt{129} + 35}}{3}, \  - \frac{5}{3} - \frac{\left(- \frac{1}{2} + \frac{\sqrt{3} i}{2}\right) \sqrt[3]{3 \sqrt{129} + 35}}{3} - \frac{4}{\left(- \frac{3}{2} + \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{3 \sqrt{129} + 35}}, \  - \frac{5}{3} - \frac{\sqrt[3]{3 \sqrt{129} + 35}}{3} - \frac{4}{3 \sqrt[3]{3 \sqrt{129} + 35}}\right]

That is, the four solutions,

.. math::
    -1

.. math::

    - \frac{5}{3} - \frac{4}{\left(- \frac{3}{2} - \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{3 \sqrt{129} + 35}} - \frac{\left(- \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \sqrt[3]{3 \sqrt{129} + 35}}{3}

.. math::

    - \frac{5}{3} - \frac{\left(- \frac{1}{2} + \frac{\sqrt{3} i}{2}\right) \sqrt[3]{3 \sqrt{129} + 35}}{3} - \frac{4}{\left(- \frac{3}{2} + \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{3 \sqrt{129} + 35}}

.. math::

    - \frac{5}{3} - \frac{\sqrt[3]{3 \sqrt{129} + 35}}{3} - \frac{4}{3 \sqrt[3]{3 \sqrt{129} + 35}}

- Say we have ``x^2 + cos(y)`` in the CAS and we solve it for just ``x`` we get, :math:`\left[ - \sqrt{- \cos{\left(y \right)}}, \  \sqrt{- \cos{\left(y \right)}}\right]`.

- Say we have ``x^2 * cos(y)`` in the CAS and we solve it for ``[x, y]`` (that is both ``x`` and ``y`` together) we get, :math:`\left[ \left( 0, \  y\right), \  \left( x, \  \frac{\pi}{2}\right), \  \left( x, \  \frac{3 \pi}{2}\right)\right]`.  The first ordered pair tells us that if :math:`x = 0` then :math:`y` can be any value.  The second ordered pair tells us that if :math:`y = \pi/2` then :math:`x` can be any value and the third ordered pair tells us that if :math:`y = 3\pi/2` then :math:`x` can be any value.  This is obviously not all of the solutions since the :math:`\cos(y)` has an infinite number of distinct values where it is 0, each of these would produce an ordered pair.

From the above example, it is clear that the Solve option will not always produce a complete set of solutions.  Below we will look at some advanced solvers, the result of solving a nonlinear system on the above equation gives us the following output.

.. math::
    \left\{\left( 0, \  y\right), \left( x, \  \left\{2 \pi n + \frac{\pi}{2}\; \middle|\; n \in \mathbb{Z}\right\}\right), \left( x, \  \left\{2 \pi n + \frac{3 \pi}{2}\; \middle|\; n \in \mathbb{Z}\right\}\right)\right\}

This gives us a complete set of solutions although they are easy to work with.  You can also solve systems of equations, simply put them in a list and select ``Algebra > Solve`` as before.  This will find solutions where all the expressions in the list are 0 at the same time.

- Say we have the following in the CAS, ``[x^2 - cos(y),x^2 + 2*x + 1]``, that is, :math:`\left[ x^{2} - \cos{\left(y \right)}, \  x^{2} + 2 x + 1\right]`, if solve this for both ``x`` and ``y`` we get, :math:`\left[ \left( -1, \  0\right), \  \left( -1, \  2 \pi\right)\right]`.  Again, not a complete set of solutions but enough to work with in most cases.

.. figure:: Images/SolveGraph001.png
    :alt: Non-Linear System Solving Example

    Non-Linear System Solving Example


Again, if we use the advanced solver for nonlinear systems we get the solution set,

.. math::
    \left\{\left( -1, \  \left\{2 \pi n\; \middle|\; n \in \mathbb{Z}\right\}\right)\right\}


.. note::
    Do not try to solve matrices (systems of equations) with this option.  For these you will want either an advanced solver or the system solver in the Matrix menu.

:index:`Advanced Solvers`
-------------------------

The advanced solvers will, in general, produce a more complete solution set, usually in set form as with the examples we did above.  When you select ``Algebra >> Advanced Solvers`` a dialog box will appear that will allow you to select the variable or variables you wish to solve for, the solving method, and any assumptions you wish to place on the variables in the expression.  If the program can detect the type of equation, or system, that is to be solved it will gray out any solver that is not valid for that equation or system.

.. figure:: Images/AdvSolve001.png
    :alt: Advanced Solvers Dialog Box

    Advanced Solvers Dialog Box

General Solve
^^^^^^^^^^^^^

This is just the same solver that is used in the Solve option.  The difference here is that you can set the domains of the variables.

For example, say we have ``sin(cos(x))`` in the CAS.  If we select ``Algebra > Solve`` and solve this for ``x`` we get,

.. math::

    \left[ \frac{\pi}{2}, \  \frac{3 \pi}{2}, \  2 \pi - \operatorname{acos}{\left(\pi \right)}, \  \operatorname{acos}{\left(\pi \right)}\right]

Looking at the graph, or simply realizing that this is clearly a periodic function, it is clear that we did not get all the solutions.

.. figure:: Images/SolveGraph002.png
    :alt: y = sin(cos(x))

    :math:`y = \sin(\cos(x))`

A closer look should reveal another thing, the third and fourth solutions both contain :math:`\operatorname{acos}(\pi)`, but since :math:`\cos(x)` has range :math:`[-1,1]` these solutions cannot be real.  Approximating the solutions gives us,

.. math::

    \left[ 1.5707963267949, \  4.71238898038469, \  6.28318530717959 - 1.81152627246085 i, \  1.81152627246085 i\right]

which verifies that these solutions are not real numbers.  Of course we can simply ignore the unreal solutions if we know we want real solutions but we could also use the General Solve in the advanced solvers and change ``x`` to be real in the variable assumptions area at the bottom of the dialog.  If we do that our result is,

.. math::

    \left[ \frac{\pi}{2}, \  \frac{3 \pi}{2}\right]

Again not a complete set of solutions but the unreal solutions were removed.

Single Equation Solve with Set Output, Real Domain
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This solver will solve a single equation for a single variable and assume that all variables are real, overriding the variable assumptions at the bottom.

For example, say we want to solve :math:`\sin(2x)` for ``x``.  Select the Single Equation Solve with Set Output, Real Domain solver and click OK. The result is,

.. math::

    \left\{\pi n\; \middle|\; n \in \mathbb{Z}\right\} \cup \left\{\pi n + \frac{\pi}{2}\; \middle|\; n \in \mathbb{Z}\right\}

Which is the entire set of solutions.

Another example, this shows that the advanced solvers may not always produce better answers.  Say we apply this solver to :math:`\sin(\cos(x))`.  The result is,

.. math::

    \left\{x\; \middle|\; x \in \mathbb{R} \wedge \sin{\left(\cos{\left(x \right)} \right)} = 0 \right\}

Which is not very enlightening.

Single Equation Solve with Set Output, Complex Domain
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This solver will solve a single equation for a single variable and assume that all variables are complex, overriding the variable assumptions at the bottom.

For example, if we wanted to solve ``x^4 + 6*x^3 + 12*x^2 + 12*x + 5``, that is, :math:`x^{4} + 6 x^{3} + 12 x^{2} + 12 x + 5`.  The solutions using the real domain would just be,

.. math::
    \left\{-1, - \frac{5}{3} - \frac{\sqrt[3]{3 \sqrt{129} + 35}}{3} - \frac{4}{3 \sqrt[3]{3 \sqrt{129} + 35}}\right\}

but using the complex domain gives us all four solutions,

.. math::

    \left\{-1, - \frac{5}{3} - \frac{\sqrt[3]{3 \sqrt{129} + 35}}{3} - \frac{4}{3 \sqrt[3]{3 \sqrt{129} + 35}}, - \frac{5}{3} + \frac{2}{3 \sqrt[3]{3 \sqrt{129} + 35}} + \frac{\sqrt[3]{3 \sqrt{129} + 35}}{6} + i \left(- \frac{2 \sqrt{3}}{3 \sqrt[3]{3 \sqrt{129} + 35}} + \frac{\sqrt{3} \sqrt[3]{3 \sqrt{129} + 35}}{6}\right), - \frac{5}{3} + \frac{2}{3 \sqrt[3]{3 \sqrt{129} + 35}} + \frac{\sqrt[3]{3 \sqrt{129} + 35}}{6} + i \left(- \frac{\sqrt{3} \sqrt[3]{3 \sqrt{129} + 35}}{6} + \frac{2 \sqrt{3}}{3 \sqrt[3]{3 \sqrt{129} + 35}}\right)\right\}

Linear System Solver
^^^^^^^^^^^^^^^^^^^^

This solver is for the solving of linear systems of equations.  The system can be input either as a list or an augmented matrix.  The output will be in general solution vector form or sometimes as a set.

For example, if we input the following matrix,

.. math::
    \left[\begin{array}{cccc}3 & -1 & -9 & -9\\-5 & 10 & -8 & 8\\-3 & 0 & 10 & 5\end{array}\right]

and apply this solver to the matrix we get the following result,

.. math::
    \left[\begin{array}{c}\frac{15}{2}\\\frac{27}{4}\\\frac{11}{4}\end{array}\right]

We can also input the system as a list of linear equations as long as they are manipulated to be equations to 0.  For example, the system,

.. math::
    -4x + 5y + -5z &= 10 \\
    -10x + 10y + -9z &= 9 \\
    -6x + 7y + -z &= -1 \\

could be input as, ``[-4*x + 5*y - 5*z - 10, -10*x + 10*y - 9*z - 9, -6*x + 7*y - z + 1]``

.. math::
    \left[ - 4 x + 5 y - 5 z - 10, \  - 10 x + 10 y - 9 z - 9, \  - 6 x + 7 y - z + 1\right]

Applying this solver gives us the solution,

.. math::
    \left[\begin{array}{c}\frac{255}{58}\\\frac{96}{29}\\- \frac{64}{29}\end{array}\right]

This solver can handle systems with an infinite number of solutions as well, say we have the following matrix in the CAS,

.. math::
    \left[\begin{array}{cccccc}8 & 2 & 6 & 1 & -3 & -9\\2 & 2 & -1 & -6 & 2 & -3\\-9 & -5 & 1 & -2 & -9 & -5\end{array}\right]

This solver returns the solution,

.. math::
    \left[\begin{array}{c}- \frac{217 x_{4}}{38} - \frac{71 x_{5}}{38} + \frac{193}{38}\\\frac{405 x_{4}}{38} + \frac{77 x_{5}}{38} - \frac{349}{38}\\\frac{74 x_{4}}{19} + \frac{44 x_{5}}{19} - \frac{99}{19}\\x_{4}\\x_{5}\end{array}\right]

Nonlinear System Solver
^^^^^^^^^^^^^^^^^^^^^^^

This solver is for the solving of nonlinear systems of equations.  In this case the system should be input as a list of equations.

For example, say we input ``[x^2 - cos(y),x^2 + 2*x + 1]``, that is, :math:`\left[ x^{2} - \cos{\left(y \right)}, \  x^{2} + 2 x + 1\right]`.  The nonlinear solver will produce,

.. math::

    \left\{\left( -1, \  \left\{2 \pi n\; \middle|\; n \in \mathbb{Z}\right\}\right)\right\}


:index:`Numeric Solution Close to x = a`
----------------------------------------

In many cases finding exact solutions to equations is very difficult, and possibly impossible.  In these cases we can still obtain numeric solutions and hence put some meaning to the solution of the expression we are working with. One tool is to find a solution close to an initial guess to the solution.  This tool is for solving single expressions in a single variable.

For example, say we wanted to find the roots of the expression :math:`x + \cos{\left(x \right)}`.  If we try to solve this algebraically with the tools mentioned above we either get an error or a result that does not mean anything.  If we graph the function we get the following,

.. figure:: Images/SolveGraph003.png
    :alt: y = x + cos(x)

    :math:`y = x + \cos(x)`

There appears to be a solution close to :math:`-1`.  If we select ``Algebra > Numeric Solution Close to x = a``, let the variable be ``x`` and input an initial guess of ``-1`` and the result is ``-0.739085133215161``.

It is possible that this method will not return a solution or that the solution it does return id not the closest one to the initial guess.  For example, put in the :math:`\sin(x)` and try this with an initial guess of :math:`\pi/2` and we get ``9.42477796076938``, that is, :math:`3\pi`, not 0 or :math:`\pi`, the closest solutions.


:index:`Numeric Solutions in [a, b]`
------------------------------------

This option allows the user to approximate all the solutions in a given interval. Like the previous tool, this option is for solving a single expression in a single variable.

For example, say we want the roots to :math:`\sin(x^2)`.  The solve tool gives us the result :math:`\left[ 0, \  - \sqrt{\pi}, \  \sqrt{\pi}\right]`, which is a good start, these are the three solutions closest to the origin.

.. figure:: Images/SolveGraph004.png
    :alt: y = sin(x^2)

    :math:`y = \sin(x^2)`

There are, of course, an infinite number of solutions to this expression.  The next three positive solutions appear to be between 2.25 and 3.75.  If we select this option a dialog box will appear asking for lower and upper bounds for the interval (we will use 2.25 and 3.75), the number of test points (we will keep this at 100), and the tolerance exponent (we will keep that at 8).  When we click OK we get,

.. math::

    \left[ 2.506628274631, \  3.06998012383947, \  3.54490770181103\right]

These are the approximations to the three solutions we wanted.  What the program did was it divided the given interval :math:`[2.25, 3.75]` into 100 evenly spaced test points, it then applied the above method of finding a solution close to each of these test points (obtaining 100 solutions).  It then removed duplicate solutions that were within the tolerance leaving the three solutions above.

Note that it is possible that this method will return solutions that are close to each other but are further away than the tolerance amount.  This is common when the curve osculates the x-axis.

:index:`Polynomial Roots`
-------------------------

This tool is for finding exact roots to a polynomial expression.  If you try to apply this to an expression that is not a polynomial you will get an error.  Note that the polynomial does not need to be in simplified or expanded form.

For example, if we applied this tool to either

.. math::

    - x^{2} + \left(x^{2} + 3 x + 2\right)^{2} + 1

or

.. math::

    x^{4} + 6 x^{3} + 12 x^{2} + 12 x + 5

which is just the expanded form of the first expression, we get

.. math::

    \left[ -1, \  - \frac{5}{3} - \frac{\sqrt[3]{3 \sqrt{129} + 35}}{3} - \frac{4}{3 \sqrt[3]{3 \sqrt{129} + 35}}, \  - \frac{5}{3} - \frac{\left(- \frac{1}{2} + \frac{\sqrt{3} i}{2}\right) \sqrt[3]{3 \sqrt{129} + 35}}{3} - \frac{4}{\left(- \frac{3}{2} + \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{3 \sqrt{129} + 35}}, \  - \frac{5}{3} - \frac{4}{\left(- \frac{3}{2} - \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{3 \sqrt{129} + 35}} - \frac{\left(- \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \sqrt[3]{3 \sqrt{129} + 35}}{3}\right]

:index:`Polynomial Root Approximations`
---------------------------------------

This tool is for finding approximations to the roots to a polynomial expression.  If you try to apply this to an expression that is not a polynomial you will get an error.  Note that the polynomial does not need to be in simplified or expanded form.

For example, if we applied this tool to either

.. math::

    - x^{2} + \left(x^{2} + 3 x + 2\right)^{2} + 1

or

.. math::

    x^{4} + 6 x^{3} + 12 x^{2} + 12 x + 5

which is just the expanded form of the first expression, we get

.. math::

    \left[ -3.35930408597178, \  -1.0, \  -0.820347957014112 - 0.903013145857004 i, \  -0.820347957014112 + 0.903013145857004 i\right]

You may have studied at one point that you can find the exact solutions to a quadratic equation (degree 2) using the quadratic formula.  You may have also studied that there are similar, but more difficult, equations to get the exact solutions to degree 3 and degree 4 equations.  Specifically, the solutions to :math:`a x^{3} + b x^{2} + c x + d = 0` are,

.. math::

    \frac{\frac{3 c}{a} - \frac{b^{2}}{a^{2}}}{3 \sqrt[3]{\frac{\sqrt{- 4 \left(- \frac{3 c}{a} + \frac{b^{2}}{a^{2}}\right)^{3} + \left(\frac{27 d}{a} - \frac{9 b c}{a^{2}} + \frac{2 b^{3}}{a^{3}}\right)^{2}}}{2} + \frac{27 d}{2 a} - \frac{9 b c}{2 a^{2}} + \frac{b^{3}}{a^{3}}}} - \frac{\sqrt[3]{\frac{\sqrt{- 4 \left(- \frac{3 c}{a} + \frac{b^{2}}{a^{2}}\right)^{3} + \left(\frac{27 d}{a} - \frac{9 b c}{a^{2}} + \frac{2 b^{3}}{a^{3}}\right)^{2}}}{2} + \frac{27 d}{2 a} - \frac{9 b c}{2 a^{2}} + \frac{b^{3}}{a^{3}}}}{3} - \frac{b}{3 a}

.. math::

    \frac{\frac{3 c}{a} - \frac{b^{2}}{a^{2}}}{\left(- \frac{3}{2} - \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{\frac{\sqrt{- 4 \left(- \frac{3 c}{a} + \frac{b^{2}}{a^{2}}\right)^{3} + \left(\frac{27 d}{a} - \frac{9 b c}{a^{2}} + \frac{2 b^{3}}{a^{3}}\right)^{2}}}{2} + \frac{27 d}{2 a} - \frac{9 b c}{2 a^{2}} + \frac{b^{3}}{a^{3}}}} - \frac{\left(- \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \sqrt[3]{\frac{\sqrt{- 4 \left(- \frac{3 c}{a} + \frac{b^{2}}{a^{2}}\right)^{3} + \left(\frac{27 d}{a} - \frac{9 b c}{a^{2}} + \frac{2 b^{3}}{a^{3}}\right)^{2}}}{2} + \frac{27 d}{2 a} - \frac{9 b c}{2 a^{2}} + \frac{b^{3}}{a^{3}}}}{3} - \frac{b}{3 a}

.. math::

    \frac{\frac{3 c}{a} - \frac{b^{2}}{a^{2}}}{\left(- \frac{3}{2} + \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{\frac{\sqrt{- 4 \left(- \frac{3 c}{a} + \frac{b^{2}}{a^{2}}\right)^{3} + \left(\frac{27 d}{a} - \frac{9 b c}{a^{2}} + \frac{2 b^{3}}{a^{3}}\right)^{2}}}{2} + \frac{27 d}{2 a} - \frac{9 b c}{2 a^{2}} + \frac{b^{3}}{a^{3}}}} - \frac{\left(- \frac{1}{2} + \frac{\sqrt{3} i}{2}\right) \sqrt[3]{\frac{\sqrt{- 4 \left(- \frac{3 c}{a} + \frac{b^{2}}{a^{2}}\right)^{3} + \left(\frac{27 d}{a} - \frac{9 b c}{a^{2}} + \frac{2 b^{3}}{a^{3}}\right)^{2}}}{2} + \frac{27 d}{2 a} - \frac{9 b c}{2 a^{2}} + \frac{b^{3}}{a^{3}}}}{3} - \frac{b}{3 a}

We will forgo the solutions to the degree 4 equations. If you studied polynomial solutions a little further you know that for degree 5 and above there are no general solution equations.  Not just that they have not been discovered yet they do not exist.  So for higher degree polynomials we might get lucky and get exact solutions or we may not.

For example, input the polynomial ``x^5 - 7*x^4 + x^3 - 5*x^2 - x + 3``, that is, :math:`x^{5} - 7 x^{4} + x^{3} - 5 x^{2} - x + 3`.  If we apply the Polynomial Roots tool we get ``[]`` in other words it could not solve the equation exactly.  If we apply the Polynomial Root Approximations tool we get the solutions,

.. math::

    \left[ -0.643227867249394, \  0.598810703479406, \  6.96121485557466, \  0.0416011540976639 - 1.05695078535511 i, \  0.0416011540976639 + 1.05695078535511 i\right]

The advantage to using this as opposed to finding solutions close to a value or in an interval is that with this tool you can get approximations to the unreal roots.

Variable Assumptions
--------------------

.. include:: ../CLAE/VariableAssumptions.md

