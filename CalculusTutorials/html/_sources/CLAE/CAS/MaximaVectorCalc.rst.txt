:index:`Maxima: Vector Calculus`
================================

:index:`Gradient`
-----------------

This returns the gradient of a multi-variable function.  When you select this option a dialog will open asking the user to input the variable list to use.  You can always add in variables to the variable list if you want to embed a lower dimensional curve into a higher dimensional space.  For example, if we take the function :math:`\sin{\left(x + y z \right)}` and take its gradient with variable list ``[x, y, z]`` we get,

.. math::
    \left[ \cos{\left(x + y z \right)}, \  z \cos{\left(x + y z \right)}, \  y \cos{\left(x + y z \right)}\right]

:index:`Curl`
-------------

This returns the curl of a vector field in 3 dimensions.  When you select this option a dialog will open asking the user to input the variable list to use.  For example, if we take the vector field :math:`\left[ x z, \  x y z, \  - y^{2}\right]` and take its curl with variable list ``[x, y, z]`` we get,

.. math::
    \left[ - x y - 2 y, \  x, \  y z\right]


:index:`Divergence`
-------------------

This returns the divergence of a vector field in 3 dimensions.  When you select this option a dialog will open asking the user to input the variable list to use.  For example, if we take the vector field :math:`\left[ x z, \  x y z, \  - y^{2}\right]` and take its divergence with variable list ``[x, y, z]`` we get :math:`x z + z`.

