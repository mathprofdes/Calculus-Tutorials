:index:`Motion in Space`
========================

Velocity, Speed, and Acceleration
---------------------------------

Velocity, speed, and acceleration of vector-valued functions is the same as they are for real-valued functions, the only difference is a vector quantity verses a scalar quantity.

.. admonition:: Definition: Velocity, Speed, and Acceleration

    Let :math:`\mathbf{r}(t)` be a vector-valued function that designates the position of an object at any moment in time and has both first and second derivatives. The velocity vector :math:`\mathbf{v}(t)` is given by

    .. math::
        \mathbf{v}(t) = \mathbf{r}'(t)

    The speed is defined to be

    .. math::
        |\mathbf{v}(t)| = |\mathbf{r}'(t)| = \frac{ds}{dt}

    The acceleration vector :math:`\mathbf{a}(t)` is given by

    .. math::
        \mathbf{a}(t) = \mathbf{v}'(t) = \mathbf{r}''(t)

Example: Rollercoaster Curve
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In this example we will find the velocity and acceleration vectors for a rollercoaster curve,

.. math::
    \left[\begin{array}{c}7 \cos{\left(t \right)}\\7 \sin{\left(t \right)}\\3 \sin{\left(4 t \right)} + 2 \cos{\left(3 t \right)}\end{array}\right]

.. figure:: Images/Motion/Motion001.png
    :alt: :math:`\left( 7 \cos{\left(t \right)}, \  7 \sin{\left(t \right)}, \  3 \sin{\left(4 t \right)} + 2 \cos{\left(3 t \right)}\right)`

    :math:`\left( 7 \cos{\left(t \right)}, \  7 \sin{\left(t \right)}, \  3 \sin{\left(4 t \right)} + 2 \cos{\left(3 t \right)}\right)`


CLAE
""""

First input the curve, we can use either direct input into the CAS or the vector input tool, either will work for this example.

.. code-block:: console

    [7*cos(t),7*sin(t),3*sin(4*t) + 2*cos(3*t)]

Graphing the curve gives us the above image. Taking the first and second derivatives of this vector-valued function gives us,

.. math::
    \mathbf{v}(t) = \left[\begin{array}{c}- 7 \sin{\left(t \right)}\\7 \cos{\left(t \right)}\\- 6 \sin{\left(3 t \right)} + 12 \cos{\left(4 t \right)}\end{array}\right] \qquad {\rm and } \qquad \mathbf{a}(t) = \left[\begin{array}{c}- 7 \cos{\left(t \right)}\\- 7 \sin{\left(t \right)}\\- 48 \sin{\left(4 t \right)} - 18 \cos{\left(3 t \right)}\end{array}\right]

To visualize these we will plot them on the graph of the curve.  Evaluate the curve as well as the velocity and acceleration vectors at *a*.

.. math::
    \mathbf{r}(a) = \left[\begin{array}{c}7 \cos{\left(a \right)}\\7 \sin{\left(a \right)}\\3 \sin{\left(4 a \right)} + 2 \cos{\left(3 a \right)}\end{array}\right] \qquad \mathbf{v}(a) = \left[\begin{array}{c}- 7 \sin{\left(a \right)}\\7 \cos{\left(a \right)}\\- 6 \sin{\left(3 a \right)} + 12 \cos{\left(4 a \right)}\end{array}\right] \qquad \mathbf{a}(a) = \left[\begin{array}{c}- 7 \cos{\left(a \right)}\\- 7 \sin{\left(a \right)}\\- 48 \sin{\left(4 a \right)} - 18 \cos{\left(3 a \right)}\end{array}\right]

Click and drag :math:`\mathbf{r}(a)` to the graph, this should come in as a point on the curve.  Also plot :math:`\mathbf{v}(a)` and :math:`\mathbf{a}(a)`, make sure to change these to vector sets and set their initial points to :math:`\mathbf{r}(a)` (using the CAS designation).

.. figure:: Images/Motion/Motion002.png
    :alt: Rollercoaster Curve with Velocity and Acceleration Vectors

    Rollercoaster Curve with Velocity and Acceleration Vectors

Use the *a* slider to get a feel for the velocity and acceleration vectors as the point moves along the curve.


Components of the Acceleration Vector
-------------------------------------

.. admonition:: Theorem: The Plane of the Acceleration Vector

    Let :math:`\mathbf{r}(t)` be a vector-valued function that designates the position of an object at any moment in time and has both first and second derivatives. The acceleration vector can be written as a linear combination of the unit tangent vector and the unit normal vector.  Hence the acceleration vector is in the plane formed by the unit tangent vector and the unit normal vector, the osculating plane.

    .. math::
        \mathbf{a}(t) = v'(t) \mathbf{T}(t) + (v(t))^2 \kappa \mathbf{N}(t)

    where :math:`v(t)` is the speed of the object and :math:`\kappa` is the curvature of the curve *C* defined by :math:`\mathbf{r}(t).`

The coefficients of :math:`\mathbf{T}(t)` and :math:`\mathbf{N}(t)` are referred to as the **tangential component of acceleration** and the **normal component of acceleration**, respectively. It is common to write :math:`a_{\mathbf{T}}` to denote the tangential component and :math:`a_{\mathbf{N}}` to denote the normal component. We will not go through the derivations of the following results, but it is another way to calculate the tangential and normal components of acceleration vector.

.. admonition:: Theorem: Tangential and Normal Components of Acceleration

    Let :math:`\mathbf{r}(t)` be a vector-valued function that designates the position of an object at any moment in time and has both first and second derivatives. The acceleration vector can be written as,

    .. math::
        \mathbf{a}(t) = a_{\mathbf{T}} \mathbf{T}(t) + a_{\mathbf{N}} \mathbf{N}(t)

    where

    .. math::
        a_{\mathbf{T}} = \frac{\mathbf{v}(t) \cdot \mathbf{a}(t)}{v(t)} \qquad {\rm and } \qquad a_{\mathbf{N}} = \frac{|\mathbf{v}(t) \times \mathbf{a}(t)|}{v(t)}


Example: Rollercoaster Curve
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In this example we will revisit the rollercoaster curve,

.. math::
    \left[\begin{array}{c}7 \cos{\left(t \right)}\\7 \sin{\left(t \right)}\\3 \sin{\left(4 t \right)} + 2 \cos{\left(3 t \right)}\end{array}\right]

.. figure:: Images/Motion/Motion001.png
    :alt: :math:`\left( 7 \cos{\left(t \right)}, \  7 \sin{\left(t \right)}, \  3 \sin{\left(4 t \right)} + 2 \cos{\left(3 t \right)}\right)`

    :math:`\left( 7 \cos{\left(t \right)}, \  7 \sin{\left(t \right)}, \  3 \sin{\left(4 t \right)} + 2 \cos{\left(3 t \right)}\right)`


CLAE
""""

