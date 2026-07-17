:index:`The Definition of the Derivative`
=========================================

Discussion & Definitions
------------------------

The Derivative is solution to the tangent problem, which is at the heart of Differential Calculus.  If you have not read through the Tangent Problem in either the :doc:`../Gen/index` or :doc:`index` you should do so before continuing.  As a quick recap, the goal is to find the slope of the tangent line to a curve at a point on the curve.  Specifically, we have a function :math:`f(x)`, and a point :math:`(a, f(a))` on the curve. Since we do not have enough information to find the slope of the tangent line we choose a value :math:`x \neq a`, construct a secant line through :math:`(a, f(a))` and :math:`(x, f(x))` and calculate its slope,

.. math::
    m_{sec} = \frac{y_2 - y_1}{x_2 - x_1} = \frac{f(x) - f(a)}{x - a}

This is an approximation to the slop of the tangent line.  To get better approximations we take values of *x* closer and closer to *a*.  That is, we take the limit as :math:`x \to a`.

.. math::
    m_{tan} = \lim_{x \to a} m_{sec} = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}

and this is how we define the slope of the tangent line to a function.  An equivalent formulation that is sometimes easier to calculate is if we let :math:`h = x-a`  then :math:`x = a + h` and letting :math:`x \to a` is the same thing as letting :math:`h \to 0`, our formula becomes,

.. math::
    m_{tan} = \lim_{x \to a} \frac{f(x) - f(a)}{x - a} = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}

At this point we simply define these limits (if they exist) as the derivative of the function at *a*.  Formally,

.. admonition:: Definition: The Derivative

    Let :math:`f(x)` be a function that is defined on an open interval containing the point *a*.  We define the derivative of :math:`f(x)` at *a* by

    .. math::

        f'(a) = \lim_{x \to a} \frac{f(x) - f(a)}{x-a}

    If this limit exists.

    Equivalently, if we let :math:`h = x-a`, this implies that :math:`x = a + h`. Furthermore, this gives :math:`x \to a` is equivalent to :math:`h \to 0`.  Substituting this into our definition above we get the alternative formulation,

    .. math::

        f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}

    If this limit exists.

.. admonition:: Definition: The Difference Quotient

    The two expressions

    .. math::

       \frac{f(x) - f(a)}{x-a}  \quad {\rm and} \quad \frac{f(a+h) - f(a)}{h}

    are called the difference quotient.


.. note::

    A quick note before going into the examples, the derivative of a function is easier to calculate using derivative formulas than using limits.  We will investigate these methods in subsequent sections.  Also, each of these software packages has a derivative function built into it and there is usually (but not always) no need to take the derivative using the definition when using a computer algebra system.  We will look at these quicker methods in subsequent sections as well.  The layout of these tutorials is to match, as closely as possible, the layout of a STEM introductory Calculus class at the college level.  Each of the software packages we are using incorporates a computer algebra system, so they are all capable of find the derivative by definition.  On the other hand, the packages we are using make different assumptions about the users and have different goals to their functionality.  GeoGebra makes finding the derivative of a function very easy but doing it by definition is very cumbersome.  For this reason we will only use CLAE and Maxima for this set of examples.

Example: :math:`f(x) = x^{3} - 3 x^{2} + x + 3`
-----------------------------------------------

For this example we will take the function :math:`f(x) = x^{3} - 3 x^{2} + x + 3` and find both the slope of the tangent line and the equation of the tangent line to the function at :math:`x = 3`.

CLAE
^^^^

Input and graph the function :math:`f(x) = x^{3} - 3 x^{2} + x + 3`.  Adjust the graph so that the curve looks nice and that :math:`x = 3` is visible on the *x*-axis.

.. code-block:: console

    f(x):=x^3-3*x^2+x+3

Create the difference quotient with :math:`a = 3` using the following syntax,

.. code-block:: console

    (f(3+h)-f(3))/h

you should get

.. math::

    \frac{h + \left(h + 3\right)^{3} - 3 \left(h + 3\right)^{2}}{h}

Note that CLAE automatically substituted the :math:`3+h` into the function and did some simplification.  Now take the limit with ``Calculus > Limit`` variable is *h*, limit point is 0, and direction is Two Sided.  The result should be 10.

To find the tangent line we use point-slope form :math:`y = m(x-a) + f(a)`, so input,

.. code-block:: console

    10*(x-3) + f(3)

The result is :math:`10 x - 24`.  Graph this along with the curve,

.. figure:: Images/Diff/DiffDef001.png
    :alt: Function and Tangent Line

    :math:`f(x) = x^{3} - 3 x^{2} + x + 3` and Tangent Line


