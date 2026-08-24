
:index:`Arithmetic Operations`
------------------------------

The basic arithmetic operations are ``+``, ``-``, ``*``, ``\``, and ``^``. All of which do what you would expect.  The ``^`` is exponentiation and you can also use ``**`` in place of the ``^`` operator, as in the Python language. Note that ``*`` must be used for multiplication, this program does not recognize juxtaposition as multiplication, so for :math:`2x` we use the syntax ``2*x`` and not ``2 x`` or ``2x``, the second two are syntax error.

:index:`Variables`
------------------

Variables, also known as symbols, can be any expression that is not a sympy function, starts with a letter or underscore and has only letters, numbers, and underscores after that.  So ``a``, ``x``, ``xpt1``, and ``John_Smith`` are all valid variables.

:index:`Previous CAS Results`
-----------------------------

Each (non error) entry in the CAS has a designation at the begging of the item's description, R1, R2, ... which is short for Result #1, Result #2, ...  These can be used in any input expression.  For example, ``R1*R2``, ``sin(R2)``, ``cos(x)*R1/(R2 + 3)`` are all legitimate expressions. When these are used in an expression, the expression for the result is substituted into the expression before it it is loaded into the CAS. So if ``R1`` is :math:`x^2` and ``R2`` is :math:`\sqrt{y}` then ``R1*R2`` is :math:`x^2 \sqrt{y}`, ``sin(R2)`` is :math:`\sin(\sqrt{y})`, and ``cos(x)*R1/(R2 + 3)`` is :math:`\displaystyle \frac{\cos(x) x^2}{\sqrt{y} + 3}.`

