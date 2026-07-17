:index:`Trace Point`
====================

Description
-----------

A trace point is a single point on the graph that is linked to one or more sliders, that is, the expression contains variables other than ``x``, ``t``, and ``y``.  When the sliders are changed the updated point is plotted along with all the previous points, thus tracing out a path that the point follows.  A trace point can be input as a list of 2 elements representing the x, and y coordinates respectively or as a :math:`2 \times 1` matrix.


Insert/Edit Dialog
------------------

The Insert/Edit Dialog for trace point is pictured below.

.. figure:: Images/Trace_dialog.png
    :alt: Trace Point Properties Dialog

    Trace Point Properties Dialog


The first edit boxes are for the x and y coordinate expressions.  This is followed by the plot objects, point size, point style, fill point, fill with same color, fill color, line width, coordinate system, and an option to clear the current trace.

Options
-------

Plot Objects
^^^^^^^^^^^^

This designates what is plotted as the trace point changes.  The options are:

- **Points:** This plots each individual point on the update.

- **Connecting Lines:** This plots lines between the individual points and does not plot the point itself.

- **Points and Lines:** This plots both the points and connecting lines.

.. note::

    When plotting the connecting lines this will plot a line between each consecutive pair of points that are evaluated.  If a slider is moved quickly then the consecutive points may be far apart and the connecting line may not be as accurate.  If you do set this to a connecting line mode it is best to animate the slider instead of moving it with the mouse.

Point Size
^^^^^^^^^^

The size of the point to be used in the image.  The default of 1 is usually sufficient for most applications.

Point Style
^^^^^^^^^^^

.. include:: ../CLAE/PointStyles2D.md

Fill Point
^^^^^^^^^^

When this option is selected it will fill in the center of the point.

Fill with Same Color
^^^^^^^^^^^^^^^^^^^^

When this is selected, if Fill Point is selected, it will fill the center of the point with the same color as the outline.

Fill Color
^^^^^^^^^^

If Fill Point is selected and Fill with Same Color is not selected, the color here will be used to fill the center of the point.  To change this color simply click on the color box and a color selection dialog will appear allowing you to select the fill color.  Note that if Fill with Same Color is selected it will override and color selection here.

Line Width
^^^^^^^^^^

If one of the connected line modes is selected this will set the width of the connecting line.

.. include:: linewidth.md

Coordinate System
^^^^^^^^^^^^^^^^^

This allows the user to select between rectangular and polar coordinates. In rectangular coordinates the expressions will evaluate an :math:`(x, y)` point and if set to polar the expressions will evaluate an :math:`(r, \theta)` point.

Clear Current Trace
^^^^^^^^^^^^^^^^^^^

This will clear the current trace data from the plot.

Example
-------

Say we plot the expression ``[cos(a), sin(a)]`` as a trace point, we will initially see the following.  The graphics manager will also include a slider for the constant ``a``.

.. figure:: Images/Trace001.png
    :alt: Trace Point Example

    Trace Point Example

If we animate the ``a`` slider we get the image.

.. figure:: Images/Trace002.png
    :alt: Trace Point Example

    Trace Point Example

Changing the plot object to connected lines we get,

.. figure:: Images/Trace003.png
    :alt: Trace Point Example

    Trace Point Example

Changing the plot object to points and lines we get,

.. figure:: Images/Trace004.png
    :alt: Trace Point Example

    Trace Point Example

Note that the above images were created by animating the slider and hence making the curves smooth and close to a continuous trace.  If we clear the above data and change the slider quickly using the mouse we would get something like the following.

.. figure:: Images/Trace005.png
    :alt: Trace Point Example

    Trace Point Example