Maxima
^^^^^^

Input and graph the function :math:`f(x) = x^{3} - 3 x^{2} + x + 3`.  Adjust the graph so that the curve looks nice and that :math:`x = 3` is visible on the *x*-axis.

.. code-block:: console

    f(x):=x^3-3*x^2+x+3

Create the difference quotient with :math:`a = 3` using the following syntax,

.. code-block:: console

    (f(3+h)-f(3))/h

you should get

.. math::

    \frac{h + \left(h + 3\right)^{3} - 3 \left(h + 3\right)^{2}}{h}

Note that Maxima automatically substituted the :math:`3+h` into the function and did some simplification.  Now take the limit, we will assume that the designation of the difference quotient was ``%o2``, use

.. code-block:: console

    limit(%o2, h, 0);

The result should be 10.

To find the tangent line we use point-slope form :math:`y = m(x-a) + f(a)`, so input,

.. code-block:: console

    10*(x-3) + f(3)

Maxima evaluated :math:`f(3)` but did not simplify the expression.  To simplify the expression select ``Simplify > Simplify equations > Try to guess which form is simple``.  The result is :math:`10 x - 24`.

Graph this along with the curve,

.. code-block:: console

    wxplot2d([f(x), 10*x-24], [x,-1,5])

.. figure:: Images/Diff/DiffDef002.png
    :alt: Function and Tangent Line

    :math:`f(x) = x^{3} - 3 x^{2} + x + 3` and Tangent Line

.. note::

    If you look at the command that Maxima choose it was ``ratsimp`` which is used to simplify rational expressions.  You could have just as easily run the command,

    .. code-block:: console

        ratsimp(%o4);

    assuming that ``%o4`` was the designation for the tangent line.


Example: :math:`f(x) = \frac{1}{x}`
-----------------------------------

For this example we will take the function :math:`f(x) = \frac{1}{x}` and find both the slope of the tangent line and the equation of the tangent line to the function at :math:`x = 2`.

CLAE
^^^^

Input and graph the function :math:`f(x) = \frac{1}{x}`.  Adjust the graph so that the curve looks nice and that :math:`x = 2` is visible on the *x*-axis.

.. code-block:: console

    f(x):=1/x

Create the difference quotient with :math:`a = 2` using the following syntax,

.. code-block:: console

    (f(2+h)-f(2))/h

you should get

.. math::

    \frac{- \frac{1}{2} + \frac{1}{h + 2}}{h}

Note that CLAE automatically substituted the :math:`2+h` into the function and did some simplification.  Now take the limit with ``Calculus > Limit`` variable is *h*, limit point is 0, and direction is Two Sided.  The result should be :math:`-1/4`.

To find the tangent line we use point-slope form :math:`y = m(x-a) + f(a)`, so input,

.. code-block:: console

    -1/4*(x-2) + f(2)

The result is :math:`1 - \frac{x}{4}`.  Graph this along with the curve,

.. figure:: Images/Diff/DiffDef003.png
    :alt: Function and Tangent Line

    :math:`f(x) = \frac{1}{x}` and Tangent Line

Maxima
^^^^^^

Input and graph the function :math:`f(x) = \frac{1}{x}`.  Adjust the graph so that the curve looks nice and that :math:`x = 2` is visible on the *x*-axis.

.. code-block:: console

    f(x):=1/x

Create the difference quotient with :math:`a = 2` using the following syntax,

.. code-block:: console

    (f(2+h)-f(2))/h

you should get

.. math::

    \frac{- \frac{1}{2} + \frac{1}{h + 2}}{h}

Note that Maxima automatically substituted the :math:`2+h` into the function and did some simplification.  Now take the limit, we will assume that the designation of the difference quotient was ``%o2``, use

.. code-block:: console

    limit(%o2, h, 0);

The result should be :math:`-1/4`.

To find the tangent line we use point-slope form :math:`y = m(x-a) + f(a)`, so input,

.. code-block:: console

    -1/4*(x-2) + f(2)

Maxima evaluated :math:`f(2)` but did not simplify the expression.  To simplify the expression select ``Simplify > Simplify equations > Try to guess which form is simple``.  The result is :math:`-\frac{x-4}{4}`.

Graph this along with the curve,

.. code-block:: console

    wxplot2d([f(x), -(x-4)/4], [x,-1,5], [y,-10,10])

.. figure:: Images/Diff/DiffDef004.png
    :alt: Function and Tangent Line

    :math:`f(x) = \frac{1}{x}` and Tangent Line


Example: :math:`f(x) = \sin(x)`
-------------------------------

