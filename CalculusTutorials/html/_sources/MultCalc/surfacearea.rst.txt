:index:`Surface Area`
=====================

Discussion & Definitions
------------------------

The formula for the area of a surface over a domain *D* is not difficult to derive and it is very similar to the derivation of the arc-length of a curve, as is the result.  We will leave the derivation to your textbook.

.. admonition:: Theorem: Surface Area

    The area of a surface :math:`z = f(x, y)` over a region *R* where both partial derivatives :math:`f_x` and :math:`f_y` are continuous is,

    .. math::
        A(S) = \iint_R \sqrt{(f_x(x, y))^2 + (f_y(x, y))^2 + 1} \; dA = \iint_R \sqrt{ 1 + \left(\frac{\partial z}{\partial x}\right)^2 + \left(\frac{\partial z}{\partial y}\right)^2} \; dA


Example: Surface Area of a Portion of a Sphere
----------------------------------------------

In this exercise we will find the surface area of the portion of the sphere :math:`x^2 + y^2 + z^2 = 4` that lies above the plane :math:`z = 1.`

CLAE
^^^^

Input the expression for the surface, equal to 0,

.. code-block:: console

    x^2 + y^2 + z^2 - 4

Also input ``1``. Graph both of these in the 3D graphics window.

.. figure:: Images/MultInt/DoublePolar012.png
    :alt: :math:`x^2 + y^2 + z^2 = 4` and :math:`z = 1`

    :math:`x^2 + y^2 + z^2 = 4` and :math:`z = 1`

So the surface area we want is the cap on the top of the sphere.   To get the bounds on this surface we need to find the intersection of the two surfaces.  Substituting :math:`z = 1` into :math:`x^2 + y^2 + z^2 = 4` gives us :math:`x^2 + y^2 = 3` which is a circle of radius :math:`\sqrt{3}` centered at the origin.  Input,

.. code-block:: console

    x^2 + y^2 - 3

Graph this in the 3D window, change its type to Implicit Relationship and its plot to grid.

.. figure:: Images/MultInt/DoublePolar013.png
    :alt: :math:`x^2 + y^2 + z^2 = 4` and :math:`z = 1`

    :math:`x^2 + y^2 + z^2 = 4` and :math:`z = 1`

Now we proceed with the calculations.  Since we are looking at the top half of the sphere we can rewrite the implicit relationship as,

.. math::
    z = \sqrt{- x^{2} - y^{2} + 4}

then using the derivative option,

.. math::
    \frac{\partial z}{\partial x} = - \frac{x}{\sqrt{- x^{2} - y^{2} + 4}} \qquad {\rm and } \qquad \frac{\partial z}{\partial y} = - \frac{y}{\sqrt{- x^{2} - y^{2} + 4}}

So our integrand is,

.. math::
    \sqrt{ 1 + \left(\frac{\partial z}{\partial x}\right)^2 + \left(\frac{\partial z}{\partial y}\right)^2} = \sqrt{\frac{x^{2}}{- x^{2} - y^{2} + 4} + \frac{y^{2}}{- x^{2} - y^{2} + 4} + 1} = 2 \sqrt{- \frac{1}{x^{2} + y^{2} - 4}}

The region that we are integrating over is a circle (disk) which would suggest using polar coordinates.  We will first try rectangular coordinates.  Approaching this as a Type I region, the *y* bounds would be :math:`- \sqrt{3 - x^{2}}` to :math:`\sqrt{3 - x^{2}}` and the *x* bounds would be :math:`- \sqrt{3}` to :math:`\sqrt{3}.`  So the integral would be,

.. math::
    2 \int\limits_{- \sqrt{3}}^{\sqrt{3}}\int\limits_{- \sqrt{3 - x^{2}}}^{\sqrt{3 - x^{2}}} \sqrt{- \frac{1}{x^{2} + y^{2} - 4}}\, dy\, dx

If we try this in CLAE it will return the integral, unsolved.  If we take the time to convert this to polar coordinates, as we thought above, we get an integrand of,

.. math::
    2 \sqrt{\frac{1}{4 - r^{2}}}

and a polar integral of,

.. math::
    \int_0^{2\pi} \int_0^{\sqrt{3}} 2 r \sqrt{\frac{1}{4 - r^{2}}} \; dr \; d\theta

This is an easy substitution that we could do by hand but inputting this into CLAE and taking the double integral gives us the result of :math:`4\pi.`

Maxima
^^^^^^

We can also solve the polar integral in Maxima but additionally, Maxima is powerful enough to calculate the double integral given in rectangular coordinates.  Inputting,

.. code-block:: console

    integrate(integrate(2*sqrt(-1/(x**2 + y**2 - 4)), y, -sqrt(3 - x**2), sqrt(3 - x**2)), x, -sqrt(3), sqrt(3));

will return the value of :math:`4\pi.`
