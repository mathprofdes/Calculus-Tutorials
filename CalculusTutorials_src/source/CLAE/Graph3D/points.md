
This program was built with the goal of quick graphics, for this reason we do not use adaptive methods to graph curves (which give better images but are slower to plot) we simply take a number of evenly-spaced points over the domain of the graphics region.  The number of points you select are the number of evaluations done over the graphing range.  If you want more resolution to the plot, simply increase the number of points.  As expected, the larger number of points used will slow down animations, zooming, and translations of the graphics view.  The default value for most of the curves in this program is 500 points, which is good for most reasonably smooth curves.

For example, if we graph :math:`\sin(1/x)`, syntax ``sin(1/x)`` with 500 points the plot is the following,

.. figure:: Images/Fct_Ex001.png
    :alt: sin(1/x) using 500 Points

    :math:`\sin(1/x)` using 500 Points

If we change the number of points to 2000 we get,

.. figure:: Images/Fct_Ex002.png
    :alt: sin(1/x) using 2000 Points

    :math:`\sin(1/x)` using 2000 Points

and if f we change the number of points to 10000 we get,

.. figure:: Images/Fct_Ex003.png
    :alt: sin(1/x) using 10000 Points

    :math:`\sin(1/x)` using 10000 Points

