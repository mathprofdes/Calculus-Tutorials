:index:`The Intermediate Value Theorem`
=======================================


Discussion & Definitions
------------------------

.. admonition:: Theorem: The Intermediate Value Theorem

    Let :math:`f(x)` be continuous over a closed, bounded (finite) interval :math:`[a, b]`. If *d* is any real number between :math:`f(a)` and :math:`f(b)`, there exists a number *c* in :math:`[a, b]` such that :math:`f(c) = d`.


The Intermediate Value Theorem has a nice pictorial representation, below.  Start with a continuous function and an interval, :math:`[a, b]`.  Take vertical lines from *a* and *b* to the curve, then from there take horizontal lines to the *y*-axis.  These are the values of :math:`f(a)` and :math:`f(b)`.  Now select any value *d* between :math:`f(a)` and :math:`f(b)` on the *y*-axis, call it *d*.  From *d*, slide horizontally to the curve, then vertically to the *x*-axis.  You now have a point *c* such that :math:`f(c) = d`.

.. figure:: Images/Continuity/IVT001.png
    :alt: The Intermediate Value Theorem Visualization

    The Intermediate Value Theorem Visualization

.. note::

    A couple notes about the Intermediate Value Theorem.

    - The theorem does not give the actual value of *c*, it simply says that *c* exists.  To find *c* we need to solve the equation :math:`f(c) = d`, which could be difficult.
    - The theorem simply tells us that at least one value of *c* exists, it does not tell us how many values of *c* satisfy this expression.  Again we would need to solve :math:`f(c) = d` for all values of *c* that are in the interval, again this could be a difficult task.



Example: :math:`f(x) = x^{3} - 4 x^{2} + x + 3` on :math:`[1, 3]`
-----------------------------------------------------------------

For the image we used above to demonstrate the Intermediate Value Theorem was the function :math:`f(x) = x^{3} - 4 x^{2} + x + 3` on the interval :math:`[1, 3]`.  This was chosen arbitrarily for the image but we will take it through the process.

GeoGebra
^^^^^^^^

Input the function,

.. code-block:: console

    x^3-4 x^2+x+3

Evaluate the function at 1 and 3 by ``f(1)`` and ``f(3)``.  The results are 1 and :math:`-3`.

We selected :math:`d = -2`, again rather arbitrarily.  We know that the function is continuous and that *d* is between the values of :math:`f(a)` and :math:`f(b)`, so we know that a *c* exists.  We will go one step further and find the value of *c*.  In GeoGebra, go to the next open cell and type in ``Solve``, select ``Solve`` and in the parentheses type in ``f(x) = -2``, this is the equation :math:`f(c) = d` we need to solve.  GeoGebra returns ``{x = -0.91223, x = 1.71354, x = 3.19869}``.  Only one of them ``x = 1.71354`` is in our interval, so :math:`c = 1.71354`.

CLAE
^^^^

Input the function,

.. code-block:: console

    x^3-4*x^2+x+3

Using ``Algebra > Evaluate`` we can evaluate the function at 1 and 3.  The results are 1 and :math:`-3`.

We selected :math:`d = -2`, again rather arbitrarily.  We know that the function is continuous and that *d* is between the values of :math:`f(a)` and :math:`f(b)`, so we know that a *c* exists.  We will go one step further and find the value of *c*.  Assuming the expression was in R1, type in ``R1 - (-2)`` or ``R1+2`` into the CAS input bar and the resulting expression will be, :math:`x^{3} - 4 x^{2} + x + 5`.  Now select ``Algebra > Solve``, a dialog box will appear asking for the variable, use *x* and click OK.  The result is,

