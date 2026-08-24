:index:`Directional Derivatives and the Gradient`
=================================================


Directional Derivative
----------------------

Rcall that the partial derivatives :math:`f_x(x, y)` and :math:`f_y(x, y)` are the rates of change in the *x* and *y* directions.  One question is can we find the rate of change on a surface at a point in a direction that is not parallel to the *x* or *y* axes.  The answer is, of course, yes, we simply need to approach the point of tangency along the line in the direction of a unit vector :math:`\mathbf{u} = (a, b).` This can be done easily by the following calculation.

.. admonition:: Definition: Directional Derivative

    The directional derivative of a function :math:`z = f(x, y)` at the point :math:`(x_0, y_0)` in the direction of a unit vector :math:`\mathbf{u} = (a, b)` is

    .. math::
        D_{\mathbf{u}}f(x_0, y_0) = \lim_{h \to 0} \frac{f(x_0 + ah, y_0 + bh) - f(x_0, y_0)}{h}

    if this limit exists.

Note that if our unit vector is :math:`\mathbf{i} = (1, 0)` then

.. math::
    D_{\mathbf{i}}f(x_0, y_0) = \lim_{h \to 0} \frac{f(x_0 + h, y_0) - f(x_0, y_0)}{h} = f_x(x_0, y_0)

and if our unit vector is :math:`\mathbf{j} = (0, 1)` then

.. math::
    D_{\mathbf{j}}f(x_0, y_0) = \lim_{h \to 0} \frac{f(x_0 , y_0+h) - f(x_0, y_0)}{h} = f_y(x_0, y_0)

So the directional derivative simply generalized the partial derivatives.

Fortunately we do not need to result to the limit definition when calculating the directional derivative, it can be written in terms of the partial derivatives and the direction vector.

.. admonition:: Theorem: Calculating Directional Derivative

    Given the function :math:`z = f(x, y)` and a unit vector :math:`\mathbf{u} = (a, b)` then,

    .. math::
        D_{\mathbf{u}}f(x, y) = f_x(x, y) a + f_y(x, y) b


The Gradient Vector
-------------------


Note from the last theorem on calculating the directional derivative, we can rewrite the expression as the dot product of two vectors.

.. math::
    D_{\mathbf{u}}f(x, y) = f_x(x, y) a + f_y(x, y) b = (f_x(x, y), f_y(x, y)) \cdot (a, b) = (f_x(x, y), f_y(x, y)) \cdot \mathbf{u}

The first vector in this dot product comes up fairly often and we give it a name.

.. admonition:: Definition: Gradient Vector

    Let :math:`f(x, y)` be a function of two variables, then the gradient of *f* is the vector function :math:`\nabla f`,

    .. math::
        \nabla f = (f_x(x, y), f_y(x, y)) = f_x(x, y) \mathbf{i} + f_y(x, y) \mathbf{j}

Given the above notation we can rewrite the directional derivative calculation.

.. admonition:: Theorem: Calculating Directional Derivative

    Given the function :math:`z = f(x, y)` and a unit vector :math:`\mathbf{u} = (a, b)` then,

    .. math::
        D_{\mathbf{u}}f(x, y) =  \nabla f(x, y) \cdot \mathbf{u}

Example: :math:`f(x, y) = x^{2} \ln{\left(y \right)}` at :math:`(3, 1)` in the direction :math:`(-5, 12)`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

