:index:`Limits at Infinity`
===========================

Discussion & Definitions
------------------------

The term *limit at infinity* is really asking the question, what is a function doing as the values of *x* get arbitrary large either positively or negatively. Another way to say this is what is the :index:`end behavior` of the function, what is it doing when its graph goes off the screen in either direction.  Remember that infinity is not a number so we cannot *approach* infinity in tht sense.  When we say we are approaching infinity we really mean we are letting *x* get arbitrarily large.  With this in mind we define our limits at infinity.

.. admonition:: Definition: Limits at Infinity

    - Let :math:`f(x)` be a function defined at all values in an open interval :math:`(c, \infty)`. If the values of the function :math:`f(x)` approach the real number *L* as the values of *x* *increase without bound*, then we say that *the limit of f(x) as x approaches* :math:`\infty` *is L*.  That is, as *x* gets arbitrarily large, :math:`f(x)` gets closer to *L*.  Symbolically we write,

    .. math::

        \lim_{x \to \infty} f(x) = L

    - Let :math:`f(x)` be a function defined at all values in an open interval :math:`(-\infty, c)`. If the values of the function :math:`f(x)` approach the real number *L* as the values of *x* *decrease without bound*, then we say that *the limit of f(x) as x approaches* :math:`-\infty` *is L*.  That is, as *x* gets arbitrarily small (that is, large negatively), :math:`f(x)` gets closer to *L*.  Symbolically we write,

    .. math::

        \lim_{x \to -\infty} f(x) = L


For example, if we graph,

.. math::
    f(x) = \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1}

.. figure:: Images/Limits/LimAtInf002.png
    :alt: y = (3x^2+2x-1)/(x^2+x+1)

    :math:`f(x) = \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1}`

Looking at the graph at the two ends it does appear that the graph is leveling out to a single number :math:`L = 3` off to the right.  It also appears that the graph is leveling out to a single number :math:`L = 3` off to the left. In our notation we would write,

.. math::

    \lim_{x \to \infty} \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1} = 3 \quad {\rm and} \quad \lim_{x \to -\infty} \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1} = 3

We can also attack this numerically, we simply let the *x* values get large and plug them into the function to see the corresponding outputs.  From the values in the second column we would conclude that same as we did with the graph.

.. math::
    \begin{array}{l|l}
    x & \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1} \\ \hline
    1.0 & 1.33333333333333 \\
    10.0 & 2.87387387387387 \\
    100.0 & 2.98970398970399 \\
    1000.0 & 2.998997003999 \\
    10000.0 & 2.999899970004 \\
    100000.0 & 2.9999899997 \\
    1000000.0 & 2.999998999997 \\
    10000000.0 & 2.99999989999997 \\
    100000000.0 & 2.99999999 \\
    1000000000.0 & 2.999999999 \\
    \end{array}

.. math::
    \begin{array}{l|l}
    x & \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1} \\ \hline
    -1.0 & 0 \\
    -10.0 & 3.06593406593407 \\
    -100.0 & 3.00969599030401 \\
    -1000.0 & 3.000996995999 \\
    -10000.0 & 3.000099969996 \\
    -100000.0 & 3.0000099997 \\
    -1000000.0 & 3.000000999997 \\
    -10000000.0 & 3.00000009999997 \\
    -100000000.0 & 3.00000001 \\
    -1000000000.0 & 3.000000001 \\
    \end{array}

As another example, if we graph,

.. math::
    f(x) = 1 + \frac{\cos{\left(x \right)}}{x}

.. figure:: Images/Limits/LimAtInf001.png
    :alt: 1 + cos(x)/x

    :math:`f(x) = 1 + \frac{\cos{\left(x \right)}}{x}`

Looking at the graph at the two ends it does appear that the graph is leveling out to a single number :math:`L = 1` off to the right.  It also appears that the graph is leveling out to a single number :math:`L = 1` off to the left. In our notation we would write,

