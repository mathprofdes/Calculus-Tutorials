:index:`Vector Fields`
======================

You see vector fields almost every day.  If you turn on a weather report on the television or look it up on a web site you may see graphs that have a grid of arrows that represent wind direction, storm fronts, jet stream, etc. These are examples of vector fields.  Below is an image of a vector field showing wind direction at a set of weather stations in the eastern half of the US along with a vector field of ocean currents in the Atlantic at 1:32 PM EST on July 4, 2026.

.. figure:: Images/VecCalc/VecField001.png
    :alt: 1:32 PM EST on July 4, 2026

    1:32 PM EST on July 4, 2026

Vector Fields
-------------

.. admonition:: Definition: Vector Fields in :math:`\mathbb{R}^2` and :math:`\mathbb{R}^3`

    A vector field in :math:`\mathbb{R}^2` is a function

    .. math::
        \mathbf{F}(x, y) = P(x, y) \mathbf{i} + Q(x, y) \mathbf{j} = (P(x, y), Q(x, y))

    that assigns each point in a region *D* in :math:`\mathbb{R}^2` a vector in :math:`\mathbb{R}^2.`

    A vector field in :math:`\mathbb{R}^3` is a function

    .. math::
        \mathbf{F}(x, y, z) = P(x, y, z) \mathbf{i} + Q(x, y, z) \mathbf{j} + R(x, y, z) \mathbf{k} = (P(x, y, z), Q(x, y, z), R(x, y, z))

    that assigns each point in a region *D* in :math:`\mathbb{R}^3` a vector in :math:`\mathbb{R}^3.`

    The functions *P*, *Q*, and *R* are called component functions for the vector field.


Example: Vector Fields in :math:`\mathbb{R}^2`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

CLAE
""""

In this example we will look at the vector field, :math:`\mathbf{F}(x, y) = \sin(x) \mathbf{i} + \cos(y) \mathbf{j} = (\sin(x), \cos(y)).`

Input the expression for the vector field,

.. code-block:: console

    [sin(x),cos(y)]

Note that you can also put this into the vector input for a column vector representation,

.. math::
    \left[\begin{array}{c}\sin{\left(x \right)}\\\cos{\left(y \right)}\end{array}\right]

Either will work fine here.  Click and drag this to the 2D graphics window and zoom in a bit, you should see,

.. figure:: Images/VecCalc/VecField002.png
    :alt: :math:`\mathbf{F}(x, y) = \sin(x) \mathbf{i} + \cos(y) \mathbf{j}`

    :math:`\mathbf{F}(x, y) = \sin(x) \mathbf{i} + \cos(y) \mathbf{j}`

In this image the arrowhead is a small diamond at the end of the vector which shows the direction of the vector at each point on the vector grid.  CLAE has many options for viewing the field in its properties.  You can increase or decrease the number of divisions in the grid as well as choose between four scaling types.  The default scaling type is the scale to window, seen above, which renders each vector as equal lengths.  This shows the directions but does not show the relative lengths (or speeds) of the field.  If you change the mode to scale to maximum vector you will see,

.. figure:: Images/VecCalc/VecField003.png
    :alt: :math:`\mathbf{F}(x, y) = \sin(x) \mathbf{i} + \cos(y) \mathbf{j}`

    :math:`\mathbf{F}(x, y) = \sin(x) \mathbf{i} + \cos(y) \mathbf{j}`

In this image all of the vectors are scaled relative to the longest vector in the field.  This shows the directions and relative lengths or speeds of the vectors.  The difficulty with this scaling mode is that if there is a vector in the field that overwhelms the others then most of the vectors in the field show up as just dots.  It is always good to view the field in these two modes to get a feel for the field.  The other two modes can also give some visual information for the field depending on the field and the viewing window.

Example: Vector Fields in :math:`\mathbb{R}^3`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

CLAE
""""

In this example we will look at the vector field, :math:`\mathbf{F}(x, y, z) = y \mathbf{i} + z \mathbf{j} + x \mathbf{k} = (y, z, x).`

Input the expression for the vector field,

.. code-block:: console

    [y,z,x]

Note that you can also put this into the vector input for a column vector representation,

.. math::
    \left[\begin{array}{c}y\\z\\x\end{array}\right]

Either will work fine here.  Click and drag this to the 3D graphics window, you should see,

.. figure:: Images/VecCalc/VecField004.png
    :alt: :math:`\mathbf{F}(x, y, z) = y \mathbf{i} + z \mathbf{j} + x \mathbf{k}`

    :math:`\mathbf{F}(x, y, z) = y \mathbf{i} + z \mathbf{j} + x \mathbf{k}`

In this image the arrowhead is a small circle at the end of the vector which shows the direction of the vector at each point on the vector grid.  CLAE has many options for viewing the field in its properties.  You can increase or decrease the number of divisions in the grid as well as choose between four scaling types.  The default scaling type is the scale to window, seen above, which renders each vector as equal lengths.  This shows the directions but does not show the relative lengths (or speeds) of the field.  If you change the mode to scale to maximum vector you will see,

