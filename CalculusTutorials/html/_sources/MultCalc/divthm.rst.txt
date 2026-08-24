:index:`The Divergence Theorem`
===============================


Discussion & Definitions
------------------------

.. admonition:: Definition: Simple Solid Region

    Regions that are simultaneously of Types I, II, and III are called simple solid regions.  For example, regions bounded by ellipsoids or rectangular boxes are simple solid regions.

.. admonition:: Theorem: The Divergence Theorem

    Let *E* be a simple solid region and let *S* be the boundary surface of *E*, given with positive (outward) orientation. Let :math:`\mathbf{F}` be a vector field whose component functions have continuous partial derivatives on an open region that contains *E*. Then

    .. math::
        \iint_S \mathbf{F} \cdot d\mathbf{S} = \iiint_E {\rm div}(\mathbf{F}) \; dV



Example
^^^^^^^

In this example we will find,

.. math::
    \iint_S \mathbf{F} \cdot d\mathbf{S}

where

.. math::
    \mathbf{F} = \left( x y, \  y^{2} \sin{\left(x \right)}, \  z e^{x}\right)

and *S* is the surface of the region *E* bounded by :math:`z = 1 - x^2`, the planes :math:`z = 0`, :math:`y = 0`, and :math:`y = 2-z.`  The region is pictured below.

.. figure:: Images/VecCalc/DivThm001.png
    :alt: The Region *E*

    The Region *E*

Since the conditions of the divergence theorem are satisfied we can complete this calculation by,

.. math::
    \iint_S \mathbf{F} \cdot d\mathbf{S} = \iiint_E {\rm div}(\mathbf{F}) \; dV

CLAE
""""

Input the vector field,

.. code-block:: console

    [x*y,y^2*sin(x),z*exp(x)]

Select ``Calculus > Vector Calculus > Divergence``, the variables should default to ``[x, y, z]``, keep these as is.  The result should be,

.. math::
    2 y \sin{\left(x \right)} + y + e^{x}

This will be the integrand to our triple integral.  We wll treat this region as a Type III region and then the integral we need to calculate is,

.. math::
    \int_{-1}^{1} \int_0^{1-x^2} \int_0^{2-z} 2 y \sin{\left(x \right)} + y + e^{x} \; dy \; dz\; dx

Select the integrand, then select ``Calculus > Multiple Integrals > Triple Integral``, the first variable is ``y`` with bounds ``0`` and ``2-z``, the second variable is ``z`` with bounds ``0`` and ``1-x^2``, the third variable is ``x`` with bounds ``-1`` and ``1``.  The result is,

.. math::
    - 4 e + \frac{184}{105} + \frac{36}{e} \approx 4.122913520716695017


