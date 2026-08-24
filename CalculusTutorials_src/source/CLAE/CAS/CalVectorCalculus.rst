:index:`Vector Calculus`
========================

These options include tools for calculating gradient, curl, and divergence.

:index:`Gradient`
-----------------

This returns the gradient of a multi-variable function.  When you select this option a dialog will open asking the user to input the variable list to use.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

You can always add in variables to the variable list if you want to embed a lower dimensional curve into a higher dimensional space.

For example, if we take the function :math:`\sin{\left(x + y z \right)}` and take its gradient with variable list ``[x, y, z]`` we get,

.. math::
    \left[\begin{array}{c}\cos{\left(x + y z \right)}\\z \cos{\left(x + y z \right)}\\y \cos{\left(x + y z \right)}\end{array}\right]

Note that the result is a column vector (matrix).

:index:`Curl`
-------------

This returns the curl of a vector field in either 2 or 3 dimensions.  When you select this option a dialog will open asking the user to input the variable list to use.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

For example, if we take the vector field :math:`\left[ x z, \  x y z, \  - y^{2}\right]` and take its curl with variable list ``[x, y, z]`` we get,

.. math::
    \left[\begin{array}{c}- x y - 2 y\\x\\y z\end{array}\right]

Note that the result is a column vector (matrix).

:index:`Divergence`
-------------------

This returns the divergence of a vector field in in either 2 or 3 dimensions.  When you select this option a dialog will open asking the user to input the variable list to use.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

For example, if we take the vector field :math:`\left[ x z, \  x y z, \  - y^{2}\right]` and take its divergence with variable list ``[x, y, z]`` we get :math:`x z + z`.


Variable Assumptions
--------------------

.. include:: ../CLAE/VariableAssumptions.md

