:index:`Higher-Order Derivatives`
=================================

Discussion & Definitions
------------------------

The derivative of a function is another function.  It is possible that the derivative is also a differentiable function and we could take the derivative ot it.  This would be the derivative of a derivative, or the **second derivative** of the original function.  It too could be differentiable and we could take its derivative which would be the **third derivative** of the original function, and so on.  These are called **higher-order derivatives** and are rates of change of rates of change.

As a quick example, we know that the rate of change of distance with respect to time is velocity, that is, the derivative of distance with respect to time is velocity.  If we then take the rate of change of velocity with respect to time we get acceleration.  That is, the derivative of velocity with respect to time is acceleration.  Thus, the second derivative of distance with respect to time is acceleration.

.. admonition:: Notation: Higher-Order Derivatives

    Denoting higher-order derivatives can take many forms,

    .. math::
        f'(x), f''(x), f'''(x), f^{(4)}(x), f^{(5)}(x), \ldots f^{(n)}(x), \ldots

    .. math::
        y'(x), y''(x), y'''(x), y^{(4)}(x), y^{(5)}(x), \ldots y^{(n)}(x), \ldots

    .. math::
        y', y'', y''', y^{(4)}, y^{(5)}, \ldots y^{(n)}, \ldots

    .. math::
        \frac{dy}{dx}, \frac{d^2y}{dx^2}, \frac{d^3y}{dx^3}, \frac{d^4y}{dx^4}, \ldots , \frac{d^ny}{dx^n}, \ldots

    In the Leibniz notation a the end,

    .. math::
        \frac{d^2y}{dx^2} = \frac{d}{dx} \left( \frac{dy}{dx} \right), \quad
        \frac{d^3y}{dx^3} = \frac{d}{dx} \left( \frac{d}{dx} \left( \frac{dy}{dx} \right) \right) = \frac{d}{dx} \left( \frac{d^2y}{dx^2} \right),  \ldots

Example: General Syntax for Higher-Order Derivatives
----------------------------------------------------

GeoGebra
^^^^^^^^