.. math::
    \left[ \frac{4}{3} - \frac{13}{\left(- \frac{3}{2} - \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{\frac{43}{2} + \frac{3 \sqrt{771} i}{2}}} - \frac{\left(- \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \sqrt[3]{\frac{43}{2} + \frac{3 \sqrt{771} i}{2}}}{3}, \  \frac{4}{3} - \frac{\left(- \frac{1}{2} + \frac{\sqrt{3} i}{2}\right) \sqrt[3]{\frac{43}{2} + \frac{3 \sqrt{771} i}{2}}}{3} - \frac{13}{\left(- \frac{3}{2} + \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{\frac{43}{2} + \frac{3 \sqrt{771} i}{2}}}, \  \frac{4}{3} - \frac{\sqrt[3]{\frac{43}{2} + \frac{3 \sqrt{771} i}{2}}}{3} - \frac{13}{3 \sqrt[3]{\frac{43}{2} + \frac{3 \sqrt{771} i}{2}}}\right]

CLAE will find exact solutions to equations when possible.  Also, the solve option in CLAE always assumes that the expression is being solved for 0.  This is why we took the equation :math:`f(c) = d` and reformed it into :math:`f(c) - d= 0` before solving.  This expression is rather complicated and you may notice that there are imaginary numbers involved.  We know that at least one of these solutions is a real number, in fact, all three are.  We will approximate this answer by ``Algebra > Approximate``.  We get,

.. math::
    \left[ 1.7135379349684, \  3.198691243516, \  -0.912229178484397\right]

When the expression was simplified and approximated the imaginary numbers in sense cancelled out leaving three real solutions.  Only one of these values is in our interval, so :math:`c = 1.7135379349684`.


Maxima
^^^^^^

Input the function,

.. code-block:: console

    kill(all);
    f(x):=x^3-4*x^2+x+3

Using

.. code-block:: console

    f(1);
    f(3)

we can evaluate the function at 1 and 3.  The results are 1 and :math:`-3`.

We selected :math:`d = -2`, again rather arbitrarily.  We know that the function is continuous and that *d* is between the values of :math:`f(a)` and :math:`f(b)`, so we know that a *c* exists.  We will go one step further and find the value of *c*.  Run the command,

.. code-block:: console

    solve(f(x)=-2,x)

We get the following, as with CLAE it is an exact expression.

.. math::
    \left[x=\left( \frac{-1}{2}-\frac{\sqrt{3} \% i}{2}\right)  {{\left( \frac{\sqrt{257} \% i}{2 {{3}^{\frac{3}{2}}}}-\frac{43}{54}\right) }^{\frac{1}{3}}}+\frac{13 \left( \frac{\sqrt{3} \% i}{2}+\frac{-1}{2}\right) }{9 {{\left( \frac{\sqrt{257} \% i}{2 {{3}^{\frac{3}{2}}}}-\frac{43}{54}\right) }^{\frac{1}{3}}}}+\frac{4}{3}\operatorname{,}x=\left( \frac{\sqrt{3} \% i}{2}+\frac{-1}{2}\right)  {{\left( \frac{\sqrt{257} \% i}{2 {{3}^{\frac{3}{2}}}}-\frac{43}{54}\right) }^{\frac{1}{3}}}+ \frac{13 \left( \frac{-1}{2}-\frac{\sqrt{3} \% i}{2}\right) }{9 {{\left( \frac{\sqrt{257} \% i}{2 {{3}^{\frac{3}{2}}}}-\frac{43}{54}\right) }^{\frac{1}{3}}}}+\frac{4}{3}\operatorname{,}x={{\left( \frac{\sqrt{257} \% i}{2 {{3}^{\frac{3}{2}}}}-\frac{43}{54}\right) }^{\frac{1}{3}}}+\frac{13}{9 {{\left( \frac{\sqrt{257} \% i}{2 {{3}^{\frac{3}{2}}}}-\frac{43}{54}\right) }^{\frac{1}{3}}}}+\frac{4}{3}\right]

Getting numerical approximations in Maxima can be a little tricky, since we know that there is at least one real root we will use both the float command and the realpart command.  Assuming that the above solution was ``%o4`` run the following,

.. code-block:: console

    float(%o4);
    realpart(%)

We get the following,

.. math::
    [x=1.713537934968399, x=-0.9122291784843963, x=3.198691243515997]

Only one of these values is in our interval, so :math:`c = 1.713537934968399`.
