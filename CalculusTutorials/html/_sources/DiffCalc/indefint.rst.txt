:index:`Antiderivatives and The Indefinite Integral`
====================================================

Discussion & Definitions
------------------------

We have seen that derivatives have numerous applications.  One of the first was velocity and acceleration.  We know that if we have a function :math:`s(t)` that represents the position of an object over time then the velocity is :math:`v(t) = s'(t)`.  Furthermore, the acceleration of the object is :math:`a(t) = v'(t) = s''(t)`.  Let's turn this around a little.  What if we had a function that represented velocity :math:`v(t)`, such as a monitor that recorded your car's speedometer as you were driving, can we find a function :math:`s(t)` that represents the position of the object?  If we can we would have to have a process that undoes the derivative in some way and apply that process to the velocity function.  We would need to develop a process that takes a rate of change and produces a total change.

As you would guess, of course there is a process to undo the derivative, this is the main topic in integral calculus but also has applications in differential calculus.  The process is called antidifferentiation or integration.

Antiderivatives
^^^^^^^^^^^^^^^

Basically we call a function :math:`F` an antiderivative of a function :math:`f` if :math:`F'(x) = f(x)`.

.. admonition:: Definition: Antiderivative

    A function :math:`F` is an antiderivative of the function :math:`f` if

    .. math::
        F'(x) = f(x)

    for all :math:`x` in the domain of :math:`f.`

**Example:** As an easy example, we know that :math:`\frac{d}{dx}\left( x^2 \right) = 2x`. Turning this around into the language of antiderivatives, an antiderivative of :math:`2x` is :math:`x^2`.  Notice that we are saying *an* antiderivative and not *the* antiderivative.  Note that :math:`x^2 + 1` is also an antiderivative of :math:`2x`, so is :math:`x^2 + 7`, :math:`x^2 -1234.5678`, :math:`x^2 + \frac{23}{47}` , and :math:`x^2 + \pi.`  In general, :math:`x^2 + C` is an antiderivative of :math:`2x` where *C* is any constant.

The above example should not be any surprise since we had a corollary to the Mean Value Theorem that stated just this.  Recall,

.. admonition:: Corollary: Constant Difference Theorem

    If :math:`f` and :math:`g` are differentiable over an interval :math:`I` and :math:`f'(x) = g'(x)` for all :math:`x \in I`, then :math:`f(x) = g(x) + C` for some constant :math:`C`.

In our language of antiderivatives, this corollary is saying that any two antiderivatives of the same function differ by a constant.  With this observation we can formalize the general form of an antiderivative.

.. admonition:: Theorem: General Form of an Antiderivative

    Let :math:`F` be an antiderivative of :math:`f` over an interval :math:`I`. Then,

    i. For each constant :math:`C,` the function :math:`F(x) + C` is also an antiderivative of :math:`f` over :math:`I`.
    ii. If :math:`G` is an antiderivative of :math:`f` over :math:`I`, there is a constant :math:`C` for which :math:`G(x) = F(x) + C` over :math:`I`.

In other words, the most general form of the antiderivative of :math:`f` over :math:`I` is :math:`F(x) + C.`


The Indefinite Integral
^^^^^^^^^^^^^^^^^^^^^^^

As you would expect this undoing process is very important and has as many applications as does differentiation and we do not want to keep writing "is an antiderivative of ..." each time so we will adopt some notation and another name for the general antiderivative.

.. admonition:: Definition: Indefinite Integral

    Given a function :math:`f`, the indefinite integral of :math:`f`, denoted

    .. math::
        \int f(x) \; dx

    is the most general antiderivative of :math:`f`. If :math:`F` is an antiderivative of :math:`f`, then

    .. math::
        \int f(x) \; dx = F(x) + C

    The expression :math:`f(x)` is called the integrand and the variable :math:`x` is the *variable of integration*.

A couple things to notice about the indefinite integral (and hence the general antiderivative) is that the result is an infinite family of functions (and hence curves).  Taking the example above,

