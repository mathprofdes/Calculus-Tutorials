:index:`Green's Theorem`
========================

Green's Theorem gives the relationship between a line integral around a simple closed curve and a double integral over the plane region bounded by the curve.

Orientation
-----------

.. admonition:: Definition: Positive and Negative Orientation

    Say we have a simple closed curve *C* that encloses a region *D*. We say that *C* has positive orientation if the traversal around *C* is counterclockwise.  That is, if we walk around the curve *C* the region *D* is always on our left.

    .. figure:: Images/VecCalc/Green001.png
        :alt: Positive Orientation

        Positive Orientation

    Similarly, *C* has a negative orientation if the traversal around *C* is clockwise.  That is, if we walk around the curve *C* the region *D* is always on our right.

    .. figure:: Images/VecCalc/Green002.png
        :alt: Negative Orientation

        Negative Orientation

Green's Theorem
---------------

.. admonition:: Theorem: Green's Theorem

    If *C* is a positively oriented, piecewise-smooth, simple closed curve and *D* is the region bounded by the curve *C*. If :math:`\mathbf{F} = (P, Q)` where *P* and *Q* have continuous partial derivatives on an open region containing *D*, then

    .. math::
        \oint_C \mathbf{F} \cdot d\mathbf{r} = \oint_C P \; dx + Q \; dy = \iint_D \left( \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} \right) \; dA


.. note::

    The notation,

    .. math::
        \oint_C P \; dx + Q \; dy

    is the same as

    .. math::
        \int_C P \; dx + Q \; dy

    The circle on the integral sign is sometimes used to represent an integral on a positively oriented closed curve *C*.

Example: Green's Theorem
^^^^^^^^^^^^^^^^^^^^^^^^

In this example we are going to calculate the line integral,

.. math::
    \oint_C x^2y^3 \; dx + \cos(x)e^y \; dy

where *C* is the positively oriented rectangle with vertices :math:`(1, 1)`, :math:`(5, 1)`, :math:`(5, 3)`, :math:`(1, 3)`.

.. math::
    P &= x^2y^3 \\
    Q &= \cos(x)e^y \\
    P_y &= 3x^2y^2 \\
    Q_x &= -\sin(x)e^y \\

So the integral is,

.. math::
    \oint_C x^2y^3 \; dx + \cos(x)e^y \; dy = \int_1^3 \int_1^5 -\sin(x)e^y - 3x^2y^2 \; dx \; dy

CLAE
""""

We could have used the CAS to help with the derivatives but they are easy to do in this example.  For the final integral, also easy to do, input,

.. code-block:: console

    -3*x^2*y^2 - exp(y)*sin(x)

Then select ``Calculus > Multiple Integrals > Double Integral``, first variable is x with bounds ``1`` and ``5``, the second variable is ``y`` with bounds ``1`` and ``3``, the result is,

.. math::
    - \frac{3224}{3} + \left(- \cos{\left(1 \right)} + \cos{\left(5 \right)}\right) e^{3} - e \left(- \cos{\left(1 \right)} + \cos{\left(5 \right)}\right) \approx -1079.1238011052806669

Note how much work this has saved.  If we had done the line integral we would have had to break the integral up into four integrals, one for each line segment, parameterize each line segment, and do the four integrals.  Green's theorem reduced all of this to a simple double integral.

Green's Theorem on General Regions
----------------------------------

Green's Theorem, as stated, does not apply to regions like region *D* in the image below.  It can easily be extended to regions of this type.

.. figure:: Images/VecCalc/Green003.png
    :alt: General Region

    General Region

If we cut the region through the internal holes maintaining a positive orientation note that the line integrals in the cuts will cancel out and

.. math::
    \oint_C \mathbf{F} \cdot d\mathbf{r} & = \oint_{C_1} \mathbf{F} \cdot d\mathbf{r} + \oint_{C_2} \mathbf{F} \cdot d\mathbf{r} \\
    & = \iint_{A} (Q_x - P_y) \; dA + \iint_{B} (Q_x - P_y) \; dA \\
    & = \iint_{D} (Q_x - P_y) \; dA

So, Green's theorem also holds for regions that have a finite number of holes in them as long as the holes are positively oriented, that is, the region is on the left.


Example: Green's Theorem on a General Region
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In this exercise we will be finding the integral,

.. math::
    \oint_C \left( \sin(x^2) - \frac{y^3}{3} \right) \; dx + \left( \frac{x^3}{3} + e^{\sqrt{y}} \right) \; dy

where *C* is the positively oriented curve enclosing the region *D* in the image below.

.. figure:: Images/VecCalc/Green004.png
    :alt: Region *D*

    Region *D*

.. math::
    P &= \sin(x^2) - \frac{y^3}{3} \\
    Q &= \frac{x^3}{3} + e^{\sqrt{y}} \\
    P_y &= -y^2 \\
    Q_x &= x^2 \\

So the integral is,

.. math::
    \oint_C \left( \sin(x^2) - \frac{y^3}{3} \right) \; dx + \left( \frac{x^3}{3} + e^{\sqrt{y}} \right) \; dy & = \iint_D x^2+y^2 \; dA \\
    & = \int_0^{2\pi} \int_1^2 r^3 \; dr \; d\theta \\
    & = \frac{15 \pi}{2}

Once again this saved us a significant amount of work and some nasty integrals.
