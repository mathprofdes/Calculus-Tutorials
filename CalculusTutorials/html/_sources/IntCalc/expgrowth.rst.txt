:index:`Exponential Growth and Decay`
=====================================

Discussion & Definitions
------------------------

Whenever you have a quantity that has a rate of change that is proportional to the size of the quantity then that quantity is experiencing exponential growth or decay.  One example is population growth, or we should say unrestricted population growth. The larger the population the more offspring.  Another example is radioactive decay, the more material you have the more decomposition of the material.

Mathematically, "a quantity that has a rate of change that is proportional to the size of the quantity" can be represented as the differential equation,

.. math::
    \frac{dy}{dt} = k y

where *y* represents the quantity size at time *t* and *t* is time.  This is a separable equation with solution,

.. math::
    f{\left(t \right)} = C_{1} e^{k t}

Also, if we let :math:`t = 0` then we have,

.. math::
    y_0 = f{\left(0 \right)} = C_{1} e^{k 0} = C_{1}

so our general solution is,

.. math::
    f{\left(t \right)} = y_0 e^{k t}

where *k* is the growth or decay constant (growth if *k* is positive and decay if *k* is negative) :math:`y_0` represents the initial quantity size, that is, the quantity size at time :math:`t = 0.`

Example
-------

GeoGebra
^^^^^^^^

Input the equation,

.. code-block:: console

    a(x,y)=k y

Note that we must include the ``a(x,y)`` or GeoGebra will not know that this is an expression in two variables.  Now in a new cell input ``SolveODE(a)``.  The result is,

.. math::
    1 \cdot e^x

There are also two sliders, one for *k* and one for *C1*, if you alter these and look at the resulting expression it is clear that the general solution is,

.. math::
    y = C_{1} e^{k x}


CLAE
^^^^

Input the differential equation,

.. code-block:: console

    f(t).diff(t)-k*f(t)

Now select, ``Calculus > Solve ODE`` and the result is,

.. math::
    f{\left(t \right)} = C_{1} e^{k t}

If you wish to graph this or work further with the solution you can extract the right hand side of the equation with ``Algebra > Equations > Right Hand Side``.

Maxima
^^^^^^

Input the expression with derivatives,

.. code-block:: console

    kill(all);
    de:k * y - 'diff(y, t);

Then solve the ODE with

.. code-block:: console

    sl:ode2(de,y,t);

The result is,

.. math::

    y={\mathrm{\% c}} {{\% e}^{k t}}\mbox{}

