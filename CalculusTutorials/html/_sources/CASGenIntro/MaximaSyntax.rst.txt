Maxima Expression Syntax
========================

The following sections outline the syntax for expressions input into the Maxima (wxMaxima) CAS.

Arithmetic Operations
---------------------

The basic arithmetic operations are ``+``, ``-``, ``*``, ``\``, and ``^``. All of which do what you would expect.  The ``^`` is exponentiation and you can also use ``**`` in place of the ``^`` operator. Note that ``*`` must be used for multiplication, this program does not recognize juxtaposition as multiplication, so for :math:`2x` we use the syntax ``2*x`` and not ``2 x`` or ``2x``, the second two are syntax error.

Variables
---------

Variables, can be any expression that is not a built-in function, starts with a letter or underscore and has only letters, numbers, and underscores after that.  So ``a``, ``x``, ``xpt1``, and ``John_Smith`` are all valid variables.

Previous CAS Results
--------------------

Note that wxMaxima labels the input and output as ``%i1`` and ``%o1`` respectively.  These can be used in the formulas for subsequent inputs.

.. code-block:: maxima

    (%i1)	1+1;
    (%o1)	2

Also, the ``%`` is a shorthand for the last output.  So if we put in a couple more inputs,

.. figure:: ../CASGenIntro/ImagesMaxima/MaximaLayout003.png
    :alt: Maxima Layout with Expressions

    Maxima Layout with Expressions


So for the second input we typed in ``5*%`` and it replaced the ``%`` by the last output of 2.  Similarly, for the third input we typed in ``%*sin(x)``.  In the input ``%o1*cos(x)`` we used the complete name of the first output which was replaced by 2.  Also note that there is a skip in the numbers, this was due to multiple inputs in the same cell.  wxMaxima numbers them sequentially but if a cell is edited and evaluated the new number will overwrite the old one.

.. code-block:: maxima

    (%i1)	1+1;
    (%o1)	2
    (%i2)	5*%;
    (%o2)	10
    (%i3)	%*sin(x);
    (%o3)	10*sin(x)
    (%i6)	%o1*cos(x);
    (%o6)	2*cos(x)

As you can also see from this series of inputs, Maxima can handle variables and exact values like any computer algebra system.

Infinity
--------

Infinity, :math:`\infty`, is represented as ``inf`` and :math:`-\infty` is represented as either ``-inf`` or ``minf``.

Special Constants
-----------------

Special constants begin with a ``%``

- ``%pi`` represents :math:`\pi`
- ``%e`` represents :math:`e`.
- ``%i`` represents :math:`i` the imaginary unit.


Absolute Value
--------------

- ``abs(x)`` represents :math:`|x|`.

Root Functions
--------------

- ``sqrt(x)`` represents :math:`\sqrt{x}`.
- Other roots can be written exponentially, for example, ``x^(1/3)`` for the cube root of ``x``.

Trigonometric Functions
-----------------------

The trigonometric functions are as you would expect,

- ``sin(x)`` for :math:`\sin(x)`.
- ``cos(x)`` for :math:`\cos(x)`.
- ``tan(x)`` for :math:`\tan(x)`.
- ``cot(x)`` for :math:`\cot(x)`.
- ``sec(x)`` for :math:`\sec(x)`.
- ``csc(x)`` for :math:`\csc(x)`.


Inverse Trigonometric Functions
-------------------------------

The inverse trigonometric functions simply have an ``a`` in front of them,

- ``asin(x)`` for :math:`\sin^{-1}(x)`.
- ``acos(x)`` for :math:`\cos^{-1}(x)`.
- ``atan(x)`` for :math:`\tan^{-1}(x)`.
- ``acot(x)`` for :math:`\cot^{-1}(x)`.
- ``asec(x)`` for :math:`\sec^{-1}(x)`.
- ``acsc(x)`` for :math:`\csc^{-1}(x)`.

In addition there is

