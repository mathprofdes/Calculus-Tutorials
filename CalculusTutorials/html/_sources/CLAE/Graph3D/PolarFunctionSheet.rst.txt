:index:`Polar Function Sheet`
=============================

Description
-----------

A function sheet is also called a function curtain.  It is when you take a function and extrude it in the third dimension.  These are easy to write parametrically but we included this type as a convenience for the user.  This version takes a polar coordinate function and extrudes it in one of three dimensions.  Specifically, it takes a function in the variable ``t`` of the form :math:`r = f(t) = f(\theta)`, plots it in polar coordinates on one of the three coordinate planes (selected by the user) and extrudes it in the third dimension.

Insert/Edit Dialog
------------------

The Insert/Edit Dialog for this type is shown below.

.. figure:: Images/PolarSheet_dialog.png
    :alt: Polar Function Sheet Dialog Box

    Polar Function Sheet Dialog Box

Below the function expression input there are options for the polar bounds on t, the number of grid divisions along the function direction, grid divisions along the extrusion direction, the plane to render the polar function in, clipping the z-values to the viewing cube, plot objects, surface mesh color, surface shading, and a selector for smooth shading.

Options
-------

Minimum t Value
^^^^^^^^^^^^^^^

This is the beginning t value for the plotting of the polar curve.

Maximum t Value
^^^^^^^^^^^^^^^

This is the ending t value for the plotting of the polar curve.

Grid Divisions Along Function
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This is the number of points plotted in for the curve.

Extrude Grid Divisions
^^^^^^^^^^^^^^^^^^^^^^

This is the number of points plotted in the extrusion direction. This is determined by the selection of the rendering plane.  Since the extrusion direction is all straight lines there does not need to be very many division in that direction.  So the function divisions can be set higher and this lower to get a smoother surface.

Render Plane
^^^^^^^^^^^^

This is the plane that that polar curve is plotted in and the extrusion is perpendicular to this plane.

Clip Values to View
^^^^^^^^^^^^^^^^^^^

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


Example
-------

If we take the expression :math:`7 \sin{\left(3 t \right)}` and use the xy-plane as the render plane (making the extruding direction ``z``) we get,

.. figure:: Images/PolarSheet001.png
    :alt: Polar Function Sheet Example with XY Render Plane

    :math:`7 \sin{\left(3 t \right)}` with XY Render Plane

If we change the render plane to the xz-plane (making the extruding direction ``y``) we get,

.. figure:: Images/PolarSheet002.png
    :alt: Polar Function Sheet Example with XZ Render Plane

    :math:`7 \sin{\left(3 t \right)}` with XZ Render Plane

Finally, if we change the render plane to the yz-plane (making the extruding direction ``x``) we get,

.. figure:: Images/PolarSheet003.png
    :alt: Polar Function Sheet Example with YZ Render Plane

    :math:`7 \sin{\left(3 t \right)}` with YZ Render Plane
