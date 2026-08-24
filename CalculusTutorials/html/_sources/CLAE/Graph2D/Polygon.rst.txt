:index:`Polygon`
================

Description
-----------

This is for plotting a polygon defined by a set of points.  The vertices to the polygon can be given as a :math:`2 \times n` matrix where each column represents a point, row 1 are the x-coordinates and row 2 are the y-coordinates.  It can also be given as a list of lists, the inner lists must have two components representing x and y respectively. For example the polygon created from the vertices :math:`\{(1, 4), (-2, 5), (2, -4) \}` could be input as the matrix,

.. math::
    \left[\begin{array}{ccc}1 & -2 & 2\\4 & 5 & -4\end{array}\right]

or as the list of lists ``[[1, 4],[-2, 5],[2, -4]]``.

Insert/Edit Dialog
------------------

The Insert/Edit Dialog for a polygon is pictured below.

.. figure:: Images/Poly_dialog.png
    :alt: Polygon Properties Dialog

    Polygon Properties Dialog

The dialog is set up in a similar manner as the matrix input dialog except that the number of columns is fixed at 2.  This is really transposed from the matrix input way of representing points but was done to make user input more natural.  The menu and toolbar have options for the input of the points in the editing grid on the left.  The options on the right are for the point and line styles and visual aspects of the polygon.

.. include:: ../CLAE/PointSetDialogOptions.md

Options
-------

Point Size
^^^^^^^^^^

The size of the point to be used in the image.  The default of 1 is usually sufficient for most applications.

Point Style
^^^^^^^^^^^

.. include:: ../CLAE/PointStyles2D.md

Line Width
^^^^^^^^^^

This is the width of the line segment between two consecutive points on the polygon.

.. include:: linewidth.md

Loop
^^^^

If checked, this will connect the last point in the set of vertices to the first and if it is not checked no last line segment will be added.

Example
-------

If we plot the polygon from the above example we would see,

.. figure:: Images/Poly001.png
    :alt: Polygon Example

    Polygon Example


Adding and Removing Vertices to and from a Polygon
--------------------------------------------------

This applications allows the user to add and remove points from a polygon using the mouse and the plot window.  Holding down the Shift key and clicking on the graphics window will add the click point to the polygon.  Holding down the Ctrl and Shift keys and clicking on the graphics window will remove the polygon point closest to the click point.  These options come in handy when you want to quickly create a polygon for a demonstration, such as matrix transformations.

