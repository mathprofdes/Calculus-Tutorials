:index:`The Net Change Theorem`
===============================

Discussion & Definitions
------------------------

The net change theorem considers the integral of a rate of change. It says that when a quantity changes, the new value equals the initial value plus the integral of the rate of change of that quantity.  It is really just a restatement of The Fundamental Theorem of Calculus but takes us back to the relationship between rates of change and total change that we saw in the discussion of the Area Problem.

.. admonition:: Theorem: Net Change Theorem

    The new value of a changing quantity equals the initial value plus the integral of the rate of change.

    .. math::
        F(b) = F(a) + \int_a^b F'(x) \; dx

    or equivalently

    .. math::
        \int_a^b F'(x) \; dx = F(b) - F(a)


Example
-------

Suppose that a particle moves along a straight line with velocity defined by :math:`v(t) = t^2 - 3t - 18`, where :math:`0 \leq t \leq 12` (in meters per second). Find the displacement at time *t* and the total distance traveled up to :math:`t = 12`.

.. figure:: Images/Int/NCT001.png
    :alt: v(t) = t^2 - 3t - 18

    :math:`v(t) = t^2 - 3t - 18`

To answer the first question we go up to the Net Change Theorem,

.. math::
    F(b) = F(a) + \int_a^b F'(x) \; dx

Here :math:`F` is the displacement function (we will replace it with :math:`s`) and hence  :math:`F'(x) = s'(x) = v(x)`.  So, this becomes,

.. math::
    s(t) = s(0) + \int_0^t v(x) \; dx

Continuing, since :math:`s(0) = 0`

.. math::
    s(t) = s(0) + \int_0^t v(x) \; dx = 0 + \int_0^t x^2 - 3x - 18 \; dx = \left. \frac{x^{3}}{3} - \frac{3 x^{2}}{2} - 18 x \right|_0^t = \frac{t^{3}}{3} - \frac{3 t^{2}}{2} - 18 t

which is our displacement function, so the displacement from :math:`0 \leq t \leq 12` is :math:`s(12) = 144` meters.

To find the total distance traveled we need to find,

.. math::
    d = \int_0^{12} |v(t)| \; dt

.. figure:: Images/Int/NCT002.png
    :alt: y = |t^2 - 3t - 18|

    :math:`|v(t)| = |t^2 - 3t - 18|`


.. math::
    d & = \int_0^{12} |v(t)| \; dt \\
    & = \int_0^{12} \left|{ t^{2} - 3 t - 18}\right| \; dt \\
    & = \int_0^{6} -\left({ t^{2} - 3 t - 18}\right) \; dt + \int_6^{12}  t^{2} - 3 t - 18 \; dt \\
    & = 90 + 234 = 324 {\rm \; meters}


GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    t^2 - 3t - 18

Now go to a new cell and type in ``Integral(f)`` to get :math:`\frac{t^{3}}{3} - \frac{3 t^{2}}{2} - 18 t`, which is our displacement function.  Evaluating this at 12 or running ``Integral(f, 0, 12)`` results in 144.  For the distance we can go to a new cell and input ``|f|``, and then take the integral of it from 0 to 12 to get the result of 324.

CLAE
^^^^

Input the function,

.. code-block:: console

    t^2 - 3*t - 18

Select the function and then ``Calculus > Indefinite Integral`` to get the displacement function of :math:`\frac{t^{3}}{3} - \frac{3 t^{2}}{2} - 18 t`.

Note that we could have followed the theory a little closer by inputting,

.. code-block:: console

    x^2 - 3*x - 18

and then selecting ``Calculus > Definite Integral`` with lower bound 0 and upper bound t, to get the displacement function of :math:`\frac{t^{3}}{3} - \frac{3 t^{2}}{2} - 18 t`.  Evaluating this at 12 gives us the 144.

For the distance, assume that the velocity function is in cell ``R1``, input into the CAS ``abs(R1)`` to get,

.. math::
    \left|{- t^{2} + 3 t + 18}\right|

Now select ``Calculus > Definite Integral`` with lower bound 0 and upper bound 12 to get the result of 324.

Maxima
^^^^^^

Input the function,

.. code-block:: console

    kill(all);
    f(t):=t^2 - 3*t - 18

To get the displacement function we can simply integrate,

.. code-block:: console

    integrate(f(t), t)

This returns,

.. math::
    \frac{{{t}^{3}}}{3}-\frac{3 {{t}^{2}}}{2}-18 t\mbox{}

Or we can follow the theory a little more closely,

.. code-block:: console

    integrate(f(x), x,0,t)

to arrive at the same result,

.. math::
    \frac{2 {{t}^{3}}-9 {{t}^{2}}-108 t}{6}\mbox{}

To get the displacement at 12 we could evaluate the above expression at 12 or take the following integral,

.. code-block:: console

    integrate(f(t), t,0,12)

Either way we end up with 144.  As for the total distance we can integrate,

.. code-block:: console

    integrate(abs(f(t)), t,0,12)

Unfortunately this just returns,

.. math::
    \int_{0}^{12}{\left. \left| {{t}^{2}}-3 t-18\right| dt\right.}\mbox{}

Since the breaking point is at 6 we can reformulate this ourselves into,

.. code-block:: console

    integrate(-f(t), t,0,6)+integrate(f(t), t,6,12);

to get the final answer of 324.