CLAE
""""

This calculation in CLAE takes only a couple of steps.  First input the expression,

.. code-block:: console

    x^2*ln(y)

Find is gradiant with ``Calculus > Vector Calculus > Gradiant``, the result should be,

.. math::
    \left[\begin{array}{c}2 x \ln{\left(y \right)}\\\frac{x^{2}}{y}\end{array}\right]

Evaluate this at :math:`(3, 1)` with ``Algebra > Evaluate``, keep the variables as ``[x, y]`` and input ``[3, 1]`` for the expressions.  The result should be,

.. math::
    \left[\begin{array}{c}0\\9\end{array}\right]

Now input the direction :math:`(-5, 12)` as a vector, the result should be,

.. math::
    \left[\begin{array}{c}-5\\12\end{array}\right]

This is not a unit vector so we will convert it using ``Vector > Normalize``, the result should be,

.. math::
    \left[\begin{array}{c}- \frac{5}{13}\\\frac{12}{13}\end{array}\right]

Finally take the dot product of this and the evaluated gradiant vector with ``Vector > Dot Product`` and the result is :math:`\frac{108}{13}.`

.. note::

    Note that all of this can be generalized to three variables,

    .. admonition:: Definition: Directional Derivative

        The directional derivative of a function :math:`w = f(x, y, z)` at the point :math:`(x_0, y_0, z_0)` in the direction of a unit vector :math:`\mathbf{u} = (a, b, c)` is

        .. math::
            D_{\mathbf{u}}f(x_0, y_0, z_0) = \lim_{h \to 0} \frac{f(x_0 + ah, y_0 + bh, z_0 + ch) - f(x_0, y_0, z_0)}{h}

        if this limit exists.

    .. admonition:: Definition: Gradient Vector

        Let :math:`f(x, y, z)` be a function of three variables, then the gradient of *f* is the vector function :math:`\nabla f`,

        .. math::
            \nabla f = (f_x(x, y, z), f_y(x, y, z), f_z(x, y, z)) = f_x(x, y, z) \mathbf{i} + f_y(x, y, z) \mathbf{j}+ f_z(x, y, z) \mathbf{k}

    .. admonition:: Theorem: Calculating Directional Derivative

        Given the function :math:`z = f(x, y, z)` and a unit vector :math:`\mathbf{u} = (a, b, c)` then,

        .. math::
            D_{\mathbf{u}}f(x, y, z) =  \nabla f(x, y, z) \cdot \mathbf{u}


Properties of the Directional Derivative and the Gradiant
---------------------------------------------------------

Suppose we have a function *f* of two or three variables and we consider all possible directional derivatives of *f* at a given point. These give the rates of change of *f* in all possible directions. We can then ask the questions: in which of these directions does *f* change fastest and what is the maximum rate of change?

This is fairly easy to determine, consider the following derivation from the equations above,

.. math::
    D_{\mathbf{u}} f = \nabla f \cdot \mathbf{u} = |\nabla f| |\mathbf{u}| \cos(\theta) = |\nabla f| \cos(\theta)

Remember that :math:`\mathbf{u}` is a unit vector and :math:`\theta` is the angle between :math:`\nabla f` and :math:`\mathbf{u}.`  This last formula is a maximum when :math:`\cos(\theta) = 1` and hence :math:`\theta = 0.`  So the maximum directional derivative is :math:`|\nabla f|` and happens when :math:`\mathbf{u}` is in the same direction as :math:`\nabla f.`

Another interesting property is between the gradiant vector and the level curves (or surfaces) of the function.  We will look at the situation with level curves, surfaces follow the same derivations and logic with three variables instead of two.  Take a level curve to a function of two variables, that is, :math:`f(x, y) = k` for some constant *k*.  The level curve is a line so it can be represented as :math:`\mathbf{r}(t) = (x(t), y(t)).` So :math:`f(x(t), y(t)) = k,` taking the derivative of both sides gives us,

.. math::
    \frac{\partial f}{\partial x} \frac{dx}{dt} + \frac{\partial f}{\partial y} \frac{dy}{dt} & = 0 \\
    f_x x'(t) + f_y y'(t) & = 0 \\
    (f_x, f_y) \cdot (x'(t), y'(t)) & = 0 \\
    \nabla f \cdot \mathbf{r}'(t) & = 0 \\

The vector :math:`\mathbf{r}'(t)` is tangent to the level curve and since the dot product of this and the gradiant is 0, the gradiant vector is perpendicular (orthogonal or normal) to the level curve or surface.

We summarize the discussion above with the following theorem.

.. admonition:: Theorem: Properties of the Gradiant Vector

    Let *f* be a differentiable function of two or three variables and suppose that :math:`\nabla f(\mathbf{x}) \neq \mathbf{0}.`

    - The directional derivative in the direction of a unit vector :math:`\mathbf{u}` is :math:`D_{\mathbf{u}}f(\mathbf{x}) =  \nabla f(\mathbf{x}) \cdot \mathbf{u}.`
    - :math:`\nabla f(\mathbf{x})` points in the direction of the maximum rate of increase of the function *f* at the point :math:`\mathbf{x}` and that maximum rate is :math:`|\nabla f(\mathbf{x})|.`
    - :math:`\nabla f(\mathbf{x})` is perpendicular (orthogonal) to the level curve or surface of *f* at the point :math:`\mathbf{x}.`

Example: Visualizing the Properties of the Gradiant Vector Theorem
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We will illustrate the second and third parts of the theorem with the function of two variables,

.. math::
    f(x, y) = \frac{x^{2} y}{x^{2} + y^{2}}

CLAE
""""