.. math::
    \int 2x \; dx = x^2 + C

A few members if the family of solutions are picture below.  For all of them you need to consider every real number *C*.

.. figure:: Images/Apps/IndefInt001.png
    :alt: Family of Antiderivatives

    Family of Antiderivatives

The Integral Formulas
^^^^^^^^^^^^^^^^^^^^^

So if we are to do this process by hand, or by computer, we need to know some formulas for integration just like we developed for differentiation.  The nifty part is that every differentiation formal produces a corresponding integration formula, just by interchanging the roles of the expressions.  We will cover the basics formulas here and the more advanced techniques of undoing a product rule or a chain rules will be the topic of the techniques of integration section in the Integral Calculus part of these tutorials.


Basic Rules
"""""""""""

.. math::
    \begin{array}{l|l}
    {\rm\bf Derivative \; Formula} & {\rm\bf Integral \; Formula} \\ \hline
    \displaystyle \frac{d}{dx} \left(c \right) = 0 & \displaystyle \int k \; dx = kx + C \\
    \displaystyle \frac{d}{dx} \left(x^n \right) = n x^{n-1} & \displaystyle \int x^n \; dx = \frac{x^{n+1}}{n+1} + C {\;\; \rm for \;\;} n \neq -1\\
    \end{array}

Exponential & Logarithmic Rules
"""""""""""""""""""""""""""""""

.. math::
    \begin{array}{l|l}
    {\rm\bf Derivative \; Formula} & {\rm\bf Integral \; Formula} \\ \hline
    \displaystyle \frac{d}{dx} \left(e^x \right) = e^x & \displaystyle \int e^k \; dx = e^x + C \\
    \displaystyle \frac{d}{dx} \left(a^x \right) = a^x \ln(a) & \displaystyle \int a^x \; dx = \frac{a^x}{\ln(a)} + C \\
    \displaystyle \frac{d}{dx} \left(\ln|x| \right) = \frac{1}{x} & \displaystyle \int \frac{1}{x} \; dx = \ln|x| + C \\
    \displaystyle \frac{d}{dx} \left(\log_b|x| \right) = \frac{1}{x \ln(b)} & \displaystyle \int \frac{1}{x \ln(b)} \; dx = \log_b|x| + C \\
    \end{array}


Trigonometric Rules
"""""""""""""""""""

.. math::
    \begin{array}{l|l}
    {\rm\bf Derivative \; Formula} & {\rm\bf Integral \; Formula} \\ \hline
    \displaystyle \frac{d}{dx} \left(\sin(x) \right) = \cos(x) & \displaystyle \int \cos(x) \; dx = \sin(x) + C \\
    \displaystyle \frac{d}{dx} \left(\cos(x) \right) = -\sin(x) & \displaystyle \int \sin(x) \; dx = -\cos(x) + C \\
    \displaystyle \frac{d}{dx} \left(\tan(x) \right) = \sec^2(x) & \displaystyle \int \sec^2(x) \; dx = \tan(x) + C \\
    \displaystyle \frac{d}{dx} \left(\cot(x) \right) = -\csc^2(x) & \displaystyle \int \csc^2(x) \; dx = -\cot(x) + C \\
    \displaystyle \frac{d}{dx} \left(\sec(x) \right) = \sec(x)\tan(x) & \displaystyle \int \sec(x)\tan(x) \; dx = \sec(x) + C \\
    \displaystyle \frac{d}{dx} \left(\csc(x) \right) = -\csc(x)\cot(x) & \displaystyle \int \csc(x)\cot(x) \; dx = -\csc(x) + C \\
    \end{array}

Inverse Trigonometric Rules
"""""""""""""""""""""""""""

