:index:`Stokes' Theorem`
========================

Discussion & Definitions
------------------------

Stokes’ theorem says we can calculate the flux of :math:`{\rm curl}(\mathbf{F})` across surface *S* by just knowing the values of :math:`\mathbf{F}` along the boundary of *S*. Conversely, we can calculate the line integral of vector field :math:`\mathbf{F}` along the boundary of a surface *S* by translating it to a double integral of :math:`{\rm curl}(\mathbf{F})` over *S*.


.. admonition:: Definition: Positive Orientation

    Let *S* be an oriented smooth surface with unit normal vector :math:`\mathbf{N}.` Furthermore, suppose the boundary of *S* is a simple closed curve *C*. The orientation of *S* induces the positive orientation of *C* if, as you walk in the positive direction around *C* with your head pointing in the direction of :math:`\mathbf{N},` the surface is always on your left.

.. admonition:: Theorem: Stokes' Theorem

    Let *S* be a piecewise smooth oriented surface with a boundary that is a simple closed curve *C* with positive orientation. If :math:`\mathbf{F}` is a vector field with component functions that have continuous partial derivatives on an open region containing *S*, then

    .. math::
        \int_C \mathbf{F} \cdot d\mathbf{r} = \iint_S {\rm curl}(\mathbf{F}) \cdot d\mathbf{S}

Example
-------

In this example we will let :math:`\mathbf{F}(x, y, z) = (-x y^2, x z, y^2 z^3)` and we will let *C* be the curve of intersection between the plane :math:`z = 2-y` and the cylinder :math:`x^2+y^2=1` moving counterclockwise if viewed from above.  We will find,

.. math::
    \int_C \mathbf{F} \cdot d\mathbf{r}

CLAE
^^^^

First we will get a visualization of the curve *C*. Input

.. code-block:: console

    2 - y

and

.. code-block:: console

    x^2 + y^2 - 1

Click and drag both over to the 3D graphics window.  Leave the first on as a function and change the second to an implicit plot.  If we also change the second to a grid instead of a surface, and zoom in, we see,

.. figure:: Images/VecCalc/Stokes001.png
    :alt: The Curve *C*

    The Curve *C*

By Stokes' Theorem we can turn this line integral into a surface integral and we can use any surface that has *C* as a boundary.  We will take the obvious surface of the plane used to construct *C*, :math:`z = g(x, y) = 2-y.`  The domain this integral is over is the unit disk.  Input the vector field,

.. code-block:: console

    [-x*y^2,x*z,y^2*z^3]

Find its curl with ``Calculus > Vector Calculus > Curl``, the result is,

.. math::
    \left[\begin{array}{c}- x + 2 y z^{3}\\0\\2 x y + z\end{array}\right]

using,

.. math::
    \int_C \mathbf{F} \cdot d\mathbf{r} & = \iint_S {\rm curl}(\mathbf{F}) \cdot d\mathbf{S} = \iint_D \left( -P \frac{\partial g}{\partial x} - Q \frac{\partial g}{\partial y} + R \right) \; dA \\
    & = \iint_D  2 x y + z \; dA \\
    & = \iint_D  2 x y + 2-y \; dA \\
    & = \int_0^{2\pi} \int_0^1  (2 r \cos(\theta) r \sin(\theta) + 2-r \sin(\theta)) r \; dr \; d\theta \\

Input the integrand,

.. code-block:: console

    r*(2*r^2*sin(t)*cos(t) - r*sin(t) + 2)

Now do the double integral with ``Calculus > Multiple Integrals > Double Integral``, first variable ``r`` with bounds ``0`` and ``1``, and second variable ``t`` with bounds ``0`` and ``2*pi``.  The result is, :math:`2\pi.`

.. note::

    Stokes’ Theorem allows us to compute a surface integral simply by knowing the values of :math:`\mathbf{F}` on the boundary curve *C*. SO if we have two surfaces :math:`S_1` and :math:`S_2` with the same boundary curve, and the other conditions of Stokes' Theorem are satisfied, then,

    .. math::
        \iint_{S_1} {\rm curl}(\mathbf{F}) \cdot d\mathbf{S} = \iint_{S_2} {\rm curl}(\mathbf{F}) \cdot d\mathbf{S}

    This can be used to simplify the integration by choosing another surface.
