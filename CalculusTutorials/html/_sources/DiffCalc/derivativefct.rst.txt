:index:`The Derivative as a Function`
=====================================

Discussion & Definitions
------------------------

One of the formulations for the derivative of :math:`f(x)` at *a* is,

.. admonition:: Definition: The Derivative

    Let :math:`f(x)` be a function that is defined on an open interval containing the point *a*.  We define the derivative of :math:`f(x)` at *a* by

    .. math::

        f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}

    If this limit exists.


We can turn this into a function and define the derivative function by simply replacing *a* in the above definition with *x*.  Formally,

.. admonition:: Definition: The Derivative as a Function

    Let :math:`f(x)` be a function. We define the derivative of :math:`f(x)` as,

    .. math::

        f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}

If we have a derivative function in general then to find the derivative at a point *a* we simply need to evaluate the derivative function at *a* ad do not need to calculate the limit again, note that,

.. math::

    f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}

A few terms about differentiability.

.. admonition:: Definition: Terms and Notations

    A function :math:`f(x)` is said to be **differentiable** at *a* if :math:`f'(a)` exists. More generally, a function is said to be **differentiable on an open interval** if it is differentiable at every point in the interval, and a **differentiable function** is one in which :math:`f(x)` exists on its domain.

    Denoting the derivatives can take several forms.  The most common is the prime notation, :math:`f'(x), y'(x), y', f', \ldots` another notation that is more useful in multivariable calculus is due to Leibniz, :math:`\displaystyle \frac{dy}{dx}`, :math:`\displaystyle \frac{df}{dx}`, and :math:`\displaystyle \frac{d}{dx} \left(f(x)\right)`.


An important theorem that relates differentiability to continuity is that if you have a function that is differentiable at *a* then that function is also continuous at *a*.

.. admonition:: Theorem: Differentiability Implies Continuity

    Let :math:`f(x)` be a function and *a* be in its domain. If :math:`f(x)` is differentiable at *a*, then :math:`f` is continuous at *a*.

.. note::

    Be careful with this theorem, it does not imply that if a function is continuous at *a* then the function is differentiable at *a*.  For example, take :math:`f(x) = |x|`,

    .. figure:: Images/Diff/Diff001.png
        :alt: y = |x|

        :math:`f(x) = |x|`

    This function is continuous at :math:`x = 0` but it is not differentiable at :math:`x = 0` since the derivative limit,

    .. math::

        f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}

    does not exist at :math:`a = 0` since the left and right hand limits are not equal.

    .. math::

        \lim_{h \to 0^+} \frac{f(0+h) - f(0)}{h} = \lim_{h \to 0^+} \frac{|h| - 0}{h} = \lim_{h \to 0^+} \frac{|h|}{h} = \lim_{h \to 0^+} \frac{h}{h} = \lim_{h \to 0^+} 1 = 1

    and

    .. math::

        \lim_{h \to 0^-} \frac{f(0+h) - f(0)}{h} = \lim_{h \to 0^-} \frac{|h| - 0}{h} = \lim_{h \to 0^-} \frac{|h|}{h} = \lim_{h \to 0^-} \frac{-h}{h} = \lim_{h \to 0^-} -1 = -1

    In general, if a function has a sharp cornet or cusp at a point then it is not differentiable at that point.

Although the converse of the theorem is not valid the contrapositive of the statement is, which gives us a nice way to determine, in some cases, if a function is not differentiable.

.. admonition:: Theorem: Discontinuity Implies Non-Differentiability

    Let :math:`f(x)` be a function and *a* be in its domain. If :math:`f` is not continuous at *a* then :math:`f(x)` is not differentiable at *a*.

As an example, if we take the floor function, :math:`f(x) = \left\lfloor{x}\right\rfloor`

.. figure:: Images/Diff/Diff002.png
    :alt: y = floor(x)

    :math:`f(x) = \left\lfloor{x}\right\rfloor`


Since the floor function is discontinuous at every integer, it is not differentiable at every integer.  Functions that are continuous at a point can still fail to be differentiable in more ways than having a cusp there, we will look at some of these in the examples.


.. note::

    A quick note before going into the examples, the derivative of a function is easier to calculate using derivative formulas than using limits.  Each of these software packages has a derivative function built into it and there is usually (but not always) no need to take the derivative using the definition when using a computer algebra system.  In the examples below we will go through the process of finding the derivative functions by definition and show the commands for finding the derivative without setting up the limits.


Example: :math:`f(x) = x^{3} - 3 x^{2} + x + 3`
-----------------------------------------------

GeoGebra
^^^^^^^^

In GeoGebra doing the derivative by definition is cumbersome, we will simply show the derivative command.

Input the function :math:`f(x) = x^{3} - 3 x^{2} + x + 3`.

.. code-block:: console

    x^3-3 x^2+x+3

