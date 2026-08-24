:index:`The Chain Rule`
=======================

For functions of a single variable the chain rule was a theoretical and calculation tool that in many cases simplified the derivative process.  This is also true for functions of several variables.  In single variable Calculus you probably memorized the chain rule with the prime notation.

.. math::
    \frac{d}{dx} (f(g(x))) = f'(g(x))g'(x)

In multivariable Calculus we need to shift to the Leibniz notation,

.. math::
    \frac{dy}{dx} = \frac{dy}{du}  \frac{du}{dx}


Chain Rule for One Independent Variable
---------------------------------------

.. admonition:: Theorem: Chain Rule for One Independent Variable

    Given :math:`z = f(x, y)` where both :math:`x = x(t)` and :math:`y = y(t)` are functions of a single variable *t*, then,

    .. math::
        \frac{dz}{dt} = \frac{\partial z}{\partial x} \frac{dx}{dt} + \frac{\partial z}{\partial y} \frac{dy}{dt}

We can visualize this calculation as a tree diagram.

.. figure:: Images/FctSevVars/ChainRule001.png
    :alt: Chain Rule

    Chain Rule



Chain Rule for Two Independent Variables
----------------------------------------

.. admonition:: Theorem: Chain Rule for Two Independent Variables

    Given :math:`z = f(x, y)` where both :math:`x = x(u, v)` and :math:`y = y(u, v)` are functions of two variables *u* and *v*, then,

    .. math::
        \frac{\partial z}{\partial u} = \frac{\partial z}{\partial x} \frac{\partial x}{\partial u} + \frac{\partial z}{\partial y} \frac{\partial y}{\partial u}

    and

    .. math::
        \frac{\partial z}{\partial v} = \frac{\partial z}{\partial x} \frac{\partial x}{\partial v} + \frac{\partial z}{\partial y} \frac{\partial y}{\partial v}

We can visualize this calculation as a tree diagram. For this diagram, to take the partial with respect to *u*, follow the *u* branches and to take the partial with respect to *v*, follow the *v* branches.

.. figure:: Images/FctSevVars/ChainRule002.png
    :alt: Chain Rule

    Chain Rule



Generalized Chain Rule
----------------------

THe chain rule, and its corresponding tree diagram, can easily be generalized to as many variables as we want, both for the main function and for each of its variables.

.. admonition:: Theorem: Generalized Chain Rule

    Given :math:`z = f(x_1, x_2, x_3, \ldots, x_n)` where each :math:`x_i = x(u_1, u_2, \ldots, u_m)`, then,

    .. math::
        \frac{\partial z}{\partial u_j} = \frac{\partial z}{\partial x_1} \frac{\partial x_1}{\partial u_j} +
        \frac{\partial z}{\partial x_2} \frac{\partial x_2}{\partial u_j} +
        \frac{\partial z}{\partial x_3} \frac{\partial x_3}{\partial u_j} + \cdots +
        \frac{\partial z}{\partial x_n} \frac{\partial x_n}{\partial u_j}

To construct the tree diagram for the general situation, there should be *n* branches off of *z*, one for each :math:`x_i` and each of the :math:`x_i` should have *m* branches off of it, one for each :math:`u_j.`

Example: Chain Rule with a CAS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The chain rule is a nice calculation tool if your expression is broken down into a composition of functions.  With a CAS, it does not mind doing the tedious expansions and simplifications.  So a CAS can just brute force the intermediate calculations.  Nonetheless, it has the generalized chain rule calculations built into it.

CLAE
""""

As a quick example, input,

.. code-block:: console

    f(x(u, v), y(u, v))

This defines *f* as a function of two variables *x* and *y* and each of these are functions of two variables *u* and *v*.  Now select ``Calculus > Derivative``, input *u* as the variable and the result will be,

.. math::
    \frac{\partial}{\partial x{\left(u,v \right)}} f{\left(x{\left(u,v \right)},y{\left(u,v \right)} \right)} \frac{\partial}{\partial u} x{\left(u,v \right)} + \frac{\partial}{\partial y{\left(u,v \right)}} f{\left(x{\left(u,v \right)},y{\left(u,v \right)} \right)} \frac{\partial}{\partial u} y{\left(u,v \right)}

Although it looks more complicated than our expression in the theorem, it is the same.

Implicit Differentiation
------------------------

One consequence of the chain rules above is that we can reformulate implicit differentiation to easier and quicker to calculate.  To see how this works, say we have :math:`f(x, y) = 0`, then,

.. math::
    \frac{d}{dx} \left(f(x, y)\right) & = \frac{d}{dx} \left(0 \right)  \\
    \frac{\partial f}{\partial x} \frac{dx}{dx} + \frac{\partial f}{\partial y} \frac{dy}{dx} & = 0 \\
    \frac{\partial f}{\partial x} + \frac{\partial f}{\partial y} \frac{dy}{dx} & = 0 \\
    \frac{\partial f}{\partial y} \frac{dy}{dx} & = - \frac{\partial f}{\partial x} \\
    \frac{dy}{dx} & = - \frac{\partial f/\partial x}{\partial f/\partial y} \\


.. admonition:: Theorem: Implicit Differentiation of a Function of Two or More Variables

    Given an expression :math:`f(x, y) = 0` we can find the implicit derivative by,

    .. math::
        \frac{dy}{dx} = - \frac{\partial f/\partial x}{\partial f/\partial y}

    as long as :math:`\partial f/\partial y \neq 0.`

    Similarly, if :math:`f(x, y, z) = 0` we can find the implicit partial derivatives by,

    .. math::
        \frac{\partial z}{\partial x} = - \frac{\partial f/\partial x}{\partial f/\partial z} \qquad {\rm and} \qquad \frac{\partial z}{\partial y} = - \frac{\partial f/\partial y}{\partial f/\partial z}

    as long as :math:`\partial f/\partial z \neq 0.`

