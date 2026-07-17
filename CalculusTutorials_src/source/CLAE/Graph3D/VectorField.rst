:index:`Vector Field`
=====================

Description
-----------

A vector field is a vector valued function :math:`F = (f(x, y, z), g(x, y, z), h(x, y, z))` where :math:`f(x, y, z)` represents the x direction of the vector at the point :math:`(x, y, z)`, :math:`g(x, y, z)` represents the y direction of the vector at the point :math:`(x, y, z)`, and :math:`h(x, y, z)` represents the z direction of the vector at the point :math:`(x, y, z)`.

There are two ways to input a vector field into this application, either a list with three expressions or a :math:`3 \times 1` matrix.  For example, the field :math:`F = (y, z, x)` could be input as either, ``[y,z,x]`` or as

.. math::
    \left[\begin{array}{c}y\\z\\x\end{array}\right]


Insert/Edit Dialog
------------------

The Insert/Edit Dialog for the vector field is pictured below.

.. figure:: Images/VF_dialog.png
    :alt: Vector Field Dialog Box

    Vector Field Dialog Box

The top three inputs are for the x, y, and z expressions defining the field :math:`F = (f(x, y, z), g(x, y, z), h(x, y, z))`, below that are options for inputting the number of x, y, and z divisions for plotting the vectors, point size, line width, clipping, and scaling mode.

Options
-------

Number of X Divisions
^^^^^^^^^^^^^^^^^^^^^

This is the number of divisions in the x direction for the field.

Number of Y Divisions
^^^^^^^^^^^^^^^^^^^^^

This is the number of divisions in the y direction for the field.

Number of Z Divisions
^^^^^^^^^^^^^^^^^^^^^

This is the number of divisions in the z direction for the field.

Point Size
^^^^^^^^^^

The size of the point to be used in the image.  The default of 7 is usually sufficient for most applications.


Line Width
^^^^^^^^^^

The width of the line for the vectors connecting the initial and terminal points.

.. include:: linewidth.md

Clip to View Box
^^^^^^^^^^^^^^^^

.. include:: clipping3d.md


Scaling
^^^^^^^

This is the scaling mode for the vectors, there are four different scaling modes.

- **Scale to Window:** This is probably the best mode visually for most applications.  It scales the vectors by the dimensions of the viewing window and the number of divisions in the x, y, and z directions.
- **Scale to Maximum Vector:** This mode scales the vectors relative to the longest vector in the visible set.  The longest vector is scaled by the viewing window and the number of divisions in the x, y, and z directions and all other vectors are scaled according to the maximum. This is good to visualize the speed of a flow.
- **Normalize:** This scales all vectors to length 1.
- **No Scaling:** This does not scale the vectors at all.

Note that most of these mode look best if the viewing is set to a 1-1 aspect ratio.

Example
-------

If we input the field, :math:`F = (y, z, x)`, and keep all the default settings we get,

.. figure:: Images/VF001.png
    :alt: Vector Field Example

    Vector Field Example

.. note::

    When a 3D vector is rendered the head of the vector is simply a point instead of an arrow or directed cone.  Although not as fancy as an arrow it still adequately represents a vector and speeds up the graphics considerably.