.. math::
    \begin{array}{l|l}
    {\rm\bf Derivative \; Formula} & {\rm\bf Integral \; Formula} \\ \hline
    \displaystyle \frac{d}{dx} \left(\sin^{-1}(x) \right) = \frac{1}{\sqrt{1-x^2}} & \displaystyle \int \frac{1}{\sqrt{1-x^2}} \; dx = \sin^{-1}(x) + C \\
    \displaystyle \frac{d}{dx} \left(\cos^{-1}(x) \right) = -\frac{1}{\sqrt{1-x^2}} & \displaystyle \int \frac{1}{\sqrt{1-x^2}} \; dx = -\cos^{-1}(x) + C \\
    \displaystyle \frac{d}{dx} \left(\tan^{-1}(x) \right) = \frac{1}{1+x^2} & \displaystyle \int \frac{1}{1+x^2} \; dx = \tan^{-1}(x) + C \\
    \displaystyle \frac{d}{dx} \left(\cot^{-1}(x) \right) = -\frac{1}{1+x^2} & \displaystyle \int \frac{1}{1+x^2} \; dx = -\cot^{-1}(x) + C \\
    \displaystyle \frac{d}{dx} \left(\sec^{-1}(x) \right) = \frac{1}{x \sqrt{x^2 - 1}} & \displaystyle \int \frac{1}{x \sqrt{x^2 - 1}} \; dx = \sec^{-1}(x) + C \\
    \displaystyle \frac{d}{dx} \left(\csc^{-1}(x) \right) = -\frac{1}{x \sqrt{x^2 - 1}} & \displaystyle \int \frac{1}{x \sqrt{x^2 - 1}} \; dx = -\csc^{-1}(x) + C \\
    \end{array}


Hyperbolic Rules
""""""""""""""""

.. math::
    \begin{array}{l|l}
    {\rm\bf Derivative \; Formula} & {\rm\bf Integral \; Formula} \\ \hline
    \displaystyle \frac{d}{dx} \left(\sinh(x) \right) = \cosh(x) & \displaystyle \int \cosh(x) \; dx = \sinh(x) + C \\
    \displaystyle \frac{d}{dx} \left(\cosh(x) \right) = \sinh(x) & \displaystyle \int \sinh(x) \; dx = \cosh(x) + C \\
    \displaystyle \frac{d}{dx} \left(\tanh(x) \right) = \text{sech}^2(x) & \displaystyle \int \text{sech}^2(x) \; dx = \tanh(x) + C \\
    \displaystyle \frac{d}{dx} \left(\coth(x) \right) = -\text{csch}^2(x) & \displaystyle \int \text{csch}^2(x) \; dx = - \coth(x) + C \\
    \displaystyle \frac{d}{dx} \left(\text{sech}(x) \right) = -\text{sech}(x)\tanh(x) & \displaystyle \int \text{sech}(x)\tanh(x) \; dx = - \text{sech}(x) + C \\
    \displaystyle \frac{d}{dx} \left(\text{csch}(x) \right) = -\text{csch}(x)\coth(x) & \displaystyle \int \text{csch}(x)\coth(x) \; dx = - \text{csch}(x) + C \\
    \end{array}


Inverse Hyperbolic Rules
""""""""""""""""""""""""

.. math::
    \begin{array}{l|l}
    {\rm\bf Derivative \; Formula} & {\rm\bf Integral \; Formula} \\ \hline
    \displaystyle \frac{d}{dx} \left(\sinh^{-1}(x) \right) = \frac{1}{\sqrt{1+x^2}} & \displaystyle \int \frac{1}{\sqrt{1+x^2}} \; dx = \sinh^{-1}(x) + C \\
    \displaystyle \frac{d}{dx} \left(\cosh^{-1}(x) \right) = \frac{1}{\sqrt{x^2 - 1}} & \displaystyle \int \frac{1}{\sqrt{x^2 - 1}} \; dx = \cosh^{-1}(x) + C \\
    \displaystyle \frac{d}{dx} \left(\tanh^{-1}(x) \right) = \frac{1}{1-x^2} & \displaystyle \int \frac{1}{1-x^2} \; dx = \tanh^{-1}(x) + C \\
    \displaystyle \frac{d}{dx} \left(\coth^{-1}(x) \right) = \frac{1}{1-x^2} & \displaystyle \int \frac{1}{1-x^2} \; dx = \coth^{-1}(x) + C \\
    \displaystyle \frac{d}{dx} \left(\text{sech}^{-1}(x) \right) = - \frac{1}{x\sqrt{1-x^2}} & \displaystyle \int \frac{1}{x\sqrt{1-x^2}} \; dx = -\text{sech}^{-1}(x) + C \\
    \displaystyle \frac{d}{dx} \left(\text{csch}^{-1}(x) \right) = - \frac{1}{|x|\sqrt{x^2 + 1}} & \displaystyle \int \frac{1}{|x|\sqrt{x^2 + 1}} \; dx = -\text{csch}^{-1}(x) + C \\
    \end{array}

Arithmetic Rules
""""""""""""""""

