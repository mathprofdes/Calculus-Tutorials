:index:`Maxima: Evaluation and Approximation`
=============================================

Approximate
-----------

This does a floating point approximation of the current expression.  For example, :math:`\pi` is approximated to, 3.141592653589793.


Approximate to Precision
------------------------

This does a floating point approximation of the current expression to the precision level input by the user.  For example, :math:`\pi` to 75 decimal places is approximated to,

.. math::
    3.14159265358979323846264338327950288419716939937510582097494459230781640629.

Note that Maxima uses what they call a Bigfloat object to do these larger approximations. The downside to this is that they are written in a nonstandard scientific notation, for example, :math:`\pi` would be returned as 3.141592653589793b0 instead of the more standard 3.141592653589793E0 or 3.141592653589793e0.  So in the conversion back to CLAE we replace the *b* with *E*.  This is done textually with simply substituting the characters *b* with *E*.  In most cases this is fine, but in some cases Maxima may produce a partial approximation that still has functions in the expression, here all *b* characters will be replaced with *E* and the result may not make any sense.


Evaluate / Substitute
---------------------

This option will substitute one expression for another.  In most cases you will simply substitute expressions for variables in the expression but you cam also substitute other expressions for subexpressions.   For example, if we have,

.. math::
    \sin^{2}{\left(x \right)} + \sin{\left(2 x \right)} + \cos{\left(x \right)}

and substitute :math:`t^3-1` for *x* we get,

.. math::
    \sin^{2}{\left(t^{3} - 1 \right)} + \sin{\left(2 t^{3} - 2 \right)} + \cos{\left(t^{3} - 1 \right)}

On the other hand, if we have the same expression and substitute *y* for :math:`\sin(x)` we get,

.. math::
    y^{2} + \sin{\left(2 x \right)} + \cos{\left(x \right)}

As another example, if we take the original expression and expand the trigonometric functions we get,

.. math::
    \sin^{2}{\left(x \right)} + 2 \sin{\left(x \right)} \cos{\left(x \right)} + \cos{\left(x \right)}

now if we substitute *y* for :math:`\sin(x)` we get,

.. math::
    y^{2} + 2 y \cos{\left(x \right)} + \cos{\left(x \right)}
