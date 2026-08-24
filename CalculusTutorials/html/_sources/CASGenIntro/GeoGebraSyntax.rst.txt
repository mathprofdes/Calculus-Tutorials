GeoGebra Expression Syntax
==========================

The following sections outline the syntax for GeoGebra expressions.  GeoGebra has an expression formatter in each of its input cells so much of the syntax is taken care of "under the hood" with this system but you still need to know some basic syntax.

If you click in an input box in the input panel on the left, an editing panel appears that has several modes.  The toolbar above the keypad will allow you switch between numbers, functions, qwerty keyboard, and special symbols. Also the three dots icon on the far right of this toolbar will open up the function quick help system that shows you all of the functions you have available for input.  Clicking on any if these will load the function syntax into the input box, you can also type in the function name from the keyboard.

.. figure:: ../CASGenIntro/Images/GeoGebraLayoutMenu006.png
    :alt: Command List

    Command List


Arithmetic Operations
---------------------

The basic arithmetic operations are ``+``, ``-``, ``*``, ``\``, and ``^``. All of which do what you would expect.  The ``^`` is exponentiation which will move the cursor into the exponent, ti get out of the exponent click the right arrow key.  Note that ``*`` can be used for multiplication but GeoGebra does understand juxtaposition as multiplication, so for :math:`2x` you can use the syntax ``2 x`` or ``2x``.

Variables
---------

The GeoGebra workspace on the left is closely linked to the graphs view on the right.  In so doing, GeoGebra is a bit more restrictive on variables.  In GeoGebra, *x*, *y*, *z*, and *t* are seen as independent variables and all other names are considered constants.  When GeoGebra encounters a constant it will automatically make a slider for the constant and substitute the slider value in for the constant in the expression.  For example, if you input ``theta`` GeoGebra will see this as ``t*heta`` and make a slider for ``heta``.  While this is a nice feature for the graphics facilities it does put some restrictions on what you can do as far as general CAS operations.

Previous Entries
----------------

GeoGebra gives a name or label to all of the entries in the CAS listing on the left.  To use any previous entry simply use the name that was given.  For example, in the image below for the lest entry we input ``f^2`` and the entry was complete.

.. figure:: ../CASGenIntro/Images/Syntax001.png
    :alt: Entry List

    Entry List

Infinity
--------

Infinity, :math:`\infty`, is represented as either ``inf`` or ``infinity`` and :math:`-\infty` is represented as either ``-inf`` or ``-infinity``.

Special Constants
-----------------

- ``pi`` represents :math:`\pi`
- ``e`` represents :math:`e`.
- ``i`` represents :math:`i` the imaginary unit.


Absolute Value
--------------

- Either ``abs(x)`` or ``|x|`` represents :math:`|x|`.

Root Functions
--------------

- ``sqrt(x)`` represents :math:`\sqrt{x}`.
- ``cbrt(x)`` represents :math:`\sqrt[3]{x}`.
- ``nroot(x, n)`` represents :math:`\sqrt[n]{x}`.
- Roots can also be written exponentially, for example, ``x^(1/3)`` for :math:`\sqrt[3]{x}`.

Trigonometric Functions
-----------------------

The trigonometric functions are as you would expect,

- ``sin(x)`` for :math:`\sin(x)`.
- ``cos(x)`` for :math:`\cos(x)`.
- ``tan(x)`` for :math:`\tan(x)`.
- ``cot(x)`` for :math:`\cot(x)`.
- ``sec(x)`` for :math:`\sec(x)`.
- ``cosec(x)`` for :math:`\csc(x)`.


Inverse Trigonometric Functions
-------------------------------

The inverse trigonometric functions simply have an ``a`` in front of them,

- ``asin(x)`` for :math:`\sin^{-1}(x)`.
- ``acos(x)`` for :math:`\cos^{-1}(x)`.
- ``atan(x)`` for :math:`\tan^{-1}(x)`.


Exponential & Logarithmic Functions
-----------------------------------

- ``exp(x)`` represents :math:`e^x`.
- ``e^x`` represents :math:`e^x`.
- ``ln(x)`` represents :math:`\ln(x)`.
- ``lg(x)`` represents :math:`\log_{10}(x)`.
- ``log10(x)`` represents :math:`\log_{10}(x)`.
- ``log(x)`` represents :math:`\log_{10}(x)`.
- ``log2(x)`` represents :math:`\log_{2}(x)`.
- ``ld(x)`` represents :math:`\log_{2}(x)`.
- ``log(b, x)`` represents :math:`\log_{b}(x)`.


Hyperbolic Functions
--------------------

The hyperbolic functions are as you would expect,

- ``sinh(x)`` for :math:`\sinh(x)`.
- ``cosh(x)`` for :math:`\cosh(x)`.
- ``tanh(x)`` for :math:`\tanh(x)`.
- ``coth(x)`` for :math:`\coth(x)`.
- ``sech(x)`` for :math:`{\rm sech}(x)`.
- ``cosech(x)`` for :math:`{\rm csch}(x)`.

Inverse Hyperbolic Functions
----------------------------

The inverse hyperbolic functions simply have an ``a`` in front of them,

- ``asinh(x)`` for :math:`\sinh^{-1}(x)`.
- ``acosh(x)`` for :math:`\cosh^{-1}(x)`.
- ``atanh(x)`` for :math:`\tanh^{-1}(x)`.


Integer Functions
-----------------

- ``floor(x)`` returns the largest integer value not greater than ``x``.
- ``ceil(x)`` returns the smallest integer value not less than ``x``.


Miscellaneous Functions
-----------------------

Some miscellaneous functions that may be of interest.

- ``sgn(x)`` returns the sign of ``x``, ``1`` if :math:`x>0`, ``0`` if :math:`x = 0`, and ``-1`` if :math:`x<0`.
- ``n!`` returns `n factorial` which is defined for non-negative integers with  :math:`0! = 1` and :math:`n! = n(n-1)(n-2) \cdots 1` for :math:`n > 0`.


Other Function Syntax
---------------------

GeoGebra has many more functions at the user's disposal, many are beyond scope of a STEM Calculus class.  Nonetheless, they can be used in expressions.  Above we covered the ones that are most pertinent for Calculus classes.
