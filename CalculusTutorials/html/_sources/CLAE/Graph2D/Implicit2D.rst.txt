:index:`Implicit Relationship f(x, y) = 0`
==========================================

Description
-----------

This type is for graphing implicitly defined expressions of the form :math:`0 = f(x, y)` or :math:`0 = f(t, y)`.  The expression variables can be ``x`` and ``y`` or ``t`` and ``y``  but not all three.  The following are examples of this type of expression,

- ``cos(x*y)``
- ``cos(t) + Y^2``
- ``x^3 - 3*x - y^2 + 1``
- ``t^3 - 3*t - y^2 + 1``


Insert/Edit Dialog
------------------

The Insert/Edit Dialog for 2D implicit relationships is below,

.. figure:: Images/Imp_dialog.png
    :alt: Implicit Relationship Properties Dialog

    Implicit Relationship Properties Dialog

The first option is the expression to be plotted, followed by the grid divisions, and finally the line width.

Options
-------

Grid Divisions
^^^^^^^^^^^^^^

The grid divisions are used in determining the location of the curve on the plane.  The larger this is the better the curve image will be, especially at places where the curve self-intersects. As is expected, the larger this is the more calculations need to be completed and the slower the graphing and animations will be.

Line Width
^^^^^^^^^^

.. include:: linewidth.md

Example
-------

For example, say we input the expression :math:`x^{3} - 3 x - y^{2} + 1` with the syntax ``x^3 - 3*x - y^2 + 1``, using the default settings we get the image,

.. figure:: Images/Imp001.png
    :alt: Implicit Relationship Example

    Implicit Relationship Example