First input the function,

.. code-block:: console

    x^2*y/(x^2 + y^2)

Click and drag this over to the 3D graphics window, the image should look like the following (we did scale the *z*-axis a little).

.. figure:: Images/FctSevVars/DirDer001.png
    :alt: :math:`f(x, y) = \frac{x^{2} y}{x^{2} + y^{2}}`

    :math:`f(x, y) = \frac{x^{2} y}{x^{2} + y^{2}}`

Select the function and take its gradiant with ``Calculus > Vector Calculus > Gradiant`` the result should be,

.. math::
    \left[\begin{array}{c}- \frac{2 x^{3} y}{\left(x^{2} + y^{2}\right)^{2}} + \frac{2 x y}{x^{2} + y^{2}}\\- \frac{2 x^{2} y^{2}}{\left(x^{2} + y^{2}\right)^{2}} + \frac{x^{2}}{x^{2} + y^{2}}\end{array}\right]

which simplifies to

.. math::
    \left[\begin{array}{c}\frac{2 x y^{3}}{\left(x^{2} + y^{2}\right)^{2}}\\\frac{x^{2} \left(x^{2} - y^{2}\right)}{x^{4} + 2 x^{2} y^{2} + y^{4}}\end{array}\right]

What we want to do now is plot a grid of gradiant vectors along with this surface so we can see a relationship between the surface and the gradiant vectors.  To do this we need to rewrite the gradiant as a three dimensional vector instead of a two dimensional vector.  Assuming that this last vector was in ``R3``, select ``Edit > Input Vector`` or hit the corresponding toolbar button.  Input ``R3, 0`` and click OK.  The result is,

.. math::
    \left[\begin{array}{c}\frac{2 x y^{3}}{\left(x^{2} + y^{2}\right)^{2}}\\\frac{x^{2} \left(x^{2} - y^{2}\right)}{x^{4} + 2 x^{2} y^{2} + y^{4}}\\0\end{array}\right]

This just put in a 0 for the *z* component.  Click and drag this vector over to the 3D graphics window, it should come in as a vector field, which is what we want.  Go into the properties and change the number of *z* divisions to 3 (which is the minimum).  Also change the *x* and *y* grid divisions to 20 each.  The image you get should look like the ones displayed below.  Move the graph around and notice that the vectors are pointing in the direction that is moving up the surface.  Hence the gradiant vectors are in the direction of the maximum increase of the function.

.. figure:: Images/FctSevVars/DirDer002.png
    :alt: Surface and Gradiant Field

    Surface and Gradiant Field

.. figure:: Images/FctSevVars/DirDer003.png
    :alt: Surface and Gradiant Field

    Surface and Gradiant Field

