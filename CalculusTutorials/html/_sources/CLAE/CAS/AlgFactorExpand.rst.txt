:index:`Factoring and Expanding`
================================

Factoring and expanding are very common operations in simplifying and manipulating algebraic expressions.

:index:`Factor`
---------------

Simply select this option to apply several factorization techniques to the expression.

For example, if we factor ``x^3*y^4 - 24*x^3*y^3 + 216*x^3*y^2 - 864*x^3*y + 1296*x^3 + 9*x^2*y^4 - 216*x^2*y^3 + 1944*x^2*y^2 - 7776*x^2*y + 11664*x^2 + 27*x*y^4 - 648*x*y^3 + 5832*x*y^2 - 23328*x*y + 34992*x + 27*y^4 - 648*y^3 + 5832*y^2 - 23328*y + 34992``, that is,

.. math::

    x^{3} y^{4} - 24 x^{3} y^{3} + 216 x^{3} y^{2} - 864 x^{3} y + 1296 x^{3} + 9 x^{2} y^{4} - 216 x^{2} y^{3} + 1944 x^{2} y^{2} - 7776 x^{2} y + 11664 x^{2} + 27 x y^{4} - 648 x y^{3} + 5832 x y^{2} - 23328 x y + 34992 x + 27 y^{4} - 648 y^{3} + 5832 y^{2} - 23328 y + 34992

we get,

.. math::

    \left(x + 3\right)^{3} \left(y - 6\right)^{4}

The expression doe not need to be a polynomial, if we factor ``x^6 + 3*x^4*sin(x) + 3*x^2*sin(x)^2 + sin(x)^3``, that is, :math:`x^{6} + 3 x^{4} \sin{\left(x \right)} + 3 x^{2} \sin^{2}{\left(x \right)} + \sin^{3}{\left(x \right)}`, we get, :math:`\left(x^{2} + \sin{\left(x \right)}\right)^{3}`.

.. note::

    - Do not use this tool for factoring an integer, use the Factor Integer option discussed below.
    - Factoring is done over the rational numbers, so if there are irrational coefficients to a factorization this option will not return them.  For example, if we factor :math:`x^{4} + 1` the program returns :math:`x^{4} + 1`.  This does not mean that :math:`x^{4} + 1` is irreducible over the real numbers and certainly not over the complex numbers. Note that  :math:`x^{4} + 1 = \left(x^{2} - \sqrt{2} x + 1\right) \left(x^{2} + \sqrt{2} x + 1\right)` over the real number system and :math:`x^{4} + 1 = \left(x - \frac{\sqrt{2}}{2} - \frac{\sqrt{2} i}{2}\right) \left(x - \frac{\sqrt{2}}{2} + \frac{\sqrt{2} i}{2}\right) \left(x + \frac{\sqrt{2}}{2} - \frac{\sqrt{2} i}{2}\right) \left(x + \frac{\sqrt{2}}{2} + \frac{\sqrt{2} i}{2}\right)` over the complex numbers.
    - The underlying computer algebra system to this program, SymPy, has many more facilities for factorization but they can be complicated and require a knowledge of more advanced mathematics.


:index:`Expand`
---------------

Expand simply does the reverse of factorization.  So expanding :math:`\left(x + 3\right)^{3} \left(y - 6\right)^{4}` gives us,

.. math::

    x^{3} y^{4} - 24 x^{3} y^{3} + 216 x^{3} y^{2} - 864 x^{3} y + 1296 x^{3} + 9 x^{2} y^{4} - 216 x^{2} y^{3} + 1944 x^{2} y^{2} - 7776 x^{2} y + 11664 x^{2} + 27 x y^{4} - 648 x y^{3} + 5832 x y^{2} - 23328 x y + 34992 x + 27 y^{4} - 648 y^{3} + 5832 y^{2} - 23328 y + 34992

and expanding :math:`\left(x^{2} + \sin{\left(x \right)}\right)^{3}` gives us :math:`x^{6} + 3 x^{4} \sin{\left(x \right)} + 3 x^{2} \sin^{2}{\left(x \right)} + \sin^{3}{\left(x \right)}`.


:index:`Factor Polynomial`
--------------------------

This tool is for factoring polynomials with numeric coefficients.  The coefficients can be real or complex and can be exact or floating point.  Use this tool with care, factoring polynomials is a difficult task and can take a long time to complete.  There are no general formulas for degree 5 or greater polynomials so you may not get a factorization or it may not look the way you expect.  In addition, with higher degree polynomials the CAS may resort to trigonometric solutions instead of radical coefficients.

When this option is selected a dialog box will appear asking the user to input the number system to factor over, rationals, reals, or complex numbers.  Select the number system and click OK.  Here are a couple of examples,

Say we wanted to factor :math:`x^{3} - 1`, using the rational or reals we would get :math:`\left(x - 1\right) \left(x^{2} + x + 1\right)` and using the complex number system we would get,

.. math::
    \left(x - 1\right) \left(x + \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \left(x + \frac{1}{2} + \frac{\sqrt{3} i}{2}\right)


Say we wanted to factor :math:`x^{4} + 1`, using the rationals owe would get :math:`x^{4} + 1`. Using the real number system we would get,

.. math::
    \left(x^{2} - \sqrt{2} x + 1\right) \left(x^{2} + \sqrt{2} x + 1\right)

Using the complex number system we would get,

.. math::
    \left(x - \frac{\sqrt{2}}{2} - \frac{\sqrt{2} i}{2}\right) \left(x - \frac{\sqrt{2}}{2} + \frac{\sqrt{2} i}{2}\right) \left(x + \frac{\sqrt{2}}{2} - \frac{\sqrt{2} i}{2}\right) \left(x + \frac{\sqrt{2}}{2} + \frac{\sqrt{2} i}{2}\right)

If we use a decimal approximation for coefficients the results will also be approximations.  For example, if we change the above example to :math:`x^{4} + 1.0` then the factorizations over the reals and complexes are respectively,

.. math::
    \left(x^{2} - 1.4142135623731 x + 1.0\right) \left(x^{2} + 1.4142135623731 x + 1.0\right)

.. math::
    \left(x - 0.707106781186548 - 0.707106781186548 i\right) \left(x - 0.707106781186548 + 0.707106781186548 i\right) \left(x + 0.707106781186548 - 0.707106781186548 i\right) \left(x + 0.707106781186548 + 0.707106781186548 i\right)


:index:`Factor Integer`
-----------------------

This tool is for factoring integers, usually large integers.  Use this tool with care, factoring integers is a difficult task and can take a long time to complete.  Even for integers in the 40-50 digit range can take more time than you have available.  The tool is easy to use, simply input the integer you wish to factor and then select this option.  The result is a list of lists.  Each inner list is base/exponent pair for the prime factorization of the integer and the base/exponent pairs are to be multiplied together.

For example, say we wanted to factor ``1959017154790775625000``, the result is

.. math::

    \left[ \left[ 2, \  3\right], \  \left[ 3, \  4\right], \  \left[ 5, \  7\right], \  \left[ 7, \  2\right], \  \left[ 13, \  1\right], \  \left[ 31, \  1\right], \  \left[ 337, \  1\right], \  \left[ 5814899, \  1\right]\right]

which means that

.. math::

    1959017154790775625000 = 2^3 \cdot 3^4 \cdot 5^7 \cdot 7^2 \cdot 13^1 \cdot  31^1  \cdot 337^1 \cdot 5814899^1