.. math::
    \begin{array}{l|l}
    {\rm\bf Derivative \; Formula} & {\rm\bf Integral \; Formula} \\ \hline
    \displaystyle \frac{d}{dx} \left(c f(x)  \right) = c f'(x) & \displaystyle \int c f(x) \; dx =  c \int f(x) \; dx \\
    \displaystyle \frac{d}{dx} \left(f(x) + g(x) \right) = f'(x) + g'(x) & \displaystyle \int f(x) + g(x) \; dx =  \int f(x) \; dx + \int g(x) \; dx \\
    \displaystyle \frac{d}{dx} \left(f(x) - g(x) \right) = f'(x) - g'(x) & \displaystyle \int f(x) - g(x) \; dx =  \int f(x) \; dx - \int g(x) \; dx \\
    \end{array}

.. note::

    Onr thing to note about these formulas is that in some cases you can use different formulas for the same integrand.  So when you are using a CAS to so an integral the result might not be what you expect.  In other cases the CAS might use a different technique to find the integral.  For example, in CLAE

    .. math::
        \int \frac{1}{x^{2} + 1} \; dx = \tan^{-1}(x) + C

    so it uses the arc tangent and not the arc cotangent.  Also,

    .. math::
        \int \frac{1}{1 - x^{2}} = - \frac{\ln{\left(x - 1 \right)}}{2} + \frac{\ln{\left(x + 1 \right)}}{2} +C

    so it used partial fractions instead of one of the formulas above.

Initial-Value Problems
^^^^^^^^^^^^^^^^^^^^^^

One application we can do at this point is solve some simple initial-value problems.  An initial-value problem is a particular type of problem you encounter in an area of mathematics known as Differential Equations.  A differential equation is simply an equation with derivatives in it amd your goal is to find a function or all functions that satisfy the equation.  For example,

.. math::
    - \frac{d}{d x} f{\left(x \right)} + \frac{d^{2}}{d x^{2}} f{\left(x \right)} = 0

is a differential equation.  The solution to this equation is

.. math::
    f{\left(x \right)} = C_{1} + C_{2} e^{x}

where :math:`C_{1}` and :math:`C_{2}` are arbitrary constants.  Both the first and second derivatives of this function are :math:`C_{2} e^{x}`, so

.. math::
    - \frac{d}{d x} f{\left(x \right)} + \frac{d^{2}}{d x^{2}} f{\left(x \right)} = - C_{2} e^{x} + C_{2} e^{x} = 0

Hence it solves the differential equation.

Note in our example above the solution had arbitrary constants in it.  So there is an infinite family of solutions to this equation just like there is for an integral.  If we knew some specific details about the function :math:`f(x)` we might be able to find particular solutions for :math:`C_{1}` and :math:`C_{2}`.  This is where initial-value problems come in.  These include a differential equation and extra information so we can find a particular solution from the family of solutions.  We will not be looking at differential equations that are as difficult as the one above, ours will be of the form,

