:index:`Vector Set`
===================

Description
-----------

This is for plotting a set of vectors.  The vectors can be given as a :math:`2 \times n` matrix where each column represents a point, row 1 are the x-coordinates and row 2 are the y-coordinates.  It can also be given as a list of lists, the inner lists must have two components representing x and y respectively. For example the set of vectors :math:`\{(1, 4), (-2, 5), (2, -4) \}` could be input as the matrix,

.. math::
    \left[\begin{array}{ccc}1 & -2 & 2\\4 & 5 & -4\end{array}\right]

or as the list of lists ``[[1, 4],[-2, 5],[2, -4]]``.

Insert/Edit Dialog
------------------

The Insert/Edit Dialog for a vector set is pictured below.

.. figure:: Images/VS_dialog.png
    :alt: Vector Set Properties Dialog

    Vector Set Properties Dialog

The dialog is set up in a similar manner as the matrix input dialog except that the number of columns is fixed at 2.  This is really transposed from the matrix input way of representing points but was done to make user input more natural.  The menu and toolbar have options for the input of the vectors in the editing grid on the left.  The options on the right are for the visual aspects of the vector set.

.. include:: ../CLAE/PointSetDialogOptions.md

Options
-------

Line Width
^^^^^^^^^^

This is the width of the lines from the initial point of the vector to the terminal point of the vector.

.. include:: linewidth.md

Initial Point
^^^^^^^^^^^^^

This is the initial point of the vector set.  The input is as a list with two elements the first is the x coordinate and the second is the y coordinate.  The expressions for the x coordinate and the y coordinate can be any valid expression that does not contain the variables ``x``, ``t``, or ``y``. They may contain constants that will link with a slider.

Show Grid / Span
^^^^^^^^^^^^^^^^

If checked the program will add in a grid of integer linear combinations of the vectors in the set, up to the first 5 vectors.  This is useful when visualizing linear combinations, change of basis, and spanning.

Span Line Width
^^^^^^^^^^^^^^^

This is the width of the span/grid lines used if that option is selected.

Grid / Span Extent
^^^^^^^^^^^^^^^^^^

This option sets the number of span lines that are created if that option is selected.  For example, if the extent is set to 5 the program will graph the grid 5 lines in each direction, that is, linear combination constants of :math:`-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5`.

Example
-------

If we added the vector set from the above examples we would see,

.. figure:: Images/VS001.png
    :alt: Vector Set Example

    Vector Set Example

If we remove the :math:`(2, -4)` vector and turn the grid on we see the following.

.. figure:: Images/VS002.png
    :alt: Vector Set Example with Grid

    Vector Set Example with Grid

This image would be good for discussions of spanning and linear combinations.

Adding and Removing Vectors to and from a Set
---------------------------------------------

This applications allows the user to add and remove vectors from a vector set using the mouse and the plot window.  Holding down the Shift key and clicking on the graphics window will add the click point to the vector set.  Holding down the Ctrl and Shift keys and clicking on the graphics window will remove the vector closest to the click point.  These options come in handy when you want to quickly create a set of vectors for a demonstration, such as linear combinations and spanning.

