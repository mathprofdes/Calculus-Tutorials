:index:`Quadric Surfaces`
=========================

:index:`Cylinders`
------------------

.. admonition:: Definition: Cylinders

    A **cylinder** is a surface that consists of all lines (called **rulings**) that are parallel to a given line and pass through a given plane curve.

Note that cylindrical surfaces are sometimes called sheets or curtains.

Example: :math:`y = \sin(x)`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In this example we will graph the cylinder formed by the function :math:`y = \sin(x).`  Note that this is a function of a single variable, which is common for cylindrical surfaces.  The way we interpret this as a cylindrical surface is that we graph the function on the *xy*-plane and then we take all lines parallel to the *z*-axis pass through the curve.  A graph is below,

.. figure:: Images/quadsurf/quadsurf001.png
    :alt: :math:`y = \sin(x)` Cylinder

    :math:`y = \sin(x)` Cylinder

You can see why these are sometimes called sheets or curtains.

GeoGebra
""""""""

In GeoGebra, to graph a cylindrical surface we must first convert the surface equation into parametric form.  The surface :math:`y = \sin(x)` can easily be rewritten as :math:`(u, \sin(u), v).` Just make the independent variable *u*, the dependent variable is the function, and the third variable is simply *v*.  Once you hve done this we can use the ``Surface`` command in GeoGebra to plot the surface.

.. code-block::

    Surface(u,sin(u),v,u,-10,10,v,-10,10)

.. figure:: Images/quadsurf/quadsurf003.png
    :alt: :math:`y = \sin(x)` Cylinder

    :math:`y = \sin(x)` Cylinder


CLAE
""""

In CLAE, we input the function,

.. code-block:: console

    sin(x)

Click and drag this over to the 3D graphics window and you should see the image,

.. figure:: Images/quadsurf/quadsurf001.png
    :alt: :math:`y = \sin(x)` Cylinder

    :math:`y = \sin(x)` Cylinder

Note that CLAE does not force the user to specify the dependent variable of the function.  We interpreted :math:`\sin(x)` as :math:`y = \sin(x)` but it could have just as easily been :math:`z = \sin(x)` and we would take the lines parallel to the *y*-axis.  To graph this cylinder go into the properties for the function sheet and change the dependent variable from *y* to *z*.  We will get the following image.

.. figure:: Images/quadsurf/quadsurf002.png
    :alt: :math:`z = \sin(x)` Cylinder

    :math:`z = \sin(x)` Cylinder


Quadric Surfaces
----------------

.. admonition:: Definition: Quadric Surfaces

    Quadric surfaces are the graphs of equations that can be expressed in the form

    .. math::
        Ax^2 + By^2 + Cz^2 + Dxy + Exz + Fyz + Gx + Hy + Jz + K = 0

    where :math:`A, B, C, D, E, F, G, H, J, K` are all constants.

In general, this can be quite complex.  Using some translations and rotations the general form above can be reduced to just a few similar expressions, we will look at a few of them here.  Also note that the above expression is given implicitly.  In same cases we can rewrite the expression explicitly.

Example: :index:`Ellipsoid`
^^^^^^^^^^^^^^^^^^^^^^^^^^^

An ellipsoid is a surface defined by

.. math::
    \frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1

Note that if :math:`a = b = c` then this expression reduces to :math:`x^2 + y^2 + z^2 = a^2` which is a sphere.

GeoGebra
""""""""

To graph an ellipsoid in GeoGebra we input the expression just like you would write it mathematically. A quick version is below,

.. code-block:: console

    x^2/a^2+y^2/b^2+z^2/c^2=1

When this is input, GeoGebra will create sliders for the constants :math:`a, b, c` and the plot will look like.

.. figure:: Images/quadsurf/quadsurf004.png
    :alt: Ellipsoid

    Ellipsoid

By adjusting the sliders you can experiment with the shape of the ellipsoid.

.. figure:: Images/quadsurf/quadsurf005.png
    :alt: Ellipsoid

    Ellipsoid


CLAE
"""""

To graph an ellipsoid in CLAE we input the expression just like you would write it mathematically, except that we first make it an equation with 0.

.. math::
    \frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} - 1 = 0

and then we drop the ``= 0``.

.. math::
    \frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} - 1


A quick version is below,

.. code-block:: console

    x^2/a^2+y^2/b^2+z^2/c^2-1

When this is input, CLAE will create sliders for the constants :math:`a, b, c` and the plot will look like.