.. math::

    \lim_{x \to \infty} 1 + \frac{\cos{\left(x \right)}}{x} = 1 \quad {\rm and} \quad \lim_{x \to -\infty} 1 + \frac{\cos{\left(x \right)}}{x} = 1

.. admonition:: Definition: Horizontal Asymptote

    If either

    .. math::

        \lim_{x \to \infty} f(x) = L \quad {\rm or } \quad \lim_{x \to -\infty} f(x) = L

    then we say that the line :math:`y = L` is a  :index:`horizontal asymptote` of :math:`f`.

Going back to our previous examples.  If we graph,

.. math::
    f(x) = \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1}

Along with the line :math:`y = 3` we get,

.. figure:: Images/Limits/LimAtInf003.png
    :alt: y = (3x^2+2x-1)/(x^2+x+1) and horizontal asymptote.

    :math:`f(x) = \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1}` and horizontal asymptote.

Notice how the two lines get close to each other at the two ends.  This is really what an asymptote means, a function that another function gets arbitrarily close to. Hence the line :math:`y = 3` is the horizontal asymptote to our function.

If we graph,

.. math::
    f(x) = 1 + \frac{\cos{\left(x \right)}}{x}

Along with the line :math:`y = 1` we get,

.. figure:: Images/Limits/LimAtInf004.png
    :alt: 1 + cos(x)/x and horizontal asymptote.

    :math:`f(x) = 1 + \frac{\cos{\left(x \right)}}{x}` and horizontal asymptote.

Hence the line :math:`y = 1` is the horizontal asymptote to our function.

On the other hand, if we graph

.. math::
    f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}

.. figure:: Images/Limits/LimAtInf005.png
    :alt: y = (x^3+7x^2-1)/(x^2+x+1)

    :math:`f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}`

It does not look like the function is leveling out at the ends, and it is not.  So we would say that,

.. math::
    \lim_{x \to \infty} \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1} \quad DNE \quad {\rm and } \quad \lim_{x \to -\infty} \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1} \quad DNE

and consequently the function does not have a horizontal asymptote.  In the next section we will investigate this more closely but from the graph it appears we can go a little further and say,

.. math::
    \lim_{x \to \infty} \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1} = \infty \quad {\rm and } \quad \lim_{x \to -\infty} \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1} = -\infty

Although this function does not have a horizontal asymptote, that does not mean that it does not heva an asymptote.  If do long division on the function we get,

.. math::
    f(x) = x + 6 - \frac{7 x + 7}{x^{2} + x + 1}

If we remove the fraction at the end and plot :math:`y = x+6` along with the original function we get,

.. figure:: Images/Limits/LimAtInf006.png
    :alt: y = (x^3+7x^2-1)/(x^2+x+1) with slant asymptote.

    :math:`f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}` with slant asymptote.

Clearly these two curves are getting close to each other as *x* gets arbitrarily large.  So the line :math:`y = x+6` is an asymptote to our function.  These are called :index:`slanted asymptotes` or :index:`oblique asymptotes`.  This can be generalized further and we will in subsequent sections.  Another visualization we can make about this slanted asymptote is if we graph the difference between the two functions,

.. math::
    \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1} - (x+6)

we get,

.. figure:: Images/Limits/LimAtInf007.png
    :alt: Function minus its slant asymptote.

    :math:`\frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1} - (x+6)`

Since this function has a horizontal asymptote at :math:`y = 0` our original function has  :math:`y = x+6` as its slanted asymptote.


Example: :math:`f(x) = \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1}`
---------------------------------------------------------------

GeoGebra
^^^^^^^^

To graph the function you can use the following syntax,

.. code-block:: console

    (3 x^2+2 x-1)/(x^2+x+1)

.. figure:: Images/Limits/LimAtInf002.png
    :alt: y = (3 x^2+2 x-1)/(x^2+x+1)

    :math:`f(x) = \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1}`