.. math::
    \frac{d}{dx}\left( f(x) \right) = g(x)  \quad {\rm or \; equivalently } \quad \frac{dy}{dx} = f(x)

and we will have some more information, such as :math:`y(0) = 5`.  With differential equations like these the solution is simply finding an antiderivative, more specifically, if we have the equation,

.. math::
    \frac{d}{dx}\left( f(x) \right) = g(x)

then

.. math::
    f(x) = \int g(x) \; dx

Although the notation here is a little misleading, keep in mind that this is a family of solutions.  The extra information we might have my allow us to narrow it down to a single solution.

For example, say we have an object that is being moved by a periodic engine and we know that the velocity of the object is given by,

.. math::
    v(t) = - 6 \sin{\left(2 t \right)} + 6 \cos{\left(3 t \right)}

.. figure:: Images/Apps/IndefInt002.png
    :alt: Velocity Example Curve

    :math:`v(t) = - 6 \sin{\left(2 t \right)} + 6 \cos{\left(3 t \right)}`

Say we also know that the object starts at position 0, so :math:`s(0) = 0`, find the displacement function :math:`s(t)` for the object.

Although we have not discussed integration techniques beyond the formula charts above, knowing the derivatives of trigonometric functions and the chain rule it is not too difficult to see that,

.. math::
    s(t) = C_{1} + 2 \sin{\left(3 t \right)} + 3 \cos{\left(2 t \right)}

With the added information we can take this a little further.  From, :math:`s(0) = 0`, we get,

.. math::
    0 = s(0) = C_{1} + 2 \sin{\left(3 \cdot 0 \right)} + 3 \cos{\left(2 \cdot 0 \right)} = C_{1} + 3

so :math:`C_{1} = -3` and :math:`s(t) = -3 + 2 \sin{\left(3 t \right)} + 3 \cos{\left(2 t \right)}`

.. figure:: Images/Apps/IndefInt003.png
    :alt: Velocity and Distance Example Curve

    :math:`v(t) = - 6 \sin{\left(2 t \right)} + 6 \cos{\left(3 t \right)}` and :math:`s(t) = -3 + 2 \sin{\left(3 t \right)} + 3 \cos{\left(2 t \right)}`

Example: Finding Indefinite Integrals
-------------------------------------

GeoGebra
^^^^^^^^

In GeoGebra you can find an indefinite integral using the ``Integral`` command.  The integral command comes in several forms the two for indefinite integrals are,

- Integral(fct): If the function is in a single variable.
- Integral(fct, var): If the function is in a several variables and you want to specify the one to integrate with respect to.

We will take the example above, input the function,

.. code-block:: console

    -6 sin(2 x)+6 cos(3 x)

Now type in and select ``Integral`` and then type ``f`` for the function, you will get,

.. math::
    3 \cos(2x) + 2 \sin(3x)

and a :math:`c_1` slider.

.. figure:: Images/Apps/IndefInt004.png
    :alt: Velocity and Distance Example Curve

    :math:`v(t) = - 6 \sin{\left(2 t \right)} + 6 \cos{\left(3 t \right)}` and Antiderivative

As you move the slider around the solution curve will move vertically and the :math:`c_1` value is added to the equation.  So even though it is not displayed this way the solution was :math:`f(x) = 3 \cos(2x) + 2 \sin(3x) + c_1`. Since GeoGebra automatically inputs values for the constant, for graphical purposes, using it to solve for :math:`c_1` given the initial value is cumbersome.  Frankly this is easy enough to do in our heads.

CLAE
^^^^

In CLAE you can find an indefinite integral using the ``Calculus > Indefinite Integral`` option.  When you do, a dialog box will appear asking you for the variable, to include the constant, and to use course techniques. There is also a variable properties editor for the variables.  This is rarely needed but is there just in case, nonetheless.

- The variable is the variable of integration.

- If you select to include the constant the program will add the :math:`C_1` to the expression, there are some cases where you do not need the entire family of antiderivatives and do not want to bother with the constant.