.. figure:: Images/VecCalc/VecField005.png
    :alt: :math:`\mathbf{F}(x, y, z) = y \mathbf{i} + z \mathbf{j} + x \mathbf{k}`

    :math:`\mathbf{F}(x, y, z) = y \mathbf{i} + z \mathbf{j} + x \mathbf{k}`

In this image all of the vectors are scaled relative to the longest vector in the field.  This shows the directions and relative lengths or speeds of the vectors.  The difficulty with this scaling mode is that if there is a vector in the field that overwhelms the others then most of the vectors in the field show up as just dots.  It is always good to view the field in these two modes to get a feel for the field.  The other two modes can also give some visual information for the field depending on the field and the viewing window.

.. note::

    For vector fields in :math:`\mathbb{R}^2` there is an option to display vectors, nicer vector images in the options.  This will produce a graph like the one below.

    .. figure:: Images/VecCalc/VecField006.png
        :alt: Vector Option

        Vector Option

    The reason we default the head of the vector to a small diamond is so that the program has a better response in animations and slider changes.  The vector graphing option may produce some sluggish response when using sliders.  The vector fields in :math:`\mathbb{R}^3` do not have a vector rendering option and always use the circle to represent the head of the vector.


Gradient Fields
---------------

A type of vector field that is very useful is a gradiant field.  This is simply the vector field produced by the gradiant of a multivariable function.

.. admonition:: Definition: Gradient Fields

    A gradiant field is the vector field produced by the gradiant of a multivariable function. Specifically,

    .. math::
        \mathbf{F}(x, y) = \nabla f(x, y) =  f_x(x, y) \mathbf{i} + f_y(x, y) \mathbf{j}

    or

    .. math::
        \mathbf{F}(x, y, z) = \nabla f(x, y, z) =  f_x(x, y, z) \mathbf{i} + f_y(x, y, z) \mathbf{j}  + f_z(x, y, z) \mathbf{k}

Not all vector fields are gradiant fields, in fact most are not.  If they are then the field will have some nice properties. Hence we will give a name to them.

.. admonition:: Definition: Conservative Vector Fields

    A vector field :math:`\mathbf{F}` is a conservative vector field if there exists a multivariable function :math:`f` such that :math:`\mathbf{F} = \nabla f.`  If this is the case then the function :math:`f` is called the potential function for the vector field :math:`\mathbf{F}.`  In addition, the potential function for a conservative vector field is unique in the sense that if :math:`f` and :math:`g` are two potential functions for the vector field :math:`\mathbf{F}` then there is a constant :math:`C` such that :math:`f = g+C.`


Example: Gradient Field of :math:`f(x, y) = y^{2} \cos{\left(x + y \right)}`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

CLAE
""""

Input the function,

.. code-block:: console

    y^2*cos(x + y)

Select ``Calculus > Vector Calculus > Gradiant``, the result should be,

.. math::
    \left[\begin{array}{c}- y^{2} \sin{\left(x + y \right)}\\- y^{2} \sin{\left(x + y \right)} + 2 y \cos{\left(x + y \right)}\end{array}\right]

Click and drag this over to the 2D graphics window and you will see,

.. figure:: Images/VecCalc/VecField007.png
    :alt: Gradient Field of :math:`f(x, y) = y^{2} \cos{\left(x + y \right)}`

    Gradient Field of :math:`f(x, y) = y^{2} \cos{\left(x + y \right)}`

As we mentioned above, most vector fields are not conservative.  To determine if a vector field is conservative we need to find a function :math:`f` such that :math:`\mathbf{F} = \nabla f.`  If such a function exists then the field is conservative and if we can show that no function exists then the field is not conservative.  We can, however, show that a vector field is not conservative in an easier manner.

.. admonition:: Theorem: The Cross-Partial Property of Conservative Vector Fields

    - If :math:`\mathbf{F}(x, y) = (P(x, y), Q(x, y))` is a conservative vector field in :math:`\mathbb{R}^2` then :math:`\displaystyle \frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}`
    - If :math:`\mathbf{F}(x, y, z) = (P(x, y, z), Q(x, y, z), R(x, y, z))` is a conservative vector field in :math:`\mathbb{R}^3` then

    .. math::
        \frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x} \qquad \frac{\partial Q}{\partial z} = \frac{\partial R}{\partial y} \qquad {\rm and } \qquad \frac{\partial R}{\partial x} = \frac{\partial P}{\partial z}

From this theorem if we have a field where any of the cross-partials are not equal we know that the field is not conservative.


Example: :math:`\left( x + y^{2}, \  y \cos{\left(x \right)}\right)`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

CLAE
""""

Input the two component functions,

.. code-block:: console

    x+y^2

and

.. code-block:: console

    y*cos(x)

Takin the partial of the first with respect to *y* and the second with respect to *x* we get

.. math::
    2 y \qquad {\rm and } \qquad - y \sin{\left(x \right)}

these are clearly not equal and hence the vector field is not conservative.


