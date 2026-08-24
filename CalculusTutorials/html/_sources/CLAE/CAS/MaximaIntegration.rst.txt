:index:`Maxima: Integration`
============================

Indefinite Integral
-------------------

This will attempt to find the indefinite integral of the current expression.  As you know, finding indefinite integrals can be difficult and there are many functions where you cannot get an elementary form for the antiderivative.  This option should be used in conjunction with the indefinite integral option in the Calculus menu.  There will be some expressions where SymPy does not return a solution or a nice solution where Maxima might, and vice versa.  So if the option in the Calculus menu does not return a nice answer you can use this one.  Note that if this option returns an error it is most likely due to Maxima not being able to find an antiderivative.

When this option is selected a dialog box will appear asking the user to input the variable of integration, whether or not to include a constant of integration, and if the result is to be real-valued.  If the user selects real valued then,

.. math::
    \int \frac{1}{x} \; dx = \ln|x| + C

which is what is taught in introductory Calculus classes, but is not true when working over the complex numbers.  If the real-valued selection is not checked then,

.. math::
    \int \frac{1}{x} \; dx = \ln(x) + C = {\rm Log}(x) + C

As an example, if we try to calculate

.. math::
    \int \sqrt[3]{\tan(x)} \; dx

using SymPy it will not give us an answer but using Maxima we get,

.. math::
    \int \sqrt[3]{\tan(x)} \; dx = - \frac{\ln{\left(\tan^{\frac{2}{3}}{\left(x \right)} + 1 \right)}}{2} + \frac{\ln{\left(\left|{\tan^{\frac{4}{3}}{\left(x \right)} - \tan^{\frac{2}{3}}{\left(x \right)} + 1}\right| \right)}}{4} + \frac{\sqrt{3} \operatorname{atan}{\left(\frac{\sqrt{3} \left(2 \tan^{\frac{2}{3}}{\left(x \right)} - 1\right)}{3} \right)}}{2} + C


Definite Integral
-----------------

This will find the definite integral of a function.  When selected a dialog box will appear asking the use for the variable, the bounds of integration, and the Maxima running mode.  Remember that you are using CLAE syntax and not Maxima, so :math:`\pi` is ``pi``, :math:`e` is ``E``, :math:`\infty` is ``oo``, and :math:`-\infty` is ``-oo``.

Definite Integral Approximation
-------------------------------

This will find an approximation to the definite integral of a function.  When selected a dialog box will appear asking the use for the variable, the bounds of integration, whether to include an error bound or not, and the Maxima running mode.  Remember that you are using CLAE syntax and not Maxima, so :math:`\pi` is ``pi``, :math:`e` is ``E``, :math:`\infty` is ``oo``, and :math:`-\infty` is ``-oo``.

If the user selects not to include an error bound then the result is simply an approximation to the integral. If the user selects to include an error bound then the result is a list of two values, the first is the approximation and the second is a bound on the error of that approximation.  For example if the user finds an approximation to,

.. math::
    \int_0^\pi \sqrt[3]{\sin{\left(x \right)}} \; dx

they get 2.587109559229791.  If they find an approximation to the above integral with an error bound they get, :math:`\left[ 2.587109559229791, \  2.045963398700223 \cdot 10^{-11}\right]`  which indicates that the approximation is 2.587109559229791 with an error tht is at most :math:`2.045963398700223 \cdot 10^{-11}.`

