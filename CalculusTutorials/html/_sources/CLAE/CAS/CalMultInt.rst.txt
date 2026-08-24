:index:`Multiple Integrals`
===========================

These tools are for taking multiple integrals.  If you are working with a single variable equation and are doing a single integral see :doc:`CalIntegration` for details on single integrals.

:index:`Double Integral`
------------------------

To take a double integral of a function select this option and a dialog box will appear asking the user to input the first (inner) integral variable, the lower and upper bounds for that integral, the second (outer) integral variable, and the lower and upper bounds for that integral.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.   The inputs can be any valid expression including using the CAS workspace entries (R1, R2, ...).

For example, say we want to take the following integral,

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

:index:`Double Integral Approximation`
--------------------------------------

To approximate a double integral of a function select this option and a dialog box will appear asking the user to input the first (inner) integral variable, the lower and upper bounds for that integral, the second (outer) integral variable, and the lower and upper bounds for that integral.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these. The inputs can be any valid expression including using the CAS workspace entries (R1, R2, ...).

For example, say we want to approximate the following integral,

.. math::
    \int_0^2 \int_{x^2}^{2x} x^2 + y^2 \; dy \; dx

Then the inputs would be

- First (Inner) Variable: ``y``
- Lower Bound: ``x^2``
- Upper Bound: ``2*x``
- Second (Outer) Variable: ``x``
- Lower Bound: ``0``
- Upper Bound: ``2``

Once these are all in and OK is clicked you should get the result 6.171428571428571, which is approximately :math:`\frac{216}{35}`, as expected.


:index:`Triple Integral`
------------------------

To take a triple integral of a function select this option and a dialog box will appear asking the user to input the first (inner) integral variable, the lower and upper bounds for that integral, the second (middle) integral variable, the lower and upper bounds for that integral, the third (outer) integral variable, and the lower and upper bounds for that integral.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.   The inputs can be any valid expression including using the CAS workspace entries (R1, R2, ...).

For example, say we want to take the following integral,

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

Once these are all in and OK is clicked you should get the result :math:`- \frac{e}{4} - \frac{e \left(1 - e\right)}{4}`.


:index:`Triple Integral Approximation`
--------------------------------------

To approximate a triple integral of a function select this option and a dialog box will appear asking the user to input the first (inner) integral variable, the lower and upper bounds for that integral, the second (middle) integral variable, the lower and upper bounds for that integral, the third (outer) integral variable, and the lower and upper bounds for that integral.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.   The inputs can be any valid expression including using the CAS workspace entries (R1, R2, ...).

For example, say we want to approximate the following integral,

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

Once these are all in and OK is clicked you should get the result 0.4881231105031399 which is an approximation to :math:`- \frac{e}{4} - \frac{e \left(1 - e\right)}{4}`, as expected.


.. tip::
    With multiple integrals there are a lot of inputs to be filled out.  The program will make sure that the expressions are legitimate before closing the dialog box and completing the operation but if the expression is legitimate but not what you want the process will finish and you will need to do it again with the correct inputs.  To help avoid mistyping expressions you can input the bounds as expressions in the CAS, hence seeing if they are correct and then use the CAS workspace designation (R1, R2, ...) to enter the expression into the multiple integral dialogs.

:index:`Jacobian`
-----------------

This option calculates the Jacobian of a transformation.  Input the :math:`(x, y)` to :math:`(u, v)` transformation (or the :math:`(x, y, z)` to :math:`(u, v, w)` transformation) into the CAS as either a list or column vector (matrix) and then select this option.  A dialog box will appear asking for the order of the :math:`(u, v)` or :math:`(u, v, w)` variables.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

**The Jacobian for Polar Coordinates**: The :math:`(x, y)` to :math:`(u, v)` transformation in this case is :math:`x = r \cos(t) \quad y = r \sin(t)`.  We will use ``r`` and ``t`` (theta) for ``u`` and ``v`` in this case.  Our input would be ``[r*cos(t), r*sin(t)]``.  Select this option and the dialog box will have automatically loaded in ``[r, t]`` for the variables, we will leave these as they are.  Once we click OK the result is :math:`r \sin^{2}{\left(t \right)} + r \cos^{2}{\left(t \right)}` which simplifies to :math:`r` as we would expect.


**The Jacobian for Spherical Coordinates**: The :math:`(x, y, z)` to :math:`(u, v, w)` transformation in this case is :math:`x = r \sin(p) \cos(t) \quad y = r \sin(p) \sin(t) \quad z = r\cos(p)`.  We will use ``r`` (rho), ``p`` (phi) and ``t`` (theta) for ``u``, ``v``, and ``w`` in this case.  Our input would be ``[r*sin(p)*cos(t), r*sin(p)*sin(t), r*cos(p)]``. Select this option and the dialog box will have automatically loaded in ``[p, r, t]`` for the variables, we will leave these as they are.  Note that this is not the order you would probably do this calculation in, ``[r, t, p]`` is more natural.  You can change the variables input to this if you would like but we will get the same final result either way. Once we click OK the result is