.. figure:: Images/quadsurf/quadsurf006.png
    :alt: Ellipsoid

    Ellipsoid

By adjusting the sliders you can experiment with the shape of the ellipsoid.

.. figure:: Images/quadsurf/quadsurf007.png
    :alt: Ellipsoid

    Ellipsoid


Example: :index:`Hyperboloid of One Sheet`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A hyperboloid of one sheet is a surface defined by

.. math::
    \frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} = 1


GeoGebra
""""""""

To graph a hyperboloid of one sheet in GeoGebra we input the expression just like you would write it mathematically. A quick version is below,

.. code-block:: console

    x^2/a^2+y^2/b^2-z^2/c^2=1

When this is input, GeoGebra will create sliders for the constants :math:`a, b, c` and the plot will look like.

.. figure:: Images/quadsurf/quadsurf008.png
    :alt: Hyperboloid of One Sheet

    Hyperboloid of One Sheet

By adjusting the sliders you can experiment with the shape of the hyperboloid.

.. figure:: Images/quadsurf/quadsurf009.png
    :alt: Hyperboloid of One Sheet

    Hyperboloid of One Sheet


CLAE
"""""

To graph a hyperboloid of one sheet in CLAE we input the expression just like you would write it mathematically, except that we first make it an equation with 0.

.. math::
    \frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} - 1 = 0

and then we drop the  ``= 0``.

.. math::
    \frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} - 1


A quick version is below,

.. code-block:: console

    x^2/a^2+y^2/b^2-z^2/c^2-1

When this is input, CLAE will create sliders for the constants :math:`a, b, c` and the plot will look like.

.. figure:: Images/quadsurf/quadsurf010.png
    :alt: Hyperboloid of One Sheet

    Hyperboloid of One Sheet

By adjusting the sliders you can experiment with the shape of the hyperboloid.

.. figure:: Images/quadsurf/quadsurf011.png
    :alt: Hyperboloid of One Sheet

    Hyperboloid of One Sheet



Example: :index:`Hyperboloid of Two Sheets`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A hyperboloid of two sheets is a surface defined by

.. math::
    - \frac{x^2}{a^2} - \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1


GeoGebra
""""""""

To graph a hyperboloid of two sheets in GeoGebra we input the expression just like you would write it mathematically. A quick version is below,

.. code-block:: console

    -x^2/a^2-y^2/b^2+z^2/c^2=1

When this is input, GeoGebra will create sliders for the constants :math:`a, b, c` and the plot will look like.

.. figure:: Images/quadsurf/quadsurf012.png
    :alt: Hyperboloid of Two Sheets

    Hyperboloid of Two Sheets

By adjusting the sliders you can experiment with the shape of the hyperboloid.

.. figure:: Images/quadsurf/quadsurf013.png
    :alt: Hyperboloid of Two Sheets

    Hyperboloid of Two Sheets


CLAE
"""""

To graph a hyperboloid of one sheet in CLAE we input the expression just like you would write it mathematically, except that we first make it an equation with 0.

.. math::
    -\frac{x^2}{a^2} - \frac{y^2}{b^2} + \frac{z^2}{c^2} - 1 = 0

and then we drop the ``= 0``.

.. math::
    -\frac{x^2}{a^2} - \frac{y^2}{b^2} + \frac{z^2}{c^2} - 1


A quick version is below,

.. code-block:: console

    -x^2/a^2-y^2/b^2+z^2/c^2-1

When this is input, CLAE will create sliders for the constants :math:`a, b, c` and the plot will look like.

.. figure:: Images/quadsurf/quadsurf014.png
    :alt: Hyperboloid of Two Sheets

    Hyperboloid of Two Sheets

By adjusting the sliders you can experiment with the shape of the hyperboloid.

.. figure:: Images/quadsurf/quadsurf015.png
    :alt: Hyperboloid of Two Sheets

    Hyperboloid of Two Sheets



Example: :index:`Hyperbolic Paraboloid`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A hyperbolic paraboloid is a surface defined by

.. math::
    \frac{z}{c} = \frac{x^2}{a^2} - \frac{y^2}{b^2}


GeoGebra
""""""""

To graph a hyperbolic paraboloid in GeoGebra we input the expression just like you would write it mathematically. A quick version is below,

.. code-block:: console

    z/c=x^2/a^2-y^2/b^2

When this is input, GeoGebra will create sliders for the constants :math:`a, b, c` and the plot will look like.

.. figure:: Images/quadsurf/quadsurf016.png
    :alt: Hyperbolic Paraboloid

    Hyperbolic Paraboloid

