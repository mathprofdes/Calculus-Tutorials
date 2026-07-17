
Surfaces have three options to what is viewed, the filled in surface, a wire-frame grid, or both the surface and the grid.

Surface
"""""""

This option plots the filled-in surface defined by the expression and selected surface options.  For example, the surface defined by the function :math:`z = f(x, y) = x^{2} - y^{2}` with just the surface plot option is pictured below.

.. figure:: Images/PlotSurface.png
    :alt: Surface Plot

    Surface Plot

Grid
""""

This option plots the wire-frame of the surface defined by the expression and selected surface options.  For example, the surface defined by the function :math:`z = f(x, y) = x^{2} - y^{2}` with just the grid plot option is pictured below.

.. figure:: Images/PlotGrid.png
    :alt: Grid Plot

    Grid Plot

This program does not have a transparent surface feature that allows the user to see through the surface to other surfaces and lines.  The reason we did incorporate this ability is that to do transparency well you need to use global image rendering techniques that require many more calculations and hence slow the system down considerably. We are sticking with strictly local graphing techniques which are very fast.  In some applications you may want to view through one or more surfaces, the grid option is a nice and quick way to do that.

Surface & Grid
""""""""""""""

This option plots the filled-in surface along with the wire-frame of the surface defined by the expression and selected surface options.  For example, the surface defined by the function :math:`z = f(x, y) = x^{2} - y^{2}` with the surface and grid plot option is pictured below.

.. figure:: Images/PlotSurfaceGrid.png
    :alt: Surface and Grid Plot

    Surface and Grid Plot

The color of the grid is defined by the mesh color option of the surface.  One artifact that is clear from the image is that the grid portion drops out at places.  This is called "stitching" and is a common problem when graphing two objects that are in the same position.  When graphing objects in 3D, as solid objects, the system determines which portions are closer to the camera, graphs these and hides objects that are behind them. So when two objects are in the same place one is in front of the other at times and at other times the second is in front of the first.  This swapping back and forth between the two is what produces the stitching.  In general, you probably will not use this mode too often, nonetheless it is here if you want it. 