Using the spreadsheet tool and methods from the previous sections we could produce the same numerical attack, we will not do that here.  We can also attack this algebraically, GeoGebra can do infinite limits.  Select a new cell and type in ``limit`` select the limit option, put in ``f`` as your function and ``inf`` as the point (``inf`` in GeoGebra is :math:`\infty`) the result will be 3.  Do the same in the next cell except use ``-inf`` as the limit point and again the result is 3.  This algebraically confirms our conclusions.

.. math::

    \lim_{x \to \infty} \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1} = 3 \quad {\rm and} \quad \lim_{x \to -\infty} \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1} = 3

CLAE
^^^^

To graph the function you can use the following syntax,

.. code-block:: console

    (3*x^2+2*x-1)/(x^2+x+1)

.. figure:: Images/Limits/LimAtInf008.png
    :alt: y = (3 x^2+2 x-1)/(x^2+x+1)

    :math:`f(x) = \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1}`

Using the spreadsheet tool and methods from the previous sections we could produce the same numerical attack, we will not do that here.  We can also attack this algebraically, CLAE can do infinite limits.  Select the function in the CAS, then select ``Calculus > Limit``, variable is ``x`` and the limit point id ``oo`` (two small o's represent :math:`\infty` in CLAE). The direction does not need to be changed, the infinity overrides the direction selection.  The result will be 3.  Do the same again but this time use ``-oo`` for :math:`-\infty` and again we get the result of 3.  This algebraically confirms our conclusions.

.. math::

    \lim_{x \to \infty} \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1} = 3 \quad {\rm and} \quad \lim_{x \to -\infty} \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1} = 3


Maxima
^^^^^^

To graph the function you can use the following syntax,

.. code-block:: console

    kill(all)

.. code-block:: console

    f(x):=(3*x^2+2*x-1)/(x^2+x+1)

.. code-block:: console

    wxplot2d([f(x)], [x,-50,50], [y,-5,5])

.. figure:: Images/Limits/LimAtInf009.png
    :alt: y = (3 x^2+2 x-1)/(x^2+x+1)

    :math:`f(x) = \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1}`

For an algebraic approach run the following commands,

.. code-block:: console

    limit(f(x),x,inf)

and

.. code-block:: console

    limit(f(x),x,-inf)

or

.. code-block:: console

    limit(f(x),x,minf)

Each of these commands will return 3, algebraically confirms our conclusions.

.. math::

    \lim_{x \to \infty} \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1} = 3 \quad {\rm and} \quad \lim_{x \to -\infty} \frac{3 x^{2} + 2 x - 1}{x^{2} + x + 1} = 3


Example: :math:`f(x) = 1 + \frac{\cos{\left(x \right)}}{x}`
-----------------------------------------------------------

GeoGebra
^^^^^^^^

To graph the function you can use the following syntax,

.. code-block:: console

    cos(x)/x+1

.. figure:: Images/Limits/LimAtInf001.png
    :alt: y = 1+cos(x)/x

    :math:`f(x) = 1 + \frac{\cos{\left(x \right)}}{x}`

Use the algebraic methods in the first example to algebraically calculate the limits at infinity. All of our methods lead us to the conclusions,

.. math::

    \lim_{x \to \infty} 1 + \frac{\cos{\left(x \right)}}{x} = 1 \quad {\rm and} \quad \lim_{x \to -\infty} 1 + \frac{\cos{\left(x \right)}}{x} = 1


CLAE
^^^^

To graph the function you can use the following syntax,

.. code-block:: console

    cos(x)/x+1

.. figure:: Images/Limits/LimAtInf010.png
    :alt: y = 1+cos(x)/x

    :math:`f(x) = 1 + \frac{\cos{\left(x \right)}}{x}`

Use the algebraic methods in the first example to algebraically calculate the limits at infinity. All of our methods lead us to the conclusions,

.. math::

    \lim_{x \to \infty} 1 + \frac{\cos{\left(x \right)}}{x} = 1 \quad {\rm and} \quad \lim_{x \to -\infty} 1 + \frac{\cos{\left(x \right)}}{x} = 1