In a new cell simply type in ``f'`` and the derivative is computed, the result should be,

.. math::

    3 x^{2} - 6 x + 1


CLAE
^^^^

By Definition
"""""""""""""

Input the function :math:`f(x) = x^{3} - 3 x^{2} + x + 3`.

.. code-block:: console

    f(x):=x^3-3*x^2+x+3

Create the difference quotient,

.. code-block:: console

    (f(x+h)-f(x))/h

you should get

.. math::

    \frac{h - x^{3} + 3 x^{2} + \left(h + x\right)^{3} - 3 \left(h + x\right)^{2}}{h}

Take the limit with ``Calculus > Limit`` variable is *h*, limit point is 0, and direction is Two Sided.  The result should be,

.. math::

    3 x^{2} - 6 x + 1

Derivative Command
""""""""""""""""""

Input the function :math:`f(x) = x^{3} - 3 x^{2} + x + 3`. Note that you do not need the ``f(x):=``,

.. code-block:: console

    x^3-3*x^2+x+3

Select the expression, then select ``Calculus > Derivative``, variable is *x*, order is 1, leave the variable properties as they are.  The result should be,

.. math::

    3 x^{2} - 6 x + 1


Maxima
^^^^^^

By Definition
"""""""""""""

Input the function :math:`f(x) = x^{3} - 3 x^{2} + x + 3`.

.. code-block:: console

    f(x):=x^3-3*x^2+x+3

Create the difference quotient,

.. code-block:: console

    (f(x+h)-f(x))/h

you should get

.. math::

    \frac{h - x^{3} + 3 x^{2} + \left(h + x\right)^{3} - 3 \left(h + x\right)^{2}}{h}

Take the limit with the following, assuming that the difference quotient is in ``%o2``,

.. code-block:: console

    limit(%o2, h, 0)

The result should be,

.. math::

    3 x^{2} - 6 x + 1

Derivative Command
""""""""""""""""""

Input the function :math:`f(x) = x^{3} - 3 x^{2} + x + 3`.

.. code-block:: console

    f(x):=x^3-3*x^2+x+3

Take the derivative with the following command,

.. code-block:: console

    diff(f(x),x)

The result should be,

.. math::

    3 x^{2} - 6 x + 1


Example: :math:`f(x) = \frac{1}{x}`
-----------------------------------


GeoGebra
^^^^^^^^

In GeoGebra doing the derivative by definition is cumbersome, we will simply show the derivative command.

Input the function :math:`f(x) = \frac{1}{x}`.

.. code-block:: console

    1/x

In a new cell simply type in ``f'`` and the derivative is computed, the result should be,

.. math::

    \frac{-1}{x^2}


CLAE
^^^^

By Definition
"""""""""""""

Input the function :math:`f(x) = \frac{1}{x}`.

.. code-block:: console

    f(x):=1/x

Create the difference quotient,

.. code-block:: console

    (f(x+h)-f(x))/h

you should get

.. math::

    \frac{\frac{1}{h + x} - \frac{1}{x}}{h}

Take the limit with ``Calculus > Limit`` variable is *h*, limit point is 0, and direction is Two Sided.  The result should be,

.. math::

    - \frac{1}{x^{2}}

Derivative Command
""""""""""""""""""

Input the function :math:`f(x) = \frac{1}{x}`. Note that you do not need the ``f(x):=``,

.. code-block:: console

    1/x

Select the expression, then select ``Calculus > Derivative``, variable is *x*, order is 1, leave the variable properties as they are.  The result should be,

.. math::

    - \frac{1}{x^{2}}


Maxima
^^^^^^

By Definition
"""""""""""""

Input the function :math:`f(x) = \frac{1}{x}`.

.. code-block:: console

    f(x):=1/x

Create the difference quotient,

.. code-block:: console

    (f(x+h)-f(x))/h

you should get

.. math::

    \frac{\frac{1}{h + x} - \frac{1}{x}}{h}

Take the limit with the following, assuming the difference quotient is in ``%o2``,

.. code-block:: console

    limit(%o2, h, 0)

The result should be,

.. math::

    - \frac{1}{x^{2}}

Derivative Command
""""""""""""""""""

Input the function :math:`f(x) = \frac{1}{x}`.

.. code-block:: console

    f(x):=1/x

Find the derivative with,

.. code-block:: console

    diff(f(x),x)

The result should be,

.. math::

    - \frac{1}{x^{2}}


Example: :math:`f(x) = \sin(x)`
-------------------------------

GeoGebra
^^^^^^^^

In GeoGebra doing the derivative by definition is cumbersome, we will simply show the derivative command.

Input the function :math:`f(x) = \sin(x)`.

.. code-block:: console

    sin(x)

In a new cell simply type in ``f'`` and the derivative is computed, the result should be,

.. math::

    \cos(x)


CLAE
^^^^