Since the previous expressions are loaded into the input expression there is no expression dependency, by design.  So if we did input ``R1*R2`` to get :math:`x^2 \sqrt{y}` and then deleted either ``R1`` or ``R2`` the :math:`x^2 \sqrt{y}` result is not affected. This also means that there is no cascading of results as in some other systems.  That is, if we changed ``R1`` to :math:`\sin(x)` (which by the way we can't, also by design) then the ``R1*R2`` remains :math:`x^2 \sqrt{y}` and not :math:`\sin(x) \sqrt{y}.`

CAS result expressions cannot be changed. So if you double-click a result and open up its editor, either copying it to the CAS input bar or opening up an editing dialog box, when the expression is edited and accepted, it is loaded in as a new result.  There are pros and cons about this design.  This eliminates dependencies and stale data, which is a good thing. One con is that in some systems you can make a change to a function and then see the changes that this makes to all the subsequent operations done on the function, here you cannot, you need to go through the same operations with the new expression.


:index:`Infinity`
-----------------

Infinity, :math:`\infty`, is represented as ``oo`` (that is two small o's) and :math:`-\infty` is represented as ``-oo``.

:index:`Special Constants`
--------------------------

- ``pi`` represents :math:`\pi`
- ``E`` represents :math:`e`, note it is uppercase, ``e`` is seen as the variable ``e``.
- ``I`` represents :math:`i` the imaginary unit, note it is also uppercase.
- ``GoldenRatio`` represents the Golden Ratio :math:`\displaystyle \frac{1+\sqrt{5}}{2}.`

:index:`Absolute Value`
-----------------------

- ``abs(x)`` or ``Abs(x)`` represents :math:`|x|.`

:index:`Root Functions`
-----------------------

- Fractional exponents can be used for root functions, for example ``x^(1/2)``, ``x^(1/3)``, and ``x^(7/5)``.  Note that when we evaluate an expression with a fractional exponent the system returns the principal root.  So if we input ``(-1)^(1/3)`` (and approximate the value) the result is not :math:`-1` it is :math:`0.5 + 0.866025403784439 i.`  The 2-D and 3-D graphics systems will convert fractional exponents with odd integer denominators to their ``real_root`` equivalent.  So in a plot ``(-1)^(1/3)`` will be ``-1``.  These conversions are done internally and the user does not see any alteration to their input. The computer algebra system portion of the program also works well with fractional exponents, as one would expect, so they are your best syntax to use when inputting root functions into the program.
- ``sqrt(x)`` represents :math:`\sqrt{x}.`
- ``cbrt(x)`` returns the principal cube root, possibly complex. So for example, if we input ``cbrt(-1)`` (and approximate the value) the result is not :math:`-1` it is :math:`0.5 + 0.866025403784439 i.`  Note that ``cbrt(x)`` is converted to ``x^(1/3)``.
- ``root(x, n)``  represents :math:`\sqrt[n]{x}.` A little caution is needed here, this is complex (i.e. primitive complex) nth root of ``x``.  So for example, if we input ``root(-1, 3)`` (and approximate the value) the result is not :math:`-1` it is :math:`0.5 + 0.866025403784439 i.`  Note that ``root(x, n)`` is converted to ``x^(1/n)``. 
- ``real_root(x, n)``  represents :math:`\sqrt[n]{x}`.  This is the real nth root. So in this case ``real_root(-1, 3)`` is :math:`-1.` Unfortunately, the ``real_root(x, n)`` is not the best function to work with for many of the Algebra and Calculus operations since it produces a piecewise defined function that can be difficult to work with. Specifically,

.. math::
    \begin{cases} x^{\frac{1}{n}} & \text{for}\: n = -1 \vee n = 1 \\\left|{x}\right|^{\frac{1}{n}} \operatorname{sign}{\left(x \right)} & \text{for}\: \operatorname{im}{\left(x\right)} = 0 \wedge n \bmod 2 = 1 \\x^{\frac{1}{n}} & \text{otherwise} \end{cases}


:index:`Trigonometric Functions`
--------------------------------

The trigonometric functions are as you would expect,

- ``sin(x)`` for :math:`\sin(x)`.
- ``cos(x)`` for :math:`\cos(x)`.
- ``tan(x)`` for :math:`\tan(x)`.
- ``cot(x)`` for :math:`\cot(x)`.
- ``sec(x)`` for :math:`\sec(x)`.
- ``csc(x)`` for :math:`\csc(x)`.


:index:`Inverse Trigonometric Functions`
----------------------------------------

The inverse trigonometric functions simply have an ``a`` in front of them,

- ``asin(x)`` for :math:`\sin^{-1}(x)`.
- ``acos(x)`` for :math:`\cos^{-1}(x)`.
- ``atan(x)`` for :math:`\tan^{-1}(x)`.
- ``acot(x)`` for :math:`\cot^{-1}(x)`.
- ``asec(x)`` for :math:`\sec^{-1}(x)`.
- ``acsc(x)`` for :math:`\csc^{-1}(x)`.

In addition there is

- ``atan2(y, x)`` for :math:`\tan^{-1}(y/x)` which also works when :math:`x = 0`. So ``atan2(1, 0)`` returns :math:`\pi/2.`


:index:`Exponential & Logarithmic Functions`
--------------------------------------------

- ``exp(x)`` represents :math:`e^x`.
- ``E^x`` represents :math:`e^x`.
- ``log(x)`` represents :math:`\ln(x)`.
- ``ln(x)`` represents :math:`\ln(x)`.
- ``log(x, n)`` represents :math:`\log_n(x)`.


:index:`Hyperbolic Functions`
-----------------------------

The hyperbolic functions are as you would expect,

- ``sinh(x)`` for :math:`\sinh(x)`.
- ``cosh(x)`` for :math:`\cosh(x)`.
- ``tanh(x)`` for :math:`\tanh(x)`.
- ``coth(x)`` for :math:`\coth(x)`.
- ``sech(x)`` for :math:`{\rm sech}(x)`.
- ``csch(x)`` for :math:`{\rm csch}(x)`.

:index:`Inverse Hyperbolic Functions`
-------------------------------------

The inverse hyperbolic functions simply have an ``a`` in front of them,

- ``asinh(x)`` for :math:`\sinh^{-1}(x)`.
- ``acosh(x)`` for :math:`\cosh^{-1}(x)`.
- ``atanh(x)`` for :math:`\tanh^{-1}(x)`.
- ``acoth(x)`` for :math:`\coth^{-1}(x)`.
- ``asech(x)`` for :math:`{\rm sech}^{-1}(x)`.
- ``acsch(x)`` for :math:`{\rm csch}^{-1}(x)`.


:index:`Complex Functions`
--------------------------

Some functions that may be of interest when dealing with complex numbers. Many of these are also menu options.

- ``re(z)`` returns the real part of ``z``.
- ``im(z)`` returns the imaginary part of ``z``.
- ``arg(z)`` returns the argument (in radians) of the complex number.
- ``conjugate(z)`` returns the complex conjugate of ``z``.


:index:`Integer Functions`
--------------------------

- ``floor(x)`` returns the largest integer value not greater than ``x``.
- ``ceiling(x)`` returns the smallest integer value not less than ``x``.
- ``frac(x)`` returns the fractional part of ``x``.


:index:`Miscellaneous Functions`
--------------------------------

Some miscellaneous functions that may be of interest.

- ``sign(x)`` returns the sign of ``x``, 1 if :math:`x>0`, 0 if :math:`x = 0`, :math:`-1` if :math:`x<0.`
- ``n!`` returns `n factorial` which is defined for non-negative integers with  :math:`0! = 1` and :math:`n! = n(n-1)(n-2) \cdots 1` for :math:`n > 0.`
- ``n!!`` returns `n double factorial` which is defined for non-negative integers with  :math:`0!! = 1` and :math:`n!! = n(n-2)(n-4) \cdots 1` for :math:`n > 0.`


:index:`User-Defined Functions`
-------------------------------

The CAS also supports declaring user-defined functions.  To create a user defined function start with a function name and variable list, as you would in writing it mathematically, then type in ``:=`` followed by any valid expression (including previous CAS results).

For example:

- ``f(x) := x^2-2*x+1``
- ``g(x) := R2``
- ``h(x, y) := sin(x)/(y^2+1)``
- ``k(t) := cos(R1)/t^3 + exp(t^2)``

Once a function is defined you can use it in expressions or evaluate it with functional notation.

For example:

- ``f(5)`` will return the expression value after 5 is substituted in for ``x``.
- ``1/g(x)`` would be equivalent to ``1/R2``
- ``h(cos(t), sin(t))`` will substitute ``cos(t)`` for ``x`` and ``sin(t)`` for ``y``.
- ``k(1/t)`` will substitute ``1/t`` for ``t``.
- ``(f(x+h) - f(x))/h`` will return the difference quotient for the function ``f``.

Once a function is input into the CAS you cannot use the same function name for another function definition.  So if you define a function called ``f`` you may not use ``f`` again.  If you delete the entry where ``f`` was defined then you can use the function name ``f``.


:index:`Other Function Syntax`
------------------------------

The program is not limited to the above expressions.  The CAS input bar will take in any SymPy "one line" expression.  So for example, ``totient(12345)`` will return the Euler totient (phi) function of 12345, that is, 6576.  The program was built with the goal to minimize the amount of syntax that the users needs to learn, nonetheless the functionality is there.
