:index:`Evaluate and Apply`
===========================

The Evaluate and Apply options are for evaluating a matrix in an analytic function and for evaluating each entry in a function.

:index:`Evaluate`
-----------------

This option is for evaluating a matrix in an analytic function. specifically, if :math:`f(x)` is a function and `M` is a matrix this option will calculate :math:`f(M)` if possible.  For example, you can calculate :math:`e^M` or :math:`\sin(M)` etc.  With this operation the matrix `M` may have restrictions.  Also, for calculations such as :math:`e^M` or :math:`\sin(M)` the matrices are substituted into the Taylor series expansion of the functions and the process can be lengthy, this should be used for smaller sized matrices.  When this option is selected a dialog box will appear asking the user for a function and the variable for substitution.  The function expression can be any valid expression including CAS workspace entries.

We will look at a few examples. Say we have the matrix,

.. math::
    \left[\begin{array}{ccc}-8 & -6 & -8\\7 & 7 & 1\\-4 & 8 & -9\end{array}\right]

If we select this option and input the expression :math:`x^2 + 3x -1` it returns

.. math::
    \left[\begin{array}{ccc}29 & -76 & 106\\10 & 35 & -55\\112 & 32 & 93\end{array}\right]

If we take this same matrix and find its characteristic polynomial we get :math:`x^{3} + 10 x^{2} - 45 x + 458`.  Say that this polynomial has the CAS workspace designation of R3.  If we select the matrix, then select the evaluate option, input ``R3`` for the function and ``x`` for the variable we get,

.. math::
    \left[\begin{array}{ccc}0 & 0 & 0\\0 & 0 & 0\\0 & 0 & 0\end{array}\right]

showing that the matrix is a solution to its characteristic polynomial.

.. note::
    To do the last example you do not want to use the Evaluate option under the Algebra menu.  If you select the characteristic polynomial then ``Algebra > Evaluate`` and then input the matrix for the expression you will get an error.  What happens here is that the program will put the matrix in for the variable x and begin the evaluation.  It will get to the point

    .. math::
        \left[\begin{array}{ccc}-458 & 0 & 0\\0 & -458 & 0\\0 & 0 & -458\end{array}\right] + 458

    and then produce an error since it cannot add a matrix to a constant.  The program (really SymPy) will not automatically change 458 to :math:`458 \cdot I_3`.  The evaluate option under the Matrix menu will do this substitution for constants and complete the operation.

As another example, say we have the matrix,

.. math::
    \left[\begin{array}{cc}-1 & -8\\3 & 6\end{array}\right]

if we select ``Matrix > Evaluate``, put in ``exp(x)`` for the expression and ``x`` for the variable the result is,

.. math::
    \left[\begin{array}{cc}\frac{7 \sqrt{47} i e^{\frac{5}{2} + \frac{\sqrt{47} i}{2}}}{94} + \frac{e^{\frac{5}{2} + \frac{\sqrt{47} i}{2}}}{2} + \frac{e^{\frac{5}{2} - \frac{\sqrt{47} i}{2}}}{2} - \frac{7 \sqrt{47} i e^{\frac{5}{2} - \frac{\sqrt{47} i}{2}}}{94} & \frac{8 \sqrt{47} i e^{\frac{5}{2} + \frac{\sqrt{47} i}{2}}}{47} - \frac{8 \sqrt{47} i e^{\frac{5}{2} - \frac{\sqrt{47} i}{2}}}{47}\\\frac{3 \sqrt{47} i e^{\frac{5}{2} - \frac{\sqrt{47} i}{2}}}{47} - \frac{3 \sqrt{47} i e^{\frac{5}{2} + \frac{\sqrt{47} i}{2}}}{47} & \frac{7 \sqrt{47} i e^{\frac{5}{2} - \frac{\sqrt{47} i}{2}}}{94} + \frac{e^{\frac{5}{2} + \frac{\sqrt{47} i}{2}}}{2} + \frac{e^{\frac{5}{2} - \frac{\sqrt{47} i}{2}}}{2} - \frac{7 \sqrt{47} i e^{\frac{5}{2} + \frac{\sqrt{47} i}{2}}}{94}\end{array}\right]

similarly, if we used :math:`\sin(x)` for the function we get ,

.. math::
    \left[\begin{array}{cc}\frac{\sin{\left(\frac{5}{2} + \frac{\sqrt{47} i}{2} \right)}}{2} - \frac{7 \sqrt{47} i \sin{\left(\frac{5}{2} - \frac{\sqrt{47} i}{2} \right)}}{94} + \frac{7 \sqrt{47} i \sin{\left(\frac{5}{2} + \frac{\sqrt{47} i}{2} \right)}}{94} + \frac{\sin{\left(\frac{5}{2} - \frac{\sqrt{47} i}{2} \right)}}{2} & - \frac{8 \sqrt{47} i \sin{\left(\frac{5}{2} - \frac{\sqrt{47} i}{2} \right)}}{47} + \frac{8 \sqrt{47} i \sin{\left(\frac{5}{2} + \frac{\sqrt{47} i}{2} \right)}}{47}\\- \frac{3 \sqrt{47} i \sin{\left(\frac{5}{2} + \frac{\sqrt{47} i}{2} \right)}}{47} + \frac{3 \sqrt{47} i \sin{\left(\frac{5}{2} - \frac{\sqrt{47} i}{2} \right)}}{47} & \frac{\sin{\left(\frac{5}{2} + \frac{\sqrt{47} i}{2} \right)}}{2} - \frac{7 \sqrt{47} i \sin{\left(\frac{5}{2} + \frac{\sqrt{47} i}{2} \right)}}{94} + \frac{7 \sqrt{47} i \sin{\left(\frac{5}{2} - \frac{\sqrt{47} i}{2} \right)}}{94} + \frac{\sin{\left(\frac{5}{2} - \frac{\sqrt{47} i}{2} \right)}}{2}\end{array}\right]

:index:`Apply`
--------------

The Apply option is similar to the evaluate option except here the function is applied to each individual matrix entry.  For example, if we used the matrix,

.. math::
    \left[\begin{array}{ccc}-8 & -6 & -8\\7 & 7 & 1\\-4 & 8 & -9\end{array}\right]

and applied the function :math:`e^x` to it by using ``exp(x)`` or ``E^x`` we would get,

.. math::
    \left[\begin{array}{ccc}e^{-8} & e^{-6} & e^{-8}\\e^{7} & e^{7} & e\\e^{-4} & e^{8} & e^{-9}\end{array}\right]