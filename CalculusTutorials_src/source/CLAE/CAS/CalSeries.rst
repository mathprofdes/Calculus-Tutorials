:index:`Sequences and Series`
=============================

The following options allow the user to investigate concepts in sequences and series.


:index:`Sequence Limit`
-----------------------

The Sequence Limit option is for finding the limit of a sequence.  When this option is selected a dialog box will appear asking the user to input the variable of interest.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.  We will look at several examples.

- If we have :math:`\frac{n}{n + 1}` loaded into the CAS and select ``Calculus > Sequence Limit``, leave ``n`` as the variable and click OK, it returns 1.

- If we have :math:`\frac{n!}{n^n}` loaded into the CAS and select ``Calculus > Sequence Limit``, leave ``n`` as the variable and click OK, it returns 0.  Note that :math:`n!` is `n factorial` and is defined for non-negative integers with  :math:`0! = 1` and :math:`n! = n(n-1)(n-2) \cdots 1` for :math:`n > 0`.

- If we have :math:`\left(1 + \frac{1}{n}\right)^{n}` loaded into the CAS and select ``Calculus > Sequence Limit``, leave ``n`` as the variable and click OK, it returns :math:`e`.

- If we have :math:`\frac{\left(2 n - 1\right)!!}{\left(2 n\right)^{n} }` loaded into the CAS and select ``Calculus > Sequence Limit``, leave ``n`` as the variable and click OK, it returns 0. Note that :math:`n!!` is `n double factorial` and is defined for non-negative integers with  :math:`0!! = 1` and :math:`n!! = n(n-2)(n-4) \cdots 1` for :math:`n > 0`.

.. note ::

    Do not use the general limit option to find limits of sequences.  With sequences there are more assumptions that can be made and different algorithms that need to be used.

:index:`Sums`
-------------

The Sums submenu contains options for calculating finite and infinite sums as well as an option to test the sum for convergence.

Sum
^^^

This is for finding the exact values of a finite or infinite sum.  Note that finding exact values to sums can be computationally intense and in many cases this could take a long time to complete or you may not get a result. When you select this option you will get a dialog asking for the variable to sum over and the lower and upper bounds of the sum.  Remember to use ``oo`` for infinity and ``-oo`` for negative infinity.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.  We will look at several examples.

- If we have :math:`\frac{1}{2^n}` loaded into the CAS and select this option, leave ``n`` as the variable, use 1 and ``oo`` for the bounds and click OK, it returns 1.

- If we have :math:`\frac{1}{2^n}` loaded into the CAS and select this option, leave ``n`` as the variable, use 1 and 1000 for the bounds and click OK, it returns,

.. math::
    \frac{10715086071862673209484250490600018105614048117055336074437503883703510511249361224931983788156958581275946729175531468251871452856923140435984577574698574803934567774824230985421074605062371141877954182153046474983581941267398767559165543946077062914571196477686542167660429831652624386837205668069375}{10715086071862673209484250490600018105614048117055336074437503883703510511249361224931983788156958581275946729175531468251871452856923140435984577574698574803934567774824230985421074605062371141877954182153046474983581941267398767559165543946077062914571196477686542167660429831652624386837205668069376}

- For some fairly nice cases the program will return a partial sum formula. If we have :math:`\frac{1}{2^n}` loaded into the CAS and select this option, leave ``n`` as the variable, use 1 and t for the bounds and click OK, it returns :math:`1 - 2 \cdot 2^{- t - 1}`.

- The program can handle a variety of sum evaluations, for example a  telescoping sum. If we have :math:`\frac{1}{n \left(n + 1\right)}` loaded into the CAS and select this option, leave ``n`` as the variable, use 1 and ``oo`` for the bounds and click OK, it returns 1.

- If we have :math:`\frac{1}{n}` loaded into the CAS and select this option, leave ``n`` as the variable, use 1 and ``oo`` for the bounds and click OK, it returns :math:`\infty`.

- As mentioned above, exact sums can be difficult to calculate.  If we have :math:`\frac{n!}{n^n}` loaded into the CAS and select this option, leave ``n`` as the variable, use 1 and ``oo`` for the bounds and click OK, it returns the following, basically that it cannot find the exact sum.

.. math::
    \sum_{n=1}^{\infty} n^{- n} n!

Approximate Sum
^^^^^^^^^^^^^^^

This option will approximate a sum, in other words, allow the user to calculate finite sums numerically.  When you select this option you will get a dialog asking for the variable to sum over and the lower and upper bounds of the sum.  Here the lower and upper bounds must be integers, you cannot use variables or the infinities. There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.  We will look at several examples.