For this example we will take the function :math:`f(x) = \sin(x)` and find both the slope of the tangent line and the equation of the tangent line to the function at :math:`x = \pi/12`.

CLAE
^^^^

Input and graph the function :math:`f(x) = \sin(x)`.  Adjust the graph so that the curve looks nice and that :math:`x = \pi/12 \approx 0.261799387799149` is visible on the *x*-axis.

.. code-block:: console

    f(x):=sin(x)

Create the difference quotient with :math:`a = \pi/12` using the following syntax,

.. code-block:: console

    (f(pi/12+h)-f(pi/12))/h

you should get

.. math::

    \frac{\sin{\left(h + \frac{\pi}{12} \right)} - \frac{\sqrt{6}}{4} + \frac{\sqrt{2}}{4}}{h}

Now take the limit with ``Calculus > Limit`` variable is *h*, limit point is 0, and direction is Two Sided.  The result should be :math:`\frac{\sqrt{2}}{4} + \frac{\sqrt{6}}{4}`.

To find the tangent line we use point-slope form :math:`y = m(x-a) + f(a)`. Since the expression for the slope is a little long we will use the shorthand notation for including a previous result into a new input.  Assuming that the slope designation was R3, input the following,

.. code-block:: console

    R3*(x-pi/12) + f(pi/12)

The result is :math:`\left(\frac{\sqrt{2}}{4} + \frac{\sqrt{6}}{4}\right) \left(x - \frac{\pi}{12}\right) - \frac{\sqrt{2}}{4} + \frac{\sqrt{6}}{4}`.  Graph this along with the curve,

.. figure:: Images/Diff/DiffDef005.png
    :alt: Function and Tangent Line

    :math:`f(x) = \sin(x)` and Tangent Line


Maxima
^^^^^^

Input and graph the function :math:`f(x) = \sin(x)`.  Adjust the graph so that the curve looks nice and that :math:`x = \pi/12 \approx 0.261799387799149` is visible on the *x*-axis.

.. code-block:: console

    f(x):=sin(x)

Create the difference quotient with :math:`a = \pi/12` using the following syntax,

.. code-block:: console

    (f(%pi/12+h)-f(%pi/12))/h

you should get

.. math::

    \frac{\sin{\left( h+\frac{{\pi} }{12}\right) }-\sin{\left( \frac{{\pi} }{12}\right) }}{h}


Now take the limit, assuming the difference quotient is in ``%o2``,

.. code-block:: console

    limit(%o2, h, 0)


The result should be :math:`\cos{\left( \frac{{\pi} }{12}\right) }`.

To find the tangent line we use point-slope form :math:`y = m(x-a) + f(a)`. Since the expression for the slope is a little long we will use the shorthand notation for including a previous result into a new input.  Assuming that the slope designation was ``%o3``, input the following,

.. code-block:: console

    %o3*(x-%pi/12) + f(%pi/12)

The result is :math:`\cos{\left( \frac{{\pi} }{12}\right) } \left( x-\frac{{\pi} }{12}\right) +\sin{\left( \frac{{\pi} }{12}\right) }`.  Graph this along with the curve, assuming ``%o4`` is the tangent line,

.. code-block:: console

    wxplot2d([f(x), %o4], [x,-0.3,1.3])

.. figure:: Images/Diff/DiffDef006.png
    :alt: Function and Tangent Line

    :math:`f(x) = \sin(x)` and Tangent Line


Example: :math:`f(x) = \sqrt{x}`
--------------------------------

For this example we will take the function :math:`f(x) = \sqrt{x}` and find both the slope of the tangent line and the equation of the tangent line to the function at :math:`x = 2`.

CLAE
^^^^

Input and graph the function :math:`f(x) = \sqrt{x}`.  Adjust the graph so that the curve looks nice and that :math:`x = 2` is visible on the *x*-axis.

.. code-block:: console

    f(x):=sqrt(x)

Create the difference quotient with :math:`a = 2` using the following syntax,

.. code-block:: console

    (f(2+h)-f(2))/h

you should get

.. math::

    \frac{\sqrt{h + 2} - \sqrt{2}}{h}

Now take the limit with ``Calculus > Limit`` variable is *h*, limit point is 0, and direction is Two Sided.  The result should be :math:`\frac{\sqrt{2}}{4}`.

To find the tangent line we use point-slope form :math:`y = m(x-a) + f(a)`. Since the expression for the slope is a little long we will use the shorthand notation for including a previous result into a new input.  Assuming that the slope designation was R3, input the following,

.. code-block:: console

    R3*(x-2) + f(2)

The result is :math:`\frac{\sqrt{2} \left(x - 2\right)}{4} + \sqrt{2}`.  Graph this along with the curve,