In GeoGebra to find the derivative of a function :math:`f` you simply type into a new cell ``f'``, to find the second, third, and so on derivative simply add more primes, that is ``f''``, ``f'''``, ``f''''``, and so on.


CLAE
^^^^

In CLAE to find the derivative of a function :math:`f` you select the expression, then select ``Calculus > Derivative`` in the dialog box you select the variable and the order.  Simply change the order to 2, 3, 4, and so on for the second, third, fourth, and so on derivative.

Maxima
^^^^^^

In Maxima to find the derivative of a function :math:`f` you first define the function and then use the command,

.. code-block:: console

    diff(f(x), x)

To find a second derivative we use the syntax,

.. code-block:: console

    diff(f(x), x, 2)

To find a third derivative we use the syntax,

.. code-block:: console

    diff(f(x), x, 3)

and so on.

Example: :math:`f(x) = x^2\sin(x \cos(x))`
------------------------------------------

The advantage, and really the whole idea, to using a computer algebra systems in mathematics education is for the ability to experiment with functions and applications that are difficult to do by hand.  As an example, we will take the first four derivatives of the function, :math:`f(x) = x^2\sin(x \cos(x))`.

The results are,

.. math::

    f'(x) & = x^{2} \left(- x \sin{\left(x \right)} + \cos{\left(x \right)}\right) \cos{\left(x \cos{\left(x \right)} \right)} + 2 x \sin{\left(x \cos{\left(x \right)} \right)} \\
    f''(x) & = - x^{2} \left(\left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{2} \sin{\left(x \cos{\left(x \right)} \right)} + \left(x \cos{\left(x \right)} + 2 \sin{\left(x \right)}\right) \cos{\left(x \cos{\left(x \right)} \right)}\right) - 4 x \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right) \cos{\left(x \cos{\left(x \right)} \right)} + 2 \sin{\left(x \cos{\left(x \right)} \right)} \\
    f'''(x) & = 15 x^{4} \sin{\left(x \right)} \sin{\left(x \cos{\left(x \right)} \right)} \cos{\left(x \right)} + 10 x^{3} \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{3} \sin{\left(x \cos{\left(x \right)} \right)} \cos{\left(x \right)} - 10 x^{3} \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{2} \sin{\left(x \right)} \cos{\left(x \cos{\left(x \right)} \right)} + 15 x^{3} \left(x \cos{\left(x \right)} + 2 \sin{\left(x \right)}\right)^{2} \sin{\left(x \right)} \cos{\left(x \cos{\left(x \right)} \right)} + 80 x^{3} \sin^{2}{\left(x \right)} \sin{\left(x \cos{\left(x \right)} \right)} - x^{3} \sin{\left(x \right)} \cos{\left(x \cos{\left(x \right)} \right)} - 35 x^{3} \sin{\left(x \cos{\left(x \right)} \right)} \cos^{2}{\left(x \right)} - x^{2} \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{5} \cos{\left(x \cos{\left(x \right)} \right)} + 20 x^{2} \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{3} \sin{\left(x \right)} \sin{\left(x \cos{\left(x \right)} \right)} + 90 x^{2} \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{2} \cos{\left(x \right)} \cos{\left(x \cos{\left(x \right)} \right)} - 15 x^{2} \left(x \cos{\left(x \right)} + 2 \sin{\left(x \right)}\right)^{2} \cos{\left(x \right)} \cos{\left(x \cos{\left(x \right)} \right)} - 300 x^{2} \sin{\left(x \right)} \sin{\left(x \cos{\left(x \right)} \right)} \cos{\left(x \right)} + 15 x^{2} \cos{\left(x \right)} \cos{\left(x \cos{\left(x \right)} \right)} + 10 x \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{4} \sin{\left(x \cos{\left(x \right)} \right)} + 120 x \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{2} \sin{\left(x \right)} \cos{\left(x \cos{\left(x \right)} \right)} - 30 x \left(x \cos{\left(x \right)} + 2 \sin{\left(x \right)}\right)^{2} \sin{\left(x \cos{\left(x \right)} \right)} - 120 x \sin^{2}{\left(x \right)} \sin{\left(x \cos{\left(x \right)} \right)} + 60 x \sin{\left(x \right)} \cos{\left(x \cos{\left(x \right)} \right)} + 180 x \sin{\left(x \cos{\left(x \right)} \right)} \cos^{2}{\left(x \right)} + 20 \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{3} \cos{\left(x \cos{\left(x \right)} \right)} + 120 \sin{\left(x \right)} \sin{\left(x \cos{\left(x \right)} \right)} \cos{\left(x \right)} - 60 \cos{\left(x \right)} \cos{\left(x \cos{\left(x \right)} \right)}  \\
    f^{(4)}(x) & = x^{2} \left(\left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{4} \sin{\left(x \cos{\left(x \right)} \right)} + 6 \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{2} \left(x \cos{\left(x \right)} + 2 \sin{\left(x \right)}\right) \cos{\left(x \cos{\left(x \right)} \right)} + \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right) \left(4 x \sin{\left(x \right)} - 12 \cos{\left(x \right)}\right) \sin{\left(x \cos{\left(x \right)} \right)} - 3 \left(x \cos{\left(x \right)} + 2 \sin{\left(x \right)}\right)^{2} \sin{\left(x \cos{\left(x \right)} \right)} + \left(x \cos{\left(x \right)} + 4 \sin{\left(x \right)}\right) \cos{\left(x \cos{\left(x \right)} \right)}\right) + 8 x \left(\left(x \sin{\left(x \right)} - 3 \cos{\left(x \right)}\right) \cos{\left(x \cos{\left(x \right)} \right)} + \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{3} \cos{\left(x \cos{\left(x \right)} \right)} - \left(3 x \sin{\left(x \right)} - 3 \cos{\left(x \right)}\right) \left(x \cos{\left(x \right)} + 2 \sin{\left(x \right)}\right) \sin{\left(x \cos{\left(x \right)} \right)}\right) - 12 \left(x \sin{\left(x \right)} - \cos{\left(x \right)}\right)^{2} \sin{\left(x \cos{\left(x \right)} \right)} - \left(12 x \cos{\left(x \right)} + 24 \sin{\left(x \right)}\right) \cos{\left(x \cos{\left(x \right)} \right)}


GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    x^2 sin(x cos(x))

In subsequent cells input ``f'``, ``f''``, ``f'''``, and ``f''''``.

CLAE
^^^^

Input the function,

.. code-block:: console

    x^2*sin(x*cos(x))

Select the function then select ``Calculus > Derivative``, in the order selector select the order of the derivative and click OK.

Maxima
^^^^^^

Input the function,

.. code-block:: console

    f(x):=x^2*sin(x*cos(x))

Then execute the commands,

.. code-block:: console

    diff(f(x), x, 1);
    diff(f(x), x, 2);
    diff(f(x), x, 3);
    diff(f(x), x, 4);


