:index:`Parametric Surface`
===========================

Description
-----------

This type is for graphing parametrically defined surfaces of the form,

.. math::
    \begin{array}{rcl} x & = & f\left(u, v \right)\\ y & = & g\left(u, v \right) \\ z & = & h\left(u, v \right)\end{array}

The parametric equations can be input in either list form with three entries representing the x, y, and z functions respectively or as a :math:`3 \times 1` matrix.  The independent variables must be ``u`` and ``v``, and not contain any other variables in the set of 3D variables (``x``, ``y``, ``z``, ``p``, ``t``, ``u``, and ``v``). All other variables outside this set are considered constants.

For example, the parametric equations,

.. math::
    \begin{array}{rcl} x & = & \sin{\left(u \right)}\\y & = & \cos{\left(v \right)}\\z & = & \frac{u}{5} + \frac{v}{5}\end{array}

can be input as :math:`\left[ \sin{\left(u \right)}, \  \cos{\left(v \right)}, \  \frac{u}{5} + \frac{v}{5}\right]` or as

.. math::
    \left[\begin{array}{c}\sin{\left(u \right)}\\\cos{\left(v \right)}\\\frac{u}{5} + \frac{v}{5}\end{array}\right]

Insert/Edit Dialog
------------------

The Insert/Edit Dialog for this type is shown below.

.. figure:: Images/Para_dialog.png
    :alt: Parametric Surface Dialog Box

    Parametric Surface Dialog Box

The first three inputs are for the x, y, and z functions then there are options for, minimum and maximum u value, minimum and maximum v values, the number of divisions in the u direction, the number of divisions in the v direction, clipping, plot object, mesh color, shading mode and smooth shading.

Options
-------

Minimum U Value
^^^^^^^^^^^^^^^

This is the starting value along the u-axis.

Maximum U Value
^^^^^^^^^^^^^^^

This is the ending value along the u-axis.

Minimum V Value
^^^^^^^^^^^^^^^

This is the starting value along the v-axis.

Maximum V Value
^^^^^^^^^^^^^^^

This is the ending value along the v-axis.

U Grid Divisions
^^^^^^^^^^^^^^^^

This is the number of divisions along the range of the u-axis.

V Grid Divisions
^^^^^^^^^^^^^^^^

This is the number of divisions along the range of the v-axis.

Clip Values to View
^^^^^^^^^^^^^^^^^^^^

.. include:: clipping3d.md

Plot
^^^^

.. include:: plotObjects3d.md

Surface Mesh Color
^^^^^^^^^^^^^^^^^^

.. include:: meshcolor.md

Surface Shading
^^^^^^^^^^^^^^^

.. include:: shading3d.md

Smooth Shading
^^^^^^^^^^^^^^

.. include:: smoothshading3d.md


Example
-------

The following image is of the equations :math:`\left[ \sin{\left(u \right)}, \  \cos{\left(v \right)}, \  \frac{u}{5} + \frac{v}{5}\right]`, both u and v are :math:`[-10,10]`

.. figure:: Images/Para001.png
    :alt: Parametric Surface Example

    :math:`\left[ \sin{\left(u \right)}, \  \cos{\left(v \right)}, \  \frac{u}{5} + \frac{v}{5}\right]`