Maxima
^^^^^^

To graph the function you can use the following syntax,

.. code-block:: console

    kill(all)

.. code-block:: console

    f(x):=cos(x)/x+1

.. code-block:: console

    wxplot2d([f(x)], [x,-50,50], [y,-1,2])

.. figure:: Images/Limits/LimAtInf011.png
    :alt: y = 1+cos(x)/x

    :math:`f(x) = 1 + \frac{\cos{\left(x \right)}}{x}`

Use the algebraic methods in the first example to algebraically calculate the limits at infinity. All of our methods lead us to the conclusions,

.. math::

    \lim_{x \to \infty} 1 + \frac{\cos{\left(x \right)}}{x} = 1 \quad {\rm and} \quad \lim_{x \to -\infty} 1 + \frac{\cos{\left(x \right)}}{x} = 1


Example: :math:`f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}`
-----------------------------------------------------------------

GeoGebra
^^^^^^^^

To graph the function you can use the following syntax,

.. code-block:: console

    (x^3+7 x^2-1)/(x^2+x+1)

.. figure:: Images/Limits/LimAtInf012.png
    :alt: y = (x^3+7 x^2-1)/(x^2+x+1)

    :math:`f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}`

Use the algebraic methods in the first example to algebraically calculate the limits at infinity. All of our methods lead us to the conclusions that both infinite limits do not exist.

From the discussion above about this function we know that there is a slanted asymptote :math:`y = x+6` to this function.  We determined that by doing long division on the expression,

.. math::
    f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}

resulting in

.. math::
    f(x) = x + 6 - \frac{7 x + 7}{x^{2} + x + 1}

In GeoGebra we can do this calculation with the partial fractions function.  Start typing in ``partialfractions`` select the ``PartialFractions`` from the popup menu, and input ``f`` as the function and you will get the above result.  Note that the PartialFractions function does more than just long division but that is part of it.  Now to graph the asymptote just type in ``x+6`` into a new cell or select ``Duplicate Output`` from the cell's menu and then remove the fractional portion in the new cell.  Either way you will get.

.. figure:: Images/Limits/LimAtInf013.png
    :alt: y = (x^3+7 x^2-1)/(x^2+x+1) with slant asymptote.

    :math:`f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}` with slant asymptote.


CLAE
^^^^

To graph the function you can use the following syntax,

.. code-block:: console

    (x^3+7*x^2-1)/(x^2+x+1)

.. figure:: Images/Limits/LimAtInf014.png
    :alt: y = (x^3+7 x^2-1)/(x^2+x+1)

    :math:`f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}`

Use the algebraic methods in the first example to algebraically calculate the limits at infinity. All of our methods lead us to the conclusions that both infinite limits do not exist.

From the discussion above about this function we know that there is a slanted asymptote :math:`y = x+6` to this function.  We determined that by doing long division on the expression,

.. math::
    f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}

resulting in

.. math::
    f(x) = x + 6 - \frac{7 x + 7}{x^{2} + x + 1}

In CLAE we can do this calculation with the partial fractions function.  Select the function in the CAS, then select ``Algebra > Partial Fractions``, the variable should be *x* and the selector can remain as Rational Numbers. The result will be,

.. math::
    x - \frac{7 x + 7}{x^{2} + x + 1} + 6

Note that the Partial Fractions function does more than just long division but that is part of it.  Now to graph the asymptote just type in ``x+6`` into the CAS input bar or double-click the partial fractioned expression to copy it to the CAS input bar and remove the fractional portion. Either way you will get.

.. figure:: Images/Limits/LimAtInf015.png
    :alt: y = (x^3+7 x^2-1)/(x^2+x+1) with slant asymptote.

    :math:`f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}` with slant asymptote.


Maxima
^^^^^^

To graph the function you can use the following syntax,

.. code-block:: console

    kill(all)

.. code-block:: console

    f(x):=(x^3+7*x^2-1)/(x^2+x+1)

.. code-block:: console

    wxplot2d([f(x)], [x,-20,20], [y,-20,20])

