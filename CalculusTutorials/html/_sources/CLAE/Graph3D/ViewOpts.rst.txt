View Options
============

The following are the viewing options for 3D plots, each of these have a corresponding toolbar button.

Toggle Axes
-----------

This toggles the visibility of the coordinate axes.  With the axes on,

.. figure:: Images/ViewOpts001.png
    :alt: Coordinate Axes On

    Coordinate Axes On

and with them off,

.. figure:: Images/ViewOpts002.png
    :alt: Coordinate Axes Off

    Coordinate Axes Off

Toggle Grid
-----------

This toggles the coordinate grid or grids, there are three possible coordinate grids this option toggles all of them. The Axes/Grids menu allows you to select them individually.  With the grid on,

.. figure:: Images/ViewOpts001.png
    :alt: Grid On

    Grid On

and with the grid off,

.. figure:: Images/ViewOpts003.png
    :alt: Grid Off

    Grid Off

Toggle View Cube Bounds
-----------------------

This toggles the viewing (or clipping) cube. With the cube on,

.. figure:: Images/ViewOpts001.png
    :alt: View Cube On

    View Cube On

and with the cube off,

.. figure:: Images/ViewOpts004.png
    :alt: View Cube Off

    View Cube Off

Reset View Window
-----------------

Resets the axes lengths and center to the default values, center at the origin and all axes ranges are :math:`[-10, 10]`.

Center at Origin
----------------

This repositions the center of the view to the origin of the coordinate system.

Translate Center to (x, y, z)
-----------------------------

This allows the user to repositions the center of the view to an input point :math:`(x, y, z)`.  When selected the following dialog box will appear.

.. figure:: Images/ViewOpts005.png
    :alt: Translate Center Dialog Box

    Translate Center Dialog Box

The user simply needs to input a list of three values for the :math:`(x, y, z)` coordinates.  The values can be any legitimate expression that evaluates to a real number.

Set View Window to 1-1
----------------------

This automatically rescales the axes to a 1-1 aspect ratio using the longest axis as a reference.  The center of the viewing cube is unchanged.

Perspective Mode
----------------

This sets the view to perspective mode.  Perspective mode looks more natural since it scales up portions of the image closer to you and scales down portions of the image further away from you.  Most of the time you will use perspective mode when viewing 3D plots.

.. figure:: Images/ViewOpts006.png
    :alt: Perspective Mode

    Perspective Mode

Orthogonal Mode
---------------

This sets the view to orthogonal mode. Orthogonal mode does not scale the image by the distance from the camera, all distances are equal.  This produces an unnatural image in most cases but is better if you are looking down one of the coordinate axes.

.. figure:: Images/ViewOpts007.png
    :alt: Orthogonal Mode

    Orthogonal Mode

For example, if you are using the 3D view to graph a color contour map of a surface you will want to shift into orthogonal mode.

.. figure:: Images/ViewOpts008.png
    :alt: Color Contour Map

    Color Contour Map

Set Mouse Mode to Camera Rotate and Zoom
----------------------------------------

This is also a Mouse Mode option but it is a quick way to set the mouse mode back to the default of camera positioning.

Snapshot Viewer
---------------

This option will open the Snapshot Viewer and load in an image of the current plot.  The snapshot viewer window has options for copying the image to the clipboard, opening ans saving images, printing and print preview, as well as a quick tool in the toolbar to add a border to the image. It also has options for inserting some simple annotations, text boxes, mathematical expressions, rectangles, ellipses, lines, and arrows.  The tool is discussed in detail in its own section :doc:`SnapshotViewer`.

.. figure:: Images/Snapshot.png
    :alt: Snapshot Viewer

    Snapshot Viewer

