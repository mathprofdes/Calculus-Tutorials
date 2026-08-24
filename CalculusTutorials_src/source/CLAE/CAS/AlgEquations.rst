:index:`Equations`
==================

In this program we take the approach of expressions equaling to 0 if we invoke a solve option.  That is, if we input the expression :math:`x^{2} - 3 x + 1` and select ``Algebra > Solve`` we are assuming that the equation that is being solved is :math:`x^{2} - 3 x + 1 = 0` and not :math:`x^{2} - 3 x = -1` or :math:`x^{2} = 3 x - 1`.  This is simply our convention and has pedagogical advantages. The program and SymPy solvers are quite capable of solving equations not equal to 0 and we can create them in this program but again this is syntax that is above where we need to go.  There are some cases where the output will be in equation form, for example, when solving ODEs.

For example, if we solve the ODE, (assumed equal to 0)

.. math::

    - f{\left(x \right)} + \frac{d^{2}}{d x^{2}} f{\left(x \right)} + 1

we get the output of

.. math::

    f{\left(x \right)} = C_{1} e^{- x} + C_{2} e^{x} + 1

All we really need here is the right had side of the equation.  Selecting ``Algebra > Equations > Right Hand Side`` will extract the right hand side of the equation for us.

.. math::

    C_{1} e^{- x} + C_{2} e^{x} + 1


:index:`Left Hand Side`
-----------------------

This simply extracts the left hand side of an equation.

:index:`Right Hand Side`
------------------------

This simply extracts the right hand side of an equation.

:index:`Equation to Expression`
-------------------------------

This simply converts an equation into an equivalent expression equal to 0 but drops the equation notation.  For example, it would take the equation :math:`x^{3} - 3 x = \sin{\left(x \right)} + 1` and convert it to the expression :math:`x^{3} - 3 x - \sin{\left(x \right)} - 1`.