By Definition
"""""""""""""

Input the function :math:`f(x) = \sin(x)`.

.. code-block:: console

    f(x):=sin(x)

Create the difference quotient,

.. code-block:: console

    (f(x+h)-f(x))/h

you should get

.. math::

    \frac{- \sin{\left(x \right)} + \sin{\left(h + x \right)}}{h}

Take the limit with ``Calculus > Limit`` variable is *h*, limit point is 0, and direction is Two Sided.  The result should be,

.. math::

    \cos(x)

Derivative Command
""""""""""""""""""

Input the function :math:`f(x) = \sin(x)`. Note that you do not need the ``f(x):=``,

.. code-block:: console

    sin(x)

Select the expression, then select ``Calculus > Derivative``, variable is *x*, order is 1, leave the variable properties as they are.  The result should be,

.. math::

    \cos(x)


Maxima
^^^^^^

By Definition
"""""""""""""

Input the function :math:`f(x) = \sin(x)`.

.. code-block:: console

    f(x):=sin(x)

Create the difference quotient,

.. code-block:: console

    (f(x+h)-f(x))/h

you should get

.. math::

    \frac{- \sin{\left(x \right)} + \sin{\left(h + x \right)}}{h}

Take the limit with the following, assuming the difference quotient is in ``%o2``,

.. code-block:: console

    limit(%o2, h, 0)

The result should be,

.. math::

    \cos(x)

Derivative Command
""""""""""""""""""

Input the function :math:`f(x) = \sin(x)`.

.. code-block:: console

    f(x):=sin(x)

Find the derivative with,

.. code-block:: console

    diff(f(x),x)

The result should be,

.. math::

    \cos(x)



Example: :math:`f(x) = x\sin\left(\frac{1}{x}\right)`
-----------------------------------------------------


GeoGebra
^^^^^^^^

In GeoGebra doing the derivative by definition is cumbersome, we will simply show the derivative command.

Input the function :math:`f(x) = x\sin\left(\frac{1}{x}\right)`.

.. code-block:: console

    x sin(1/x)

In a new cell simply type in ``f'`` and the derivative is computed, the result should be,

.. math::

    \frac{x \sin{\left(\frac{1}{x} \right)} - \cos{\left(\frac{1}{x} \right)}}{x}


CLAE
^^^^

By Definition
"""""""""""""

Input the function :math:`f(x) = x\sin\left(\frac{1}{x}\right)`.

.. code-block:: console

    f(x):=x*sin(1/x)

Create the difference quotient,

.. code-block:: console

    (f(x+h)-f(x))/h

you should get

.. math::

    \frac{- x \sin{\left(\frac{1}{x} \right)} + \left(h + x\right) \sin{\left(\frac{1}{h + x} \right)}}{h}

Take the limit with ``Calculus > Limit`` variable is *h*, limit point is 0, and direction is Two Sided.  The result should be,

.. math::

    \frac{x \sin{\left(\frac{1}{x} \right)} - \cos{\left(\frac{1}{x} \right)}}{x}

Derivative Command
""""""""""""""""""

Input the function :math:`f(x) = x\sin\left(\frac{1}{x}\right)`. Note that you do not need the ``f(x):=``,

.. code-block:: console

    x*sin(1/x)

Select the expression, then select ``Calculus > Derivative``, variable is *x*, order is 1, leave the variable properties as they are.  The result should be,

.. math::

    \sin{\left(\frac{1}{x} \right)} - \frac{\cos{\left(\frac{1}{x} \right)}}{x}

Note that the outputs from the limit and the derivative option are slightly different, although easily seen to be equivalent.  Since we applied a different algorithm we should expect possibly different, but equivalent, results.

Maxima
^^^^^^

By Definition
"""""""""""""

Input the function :math:`f(x) = x\sin\left(\frac{1}{x}\right)`.

.. code-block:: console

    f(x):=x*sin(1/x)

Create the difference quotient,

.. code-block:: console

    (f(x+h)-f(x))/h

you should get

.. math::

    \frac{- x \sin{\left(\frac{1}{x} \right)} + \left(h + x\right) \sin{\left(\frac{1}{h + x} \right)}}{h}

Take the limit, assuming the difference quotient is in ``%o2``.

.. code-block:: console

    limit(%o2, h, 0)

The result should be,

.. math::

    \sin{\left(\frac{1}{x} \right)} - \frac{\cos{\left(\frac{1}{x} \right)}}{x}

Derivative Command
""""""""""""""""""

Input the function :math:`f(x) = x\sin\left(\frac{1}{x}\right)`.

.. code-block:: console

    f(x):=x*sin(1/x)

Find the derivative with,

.. code-block:: console

    diff(f(x),x)

The result should be,

.. math::

    \sin{\left(\frac{1}{x} \right)} - \frac{\cos{\left(\frac{1}{x} \right)}}{x}

