:index:`Function Properties`
============================

This submenu contains some standard function properties that are normally studied in conjunction with Calculus.  In each case it takes a single expression to analyze, if you try to do any of these on a matrix or on a piecewise defined function you will get an error.

:index:`Continuous Domain`
--------------------------

This option will open a dialog box asking for the independent variable to use, if the program is to use the entire real line or an interval as the encompassing domain and the bounds for the interval if that is selected.  The result is a union of intervals inside the encompassing domain where the function is continuous.  While this is not technically the domain of the function, with most functions studied in Calculus the domain and the continuous domain are the same.

For example, if we take the function :math:`\tan(x)` on the entire real line the result is,

.. math::
    \mathbb{R} \setminus \left(\left\{2 \pi k + \frac{\pi}{2}\; \middle|\; k \in \mathbb{Z}\right\} \cup \left\{2 \pi k + \frac{3 \pi}{2}\; \middle|\; k \in \mathbb{Z}\right\}\right)

which is :math:`\mathbb{R}` minus the singularities. If we used the same function on the interval :math:`[0, 10]` we get,

.. math::
    \left[0, \frac{\pi}{2}\right) \cup \left(\frac{\pi}{2}, \frac{3 \pi}{2}\right) \cup \left(\frac{3 \pi}{2}, \frac{5 \pi}{2}\right) \cup \left(\frac{5 \pi}{2}, 10\right]

.. note::

    In cases where there are a lot of singularities, such as :math:`\tan(x)`, it is better to use the entire real line and not a large interval.  If there are a lot of intervals in the union the process can be lengthy.

:index:`Range`
--------------

This option will open a dialog box asking for the independent variable to use, if the program is to use the entire real line or an interval as the encompassing domain and the bounds for the interval if that is selected.  The result is the range of the function inside the encompassing domain.

For example, if we take the function :math:`\tan(x)` on the entire real line the result is, :math:`\left(-\infty, \infty\right)`.  If we take the function :math:`\sin(x)` on the entire real line the result is, :math:`\left[-1, 1\right]`.  Finally if we take the function :math:`\sin(x)` on the interval :math:`[\pi/4, 3\pi/4]` the result is, :math:`\left[\frac{\sqrt{2}}{2}, 1\right]`.


:index:`Singularities`
----------------------

This option will open a dialog box asking for the independent variable to use, if the program is to use the entire real line, the complex numbers, or an interval of the real line as the encompassing domain and the bounds for the interval if that is selected.  The result is the set of singularities of the function inside the encompassing domain.

For example, if we use the expression,

.. math::
    \frac{1}{x^{4} - 1}

with the real numbers the singularities are :math:`\left\{-1, 1\right\}`, with the complex numbers the singularities are :math:`\left\{-1, 1, - i, i\right\}`, and on the interval :math:`[0, 10]` the singularities are :math:`\left\{1\right\}`.

:index:`Periodicity`
--------------------

This option attempts to find the period of the function.  If the function is not periodic or if the program cannot determine the period of the function it will return an error.  A constant function will have period 0.  In some rare cases the reported period will be a multiple of the actual period.  If the program detects that there is only one variable to the function it will attempt to find the periodicity with respect to that variable.  If the function has more than one variable a dialog box will open asking for the independent variable.

For example, the period of :math:`\sin(x)` is reported correctly as :math:`2\pi`. The period of :math:`\sin{\left(2 x \right)} + \cos{\left(7 x \right)}` is also :math:`2\pi`. The period of :math:`\sin{\left(2 x \right)} + \cos{\left(\frac{x}{7} \right)}` is :math:`14\pi`.


