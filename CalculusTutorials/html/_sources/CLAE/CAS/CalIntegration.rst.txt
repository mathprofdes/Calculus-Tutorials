:index:`Integration`
====================

Limits, derivatives, and integration are at the heart of an introductory Calculus sequence.  Here we will look at integration, limits and derivatives are covered in the :doc:`CalLimitsDerivatives` section.  These also deal with integrals of single variable functions, for double and triple integrals please see the :doc:`CalMultInt` section.

:index:`Indefinite Integral`
----------------------------

To calculate an indefinite integral of a function simply select ``Calculus > Indefinite Integral`` from the main menu.  When you do, a dialog box will appear asking the user to input the variable to integrate with respect to, whether or not to include a constant of integration, and whether or not to use "Course Techniques" to solve the integral.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

The including of a constant of integration simply adds in a constant of the form, :math:`C_1`, :math:`C_2`, :math:`C_3`, ... The "Course Techniques" selection will tell the program to use techniques that are commonly covered in an introductory integral calculus class.  This will produce an answer that is closer to what a human would get if doing it by hand.  On the other hand, it also restricts the techniques it can use for solving the integral and hence may not return a result and may take much longer to produce a result. The default setting for this option is off, which will use the full power of the integration routines to find the integral.  If the result is too complicated you can rerun the the integration with the Course Techniques selected.

For example, take the function, :math:`x \cos{\left(x^{2} \right)}`.  If we integrate using course techniques and no constant we get, :math:`\frac{\sin{\left(x^{2} \right)}}{2}`, as would be expected from an easy substitution.  If we include the constant of integration the result is, :math:`C_{1} + \frac{\sin{\left(x^{2} \right)}}{2}`.  If we were to click and drag this over to the graph we would automatically get a ``C1`` slider that illustrates the family of indefinite integrals nicely.  If we turn off the course techniques we will get the same solution, this is not a difficult integral to do and we did not need to employ more sophisticated techniques.

As another example, if we take the function,

.. math::
    \frac{1}{x \sqrt{x - 1}}

and find the indefinite integral with course techniques turned off we get,

.. math::
    \begin{cases} 2 i \operatorname{acosh}{\left(\frac{1}{\sqrt{x}} \right)} & \text{for}\: \left(x > -1 \vee x > 0\right) \wedge \left(x > -1 \vee x < 1\right) \wedge \left(x > 0 \vee x < 0\right) \wedge \left(x < 0 \vee x < 1\right) \\- 2 \operatorname{asin}{\left(\frac{1}{\sqrt{x}} \right)} & \text{otherwise} \end{cases}

and with course techniques turned on we get,

.. math::
    2 \operatorname{atan}{\left(\sqrt{x - 1} \right)}

Note that

.. math::
    2 \operatorname{atan}{\left(\sqrt{x - 1} \right)} - \left(- 2 \operatorname{asin}{\left(\frac{1}{\sqrt{x}} \right)} \right) = \pi

Also, it should be noted that from time to time you will get better answers with the course techniques turned off.  It is good to try both if the first answer you get is not very nice.  As an example, take the function we were working with above, :math:`x \cos{\left(x^{2} \right)}`, and take its derivative, giving, :math:`- 2 x^{2} \sin{\left(x^{2} \right)} + \cos{\left(x^{2} \right)}`.  Now if we take the integral of this we should be back to the original expression.  If we leave the course techniques off we get, :math:`x \cos{\left(x^{2} \right)}` as expected.  If we turn the course techniques on we get,

.. math::
    \sqrt{2} \sqrt{\pi} \left(\frac{\sqrt{2} x^{5} \Gamma\left(\frac{3}{4}\right) \Gamma\left(\frac{5}{4}\right) {{}_{2}F_{3}\left(\begin{matrix} \frac{3}{4}, \frac{5}{4} \\ \frac{3}{2}, \frac{7}{4}, \frac{9}{4} \end{matrix}\middle| {- \frac{x^{4}}{4}} \right)}}{8 \sqrt{\pi} \Gamma\left(\frac{7}{4}\right) \Gamma\left(\frac{9}{4}\right)} - x^{2} S\left(\frac{\sqrt{2} x}{\sqrt{\pi}}\right) + \frac{C\left(\frac{\sqrt{2} x}{\sqrt{\pi}}\right)}{2}\right)



:index:`Definite Integral`
--------------------------

To calculate a definite integral of a function simply select ``Calculus > Definite Integral`` from the main menu.  When you do, a dialog box will appear asking the user to input the variable to integrate with respect to, the lower and upper bounds of integration, and whether or not to use "Course Techniques" to solve the integral.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

The use of "Course Techniques", as discussed above, restricts the methods to those commonly covered in an introductory integral calculus class. The lower and upper bounds can be any valid expression including the use of previous CAS workspace items.  For a refresher on the syntax please see :doc:`../CLAE/syntax`.

For example, we will use the same function as we did above, :math:`x \cos{\left(x^{2} \right)}`, and calculate the definite integral over the interval :math:`[0, \pi/2]`.  Image below,

