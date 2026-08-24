Spreadsheet Expression Syntax
=============================


:index:`Arithmetic Operations`
------------------------------

The basic arithmetic operations are ``+``, ``-``, ``*``, ``\``, and ``^``. All of which do what you would expect.  The ``^`` is exponentiation and you can also use ``**`` in place of the ``^`` operator, as in the Python language. Note that ``*`` must be used for multiplication, this program does not recognize juxtaposition as multiplication, so for :math:`2x` we use the syntax ``2*x`` and not ``2 x``, the later is a syntax error.

:index:`Variables`
------------------

Variables, also known as symbols, can be any expression that is not a sympy function, starts with a letter or underscore and has only letters, numbers, and underscores after that.  So ``a``, ``x``, ``xpt1``, and ``John_Smith`` are all valid variables.

:index:`Cell Entries`
---------------------

Any cell entry designation can be used in a cell formula, simply include syntax such as A1, B7, Z50, ... in the formula. When you use a cell entry designation in the formula of another cell, the cell formula will retain the cell entry designation but be replaced with the referenced cell's contents in determining the cell value.  For example, if cell ``A1`` contains ``x + 3`` and the cell ``B3`` contains ``sin(t)`` then if in another cell you input the formula ``A1 * B3 + 7`` the formula for that cell will be ``A1 * B3 + 7`` and the value of that cell will be ``(x + 3) * sin(t) + 7``.  As another example, if ``A1`` contains ``A2 + A3`` and the cell ``B3`` contains ``sin(t)`` then if in another cell you input the formula ``A1 * B3 + 7`` the formula for that cell will still be ``A1 * B3 + 7`` and the value, assuming that cell ``A2`` contains ``x^2`` and cell ``A3`` contains ``y^3``, of that cell will be ``(x^2 + y^3) * sin(t) + 7``.

The program will return an error to a cell if any reference is outside of the spreadsheet bounds or if there is a circular reference created by an input.  These errors have a tendency to cascade to dependent cells, so one error may propagate several cell error messages.  Also, if a cell is referenced that has no value the program will keep the cell reference in the formula but replace it with 0 in the cell value.

When a cell is changed the program goes through the grid to determine all the cells that are dependent on the one that was changed and updates the values of these cells, the formulas are unaltered.  This, in turn, creates a set of changed cells that are treated the same way, the values of all cells dependent on them are changed, etc.  Since there can be no circular references this process does stop.  If there is a lot of cell dependency in the grid updates my take a few seconds to complete, remember that the cells are expressions in a computer algebra system and updates will take longer than those in a numeric spreadsheet.


:index:`Previous CAS Results`
-----------------------------

Each (non error) entry in the CAS has a designation at the begging of the item's description, R1, R2, ... which is short for Result #1, Result #2, ...  These can be used in any input expression except that you need to use two Rs instead of one R as you would with the CAS input, this is because R1, R2, ... represent cell locations .  For example, ``RR1*RR2``, ``sin(RR2)``, ``cos(x)*RR1/(RR2 + 3)`` are all legitimate expressions. When these are used in an expression, the expression for the result is substituted into the expression before it it is loaded into the spreadsheet. So if ``RR1`` is :math:`x^2` and ``RR2`` is :math:`\sqrt{y}` then ``RR1*RR2`` is :math:`x^2 \sqrt{y}`, ``sin(RR2)`` is :math:`\sin(\sqrt{y})`, and ``cos(x)*RR1/(RR2 + 3)`` is :math:`\displaystyle \frac{\cos(x) x^2}{\sqrt{y} + 3}`.

Since the previous expressions are loaded into the input expression immediately there is no expression dependency with the CAS, by design.  So if we did input ``RR1*RR2`` to get :math:`x^2 \sqrt{y}` and then deleted either ``R1`` or ``R2`` the :math:`x^2 \sqrt{y}` result is not affected.

You can use CAS entry designations as well as CAS designations in the same input formula, the difference is that the CAS designations will be replaced and the cell designations will be references in the formula but still substituted in the cell's value.


:index:`Infinity`
-----------------

Infinity, :math:`\infty`, is represented as ``oo`` (that is two small o's) and :math:`-\infty` is represented as ``-oo``.

:index:`Special Constants`
--------------------------

- ``pi`` represents :math:`\pi`
- ``E`` represents :math:`e`, note it is uppercase, ``e`` is seen as the variable ``e``.
- ``I`` represents :math:`i` the imaginary unit, note it is also uppercase.
- ``GoldenRatio`` represents the Golden Ratio :math:`\displaystyle \frac{1+\sqrt{5}}{2}`.

:index:`Absolute Value`
-----------------------

- ``abs(x)`` or ``Abs(x)`` represents :math:`|x|`.

:index:`Root Functions`
-----------------------

- ``sqrt(x)`` represents :math:`\sqrt{x}`.
- ``cbrt(x)`` returns the principal cube root, possibly complex. So for example, if we input ``root(-1, 3)`` (and approximate the value) the result is not :math:`-1` it is :math:`0.5 + 0.866025403784439 i`.
- ``root(x, n)``  represents :math:`\sqrt[n]{x}`. A little caution is needed here, this is complex (i.e. primitive complex) nth root of ``x``.  So for example, if we input ``root(-1, 3)`` (and approximate the value) the result is not :math:`-1` it is :math:`0.5 + 0.866025403784439 i`.  Hence this works well for calculations but not as well for real-valued plots.
- ``real_root(x, n)``  represents :math:`\sqrt[n]{x}`.  This is the real nth root. So in this case ``real_root(-1, 3)`` is :math:`-1`, unfortunately, the ``real_root(x, n)`` is not the best function to work with for many of the Algebra ans Calculus operations, but it does produce better graphs.

.. tip::

    For fractional exponents like :math:`x^{2/3}` it is better to input this as ``root(x^2, 3)``.

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

- ``atan2(y, x)`` for :math:`\tan^{-1}(y/x)` which also works when :math:`x = 0`. So ``atan2(1, 0)`` returns :math:`\pi/2`


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

- ``sign(x)`` returns the sign of ``x``, 1 if :math:`x>0`, 0 if :math:`x = 0`, :math:`-1` if :math:`x<0`.
- ``n!`` returns `n factorial` which is defined for non-negative integers with  :math:`0! = 1` and :math:`n! = n(n-1)(n-2) \cdots 1` for :math:`n > 0`.
- ``n!!`` returns `n double factorial` which is defined for non-negative integers with  :math:`0!! = 1` and :math:`n!! = n(n-2)(n-4) \cdots 1` for :math:`n > 0`.


:index:`User-Defined Functions`
-------------------------------

The CAS supports declaring user-defined functions, see :doc:`cassyntax` for more details.  If a function is defined in the CAS you can use it in a cell expressions or evaluate it with functional notation.

For example:

- ``f(x)`` will substitute the CAS expression for the function ``f(x)`` into the cell formula.
- ``f(5)`` will substitute the CAS expression for ``f(x)`` after the value 5 is substituted in for ``x``.
- You can incorporate these into expressions, such as ``1/g(x)``, ``h(cos(t), sin(t))``, ``k(1/t)``, and ``(f(x+h) - f(x))/h`` will return the difference quotient for the function ``f``.


:index:`Other Function Syntax`
------------------------------

The program is not limited to the above expressions.  As with the CAS input bar, you can use in any SymPy "one line" expression.  So for example, ``totient(12345)`` will return the Euler totient (phi) function of 12345, that is, 6576.  The program was built with the goal to minimize the amount of syntax that the users needs to learn, nonetheless the functionality is there.
