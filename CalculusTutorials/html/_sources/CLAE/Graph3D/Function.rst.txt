:index:`Function z = f(x, y)`
=============================

Description
-----------

This type graphs surfaces of the form :math:`z = f(x, y)`.  The independent variables in the expressions must be ``x`` and ``y``, the variable ``z`` cannot be in the expression either.  All other variables outside the set of 3D variables (``x``, ``y``, ``z``, ``p``, ``t``, ``u``, and ``v``) are considered constants.  The following are examples of this type of expression,

- ``cos(x + y)``
- ``cos(x) + y^2``
- ``a*sin(b*x^2 + d*cos(y) + c)``

Insert/Edit Dialog
------------------

The Insert/Edit Dialog for this type is shown below.

.. figure:: Images/fxy_dialog.png
    :alt: Function Dialog Box

    Function Dialog Box

Below the expression being graphed there are options for the number of x and y grid divisions, clipping the z-values to the viewing cube, plot objects, surface mesh color, surface shading, and a selector for smooth shading.

Options
-------

X Grid Divisions
^^^^^^^^^^^^^^^^

This is the number of points plotted in the x-direction to establish a grid of function points that will be used to triangulate the surface.  The total number of points used is the product of the x grid divisions and the y grid divisions.

Y Grid Divisions
^^^^^^^^^^^^^^^^

This is the number of points plotted in the y-direction to establish a grid of function points that will be used to triangulate the surface.  The total number of points used is the product of the x grid divisions and the y grid divisions.

Clip Z Values to View
^^^^^^^^^^^^^^^^^^^^^^

.. include:: clipping3d.md

Plot
^^^^

.. include:: plotObjects3d.md

Surface Mesh Color
^^^^^^^^^^^^^^^^^^

.. include:: meshcolor.md

Surface Shading
^^^^^^^^^^^^^^^

.. include:: shading3d.md

Smooth Shading
^^^^^^^^^^^^^^

.. include:: smoothshading3d.md