- If we have :math:`\frac{(-1)^n}{n}` loaded into the CAS and select the sum option, leave ``n`` as the variable, use 1 and ``oo`` for the bounds and click OK, it returns :math:`- \ln{\left(2 \right)} \approx -0.693147180559945`.  If we select this option and use 1 and 1000 for the bounds and click OK, it returns :math:`-0.6926474305598223` and if we use 1 and 1000000 for the bounds and click OK, it returns :math:`-0.6931466805602525`.  A fairly slow convergence.

- In the above example of :math:`\frac{n!}{n^n}`, the program could not find the exact value of the infinite sum.  If we jump ahead to the convergence tests we see that the sum is convergent.  So with this option we can get an approximation of the sum.  Select this option and use 1 and 100 for the bounds and we get 1.879853862175259.  If we rerun this using 150 as the upper bound we get 1.879853862175259, the same approximation.  So it is `safe` to say that the approximate infinite sum is close to  1.879853862175259.  Note that if you input 200 as the upper bound you will get an error, this is because there was an overload in the numeric values.  Although this is a computer algebra system and does exact arithmetic, when doing approximations you encounter the same numeric limitations as you do in numeric programs.


Test Sum Convergence
^^^^^^^^^^^^^^^^^^^^

The test of convergence is simply testing the sum expression using many of the convergence and divergence techniques you study in a Calculus class, and some more sophisticated tests.  The result is either True or False, or an error if can not determine convergence or divergence.  When you select this option you will get a dialog asking for the variable to sum over and the lower and upper bounds of the sum.  Remember to use ``oo`` for infinity and ``-oo`` for negative infinity.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.  We will look at several examples.

- If we test :math:`\frac{n!}{n^n}` from 1 to ``oo`` we get True, so the series converges.

- If we test :math:`\frac{n!}{2^n}` from 1 to ``oo`` we get False, so the series diverges.


:index:`Products`
-----------------

Products are usually not studied in introductory Calculus classes we included them here anyway.  In most respects these work the same way as with their sum counterparts.

Product
^^^^^^^

This is for finding the exact values of a finite or infinite product.  Note that finding exact values to products can be computationally intense and in many cases this could take a long time to complete or you may not get a result, which happens more often than with sums. When you select this option you will get a dialog asking for the variable to multiply over and the lower and upper bounds of the product.  Remember to use ``oo`` for infinity and ``-oo`` for negative infinity.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.  We will look at several examples.

- If we have :math:`\frac{1}{2^n}` loaded into the CAS and select this option, leave ``n`` as the variable, use 1 and ``oo`` for the bounds and click OK, it returns 0.

- If we have :math:`\frac{n + 1}{n}` loaded into the CAS and select this option, leave ``n`` as the variable, use 1 and ``oo`` for the bounds and click OK, it returns the following, meaning that it could not calculate the product.  This product does diverge but the program could not determine this.

.. math::
    \prod_{n=1}^{\infty} \frac{n + 1}{n}

- If we have :math:`\frac{n}{n + 1}` loaded into the CAS and select this option, leave ``n`` as the variable, use 1 and ``oo`` for the bounds and click OK, it returns the sum formula as in the last example, even though the product is 0.

In general, the Product option is not the most useful tool in this program but it is here if you want to use it.

Approximate Product
^^^^^^^^^^^^^^^^^^^

This option will approximate a product, in other words, allow the user to calculate finite products numerically.  When you select this option you will get a dialog asking for the variable to multiply over and the lower and upper bounds of the product.  Here the lower and upper bounds must be integers, you cannot use variables or the infinities. There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.  We will look at several examples.

- If we have :math:`\frac{n + 1}{n}` loaded into the CAS and select this option, leave ``n`` as the variable, use 1 and 1000 for the bounds and click OK, it returns 1000.9999999999947.  If we change the upper bound to 1000000 we get 1000000.9999998641.  Although this is far from proof, it does appear that the product is diverging.

- If we have :math:`\cos{\left(\frac{\pi}{n} \right)}` loaded into the CAS and we jump ahead to the convergence test for this product we see that the product does converge to a nonzero value.  If we select this option, leave ``n`` as the variable, use 1 and 1000 for the bounds and click OK, it returns :math:`-7.072970756374111 \cdot 10^{-18}`, 1 to 1000000 gives :math:`-7.038205097898972 \cdot 10^{-18}` and 1 to 10000000 gives :math:`-7.038173839064985 \cdot 10^{-18}`.

Test Product Convergence
^^^^^^^^^^^^^^^^^^^^^^^^

The test for convergence is similar to that for the sum except that it will also return False if the product is 0.  From the SymPy documentation:

The infinite product: :math:`\displaystyle \prod_{1 \leq i < \infty} f(i)` is defined by the sequence of partial products:
:math:`\displaystyle \prod_{i=1}^{n} f(i) = f(1) f(2) \cdots f(n)` as n increases without bound. The product converges to a nonzero value if and only if the sum: :math:`\displaystyle \sum_{1 \leq i < \infty} \log{f(n)}` converges.

