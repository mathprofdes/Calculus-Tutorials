:index:`Volumes of Revolution by Cylindrical Shells`
====================================================

Discussion & Definitions
------------------------

As with the disk ans washer method discussed in the precious section the method of cylindrical shells is for finding the volume of a solid of revolution.  Depending on the curve or region being revolved this method may be easier to calculate than using disks or washers.  There are two big differences between this method and the disk and washer method.

- Here we are adding up the volumes of thin cylinders and not volumes of thin disks.
- Here we integrate along the coordinate axis perpendicular to the axis of revolution and not parallel to it as with disks and washers.


.. admonition:: Theorem: The Method of Cylindrical Shells

    Let :math:`f(x)` be continuous and nonnegative. Define :math:`R` as the region bounded above by the graph of :math:`f(x)`, below by the *x*-axis, on the left by the line :math:`x = a`, and on the right by the line :math:`x = b`. Then the volume of the solid of revolution formed by revolving :math:`R` around the *y*-axis is given by

    .. math::
        V = \int_a^b 2\pi x f(x) \; dx

    .. figure:: Images/Apps/CylShell001.png
        :alt: Cylindrical Shell Method Visualization

        Cylindrical Shell Method Visualization


.. note::

    We can revolve the curve around other axes, using the *x*-axis is simply interchanging the roles of *x* and *y*, given specifically below.  We can also rotate the curve around axes :math:`x = c` and :math:`y = c`.  In these cases it iw best not to try to use the formula above but thing of it as

    .. math::
        \int 2\pi r y dx

    Where :math:`r` is the radius (or formula for the radius) of the cylindrical slice and :math:`y` is the height (or formula for the height) of the cylindrical slice.


.. admonition:: Theorem: The Method of Cylindrical Shells for Solids of Revolution around the *x*-axis

    Let :math:`g(y)` be continuous and nonnegative. Define :math:`Q` as the region bounded on the right by the graph of :math:`g(y)`, on the left by the *y*-axis, below by the line :math:`y = c`, and above by the line :math:`y = d`. Then, the volume of the solid of revolution formed by revolving :math:`Q` around the *x*-axis is given by

    .. math::
        V = \int_c^d 2\pi y g(y) \; dy


Example: :math:`f(x) = 2x − x^2`
--------------------------------

Define :math:`R` as the region bounded above by the graph of :math:`f(x) = 2x − x^2` and below by the *x*-axis over the interval :math:`[0, 2]`. Find the volume of the solid of revolution formed by revolving :math:`R` around the *y*-axis.

.. math::
    V = \int_0^2 2\pi x (2x − x^2) \; dx = \frac{8 \pi}{3}

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    2 pi x (2x - x^2)

Then integrate with ``Integral(f,0,2)``.  The result is, 8.37758.

CLAE
^^^^

Input the function,

.. code-block:: console

    2*pi*x*(2*x - x^2)

Then select ``Calculus > Definite Integral``, lower bound of 0 and upper bound of 2 results in :math:`\frac{8 \pi}{3}`.

To get a visual of the solid, select the 3-D Graphics tab.  Click and drag the expression over to the graph.  Change the type to Surface of Revolution.  Click on the settings tool, change the dependent variable to *z*, and the function start and end to 0 and 2.  You may want to scale the *xy*-plane a little to see,

.. figure:: Images/Apps/CylShell002.png
    :alt: y = 2x-x^2

    :math:`f(x) = 2x − x^2`

Maxima
^^^^^^

Input the function,

.. code-block:: console

    kill(all);
    cs:2*%pi*x*(2*x - x^2)

Then

.. code-block:: console

    integrate(cs, x, 0, 2)

The result is :math:`\frac{8 \pi}{3}`.