Another way to see this is using a color contour map.  Here is how we can do this.  For the surface, go into the properties and change the surface shading  to shade surface by height.  Change the gradiant vector colors to black. Select ``Camera > Position to Top of Z-Axis`` and select ``View > Orthogonal Mode``.  You should see the following image.

.. figure:: Images/FctSevVars/DirDer004.png
    :alt: Surface Color Contour and Gradiant Field

    Surface Color Contour and Gradiant Field

The colors go ROYGBIV from top to bottom.  Here again we can see that the gradiant vectors point in the direction of moving up the surface.

To visualize the third statement we will use the 2D graphics window.  Click and drag the original function over to the 2D graphics window, change the type to Contour Map, select ``View > Set View Window to 1-1``.  Click and drag the gradiant vector (2D version) to the 2D graphics window, it should come in as a vector field.  The image should look like the following.

.. figure:: Images/FctSevVars/DirDer005.png
    :alt: Contour Map and Gradiant Field

    Contour Map and Gradiant Field

Note that the gradiant vectors are perpendicular to each of the graphed level curves.


Tangent Planes to Level Surfaces
--------------------------------

Extending the above theorem just a little. If we have a level surface, that is, :math:`f(x, y, z) = k` and a point :math:`P = (x_0, y_0, z_0)` on the surface, we know that the gradient vector :math:`\nabla f(x_0, y_0, z_0)` is normal to the surface at *P*, and hence is a normal vector to the tangent plane to the surface at *P*.  Hence the equation of the tangent plane to *f* at *P* can be written as,

.. math::
    f_x(x_0, y_0, z_0) (x-x_0) + f_y(x_0, y_0, z_0) (y-y_0) + f_z(x_0, y_0, z_0) (z-z_0) = 0


Example: Tangent Plane to :math:`x y^{2} z^{3} = 8` at :math:`(2, 2, 1)`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here we will use the above theorem to find the tangent plane to the surface :math:`x y^{2} z^{3} = 8` at the point :math:`(2, 2, 1).`

CLAE
""""

First input the surface, in CALE we need to define all implicit curves and surfaces as expressions equal to 0, so we rewrite this as :math:`x y^{2} z^{3} - 8 = 0.`

.. code-block:: console

    x*y^2*z^3 - 8

CLick and drag this over to the 3D graphics window.  The plot may look a little rough, to smooth it out go into the properties and set the grid divisions to 50 each.  We did zoom in a little for the following image.

.. figure:: Images/FctSevVars/DirDer006.png
    :alt: Surface

    Surface

The tangent plane takes only a couple steps, take the gradiant vector with ``Calculus > Vector Calculus > Gradiant`` the result is,

.. math::
    \left[\begin{array}{c}y^{2} z^{3}\\2 x y z^{3}\\3 x y^{2} z^{2}\end{array}\right]

Now evaluate it at the point :math:`(2, 2, 1)` with ``Algebra > Evaluate``, leave the variables as ``[x, y, z]`` and input for the expressions ``[2,2,1]``.  The result is,

.. math::
    \left[\begin{array}{c}4\\8\\24\end{array}\right]

This is a normal vector to the tangent plane.  To make the editing a minimum we will create the vector,

.. math::
    \left[\begin{array}{c}x - 2\\y - 2\\z - 1\end{array}\right]

Use the vector input dialog and input ``[x-2, y-2, z-1]``.  Now take the dot product of this and the evaluated gradiant vector to get the tangent plane,

.. math::
    4 x + 8 y + 24 z - 48

which means

.. math::
    4 x + 8 y + 24 z - 48 = 0  \qquad {\rm or } \qquad 4 x + 8 y + 24 z = 48

CLick and drag this over to the 3D graphics window.

.. figure:: Images/FctSevVars/DirDer007.png
    :alt: Surface and Tangent Plane

    Surface and Tangent Plane