By adjusting the sliders you can experiment with the shape of the paraboloid.

.. figure:: Images/quadsurf/quadsurf017.png
    :alt: Hyperbolic Paraboloid

    Hyperbolic Paraboloid


CLAE
"""""

To graph a hyperbolic paraboloid in CLAE we input the expression just like you would write it mathematically, except that we first make it an equation with 0.

.. math::
    -\frac{z}{c} + \frac{x^2}{a^2} - \frac{y^2}{b^2} = 0

and then we drop the ``= 0``.

.. math::
    -\frac{z}{c} + \frac{x^2}{a^2} - \frac{y^2}{b^2}


A quick version is below,

.. code-block:: console

    x^2/a^2-y^2/b^2-z/c

When this is input, CLAE will create sliders for the constants :math:`a, b, c` and the plot will look like.

.. figure:: Images/quadsurf/quadsurf018.png
    :alt: Hyperbolic Paraboloid

    Hyperbolic Paraboloid

By adjusting the sliders you can experiment with the shape of the paraboloid.

.. figure:: Images/quadsurf/quadsurf019.png
    :alt: Hyperbolic Paraboloid

    Hyperbolic Paraboloid



Example: :index:`Elliptic Paraboloid`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

An elliptic paraboloid is a surface defined by

.. math::
    \frac{z}{c} = \frac{x^2}{a^2} + \frac{y^2}{b^2}


GeoGebra
""""""""

To graph an elliptic paraboloid in GeoGebra we input the expression just like you would write it mathematically. A quick version is below,

.. code-block:: console

    z/c=x^2/a^2+y^2/b^2

When this is input, GeoGebra will create sliders for the constants :math:`a, b, c` and the plot will look like.

.. figure:: Images/quadsurf/quadsurf020.png
    :alt: Elliptic Paraboloid

    Elliptic Paraboloid

By adjusting the sliders you can experiment with the shape of the paraboloid.

.. figure:: Images/quadsurf/quadsurf021.png
    :alt: Elliptic Paraboloid

    Elliptic Paraboloid


CLAE
"""""

To graph an elliptic paraboloid in CLAE we input the expression just like you would write it mathematically, except that we first make it an equation with 0.

.. math::
    -\frac{z}{c} + \frac{x^2}{a^2} + \frac{y^2}{b^2} = 0

and then we drop the ``= 0``.

.. math::
    -\frac{z}{c} + \frac{x^2}{a^2} + \frac{y^2}{b^2}


A quick version is below,

.. code-block:: console

    x^2/a^2+y^2/b^2-z/c

When this is input, CLAE will create sliders for the constants :math:`a, b, c` and the plot will look like.

.. figure:: Images/quadsurf/quadsurf022.png
    :alt: Elliptic Paraboloid

    Elliptic Paraboloid

By adjusting the sliders you can experiment with the shape of the paraboloid.

.. figure:: Images/quadsurf/quadsurf023.png
    :alt: Elliptic Paraboloid

    Elliptic Paraboloid



Example: :index:`Cone`
^^^^^^^^^^^^^^^^^^^^^^

A cone is a surface defined by

.. math::
    \frac{z^2}{c^2} = \frac{x^2}{a^2} + \frac{y^2}{b^2}


GeoGebra
""""""""

To graph a cone in GeoGebra we input the expression just like you would write it mathematically. A quick version is below,

.. code-block:: console

    z^2/c^2=x^2/a^2+y^2/b^2

When this is input, GeoGebra will create sliders for the constants :math:`a, b, c` and the plot will look like.

.. figure:: Images/quadsurf/quadsurf024.png
    :alt: Cone

    Cone

By adjusting the sliders you can experiment with the shape of the cone.

.. figure:: Images/quadsurf/quadsurf025.png
    :alt: Cone

    Cone


CLAE
"""""

To graph a cone in CLAE we input the expression just like you would write it mathematically, except that we first make it an equation with 0.

.. math::
    \frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} = 0

and then we drop the ``= 0``.

.. math::
    \frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2}


A quick version is below,

.. code-block:: console

    x^2/a^2+y^2/b^2-z^2/c^2

When this is input, CLAE will create sliders for the constants :math:`a, b, c` and the plot will look like.

.. figure:: Images/quadsurf/quadsurf026.png
    :alt: Cone

    Cone

By adjusting the sliders you can experiment with the shape of the cone.

.. figure:: Images/quadsurf/quadsurf027.png
    :alt: Cone

    Cone