So the determination of the convergence of the product depends on the convergence of the associated sum.  If the product is 0 then this sum diverges and the result is returned as False.

When you select this option you will get a dialog asking for the variable to sum over and the lower and upper bounds of the sum.  Remember to use ``oo`` for infinity and ``-oo`` for negative infinity.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.  We will look at several examples.

- If we have :math:`\cos{\left(\frac{\pi}{n} \right)}` loaded into the CAS and select this option using 1 and ``oo`` we get True.

- If we have :math:`\frac{1}{2^n}` loaded into the CAS and select this option, leave ``n`` as the variable, use 1 and ``oo`` for the bounds and click OK, it returns False.  In this case the product is 0.

- If we have :math:`\frac{\left(-1\right)^{n} n}{n + 1}` loaded into the CAS and select this option, leave ``n`` as the variable, use 2 and ``oo`` for the bounds and click OK, it returns False.  Note that if we start the product at 1 we get an error.


:index:`Taylor Series`
----------------------

This option will return a finite Taylor series expansion of a function.  When you select this option a dialog box will appear asking the user for the variable to expand over, the point to expand about, and the order of the Taylor polynomial to calculate.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

The order must be finite for this program and the expansion point can be any valid expression including CAS entries. We will look at several examples.

Example: Taylor Series Expansion of :math:`\sin(x)`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This option is nice for showing convergence of the Taylor Series to a function as well as intervals of convergence when you also use the graphics systems.  Start with :math:`\sin(x)` in the CAS and graph it.

.. figure:: Images/Taylor001.png
    :alt: y = sin(x)

    :math:`y = \sin{\left(x \right)}`

Select this option use 0 for the expansion point and order 10, the result is,

.. math::
    \frac{x^{9}}{362880} - \frac{x^{7}}{5040} + \frac{x^{5}}{120} - \frac{x^{3}}{6} + x

Now select this option use 0 for the expansion point and order 15, the result is,

.. math::
    \frac{x^{13}}{6227020800} - \frac{x^{11}}{39916800} + \frac{x^{9}}{362880} - \frac{x^{7}}{5040} + \frac{x^{5}}{120} - \frac{x^{3}}{6} + x

Now select this option use 0 for the expansion point and order 20, the result is,

.. math::
    - \frac{x^{19}}{121645100408832000} + \frac{x^{17}}{355687428096000} - \frac{x^{15}}{1307674368000} + \frac{x^{13}}{6227020800} - \frac{x^{11}}{39916800} + \frac{x^{9}}{362880} - \frac{x^{7}}{5040} + \frac{x^{5}}{120} - \frac{x^{3}}{6} + x

Graph these three polynomials along with :math:`\sin(x)` and we see,

.. figure:: Images/Taylor002.png
    :alt: y = sin(x) and Taylor Polynomials

    :math:`y = \sin{\left(x \right)}` and Taylor Polynomials

This gives a nice feeling about the convergence of the Taylor Series and the function :math:`\sin(x)`.

Now expand the series about :math:`\pi`, just use ``pi`` for the point, use order 10 as well.  This gives,

.. math::
    - x - \frac{\left(x - \pi\right)^{9}}{362880} + \frac{\left(x - \pi\right)^{7}}{5040} - \frac{\left(x - \pi\right)^{5}}{120} + \frac{\left(x - \pi\right)^{3}}{6} + \pi

and if we graph this along with the curve we get,

.. figure:: Images/Taylor003.png
    :alt: y = sin(x) and Taylor Polynomial

    :math:`y = \sin{\left(x \right)}` and Taylor Polynomial

Example: Taylor Series Expansion of :math:`\frac{1}{1-x}`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Another standard example in Calculus is the Taylor Series expansion of :math:`\frac{1}{1-x}`.  Input :math:`\frac{1}{1-x}` into the CAS and find the order 10 and order 20 Taylor series for this function centered at 0.  You should get

.. math::
    x^{9} + x^{8} + x^{7} + x^{6} + x^{5} + x^{4} + x^{3} + x^{2} + x + 1

and

.. math::
    x^{19} + x^{18} + x^{17} + x^{16} + x^{15} + x^{14} + x^{13} + x^{12} + x^{11} + x^{10} + x^{9} + x^{8} + x^{7} + x^{6} + x^{5} + x^{4} + x^{3} + x^{2} + x + 1

Graphing the function along with the two Taylor Series above gives,

.. figure:: Images/Taylor004.png
    :alt: y = 1/(1-x) and Taylor Polynomials

    :math:`y = \frac{1}{1-x}` and Taylor Polynomials

This should give the student a good feel that the series converge to the function in the interval :math:`(-1, 1)` but there are some problems outside that interval.

Variable Assumptions
--------------------

.. include:: ../CLAE/VariableAssumptions.md

