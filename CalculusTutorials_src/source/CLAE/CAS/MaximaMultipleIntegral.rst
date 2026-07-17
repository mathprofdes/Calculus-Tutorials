:index:`Maxima: Multiple Integrals and Partial Differentiation`
===============================================================

Multiple Partial Derivatives
----------------------------

The derivative option will take a partial derivative of a multivariable function.  This option allows the user to take multiple partial derivatives at one time.  When selected, a dialog box will appear asking the user for a list of variables and a list of orders.  So if the user inputs ``[x, y, z]`` for the variables and ``[1, 2, 3]`` for the orders then the program will take the partial with respect to *x*, the second partial with respect to *y*, and the third partial with respect to *z*.  For example, with the function :math:`\sin{\left(x y \right)}` if we input ``[x, y]`` and ``[2, 3]`` we get,

.. math::
    x^{3} y^{2} \cos{\left(x y \right)} + 6 x^{2} y \sin{\left(x y \right)} - 6 x \cos{\left(x y \right)}

Double Integral
---------------

To take a double integral of a function select this option and a dialog box will appear asking the user to input the first (inner) integral variable, the lower and upper bounds for that integral, the second (outer) integral variable, and the lower and upper bounds for that integral. For example, say we want to take the following integral,

.. math::
    \int_0^2 \int_{x^2}^{2x} x^2 + y^2 \; dy \; dx

Then the inputs would be

- First (Inner) Variable: ``y``
- Lower Bound: ``x^2``
- Upper Bound: ``2*x``
- Second (Outer) Variable: ``x``
- Lower Bound: ``0``
- Upper Bound: ``2``

Once these are all in and OK is clicked you should get the result :math:`\frac{216}{35}`.

Triple Integral
---------------

To take a triple integral of a function select this option and a dialog box will appear asking the user to input the first (inner) integral variable, the lower and upper bounds for that integral, the second (middle) integral variable, the lower and upper bounds for that integral, the third (outer) integral variable, and the lower and upper bounds for that integral. For example, say we want to take the following integral,

.. math::
    \int_0^1 \int_0^1 \int_{0}^{2 - x^2 -y^2} xye^z \; dz \; dy \; dx

Then the inputs would be

- First (Inner) Variable: ``z``
- Lower Bound: ``0``
- Upper Bound: ``2 - x^2 -y^2``
- Second (Middle) Variable: ``y``
- Lower Bound: ``0``
- Upper Bound: ``1``
- Third (Outer) Variable: ``x``
- Lower Bound: ``0``
- Upper Bound: ``1``

Once these are all in and OK is clicked you should get the result :math:`- \frac{e}{2} + \frac{e^{2}}{4}`.

Jacobian Matrix
---------------

This option calculates the Jacobian Matrix of a transformation.  Input the :math:`(x, y)` to :math:`(u, v)` transformation (or the :math:`(x, y, z)` to :math:`(u, v, w)` transformation) into the CAS as either a list or column vector (matrix) and then select this option.  A dialog box will appear asking for the order of the :math:`(u, v)` or :math:`(u, v, w)` variables.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

**The Jacobian for Polar Coordinates**: The :math:`(x, y)` to :math:`(u, v)` transformation in this case is :math:`x = r \cos(t) \quad y = r \sin(t)`.  We will use ``r`` and ``t`` (theta) for ``u`` and ``v`` in this case.  Our input would be ``[r*cos(t), r*sin(t)]``.  Select this option and the dialog box will have automatically loaded in ``[r, t]`` for the variables, we will leave these as they are.  Once we click OK the result is

.. math::
    \left[\begin{array}{cc}\cos{\left(t \right)} & - r \sin{\left(t \right)}\\\sin{\left(t \right)} & r \cos{\left(t \right)}\end{array}\right]

whose determinant is :math:`r \sin^{2}{\left(t \right)} + r \cos^{2}{\left(t \right)} = r`.

**The Jacobian for Spherical Coordinates**: The :math:`(x, y, z)` to :math:`(u, v, w)` transformation in this case is :math:`x = r \sin(p) \cos(t) \quad y = r \sin(p) \sin(t) \quad z = r\cos(p)`.  We will use ``r`` (rho), ``p`` (phi) and ``t`` (theta) for ``u``, ``v``, and ``w`` in this case.  Our input would be ``[r*sin(p)*cos(t), r*sin(p)*sin(t), r*cos(p)]``. Select this option and the dialog box will have automatically loaded in ``[p, r, t]`` for the variables, we will leave these as they are.  Note that this is not the order you would probably do this calculation in, ``[r, t, p]`` is more natural.  You can change the variables input to this if you would like, this will permute the columns of the matrix. When taking the determinant this will result in a :math:`(-1)^n` factor but when we take the absolute value of the determinant we will get the same final result. Once we click OK the result is

.. math::
    \left[\begin{array}{ccc}\sin{\left(p \right)} \cos{\left(t \right)} & - r \sin{\left(p \right)} \sin{\left(t \right)} & r \cos{\left(p \right)} \cos{\left(t \right)}\\\sin{\left(p \right)} \sin{\left(t \right)} & r \sin{\left(p \right)} \cos{\left(t \right)} & r \sin{\left(t \right)} \cos{\left(p \right)}\\\cos{\left(p \right)} & 0 & - r \sin{\left(p \right)}\end{array}\right]

whose determinant is

.. math::
    - r^{2} \sin^{3}{\left(p \right)} \sin^{2}{\left(t \right)} - r^{2} \sin^{3}{\left(p \right)} \cos^{2}{\left(t \right)} - r^{2} \sin{\left(p \right)} \sin^{2}{\left(t \right)} \cos^{2}{\left(p \right)} - r^{2} \sin{\left(p \right)} \cos^{2}{\left(p \right)} \cos^{2}{\left(t \right)} = - r^{2} \sin{\left(p \right)}