.. math::
    - r^{2} \sin^{3}{\left(p \right)} \sin^{2}{\left(t \right)} - r^{2} \sin^{3}{\left(p \right)} \cos^{2}{\left(t \right)} - r^{2} \sin{\left(p \right)} \sin^{2}{\left(t \right)} \cos^{2}{\left(p \right)} - r^{2} \sin{\left(p \right)} \cos^{2}{\left(p \right)} \cos^{2}{\left(t \right)}

which simplifies to :math:`- r^{2} \sin{\left(p \right)}`.  As you know the Jacobian is the absolute value of the determinant of the Jacobian Matrix so sometimes (like here) we need to go a little further in examining the domains of the variables.  Since :math:`0 \leq p \leq \pi`, we have :math:`\sin{\left(p \right)} \geq 0` so we need to remove the minus sign and our result is :math:`r^{2} \sin{\left(p \right)}`.

.. note::
    Note that the result of the Jacobian was not simplified.  The expressions for the Jacobian can be lengthy and since simplification can be a long process we decided to separate these operations and not have the Jacobian tool automatically simplify the result of the determinant.

:index:`Jacobian Matrix`
------------------------

This option calculates the Jacobian Matrix of a transformation.  Input the :math:`(x, y)` to :math:`(u, v)` transformation (or the :math:`(x, y, z)` to :math:`(u, v, w)` transformation) into the CAS as either a list or column vector (matrix) and then select this option.  A dialog box will appear asking for the order of the :math:`(u, v)` or :math:`(u, v, w)` variables.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

**The Jacobian for Polar Coordinates**: The :math:`(x, y)` to :math:`(u, v)` transformation in this case is :math:`x = r \cos(t) \quad y = r \sin(t)`.  We will use ``r`` and ``t`` (theta) for ``u`` and ``v`` in this case.  Our input would be ``[r*cos(t), r*sin(t)]``.  Select this option and the dialog box will have automatically loaded in ``[r, t]`` for the variables, we will leave these as they are.  Once we click OK the result is

.. math::
    \left[\begin{array}{cc}\cos{\left(t \right)} & - r \sin{\left(t \right)}\\\sin{\left(t \right)} & r \cos{\left(t \right)}\end{array}\right]

whose determinant is :math:`r \sin^{2}{\left(t \right)} + r \cos^{2}{\left(t \right)} = r`.

**The Jacobian for Spherical Coordinates**: The :math:`(x, y, z)` to :math:`(u, v, w)` transformation in this case is :math:`x = r \sin(p) \cos(t) \quad y = r \sin(p) \sin(t) \quad z = r\cos(p)`.  We will use ``r`` (rho), ``p`` (phi) and ``t`` (theta) for ``u``, ``v``, and ``w`` in this case.  Our input would be ``[r*sin(p)*cos(t), r*sin(p)*sin(t), r*cos(p)]``. Select this option and the dialog box will have automatically loaded in ``[p, r, t]`` for the variables, we will leave these as they are.  Note that this is not the order you would probably do this calculation in, ``[r, t, p]`` is more natural.  You can change the variables input to this if you would like, this will permute the columns of the matrix. When taking the determinant this will result in a :math:`(-1)^n` factor but when we take the absolute value of the determinant we will get the same final result. Once we click OK the result is

.. math::
    \left[\begin{array}{ccc}r \cos{\left(p \right)} \cos{\left(t \right)} & \sin{\left(p \right)} \cos{\left(t \right)} & - r \sin{\left(p \right)} \sin{\left(t \right)}\\r \sin{\left(t \right)} \cos{\left(p \right)} & \sin{\left(p \right)} \sin{\left(t \right)} & r \sin{\left(p \right)} \cos{\left(t \right)}\\- r \sin{\left(p \right)} & \cos{\left(p \right)} & 0\end{array}\right]

whose determinant is

.. math::
    - r^{2} \sin^{3}{\left(p \right)} \sin^{2}{\left(t \right)} - r^{2} \sin^{3}{\left(p \right)} \cos^{2}{\left(t \right)} - r^{2} \sin{\left(p \right)} \sin^{2}{\left(t \right)} \cos^{2}{\left(p \right)} - r^{2} \sin{\left(p \right)} \cos^{2}{\left(p \right)} \cos^{2}{\left(t \right)} = - r^{2} \sin{\left(p \right)}


Variable Assumptions
--------------------

.. include:: ../CLAE/VariableAssumptions.md
