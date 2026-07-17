:index:`2-D Polar Space Curve`
==============================


Description
-----------

This type graphs a polar function of the form :math:`r = f(t)` as a space curve in 3D. These are easy to define parametrically but we included this option for user convince and to save them a couple steps.  The independent variable must be ``t``.  All other variables outside the set of 3D variables (``x``, ``y``, ``z``, ``p``, ``t``, ``u``, and ``v``) are considered constants.  This option allows the user to select the coordinate plane the curve is plotted in, either xy, xz, or yz planes.


Insert/Edit Dialog
------------------

The Insert/Edit Dialog for this type is shown below.

.. figure:: Images/Fct2DSCPolar_dialog.png
    :alt: 2-D Polar Space Curve Dialog Box

    2-D Polar Space Curve Dialog Box


Below the expression that are options for the minimum and maximum t values, the number of points to use for the plot, the render plane, the line width, and clipping.

Options
-------

Minimum t Value
^^^^^^^^^^^^^^^

This is the beginning t value for the plotting of the polar curve.

Maximum t Value
^^^^^^^^^^^^^^^

This is the ending t value for the plotting of the polar curve.

Points
^^^^^^

.. include:: points.md

Render Plane
^^^^^^^^^^^^

This is the plane that that polar curve is plotted.


Line Width
^^^^^^^^^^

.. include:: linewidth.md

Clip Values to View
^^^^^^^^^^^^^^^^^^^^

.. include:: clipping3d.md

Example
-------

If we plot :math:`7 \sin{\left(3 t \right)}` in the xy-plane we get,

.. figure:: Images/Fct2DSCPolar001.png
    :alt: 2-D Polar Space Curve Example in the XY-Plane

    2-D Polar Space Curve Example in the XY-Plane

in the xz-plane we get,

.. figure:: Images/Fct2DSCPolar002.png
    :alt: 2-D Polar Space Curve Example in the XZ-Plane

    2-D Polar Space Curve Example in the XZ-Plane

and in the yz-plane we get,

.. figure:: Images/Fct2DSCPolar003.png
    :alt: 2-D Polar Space Curve Example in the YZ-Plane

    2-D Polar Space Curve Example in the YZ-Plane