First input the curve, we can use either direct input into the CAS or the vector input tool, either will work for this example.

.. code-block:: console

    [7*cos(t),7*sin(t),3*sin(4*t) + 2*cos(3*t)]

Graphing the curve gives us the above image. Taking the first and second derivatives of this vector-valued function gives us,

.. math::
    \mathbf{v}(t) = \left[\begin{array}{c}- 7 \sin{\left(t \right)}\\7 \cos{\left(t \right)}\\- 6 \sin{\left(3 t \right)} + 12 \cos{\left(4 t \right)}\end{array}\right] \qquad {\rm and } \qquad \mathbf{a}(t) = \left[\begin{array}{c}- 7 \cos{\left(t \right)}\\- 7 \sin{\left(t \right)}\\- 48 \sin{\left(4 t \right)} - 18 \cos{\left(3 t \right)}\end{array}\right]

and

.. math::
    v(t) = |\mathbf{v}(t)| = \sqrt{\left(- 6 \sin{\left(3 t \right)} + 12 \cos{\left(4 t \right)}\right)^{2} + 49 \sin^{2}{\left(t \right)} + 49 \cos^{2}{\left(t \right)}}

Calculating

.. math::
    \mathbf{v}(t) \cdot \mathbf{a}(t) = \left(36 \sin{\left(3 t \right)} - 72 \cos{\left(4 t \right)}\right) \left(8 \sin{\left(4 t \right)} + 3 \cos{\left(3 t \right)}\right)

so

.. math::
    a_{\mathbf{T}} = \frac{\mathbf{v}(t) \cdot \mathbf{a}(t)}{v(t)} = \frac{\left(36 \sin{\left(3 t \right)} - 72 \cos{\left(4 t \right)}\right) \left(8 \sin{\left(4 t \right)} + 3 \cos{\left(3 t \right)}\right)}{\sqrt{\left(- 6 \sin{\left(3 t \right)} + 12 \cos{\left(4 t \right)}\right)^{2} + 49 \sin^{2}{\left(t \right)} + 49 \cos^{2}{\left(t \right)}}}

and

.. math::
    \mathbf{v}(t) \times \mathbf{a}(t) = \left[\begin{array}{c}\left(- 42 \sin{\left(3 t \right)} + 84 \cos{\left(4 t \right)}\right) \sin{\left(t \right)} - \left(336 \sin{\left(4 t \right)} + 126 \cos{\left(3 t \right)}\right) \cos{\left(t \right)}\\\left(42 \sin{\left(3 t \right)} - 84 \cos{\left(4 t \right)}\right) \cos{\left(t \right)} - \left(336 \sin{\left(4 t \right)} + 126 \cos{\left(3 t \right)}\right) \sin{\left(t \right)}\\49\end{array}\right]

.. math::
    |\mathbf{v}(t) \times \mathbf{a}(t)| = \sqrt{\left(\left(- 42 \sin{\left(3 t \right)} + 84 \cos{\left(4 t \right)}\right) \sin{\left(t \right)} - \left(336 \sin{\left(4 t \right)} + 126 \cos{\left(3 t \right)}\right) \cos{\left(t \right)}\right)^{2} + \left(\left(42 \sin{\left(3 t \right)} - 84 \cos{\left(4 t \right)}\right) \cos{\left(t \right)} - \left(336 \sin{\left(4 t \right)} + 126 \cos{\left(3 t \right)}\right) \sin{\left(t \right)}\right)^{2} + 2401}

so

.. math::
    \qquad a_{\mathbf{N}} = \frac{\mathbf{v}(t) \times \mathbf{a}(t)}{v(t)} = \frac{\sqrt{\left(\left(- 42 \sin{\left(3 t \right)} + 84 \cos{\left(4 t \right)}\right) \sin{\left(t \right)} - \left(336 \sin{\left(4 t \right)} + 126 \cos{\left(3 t \right)}\right) \cos{\left(t \right)}\right)^{2} + \left(\left(42 \sin{\left(3 t \right)} - 84 \cos{\left(4 t \right)}\right) \cos{\left(t \right)} - \left(336 \sin{\left(4 t \right)} + 126 \cos{\left(3 t \right)}\right) \sin{\left(t \right)}\right)^{2} + 2401}}{\sqrt{\left(- 6 \sin{\left(3 t \right)} + 12 \cos{\left(4 t \right)}\right)^{2} + 49 \sin^{2}{\left(t \right)} + 49 \cos^{2}{\left(t \right)}}}