- ``atan2(y, x)`` for :math:`\tan^{-1}(y/x)` which also works when :math:`x = 0`. So ``atan2(1, 0)`` returns :math:`\pi/2`


Exponential & Logarithmic Functions
-----------------------------------

- ``exp(x)`` represents :math:`e^x`.
- ``log(x)`` represents :math:`\ln(x)`.
- To calculate :math:`\log_n(x)`, use the base change formula, :math:`\log_n(x) = \frac{\log(x)}{\log(a)}`.


Hyperbolic Functions
--------------------

The hyperbolic functions are as you would expect,

- ``sinh(x)`` for :math:`\sinh(x)`.
- ``cosh(x)`` for :math:`\cosh(x)`.
- ``tanh(x)`` for :math:`\tanh(x)`.
- ``coth(x)`` for :math:`\coth(x)`.
- ``sech(x)`` for :math:`{\rm sech}(x)`.
- ``csch(x)`` for :math:`{\rm csch}(x)`.

Inverse Hyperbolic Functions
----------------------------

The inverse hyperbolic functions simply have an ``a`` in front of them,

- ``asinh(x)`` for :math:`\sinh^{-1}(x)`.
- ``acosh(x)`` for :math:`\cosh^{-1}(x)`.
- ``atanh(x)`` for :math:`\tanh^{-1}(x)`.
- ``acoth(x)`` for :math:`\coth^{-1}(x)`.
- ``asech(x)`` for :math:`{\rm sech}^{-1}(x)`.
- ``acsch(x)`` for :math:`{\rm csch}^{-1}(x)`.


Integer Functions
-----------------

- ``floor(x)`` returns the largest integer value not greater than ``x``.
- ``ceiling(x)`` returns the smallest integer value not less than ``x``.


Miscellaneous Functions
-----------------------

Some miscellaneous functions that may be of interest.

- ``sign(x)`` returns the sign of ``x``, ``pos`` if :math:`x>0`, ``zero`` if :math:`x = 0`, and ``neg`` if :math:`x<0`.
- ``n!`` returns `n factorial` which is defined for non-negative integers with  :math:`0! = 1` and :math:`n! = n(n-1)(n-2) \cdots 1` for :math:`n > 0`.
- ``n!!`` returns `n double factorial` which is defined for non-negative integers with  :math:`0!! = 1` and :math:`n!! = n(n-2)(n-4) \cdots 1` for :math:`n > 0`.


User-Defined Functions
----------------------

The CAS also supports declaring user-defined functions.  To create a user defined function start with a function name and variable list, as you would in writing it mathematically, then type in ``:=`` followed by any valid expression (including previous CAS results).

For example:

- ``f(x) := x^2-2*x+1``
- ``g(x) := %o7``
- ``h(x, y) := sin(x)/(y^2+1)``
- ``k(t) := cos(%o7)/t^3 + exp(t^2)``

Once a function is defined you can use it in expressions or evaluate it with functional notation.

For example:

- ``f(5)`` will return the expression value after 5 is substituted in for ``x``.
- ``1/g(x)`` would be equivalent to ``1/%o7``
- ``h(cos(t), sin(t))`` will substitute ``cos(t)`` for ``x`` and ``sin(t)`` for ``y``.
- ``k(1/t)`` will substitute ``1/t`` for ``t``.
- ``(f(x+h) - f(x))/h`` will return the difference quotient for the function ``f``.

Once a function is input into the CAS you can use the same function name for another function definition.  So if you define a function called ``f`` you may use ``f`` again.  The current function definition is the last one that was input.  Any cells that are dependent on a function whose definition has changed are not automatically updated.  You can reevaluate these cells by selecting them and hitting Ctrl+Enter.  The user should be cautious about this feature since if a function is changed any dependent cells will contain stale or out-of-date results.


Other Function Syntax
---------------------

Maxima has literally thousands of functions, many are beyond scope of a STEM Calculus class.  Nonetheless, they can be used in expressions.  Above we covered the ones that are most pertinent for Calculus classes.