- The course techniques selection will tell CLAE to use techniques that you would most likely see in a Calculus class.  If unselected it will use whatever technique it feels is best.  Keeping this option selected will make the output as reasonable as possible, when not selected you may see some functions ate are beyond the scope of a college Calculus course.  With this said, if CLAE does not Calculate the integral with this option set you can always retry it with the option deselected.

We will take the example above, input the function,

.. code-block:: console

    -6*sin(2*x) + 6*cos(3*x)

Select the function then select ``Calculus > Indefinite Integral``, variable *x*, select include constant and course techniques, the result is,

.. math::
    C_{1} + 2 \sin{\left(3 x \right)} + 3 \cos{\left(2 x \right)}

If you graph the original function and the integral you will see,

.. figure:: Images/Apps/IndefInt005.png
    :alt: Velocity and Distance Example Curve

    :math:`v(t) = - 6 \sin{\left(2 t \right)} + 6 \cos{\left(3 t \right)}` and Antiderivative

and there is a :math:`C_1` slider that will move the function vertically.  Although we can do the remainder of the initial-value problem by hand we can also use CLAE.  Select the integral expression, select ``Algebra > Evaluate``, the variable is *x* and the expression is 0.  As expected, you will get :math:`C_{1} + 3`, so obviously :math:`C_{1} = -3`.  You can also select this expression and then ``Algebra > Solve`` to get :math:`\left[ -3\right]`.  In any case our initial value solution is,

.. math::
    f(x) = -3 + 2 \sin{\left(3 x \right)} + 3 \cos{\left(2 x \right)}

Maxima
^^^^^^

In Maxima you can find an indefinite integral using the ``integrate`` command.  The syntax is ``integrate(exp, var)`` where the first argument is the expression to integrate and the second is the variable to integrate with respect to.

We will take the example above, input the function,

.. code-block:: console

    f(x) := -6*sin(2*x) + 6*cos(3*x)

Then to integrate the function we use

.. code-block:: console

    fp:integrate(f(x), x)

The result is,

.. math::
    2 \sin{\left( 3 x\right) }+3 \cos{\left( 2 x\right) }\mbox{}

Note that it does not include a constant of integration, it assumes that user can do that themselves.  We can graph these expressions together with,

.. code-block:: console

    wxplot2d([f(x), fp], [x,-1, 10]);

.. figure:: Images/Apps/IndefInt006.png
    :alt: Velocity and Distance Example Curve

    :math:`v(t) = - 6 \sin{\left(2 t \right)} + 6 \cos{\left(3 t \right)}` and Antiderivative


Example: More Indefinite Integrals
----------------------------------

The following are simply some expressions to find the integrals of using the software.  In each case, use the software you would like and follow the procedures  outlines in the first example to complete the calculation.  Note that your results may differ since the software packages may use different techniques in their calculations.

.. math::
    \int 6 x \cos{\left(3 x^{2} \right)} \; dx = \sin{\left(3 x^{2} \right)} + C

.. math::
    \int \frac{2 x}{\left(x^{2} - 1\right)^{2}} \; dx = -\frac{1}{x^{2} - 1} + C

.. math::
    \int \frac{1}{x^{2} - 1} \; dx = \frac{\ln{\left(x - 1 \right)}}{2} - \frac{\ln{\left(x + 1 \right)}}{2} + C

Try some more on your own.

Note that integration takes a bit more effort in general than does differentiation.  Also in some cases finding an antiderivative is very difficult or impossible.  By impossible, we usually mean that the antiderivative is not an elementary function.  In other words, it is not built up from functions you are familiar with, like polynomials, rational functions, trigonometric functions, etc.   For example try to find the integrals of :math:`f(x) = \sin(\cos(x))` or :math:`f(x) = e^{\sin(x)}`.  In GeoGebra the result will probably be a question mark and in CLAE and Maxima it will probably just return the integral back to you.  In either case this simply means that the software could not do the integral.
