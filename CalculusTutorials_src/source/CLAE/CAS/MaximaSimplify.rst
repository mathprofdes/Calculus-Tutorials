:index:`Maxima: Simplification`
===============================

Simplify
--------

Simplifies the expression and all of its subexpressions, including the arguments to non-rational functions. This includes some simplifications of logarithms and powers. For example,

.. math::
    e^{\left(\ln{\left(x \right)} + 1\right)^{2} - \ln{\left(x \right)}^{2}} + \sin{\left(\frac{x}{x^{2} + x} \right)}

simplifies to

.. math::
    e x^{2} + \sin{\left(\frac{1}{x + 1} \right)}

Special Simplifications
-----------------------

Simplify
^^^^^^^^

This is the same as the Simplify option, it simplifies the expression and all of its subexpressions, including the arguments to non-rational functions. This includes some simplifications of logarithms and powers.  For example,

.. math::
    e^{\left(\ln{\left(x \right)} + 1\right)^{2} - \ln{\left(x \right)}^{2}} + \sin{\left(\frac{x}{x^{2} + x} \right)}

simplifies to

.. math::
    e x^{2} + \sin{\left(\frac{1}{x + 1} \right)}

Simplify Radicals, Logs, and Exponents
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Simplifies expressions which can contain logs, exponentials, and radicals, by converting it into a form which is canonical over a large class of expressions and a given ordering of variables.  For some expressions this can be quite time consuming. For example,

.. math::
    \left(- \ln{\left(x \right)} + \ln{\left(x^{2} + x \right)}\right)^{a} \ln{\left(x + 1 \right)}^{- \frac{a}{2}}

simplifies to

.. math::
    \ln{\left(x + 1 \right)}^{\frac{a}{2}}

Write with Common Denominator
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This option combines all terms of the expression which should be a sum over a common denominator without expanding products and exponentiated sums.  This option cancels common factors in the numerator and denominator of rational expressions but only if the factors are explicit.  Sometimes this gives a better result for rational expression than using Simplify. For example,

.. math::
    - \frac{x}{\left(x + y\right)^{5}} + \frac{- 2 y + \left(x + 2\right)^{2}}{\left(x + y\right)^{2}} + \frac{1}{\left(x - y\right)^{9}}

simplifies to

.. math::
    \frac{- x \left(x - y\right)^{9} + \left(x - y\right)^{9} \left(x + y\right)^{3} \left(- 2 y + \left(x + 2\right)^{2}\right) + \left(x + y\right)^{5}}{\left(x - y\right)^{9} \left(x + y\right)^{5}}


Contract Logarithms
^^^^^^^^^^^^^^^^^^^

Contracts logarithmic expressions and subexpressions using the sum and exponent formulas, such as, :math:`\ln{\left(x \right)} + \ln{\left(y \right)} = \ln{\left(x y \right)}` and :math:`5 \ln{\left(x \right)} = \ln{\left(x^{5} \right)}.` For example,

.. math::
    2 a \ln{\left(x \right)} + 4 a \ln{\left(y \right)}

simplifies to

.. math::
    a \ln{\left(x^{2} y^{4} \right)}

Note that the integers are taken to exponents but the variable *a* is not.

Expand Logarithms
^^^^^^^^^^^^^^^^^

Expands logarithmic expressions and subexpressions using the sum and exponent formulas, such as, :math:`\ln{\left(x \right)} + \ln{\left(y \right)} = \ln{\left(x y \right)}` and :math:`5 \ln{\left(x \right)} = \ln{\left(x^{5} \right)}.` For example,


.. math::
    a \ln{\left(x^{2} y^{4} \right)}

simplifies to

.. math::
    2 a \ln{\left(x \right)} + 4 a \ln{\left(y \right)}

Simplify Trigonometric Expressions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Employs the identities :math:`\sin^2(x) + \cos^2(x) = 1` and :math:`\cosh^2(x) - \sinh^2(x) = 1` to simplify expressions containing tan, sec, etc., to sin, cos, sinh, cosh.  For example,

.. math::
    \left(\sin{\left(x \right)} + \cos{\left(x \right)}\right)^{2}

simplifies to

.. math::
    2 \sin{\left(x \right)} \cos{\left(x \right)} + 1

Reduce Trigonometric Expressions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Combines products and powers of trigonometric and hyperbolic sin’s and cos’s into those of multiples. It also tries to eliminate these functions when they occur in denominators. For example,

.. math::
    x - \sin^{2}{\left(x \right)} + 3 \cos^{2}{\left(x \right)}

simplifies to

.. math::
    x + 2 \cos{\left(2 x \right)} + 1

Expand Trigonometric Expressions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Expands trigonometric and hyperbolic functions of sums of angles and of multiple angles occurring in the expression. For example,

.. math::
    \sin{\left(x + y \right)}

simplifies to

.. math::
    \sin{\left(x \right)} \cos{\left(y \right)} + \sin{\left(y \right)} \cos{\left(x \right)}

Write Trigonometric Expressions in Canonical Form
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Gives a canonical simplified quasilinear form of a trigonometrical expression.  For example,

.. math::
    \frac{\sin{\left(3 a \right)}}{\sin{\left(a + \frac{\pi}{3} \right)}}

simplifies to

.. math::
    \sqrt{3} \sin{\left(2 a \right)} + \cos{\left(2 a \right)} - 1

Partial Fractions
^^^^^^^^^^^^^^^^^

Expands the expression in partial fractions with respect to the main variable that is input in the dialog box. This option does a complete partial fraction decomposition. The algorithm employed is based on the fact that the denominators of the partial fraction expansion (the factors of the original denominator) are relatively prime. The numerators can be written as linear combinations of denominators, and the expansion falls out. For example,

.. math::
    - \frac{x}{x^{3} + 4 x^{2} + 5 x + 2}

simplifies to

.. math::
    \frac{2}{x + 2} - \frac{2}{x + 1} + \frac{1}{\left(x + 1\right)^{2}}

