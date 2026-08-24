:index:`Parametric Equations`
=============================

Discussion & Definitions
------------------------

.. admonition:: Definition: Parametric Equations

    If :math:`x` and :math:`y` are continuous functions of :math:`t` on an interval :math:`I`, then the equations

    .. math::
        x = x(t) \qquad {\rm and} \qquad  y = y(t)

    are called parametric equations and :math:`t` is called the parameter. The set of points :math:`(x, y)` obtained as :math:`t` varies over the interval :math:`I` is called the graph of the parametric equations. The graph of parametric equations is called a parametric curve or plane curve.

Example: The Cycloid
--------------------

The Cycloid is defined parametrically as,

.. math::
    x(t) = a \left(t - \sin{\left(t \right)}\right) \qquad y(t)= a \left(1 - \cos{\left(t \right)}\right)

with :math:`-\infty < t < \infty.`  The Cycloid is the curve traced out by a fixed point on a moving wheel.

GeoGebra
^^^^^^^^

There are two primary ways to load a parametrically defined curve into GeoGebra, either as an ordered pair ``(x(t), y(t))`` or using the ``Curve`` command.  As an ordered pair we would input,

.. code-block:: console

    (a (t - sin(t)), a (1 - cos(t)))

Note that this is automatically converted to the ``Curve`` command.  The curve command has the form,

``Curve(x(t), y(t), parameter variable, lower bound, upper bound)``

GeoGebra also saw the trigonometric functions in the expressions and automatically assumed that the bounds for the parameter should be :math:`[0, 2\pi].`  This is not the case for the Cycloid so change these to about :math:`[-10, 10].`

Alternatively you could input the curve using the ``Curve`` command as below,

.. code-block:: console

    Curve((a (t-sin(t)),a (1-cos(t))),t,-10,10)

.. figure:: Images/Para/Para001.png
    :alt: The Cycloid

    The Cycloid

CLAE
^^^^

In CLAE, you can use either a list of two expressions ``[x(t), y(t)]`` or a :math:`2 \times 1` matrix.  In most cases you will probably just use a list, we will show the matrix input in the note at the end.

.. code-block:: console

    [a*(t - sin(t)), a*(1 - cos(t))]

Now just click and drag this over to the graphic area.  It should default to a parametric equation, if not, change its type to Parametric Equations.

.. figure:: Images/Para/Para002.png
    :alt: The Cycloid

    The Cycloid

.. note::

    CLAE also recognizes a :math:`2 \times 1` matrix with expression entries for *x* and *y* as a parametric equation.  For example, the following matrix is also the cycloid.

    .. math::
        \left[\begin{array}{c}a \left(t - \sin{\left(t \right)}\right)\\a \left(1 - \cos{\left(t \right)}\right)\end{array}\right]

    You can input these either with the matrix editor, the preferred method, or with the matrix syntax for SymPy.

    .. code-block:: console

        Matrix([[a*(t - sin(t))], [a*(1 - cos(t))]])


Example: The Hypocycloid
------------------------

The Hypocycloid is defined parametrically as,

.. math::
    x(t) = b \cos{\left(\frac{t \left(a - b\right)}{b} \right)} + \left(a - b\right) \cos{\left(t \right)} \qquad y(t)= - b \sin{\left(\frac{t \left(a - b\right)}{b} \right)} + \left(a - b\right) \sin{\left(t \right)}

with :math:`-\infty < t < \infty.`  The Hypocycloid i similar to the Cycloid except that it is the curve traced out by a fixed point on a moving wheel of radius *b* rolling inside the circle of radius *a*.

.. figure:: Images/Para/Para003.png
    :alt: The Hypocycloid Construction

    The Hypocycloid Construction

Alter the *a* and *b* sliders to see the different curves, you may want to increase the parameter range.

GeoGebra
^^^^^^^^

There are two primary ways to load a parametrically defined curve into GeoGebra, either as an ordered pair ``(x(t), y(t))`` or using the ``Curve`` command.  As an ordered pair we would input,

.. code-block:: console

    (b cos(t (a - b)/b) + (a - b) cos(t), -b sin(t (a - b)/b) + (a - b) sin(t))

Note that this is automatically converted to the ``Curve`` command.  The curve command has the form,

``Curve(x(t), y(t), parameter variable, lower bound, upper bound)``

GeoGebra also saw the trigonometric functions in the expressions and automatically assumed that the bounds for the parameter should be :math:`[0, 2\pi].`  This is not the case for the Hypocycloid so change these to about :math:`[-10, 10].`

Alternatively you could input the curve using the ``Curve`` command as below,

.. code-block:: console

    Curve((b cos(t ((a-b)/(b)))+(a-b) cos(t),-b sin(t ((a-b)/(b)))+(a-b) sin(t)),t,-10,10)

.. figure:: Images/Para/Para005.png
    :alt: The Hypocycloid

    The Hypocycloid

CLAE
^^^^

In CLAE, you can use either a list of two expressions ``[x(t), y(t)]`` or a :math:`2 \times 1` matrix.  In most cases you will probably just use a list, we will show the matrix input in the note at the end.

.. code-block:: console

    [b*cos(t*(a - b)/b) + (a - b)*cos(t), -b*sin(t*(a - b)/b) + (a - b)*sin(t)]

Now just click and drag this over to the graphic area.  It should default to a parametric equation, if not, change its type to Parametric Equations.

.. figure:: Images/Para/Para004.png
    :alt: The Hypocycloid

    The Hypocycloid

Alter the *a* and *b* sliders to see the different curves, you may want to increase the parameter range and the number of points plotted.

.. note::

    CLAE also recognizes a :math:`2 \times 1` matrix with expression entries for *x* and *y* as a parametric equation.  For example, the following matrix is also the cycloid.

    .. math::
        \left[\begin{array}{c}b \cos{\left(\frac{t \left(a - b\right)}{b} \right)} + \left(a - b\right) \cos{\left(t \right)}\\- b \sin{\left(\frac{t \left(a - b\right)}{b} \right)} + \left(a - b\right) \sin{\left(t \right)}\end{array}\right]

    You can input these either with the matrix editor, the preferred method, or with the matrix syntax for SymPy.

    .. code-block:: console

        Matrix([[b*cos(t*(a - b)/b) + (a - b)*cos(t)], [-b*sin(t*(a - b)/b) + (a - b)*sin(t)]])