.. figure:: Images/Int001.png
    :alt: y = x*cos(x^2)

    :math:`y = x \cos{\left(x^{2} \right)}`

Select the definite integral menu option, put in ``0`` for the lower bound and ``pi/2`` for the upper bound. The result will be :math:`\displaystyle \frac{\sin{\left(\frac{\pi^{2}}{4} \right)}}{2}`, as expected.

:index:`Definite Integral Approximation`
----------------------------------------

This option will approximate the definite integral.  This comes in handy when you are integrating something that does not have an elementary anti-derivative.  When this option is invoked a dialog will appear asking the user to input the variable to integrate with respect to, and the lower and upper bounds of integration.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

For example, lets calculate the integral of :math:`\sin{\left(\cos{\left(x \right)} \right)}` over the interval :math:`[0, \pi/2]`, image below.

.. figure:: Images/Int002.png
    :alt: y = sin(cos(x))

    :math:`y = \sin{\left(\cos{\left(x \right)} \right)}`

If we try to find an indefinite integral of this function we get,

.. math::
    \int \sin{\left(\cos{\left(x \right)} \right)}\, dx

Since it gave back the question it could not calculate an anti-derivative.  If we tried the definite integral between 0 and :math:`\pi/2` we get,

.. math::
    \int\limits_{0}^{\frac{\pi}{2}} \sin{\left(\cos{\left(x \right)} \right)}\, dx

not surprising.  If we instead use this approximation method we get the result :math:`0.893243740975026`.  The technique used to find this approximation is not generally studied in introductory Calculus, the tanh-sinh quadrature algorithm is used to evaluate integrals. This algorithm is very efficient and robust for smooth integrands.

:index:`Integral Approximation Techniques`
------------------------------------------

Although the integral approximation option discussed above is fr more accurate in general we have included the three methods commonly studied in introductory Calculus, Riemann Sums, The Trapezoidal Rule, and Simpson's Rule.

:index:`Riemann Sum`
^^^^^^^^^^^^^^^^^^^^

The Riemann Sum option calculates a Riemann sum of a function over an interval with a few options.  When invoked a dialog box will appear asking the user for the variable, lower and upper bounds, a test point position, and the number of divisions for the interval. There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

The lower and upper bounds can be any valid expression, including CAS workspace entries.  The number of divisions is simply the number of rectangles the program will use in the calculation.  The test point position is the position in the sub-interval where the function is evaluated to get the height of the rectangle.  This value is to be between 0 and 1.  A position of 0 would mean that the program will use the left-hand endpoint of each sub-interval to evaluate the function and determine the rectangle height.  A value of 1 would use the right-hand endpoint, and a value of 0.5 is the midpoint rule.  You can set this any value between 0 and 1, so you could set it to 0.25 and do a "one-quarter rule" or to 0.75 and do a  "three-quarters rule", etc.

For example, if we use the function :math:`\sin{\left(\cos{\left(x \right)} \right)}` and do a left-hand endpoint Riemann sum with 10 rectangles on :math:`[0, \pi/2]` we get 0.9572748528628714, using the right-hand endpoint we get 0.8250968996587985, and the midpoint rule gives 0.8942733103195926.  You can also do approximations with many rectangles, for example a midpoint rule with the same settings and 1,000,000 rectangles gives 0.8932437409751336, which matches the more advanced method to 12 decimal places.

:index:`Trapezoidal Rule`
^^^^^^^^^^^^^^^^^^^^^^^^^

The Trapezoidal Rule option applies the Trapezoidal Rule to a function over an interval with a specified number of trapezoids.  When invoked a dialog box will appear asking the user for the variable, lower and upper bounds, and the number of divisions for the interval. There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

The lower and upper bounds can be any valid expression, including CAS workspace entries.  The number of divisions is simply the number of rectangles the program will use in the calculation.  For example, lets take the function :math:`\sin{\left(\cos{\left(x \right)} \right)}` and do a Trapezoidal Rule approximation with 10 trapezoids on :math:`[0, \pi/2]` we get 0.8911858762608349, and with 1,000,000 trapezoids we get 0.893243740974833.

:index:`Simpson's Rule`
^^^^^^^^^^^^^^^^^^^^^^^

The Simpson's Rule option applies Simpson's Rule to a function over an interval with a specified number of divisions.  When invoked a dialog box will appear asking the user for the variable, lower and upper bounds, and the number of divisions for the interval. There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

The lower and upper bounds can be any valid expression, including CAS workspace entries.  The number of divisions is simply the number of segments the program will use in the calculation.  Recall that for Simpson's Rule the number of divisions needs to be even.  Even though the number of divisions selector will allow you to put in an odd number the program will give you an error message if you try to use an odd number of divisions.

For example, lets take the function :math:`\sin{\left(\cos{\left(x \right)} \right)}` and do a Simpson's Rule approximation with 10 divisions on :math:`[0, \pi/2]` we get 0.8932506281378304, and with 1,000,000 divisions we get 0.8932437409750311.


Variable Assumptions
--------------------

.. include:: ../CLAE/VariableAssumptions.md



