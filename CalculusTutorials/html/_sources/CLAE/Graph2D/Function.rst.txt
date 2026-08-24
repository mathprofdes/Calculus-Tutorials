:index:`Function y = f(x)`
==========================

Description
-----------

This type is your standard Cartesian plane function :math:`y = f(x)` or :math:`y = f(t)`.  The independent variable in the expression can be ``x`` or ``t`` but not both.  The variable ``y`` cannot be in the expression either.  All other variables are considered constants.  The following are examples of this type of expression,

- ``cos(x)``
- ``cos(t) + t^2``
- ``a*sin(b*x + c)``

Insert/Edit Dialog
------------------

This type has just a couple properties, the number of points plotted for the curve and the line width used to graph the curve.

.. figure:: Images/y_fx_dialog.png
    :alt: Function Properties Dialog

    Function Properties Dialog

Options
-------

Points
^^^^^^

.. include:: points.md

Line Width
^^^^^^^^^^

.. include:: linewidth.md
