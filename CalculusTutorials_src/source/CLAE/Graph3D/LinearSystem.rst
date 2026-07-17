:index:`Linear System`
======================

Description
-----------

This type is for graphing a linear system of planes defined by the rows of a matrix that defines the linear system.  The input is an :math:`n \times 4` matrix where each row defines a linear equation in three variables.  For example, the matrix,

.. math::
    \left[\begin{array}{cccc}8 & -7 & -3 & 5\\2 & -1 & 9 & -3\\-9 & -8 & -9 & -4\end{array}\right]

defines the linear system, :math:`\{8x -7y -3z = 5, 2x -y + 9z = -3, -9x -8y -9z = -4\}`.


Insert/Edit Dialog
------------------

The Insert/Edit Dialog for a 3D linear system is pictured below.

.. figure:: Images/LS_dialog.png
    :alt: Linear System Dialog Box

    Linear System Dialog Box


The dialog is set up in a similar manner as the matrix input dialog except that the number of columns is fixed at 4. The menu and toolbar have options for the input of the equation coefficients in the editing grid on the left.  In the grid, note that the headers are labeled ``x``, ``y``, ``z``, and ``c``.  So each row represents the linear equation :math:`ax + by + dz = c`. The options on the right are for the grid divisions in plotting the planes,clipping, plot objects, surface mesh color, surface shading, and a selector for smooth shading.

.. include:: ../CLAE/PointSetDialogOptions.md

Options
-------

Grid Divisions
^^^^^^^^^^^^^^

This is the number of divisions in both directions for plotting each plane.  Since these are planes with no curving only a small number of divisions are necessary.

Clip to View Box
^^^^^^^^^^^^^^^^

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

If we plot the linear system from the example above we get the image.

.. figure:: Images/LS001.png
    :alt: Linear System Example

    Linear System Example

With linear systems it may be difficult to see the differences in the plane orientations with the default shading.  In general, changing the shading to surface normals or camera and normals will distinguish the planes a bit better.  For example, the same system with camera and normals shading gives the following.

.. figure:: Images/LS002.png
    :alt: Linear System Example

    Linear System Example

