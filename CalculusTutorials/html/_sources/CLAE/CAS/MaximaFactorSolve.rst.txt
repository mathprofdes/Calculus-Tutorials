:index:`Maxima: Solve`
======================

Solving Equations
-----------------

As with the solve command in the Algebra menu all solving is done with the expression equated to zero.  The solve command in Maxima is very powerful, but we are only using a fraction of its capabilities since we need to convert the results back to CLAE (SymPy).  In same cases, the conversion back to CLAE does not go so well and the result is uninformative.  These cases are usually easy to spot.

For example, if we have the expression,

.. math::
    x^{3} - 3 x^{2} - x + 1

and select solve, with the variable *x*, the result is

.. math::
    \left[ 1 + \left(- \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \sqrt[3]{1 + \frac{\sqrt{111} i}{9}} + \frac{-2 + 2 \sqrt{3} i}{3 \sqrt[3]{1 + \frac{\sqrt{111} i}{9}}}, \  1 + \frac{-2 - 2 \sqrt{3} i}{3 \sqrt[3]{1 + \frac{\sqrt{111} i}{9}}} + \left(- \frac{1}{2} + \frac{\sqrt{3} i}{2}\right) \sqrt[3]{1 + \frac{\sqrt{111} i}{9}}, \  1 + \frac{4}{3 \sqrt[3]{1 + \frac{\sqrt{111} i}{9}}} + \sqrt[3]{1 + \frac{\sqrt{111} i}{9}}\right]

which are the exact solutions to, :math:`x^{3} - 3 x^{2} - x + 1 = 0.`

If we have the expression,

.. math::
    \sin{\left(5 x \right)} - \frac{1}{2}

the result of solving is,

.. math::
    \left[ \frac{\pi}{30}\right]

Note that it returns only a single solution instead of an expression representing an infinite number of solutions like the advanced solvers in the Algebra menu will,

.. math::
    \left\{\frac{2 \pi k}{5} + \frac{\pi}{30}\; \middle|\; k \in \mathbb{Z}\right\} \cup \left\{\frac{2 \pi k}{5} + \frac{\pi}{6}\; \middle|\; k \in \mathbb{Z}\right\}

If we have the expression,

.. math::
    \ln{\left(x^{2} - 5 \right)} + 17

the result of solving is,

.. math::
    \left[ - \frac{\sqrt{1 + 5 e^{17}}}{e^{\frac{17}{2}}}, \  \frac{\sqrt{1 + 5 e^{17}}}{e^{\frac{17}{2}}}\right]