.. figure:: Images/Limits/LimAtInf016.png
    :alt: y = (x^3+7 x^2-1)/(x^2+x+1)

    :math:`f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}`

Use the algebraic methods in the first example to algebraically calculate the limits at infinity. All of our methods lead us to the conclusions that both infinite limits do not exist.

From the discussion above about this function we know that there is a slanted asymptote :math:`y = x+6` to this function.  We determined that by doing long division on the expression,

.. math::
    f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}

resulting in

.. math::
    f(x) = x + 6 - \frac{7 x + 7}{x^{2} + x + 1}

In Maxima we can do this calculation with the partial fractions function.

.. code-block:: console

    partfrac(f(x),x)

Note that the partfrac function does more than just long division but that is part of it.  You can graph both of these together with the command,

.. code-block:: console

    wxplot2d([f(x), x+6], [x,-20,20], [y,-20,20])

.. figure:: Images/Limits/LimAtInf017.png
    :alt: y = (x^3+7 x^2-1)/(x^2+x+1) with slant asymptote.

    :math:`f(x) = \frac{x^{3} + 7 x^{2} - 1}{x^{2} + x + 1}` with slant asymptote.


Example: :math:`f(x) = \tan^{-1}(x)`
------------------------------------

It is possible to have two different horizontal asymptotes for a function, one to the right and a different one to the left,  :math:`f(x) = \tan^{-1}(x)` is an example of such a function.

GeoGebra
^^^^^^^^

To graph the function you can use the following syntax,

.. code-block:: console

    atan(x)

.. figure:: Images/Limits/LimAtInf018.png
    :alt: y = arctan(x)

    :math:`f(x) = \tan^{-1}(x)`

From the graph it appears that there is a horizontal asymptote to the right at about 1.5 and one to the left at about :math:`-1.5`.  If we use the limit command we get 1.5708 and -1.5708.  The exact values here are :math:`\pi/2` and :math:`-\pi/2`.  GeoGebra will sometimes approximate values.

CLAE
^^^^

To graph the function you can use the following syntax,

.. code-block:: console

    atan(x)

.. figure:: Images/Limits/LimAtInf019.png
    :alt: y = arctan(x)

    :math:`f(x) = \tan^{-1}(x)`

From the graph it appears that there is a horizontal asymptote to the right at about 1.5 and one to the left at about :math:`-1.5`.  If we use the limit command we get the exact values of :math:`\pi/2` and :math:`-\pi/2`.  We can graph these with the curve fairly easily, just put the two values in a list,

.. code-block:: console

    [-pi/2, pi/2]

Then drag them from the CAS to the graph, they should come in as horizontal lines,

.. figure:: Images/Limits/LimAtInf020.png
    :alt: y = arctan(x) with asymptotes.

    :math:`f(x) = \tan^{-1}(x)` with asymptotes.


Maxima
^^^^^^

To graph the function you can use the following syntax,

.. code-block:: console

    kill(all)

.. code-block:: console

    f(x):=atan(x)

.. code-block:: console

    wxplot2d([f(x)], [x,-20,20], [y,-3,3])

.. figure:: Images/Limits/LimAtInf021.png
    :alt: y = arctan(x)

    :math:`f(x) = \tan^{-1}(x)`

From the graph it appears that there is a horizontal asymptote to the right at about 1.5 and one to the left at about :math:`-1.5`.  If we use the limit command we get the exact values of :math:`\pi/2` and :math:`-\pi/2`.  We can graph these with the curve fairly easily, just put the two values into the function list (don't forget the ``%``),

.. code-block:: console

    wxplot2d([f(x), -%pi/2, %pi/2], [x,-20,20], [y,-3,3])

Then drag them from the CAS to the graph, they should come in as horizontal lines,

.. figure:: Images/Limits/LimAtInf022.png
    :alt: y = arctan(x) with asymptotes.

    :math:`f(x) = \tan^{-1}(x)` with asymptotes.
