:index:`Volumes by Slicing`
===========================

Discussion & Definitions
------------------------

Just like the area between two curves, this is a good introductory exercise in going through the process of representing a quantity as the limit of a Riemann sum and hence establishing that it is a definite integral.  This is a good exercise to do since many quantities in the physical sciences and economics (among others) can be represented this way, but we will leave the details to the textbook you are using.

.. admonition:: Theorem: Finding the Volume of an Object by Cross Sections

    If :math:`A(x)` represents the cross sectional area of an object that extends from :math:`x = a` to :math:`x = b` then the volume of the object is given by

    .. math::
        V = \int_a^b A(x) \; dx


The above theorem is called the **slicing method**.

.. admonition:: Problem Solving: Finding Volumes by the Slicing Method

    1. Examine the solid, put an x-axis along the object so that the cross sections perpendicular to the axis form a familiar shape, circle, rectangle, triangle, etc.
    2. Determine a formula for the area of the cross-section at any point *x* on the axis, :math:`A(x)`.
    3. Integrate the area formula over the appropriate interval to get the volume.

    .. math::
        V = \int_a^b A(x) \; dx

    .. figure:: Images/Apps/CrossArea001.png
        :alt: Cross-Section Visualization

        Cross-Section Visualization

Example: Volume of a Right Tetrahedron
--------------------------------------

Find the volume of the given right tetrahedron.

.. figure:: Images/Apps/CrossArea002.png
    :alt: Example Visualization

    Example Visualization

First we will take a cross section perpendicular to the *x*-axis at a point *x*.  The cross section is a right triangle with base length *b* and height *a*.

.. figure:: Images/Apps/CrossArea003.png
    :alt: Example Visualization

    Example Visualization

The area of the cross section triangle is,

.. math::
    A = \frac{1}{2}ab

We can find *a* and *b* in terms of *x* by using similar triangles.  Looking at the triangle containing *a* we have,

.. math::
    \frac{5-x}{a} = \frac{5}{3}

so

.. math::
    a = \frac{3}{5}(5-x)

Doing the same with the triangle containing *b* we have,

.. math::
    \frac{5-x}{b} = \frac{5}{4}

so

.. math::
    b = \frac{4}{5}(5-x)

and hence,

.. math::
    A(x) = \frac{1}{2}ab = \frac{1}{2} \left( \frac{3}{5}(5-x) \right) \left( \frac{4}{5}(5-x) \right) = \frac{6 \left(x - 5\right)^{2}}{25}

The interval we need to integrate over is :math:`[0, 5]`, hence the volume is,

.. math::
    V = \int_0^5 \frac{6 \left(x - 5\right)^{2}}{25} \; dx = 10

GeoGebra
^^^^^^^^

The majority of these types of exercises are done by hand but the CAS can com in handy if there are difficult integrals to take at the end or if there are complex simplifications that need to be done. In this exercise there is really neither but we will do the last integral.

Input the function,

.. code-block:: console

    6 (x - 5)^2/25

Select a new cell and input ``Integral(f, 0, 5)``.  The result will be 10.

CLAE
^^^^

The majority of these types of exercises are done by hand but the CAS can com in handy if there are difficult integrals to take at the end or if there are complex simplifications that need to be done. In this exercise there is really neither but we will do the last integral.

Input the function,

.. code-block:: console

    6*(x - 5)^2/25

Select ``Calculus > Definite Integral``, using the 0 and 5 bounds.  The result will be 10.

Maxima
^^^^^^

The majority of these types of exercises are done by hand but the CAS can com in handy if there are difficult integrals to take at the end or if there are complex simplifications that need to be done. In this exercise there is really neither but we will do the last integral.

Input the function,

.. code-block:: console

    kill(all);
    f(x):=6*(x - 5)^2/25

then integrate with,

.. code-block:: console

    integrate(f(x),x,0,5)

The result will be 10.

Example: Volume of a General Right Tetrahedron
----------------------------------------------

Find the volume of the given general right tetrahedron.  This is just an extension of the example above and is done in the same manner.

.. figure:: Images/Apps/CrossArea004.png
    :alt: Example Visualization

    Example Visualization

First we will take a cross section perpendicular to the *x*-axis at a point *x*.  The cross section is a right triangle with base length *k* and height *h*.

.. figure:: Images/Apps/CrossArea005.png
    :alt: Example Visualization

    Example Visualization

The area of the cross section triangle is,

.. math::
    A = \frac{1}{2}hk

We can find *h* and *k* in terms of *x* by using similar triangles.  Looking at the triangle containing *h* we have,

.. math::
    \frac{a-x}{h} = \frac{a}{b}

so

.. math::
    h = \frac{b}{a}(a-x)

Doing the same with the triangle containing *k* we have,

.. math::
    \frac{a-x}{k} = \frac{a}{c}

so

.. math::
    k = \frac{c}{a}(a-x)

and hence,

.. math::
    A(x) = \frac{1}{2}hk = \frac{1}{2} \left( \frac{b}{a}(a-x) \right) \left( \frac{c}{a}(a-x) \right) = \frac{bc(a-x)^2}{2a^2}

The interval we need to integrate over is :math:`[0, a]`, hence the volume is,

.. math::
    V = \int_0^a \frac{bc(a-x)^2}{2a^2} \; dx = \frac{a b c}{6}

CLAE
^^^^

Again this is an easy integral but we will use the CAS just for practice.

Input the function,

.. code-block:: console

    b*c*(a - x)^2/(2*a^2)

Then select ``Calculus > Definite Integral``, variable *x*, lower bound 0 and upper bound *a*.  The result is

.. math::
    \frac{a b c}{6}


Maxima
^^^^^^

Again this is an easy integral but we will use the CAS just for practice.

Input the function,

.. code-block:: console

    kill(all);
    f(x):=b*c*(a - x)^2/(2*a^2)

Then integrate with,

.. code-block:: console

    integrate(f(x), x, 0, a)

The result is

.. math::
    \frac{a b c}{6}