.. figure:: Images/Diff/DiffDef007.png
    :alt: Function and Tangent Line

    :math:`f(x) = \sqrt{x}` and Tangent Line


Maxima
^^^^^^

Input and graph the function :math:`f(x) = \sqrt{x}`.  Adjust the graph so that the curve looks nice and that :math:`x = 2` is visible on the *x*-axis.

.. code-block:: console

    f(x):=sqrt(x)

Create the difference quotient with :math:`a = 2` using the following syntax,

.. code-block:: console

    (f(2+h)-f(2))/h

you should get

.. math::

    \frac{\sqrt{h + 2} - \sqrt{2}}{h}

Now take the limit, assuming the difference quotient is in ``%o2``,

.. code-block:: console

    limit(%o2, h, 0);

The result should be :math:`\frac{1}{{{2}^{\frac{3}{2}}}}`.

To find the tangent line we use point-slope form :math:`y = m(x-a) + f(a)`. Since the expression for the slope is a little long we will use the shorthand notation for including a previous result into a new input.  Assuming that the slope designation was ``%o3``, input the following,

.. code-block:: console

    %o3*(x-2) + f(2)

The result is :math:`\frac{x-2}{{{2}^{\frac{3}{2}}}}+\sqrt{2}`.  Graph this along with the curve, assuming that the tangent line designation was ``%o4``, input the following,

.. code-block:: console

    wxplot2d([f(x), %o4], [x,-1,5])

.. figure:: Images/Diff/DiffDef008.png
    :alt: Function and Tangent Line

    :math:`f(x) = \sqrt{x}` and Tangent Line


Example: :math:`f(x) = x^{2/3}` at :math:`x = 2`
------------------------------------------------

For this example we will take the function :math:`f(x) = x^{2/3}` and find both the slope of the tangent line and the equation of the tangent line to the function at :math:`x = 2`.

CLAE
^^^^

Input and graph the function :math:`f(x) = x^{2/3}`.  A little caution needs to be takes here, if we input and graph this as,

.. code-block:: console

    f(x):=x^(2/3)

.. figure:: Images/Diff/DiffDef009.png
    :alt: x^(2/3)

    :math:`f(x) = x^{2/3}`

which we know is only half the graph.  As an alternative you can use the following, which will produce the entire graph.

.. code-block:: console

    f(x):=(x^2)^(1/3)

.. figure:: Images/Diff/DiffDef010.png
    :alt: x^(2/3)

    :math:`f(x) = x^{2/3}`

Adjust the graph so that the curve looks nice and that :math:`x = 2` is visible on the *x*-axis.

Create the difference quotient with :math:`a = 2` using the following syntax,

.. code-block:: console

    (f(2+h)-f(2))/h

you should get

.. math::

    \frac{\sqrt[3]{\left(h + 2\right)^{2}} - 2^{\frac{2}{3}}}{h}

Now take the limit with ``Calculus > Limit`` variable is *h*, limit point is 0, and direction is Two Sided.  The result should be :math:`\frac{2^{\frac{2}{3}}}{3}`.

To find the tangent line we use point-slope form :math:`y = m(x-a) + f(a)`. Since the expression for the slope is a little long we will use the shorthand notation for including a previous result into a new input.  Assuming that the slope designation was R3, input the following,

.. code-block:: console

    R3*(x-2) + f(2)

The result is :math:`\frac{2^{\frac{2}{3}} \left(x - 2\right)}{3} + 2^{\frac{2}{3}}`.  Graph this along with the curve,

.. figure:: Images/Diff/DiffDef011.png
    :alt: x^(2/3) and Tangent Line

    :math:`f(x) = x^{2/3}` and Tangent Line


Maxima
^^^^^^

Input and graph the function :math:`f(x) = x^{2/3}`,

.. code-block:: console

    f(x):=x^(2/3)

Adjust the graph so that the curve looks nice and that :math:`x = 2` is visible on the *x*-axis.  Create the difference quotient with :math:`a = 2` using the following syntax,

.. code-block:: console

    (f(2+h)-f(2))/h

you should get

.. math::

    \frac{{{\left( h+2\right) }^{\frac{2}{3}}}-{{2}^{\frac{2}{3}}}}{h}

Now take the limit, assuming the difference quotient is in ``%o2``,

.. code-block:: console

    limit(%o2, h, 0)

The result should be :math:`\frac{{{2}^{\frac{2}{3}}}}{3}`.

To find the tangent line we use point-slope form :math:`y = m(x-a) + f(a)`. Since the expression for the slope is a little long we will use the shorthand notation for including a previous result into a new input.  Assuming that the slope designation was ``%o3``, input the following,

