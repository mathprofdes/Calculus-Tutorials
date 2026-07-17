:index:`Polygon`
================

Description
-----------

This is for plotting a polygon defined by a set of points.  The vertices to the polygon can be given as a :math:`3 \times n` matrix where each column represents a point, row 1 are the x-coordinates, row 2 are the y-coordinates, and  row 3 are the z-coordinates.  It can also be given as a list of lists, the inner lists must have three components representing x, y, and z respectively. For example the polygon created from the vertices :math:`\{(6, 9, -7), (-2, 6, 7), (7, 9, 8) \}` could be input as the matrix,

.. math::
    \left[\begin{array}{ccc}6 & -2 & 7\\9 & 6 & 9\\-7 & 7 & 8\end{array}\right]

or as the list of lists ``[[6, 9, -7],[-2, 6, 7],[7, 9, 8]]``.

Insert/Edit Dialog
------------------

The Insert/Edit Dialog for a 3D point set is pictured below.

.. figure:: Images/Poly_dialog.png
    :alt: Polygon Dialog Box

    Polygon Dialog Box

The dialog is set up in a similar manner as the matrix input dialog except that the number of columns is fixed at 3.  This is really transposed from the matrix input way of representing points but was done to make user input more natural.  The menu and toolbar have options for the input of the points in the editing grid on the left.  The options on the right are for the point size, line width, looping, and clipping.

.. include:: ../CLAE/PointSetDialogOptions.md

Options
-------

Point Size
^^^^^^^^^^

The size of the point to be used in the image.  The default of 7 is usually sufficient for most applications.

Line Width
^^^^^^^^^^

This is the width of the line segment between two consecutive points on the polygon.

.. include:: linewidth.md

Loop
^^^^

If checked, this will connect the last point in the set of vertices to the first and if it is not checked no last line segment will be added.

Clip to View Box
^^^^^^^^^^^^^^^^

.. include:: clipping3d.md


Example
-------

If we plot the polygon from the above examples we would see,

.. figure:: Images/Poly001.png
    :alt: Polygon Example

    Polygon Example

