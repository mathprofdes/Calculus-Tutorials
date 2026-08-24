:index:`Cylindrical Coordinate Surface`
=======================================

Description
-----------

This type is for graphing functions in the cylindrical coordinate system.  Functions must use the variables ``r`` and ``t``, radius and angle respectively.  The program will allow the user to change the linear direction to any of the three coordinate axes.  While the z-axis is customary here there could be applications where this is better with either the x or y axes.

Insert/Edit Dialog
------------------

The Insert/Edit Dialog for this type is shown below.

.. figure:: Images/Cyl_dialog.png
    :alt: Cylindrical Coordinate Surface Edit Dialog

    Cylindrical Coordinate Surface Edit Dialog

The first input is for the function then there are options for, the linear direction, minimum and maximum r values, minimum and maximum theta values, the number of divisions in the r direction, the number of divisions in the theta direction, clipping, plot object, mesh color, shading mode and smooth shading.

Options
-------

Linear Direction
^^^^^^^^^^^^^^^^

This is simply the direction of the linear component of the coordinate system.  The z direction is customary with the xy-plane being in polar coordinates but if the y direction is selected for the linear direction then the xz-plane will be in polar coordinates, and the same for x as the linear direction will make the yz-plane polar.   For example, if our function is :math:`\sin(r + t)` with the z direction linear give us,

.. figure:: Images/Cyl001.png
    :alt: sin(r + t) with Linear Z Direction

    :math:`\sin(r + t)` with Linear Z Direction

using y as the linear direction we get,

.. figure:: Images/Cyl002.png
    :alt: sin(r + t) with Linear Y Direction

    :math:`\sin(r + t)` with Linear Y Direction

and using x as the linear direction we get,

.. figure:: Images/Cyl003.png
    :alt: sin(r + t) with Linear X Direction

    :math:`\sin(r + t)` with Linear X Direction

Minimum R Value
^^^^^^^^^^^^^^^

This is the starting value for the r variable.

Maximum R Value
^^^^^^^^^^^^^^^

This is the ending value for the r variable.

Minimum Theta Value
^^^^^^^^^^^^^^^^^^^

This is the starting value for the t (theta) variable.

Maximum Theta Value
^^^^^^^^^^^^^^^^^^^

This is the ending value for the t (theta) variable.

R Grid Divisions
^^^^^^^^^^^^^^^^

This is the number of divisions along the r range.

Theta Grid Divisions
^^^^^^^^^^^^^^^^^^^^

This is the number of divisions along the t (theta) range.

Clip Values to View
^^^^^^^^^^^^^^^^^^^^

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

From above with the function :math:`\sin(r + t)` with the z direction linear we get,

.. figure:: Images/Cyl001.png
    :alt: sin(r + t) with Linear Z Direction

    :math:`\sin(r + t)` with Linear Z Direction

As another quick example, with the function :math:`t + \sin{\left(r \right)}` with the z direction linear, r from 0 to 10 and t from 0 to :math:`6\pi` we get,

.. figure:: Images/Cyl004.png
    :alt: t + sin(r) with Linear Z Direction

    :math:`t + \sin{\left(r \right)}` with Linear Z Direction