.. code-block:: console

    %o3*(x-2) + f(2)

The result is :math:`\frac{{{2}^{\frac{2}{3}}} \left( x-2\right) }{3}+{{2}^{\frac{2}{3}}}`.  Graph this along with the curve, assuming that the tangent line is in ``%o4``,

.. code-block:: console

    wxplot2d([f(x), %o4], [x,-1,5])

.. figure:: Images/Diff/DiffDef012.png
    :alt: x^(2/3) and Tangent Line

    :math:`f(x) = x^{2/3}` and Tangent Line


Example: :math:`f(x) = x^{2/3}` at :math:`x = 0`
------------------------------------------------

For this example we will investigate the function :math:`f(x) = x^{2/3}` at :math:`x = 0`.  The graph of the function is below.

.. figure:: Images/Diff/DiffDef010.png
    :alt: x^(2/3)

    :math:`f(x) = x^{2/3}`

Notice that at :math:`x = 0` the graph has a sharp corner or cusp.  Whenever this happens the derivative will not exist at that point.  This example will show why that is the case.


CLAE
^^^^

Input and graph the function :math:`f(x) = x^{2/3}`.

.. code-block:: console

    f(x):=x^(2/3)

Create the difference quotient with :math:`a = 0` using the following syntax,

.. code-block:: console

    (f(h)-f(0))/h

you should get

.. math::

    \frac{1}{\sqrt[3]{h}}

Now take the limit with ``Calculus > Limit`` variable is *h*, limit point is 0, and direction is Two Sided.  The result should be zoo, our complex infinity which says that the limit does not exist.  If we go further and take the one-sided limits we get

.. math::

    - \infty \left(-1\right)^{\frac{2}{3}} \quad {\rm and} \quad \infty

telling us that the limits are infinite, in either case the limit of the difference quotient does not exist and hence we do not have a derivative at :math:`x = 0`.


Maxima
^^^^^^

Input and graph the function :math:`f(x) = x^{2/3}`,

.. code-block:: console

    f(x):=x^(2/3)

Create the difference quotient with :math:`a = 0` using the following syntax,

.. code-block:: console

    (f(0+h)-f(0))/h

you should get

.. math::

    \frac{1}{{{h}^{\frac{1}{3}}}}

Now take the limit, assuming the difference quotient is in ``%o2``,

.. code-block:: console

    limit(%o2, h, 0)

The result should be infinity.  If we take the one-sided limits we get :math:`-\infty` and :math:`\infty`.  In either case the limit of the difference quotient does not exist and hence we do not have a derivative at :math:`x = 0`.


Example: :math:`f(x) = x \sin\left(\frac{1}{x}\right)`
------------------------------------------------------

Let's look at a more complicated function, :math:`f(x) = x \sin\left(\frac{1}{x}\right)`.

.. figure:: Images/Diff/DiffDef013.png
    :alt: x sin(1/x)

    :math:`f(x) = x \sin\left(\frac{1}{x}\right)`

This function is not continuous at :math:`x = 0` since :math:`f(0)` does not exist.  On the other hand, the discontinuity is removable and we will remove it by defining :math:`f(0) = 0`.  Specifically,

.. math::
    f(x) = \begin{cases} x \sin{\left(\frac{1}{x} \right)} & \text{for}\: x \neq 0 \\0 & x = 0 \end{cases}

We will show in the procedures below that this function, although continuous at :math:`x = 0` still does not have a derivative at :math:`x = 0`.  In this case neither of the right or left hand limits of the difference quotient exist.  This gives us another case where a derivative does not exist and it is not just a cusp in the graph.

CLAE
^^^^

Input the function, we really only need the non-zero portion.

.. code-block:: console

    f(x):=x*sin(1/x)

Create the difference quotient, since :math:`a = 0` and we defined :math:`f(0) = 0`, the difference quotient reduces to,

.. code-block:: console

    f(h)/h

The result is :math:`\sin{\left(\frac{1}{h} \right)}`. We already know from the limit examples that

.. math::
    \lim_{h \to 0} \sin{\left(\frac{1}{h} \right)}

Does not exist.

Maxima
^^^^^^

Input the function, we really only need the non-zero portion.

.. code-block:: console

    f(x):=x*sin(1/x)

Create the difference quotient, since :math:`a = 0` and we defined :math:`f(0) = 0`, the difference quotient reduces to,

.. code-block:: console

    f(h)/h

The result is :math:`\sin{\left(\frac{1}{h} \right)}`. We already know from the limit examples that

.. math::
    \lim_{h \to 0} \sin{\left(\frac{1}{h} \right)}

Does not exist.
