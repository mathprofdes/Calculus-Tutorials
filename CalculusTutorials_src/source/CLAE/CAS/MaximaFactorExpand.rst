:index:`Maxima: Factoring and Expanding`
========================================

Factor Expression
-----------------

Factors the expression, containing any number of variables or functions, into factors irreducible over the integers.  For example, the expression,

.. math::
    x^{7} + 9 x^{6} + 18 x^{5} - 50 x^{4} - 195 x^{3} - 27 x^{2} + 432 x + 324

factors as,

.. math::
    \left(x - 2\right)^{2} \left(x + 1\right) \left(x + 3\right)^{4}

The expression,

.. math::
    \sin^{3}{\left(x \right)} + 3 \sin^{2}{\left(x \right)} \cos{\left(x \right)} + 3 \sin{\left(x \right)} \cos^{2}{\left(x \right)} + \cos^{3}{\left(x \right)}

factors as,

.. math::
    \left(\sin{\left(x \right)} + \cos{\left(x \right)}\right)^{3}

Expand
------

Products of sums and exponentiated sums are multiplied out, numerators of rational expressions which are sums are split into their respective terms, and multiplication (commutative and non-commutative) are distributed over addition at all levels of the expression.  For example, the expression,

.. math::
    \left(x - 2\right)^{2} \left(x + 1\right) \left(x + 3\right)^{4}

expands to

.. math::
    x^{7} + 9 x^{6} + 18 x^{5} - 50 x^{4} - 195 x^{3} - 27 x^{2} + 432 x + 324

The expression,

.. math::
    \left(\sin{\left(x \right)} + \cos{\left(x \right)}\right)^{3}

expands to

.. math::
    \sin^{3}{\left(x \right)} + 3 \sin^{2}{\left(x \right)} \cos{\left(x \right)} + 3 \sin{\left(x \right)} \cos^{2}{\left(x \right)} + \cos^{3}{\left(x \right)}


Factor Integer
--------------

This option factors an integer into its prime factorization and returns the result as a list of lists. For example, if we factor, 89812552300216637943190741488, we get,

.. math::
    \left[ \left[ 2, \  4\right], \  \left[ 3, \  3\right], \  \left[ 1553, \  1\right], \  \left[ 1544469973, \  1\right], \  \left[ 86676699645961, \  1\right]\right]

This represents a product of factors from each sublist which are the prime factors and their exponents.  So in the above example we have,

.. math::
    89812552300216637943190741488 = 2^4 \cdot 3^3 \cdot 1553 \cdot 1544469973 \cdot 86676699645961

One must always be careful when factoring large integers.  Factoring large integers can take an significant amount of time even for relatively small numbers in the 40 to 50 digit range.  For example, this 55 digit number,

.. math::
    6625201490275387239416371207679474841313522226976616357 = 76235972897593275692756937481 \cdot 86903875407675697265924797

The integer factorization built into CLAE (which is SymPy) returned this result in about 5 minutes on my (i7) laptop.  Using the Maxima integer factorization the result was not returned inside the 10 minute timeout we had set.

