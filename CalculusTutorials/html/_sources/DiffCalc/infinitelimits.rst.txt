:index:`Infinite Limits`
========================

Discussion & Definitions
------------------------

It is possible that when *x* gets close to *a* the functional values of :math:`f(x)` either increase without bound or decrease without bound.  That is, the graph of the function goes straight up or straight down.  These limits do not exist either but we denote them a little differently to give the reader more information about the behavior of the function close to the value *a*.  These definitions are still intuitive but are sufficient for most casess.

.. admonition:: Definition: Infinite Limits

    - Let :math:`f(x)` be a function defined at all values in an open interval :math:`(c, a)` with :math:`c < a`. If the values of the function :math:`f(x)` *increase without bound* as *x* approaches *a*, with :math:`x < a`, we say that *the limit as x approaches a from the left is positive infinity*.  Symbolically we write,

    .. math::

        \lim_{x \to a^-} f(x) = \infty


    - Let :math:`f(x)` be a function defined at all values in an open interval :math:`(a, c)` with :math:`c > a`. If the values of the function :math:`f(x)` *increase without bound* as *x* approaches *a*, with :math:`x > a`, we say that *the limit as x approaches a from the right is positive infinity*.  Symbolically we write,

    .. math::

        \lim_{x \to a^+} f(x) = \infty


    - Let :math:`f(x)` be a function defined at all values in an open interval :math:`(c, a)` with :math:`c < a`. If the values of the function :math:`f(x)` *decrease without bound* as *x* approaches *a*, with :math:`x < a`, we say that *the limit as x approaches a from the left is negative infinity*.  Symbolically we write,

    .. math::

        \lim_{x \to a^-} f(x) = -\infty


    - Let :math:`f(x)` be a function defined at all values in an open interval :math:`(a, c)` with :math:`c > a`. If the values of the function :math:`f(x)` *decrease without bound* as *x* approaches *a*, with :math:`x > a`, we say that *the limit as x approaches a from the right is negative infinity*.  Symbolically we write,

    .. math::

        \lim_{x \to a^+} f(x) = -\infty


    - Let :math:`f(x)` be a function defined at all values in an open interval containing the number *a*, except for *a* itself. If the values of the function :math:`f(x)` *increase without bound* as *x* approaches *a* from either side, we say that *the limit as x approaches a is positive infinity*.  Symbolically we write,

    .. math::

        \lim_{x \to a} f(x) = \infty

    - Let :math:`f(x)` be a function defined at all values in an open interval containing the number *a*, except for *a* itself. If the values of the function :math:`f(x)` *decrease without bound* as *x* approaches *a* from either side, we say that *the limit as x approaches a is negative infinity*.  Symbolically we write,

    .. math::

        \lim_{x \to a} f(x) = -\infty


Positive infinity (:math:`\infty`) and negative infinity (:math:`-\infty`) are **not** real numbers.  So in all the cases above, the limit does not exist.  We write :math:`\lim_{x \to a} f(x) = \infty` and :math:`\lim_{x \to a} f(x) = -\infty` (instead of DNE) to indicate how the limit does not exist and subsequently give us more information about the behavior of the function.

.. admonition:: Definition: Vertical Asymptote

    Let :math:`f(x)` be a function.  If any of the following conditions hold, then the line :math:`x = a` is a :index:`vertical asymptote` of :math:`f(x)`.

    .. math::
        \lim_{x \to a^+} f(x) = \pm\infty, \quad \lim_{x \to a^-} f(x) = \pm\infty, \quad {\rm or} \quad  \lim_{x \to a} f(x) = \pm\infty

    where :math:`\pm\infty` means either :math:`\infty` or :math:`-\infty`.


Example: :math:`f(x) = \frac{1}{x}`
-----------------------------------

For this example we are interested in what is happening close to :math:`x = 0`.

Numeric Approach
^^^^^^^^^^^^^^^^

If we attack this numerically we can see that the functional values get very large (positively and negatively) as :math:`x \to 0`.

.. math::
    \begin{array}{l|l}
    x & \frac{1}{x} \\ \hline
    1 & 1 \\
    0.1 & 10.0 \\
    0.01 & 100.0 \\
    0.001 & 1000.0 \\
    0.0001 & 10000.0 \\
    1.0 \cdot 10^{-5} & 100000.0 \\
    1.0 \cdot 10^{-6} & 1000000.0 \\
    1.0 \cdot 10^{-7} & 10000000.0 \\
    1.0 \cdot 10^{-8} & 100000000.0 \\
    1.0 \cdot 10^{-9} & 1000000000.0 \\
    \end{array}

.. math::
    \begin{array}{l|l}
    x & \frac{1}{x} \\ \hline
    -1 & -1 \\
    -0.1 & -10.0 \\
    -0.01 & -100.0 \\
    -0.001 & -1000.0 \\
    -0.0001 & -10000.0 \\
    -1.0 \cdot 10^{-5} & -100000.0 \\
    -1.0 \cdot 10^{-6} & -1000000.0 \\
    -1.0 \cdot 10^{-7} & -10000000.0 \\
    -1.0 \cdot 10^{-8} & -100000000.0 \\
    -1.0 \cdot 10^{-9} & -1000000000.0 \\
    \end{array}

From the definitions above we would say,

.. math::
    \lim_{x \to 0^+} \frac{1}{x} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x} = -\infty

Since the one-sided limits are "going to" different infinities we cannot use this notation for the two-sided limit, all we can write here is,

.. math::
    \lim_{x \to 0} \frac{1}{x} \quad DNE

We would also say that :math:`f(x) = \frac{1}{x}` has a vertical asymptote :math:`x = 0`, or that :math:`f(x) = \frac{1}{x}` has a vertical asymptote at :math:`x = 0`.


Graphical Approach
^^^^^^^^^^^^^^^^^^

Graphing the function :math:`f(x) = \frac{1}{x}` shows the same behavior as we saw with the numeric approach.  As we approach 0 from the right the corresponding functional values get larger and larger, and as we approach 0 from the left the corresponding functional values get larger and larger negatively.

.. figure:: Images/Limits/Inf001.png
    :alt: y = 1/x

    :math:`f(x) = \frac{1}{x}`

This gives us the same conclusions,

.. math::
    \lim_{x \to 0^+} \frac{1}{x} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x} = -\infty

Since the one-sided limits are "going to" different infinities we cannot use this notation for the two-sided limit, all we can write here is,

.. math::
    \lim_{x \to 0} \frac{1}{x} \quad DNE

We would also say that :math:`f(x) = \frac{1}{x}` has a vertical asymptote :math:`x = 0`, or that :math:`f(x) = \frac{1}{x}` has a vertical asymptote at :math:`x = 0`.


GeoGebra
^^^^^^^^

Numerical Approach
""""""""""""""""""

#. Input the function, syntax is below, this should come into GeoGebra as ``f(x)``

    .. code-block:: console

        1/x

#. Open the spreadsheet tool, ``Main Menu > View > Spreadsheet``.

#. Input the *x* values in the *A* column.

#. In the ``B1`` cell input ``f(A1)``.  This will substitute the ``A1`` value into the function and evaluate it.

#. Select ``B1``, copy it either with a right click and the popup menu or keyboard shortcut.

#. Select ``B2`` down to the last row of *x* values.

#. Paste either with a right click and the popup menu or keyboard shortcut.  This will evaluate the function at each of the values in column ``A``.

.. figure:: Images/Limits/Inf002.png
    :alt: y = 1/x

    :math:`f(x) = \frac{1}{x}`

From the values we come to the conclusions,

.. math::
    \lim_{x \to 0^+} \frac{1}{x} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x} = -\infty

Since the one-sided limits are "going to" different infinities we cannot use this notation for the two-sided limit, all we can write here is,

.. math::
    \lim_{x \to 0} \frac{1}{x} \quad DNE

We would also say that :math:`f(x) = \frac{1}{x}` has a vertical asymptote :math:`x = 0`, or that :math:`f(x) = \frac{1}{x}` has a vertical asymptote at :math:`x = 0`.

Graphical Approach
""""""""""""""""""

#. Input the function, syntax is below, this should come into GeoGebra as ``f(x)``

    .. code-block:: console

        1/x

#. GeoGebra will automatically graph the function.

#. Using the Shift-Click and Drag on the axes and repositioning, zoom to a view that still contains :math:`x = 0` and is nicely readable.

.. figure:: Images/Limits/Inf001.png
    :alt: y = 1/x

    :math:`f(x) = \frac{1}{x}`

From the graph we come to the same conclusions,

.. math::
    \lim_{x \to 0^+} \frac{1}{x} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x} = -\infty

Since the one-sided limits are "going to" different infinities we cannot use this notation for the two-sided limit, all we can write here is,

.. math::
    \lim_{x \to 0} \frac{1}{x} \quad DNE

We would also say that :math:`f(x) = \frac{1}{x}` has a vertical asymptote :math:`x = 0`, or that :math:`f(x) = \frac{1}{x}` has a vertical asymptote at :math:`x = 0`.


Algebraic Approach
""""""""""""""""""

Although we have not yet discussed limit laws and methods we can let the software do that work for us.  GeoGebra has a built in computer algebra system that does exact mathematics.

#. Input the function, syntax is below, this should come into GeoGebra as ``f(x)``

    .. code-block:: console

        1/x

#. In the next input cell start typing ``limit``, after three characters or so an autocompletion menu will appear with ``LimitBelow`` as one of the options, select it, the parameters for this function are a function and a value, input ``f`` for the function, hit tab, then input 0 for the value.  The cell will display the limit command and the value of :math:`-\infty`.  Hence,

#. In the next input cell start typing ``limit``, after three characters or so an autocompletion menu will appear with ``LimitAbove`` as one of the options, select it, the parameters for this function are a function and a value, input ``f`` for the function, hit tab, then input 0 for the value.  The cell will display the limit command and the value of :math:`\infty`.  Hence,

.. math::
    \lim_{x \to 0^+} \frac{1}{x} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x} = -\infty

and

.. math::
    \lim_{x \to 0} \frac{1}{x} \quad DNE


CLAE
^^^^

Numerical Approach
""""""""""""""""""

#. Input the function, syntax is below, you can copy this and paste it into the CAS input bar with a right click popup menu or keyboard shortcut.  Note that CLAE does not automatically assign function names to inputs.

    .. code-block:: console

        f(x):=1/x

#. Click the Spreadsheet tab.

#. Input the *x* values in the *A* column.

#. In the ``B1`` cell input ``f(A1)``.  This will substitute ``A1`` into the function and evaluate it.

#. Select ``B1``, copy its formula with ``Edit > Copy Formulas`` or the corresponding toolbar button.

#. Select ``B2`` down to the last row of *x* values.

#. Paste with either ``Edit > Paste`` or the corresponding toolbar button.

.. figure:: Images/Limits/Inf003.png
    :alt: y = 1/x

    :math:`f(x) = \frac{1}{x}`

From the graph we come to the conclusions,

.. math::
    \lim_{x \to 0^+} \frac{1}{x} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x} = -\infty

and

.. math::
    \lim_{x \to 0} \frac{1}{x} \quad DNE

So there is a vertical asymptote to :math:`f(x) = \frac{1}{x}` at :math:`x = 0`.

Graphical Approach
""""""""""""""""""

#. Input the function, syntax is below, you can copy this and paste it into the CAS input bar with a right click popup menu or keyboard shortcut.  Note that CLAE does not automatically assign function names to inputs.

    .. code-block:: console

        f(x):=1/x

#. Click the 2-D Graphs tab.

#. Click and drag the expression from the CAS workspace to the graph, or graphics manager.  This will plot the function.  Use the right-click and drag on the axes and repositioning, zoom to a view that still contains :math:`x = 0` and is nicely readable.

.. figure:: Images/Limits/Inf004.png
    :alt: y = 1/x

    :math:`f(x) = \frac{1}{x}`

From the graph we come to the same conclusions,

.. math::
    \lim_{x \to 0^+} \frac{1}{x} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x} = -\infty

and

.. math::
    \lim_{x \to 0} \frac{1}{x} \quad DNE

So there is a vertical asymptote to :math:`f(x) = \frac{1}{x}` at :math:`x = 0`.


Algebraic Approach
""""""""""""""""""

Although we have not yet discussed limit laws and methods we can let the software do that work for us.  CLAE has a built in computer algebra system that does exact mathematics.

#. Input the function, syntax is below. Note we do not need the ``f(x)`` here but it will work equally well if we include it.

    .. code-block:: console

        1/x

#. Select the expression and then select ``Calculus > Limit``, a dialog box will appear, here are the settings.
    - Variable: ``x``.
    - Limit Point: 0.
    - Direction: Left
    - Leave the variable properties as they are.
    - Select OK

#. The CAS workspace will show the limit in the description and :math:`-\infty` as the value.

#. Select the expression and then select ``Calculus > Limit``, a dialog box will appear, here are the settings.
    - Variable: ``x``.
    - Limit Point: 0.
    - Direction: Right
    - Leave the variable properties as they are.
    - Select OK

#. The CAS workspace will show the limit in the description and :math:`\infty` as the value.

Hence we would conclude,

.. math::
    \lim_{x \to 0^+} \frac{1}{x} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x} = -\infty

and

.. math::
    \lim_{x \to 0} \frac{1}{x} \quad DNE

So there is a vertical asymptote to :math:`f(x) = \frac{1}{x}` at :math:`x = 0`.


Maxima
^^^^^^

Numerical Approach
""""""""""""""""""

Creating tables in Maxima is not the easiest thing to do and requires a little programming.  You can simply evaluate the function at each *x* value one at a time to obtain the same information or try using a Maxima for loop.

#. Clear any variable names you are using.

    .. code-block:: console

        kill(f,x)

#. Input the function, syntax is below,

    .. code-block:: console

        f(x):=1/x

#. Now either evaluate ``f(0.1)``, ``f(0.01)``, ``f(0.001)``, and so on or do the following loop.

    .. code-block:: maxima

        (print("x", "f"),
        for i:1 thru 10 do
        (x: 1.0/(10^i),
        L: f(x)*1.0,
        print(x,L))
        );

    .. code-block:: maxima

        x f
        0.1 10.0
        0.01 100.0
        0.001 1000.0
        1.0*10^-4 10000.0
        1.0*10^-5 100000.0
        9.999999999999999*10^-7 1000000.0
        1.0*10^-7 10000000.0
        1.0*10^-8 1.0*10^8
        1.0*10^-9 9.999999999999999*10^8
        1.0*10^-10 1.0*10^10

#. Now either evaluate ``f(-0.1)``, ``f(-0.01)``, ``f(-0.001)``, and so on or do the following loop.

    .. code-block:: maxima

        (print("x", "f"),
        for i:1 thru 10 do
        (x: -1.0/(10^i),
        L: f(x)*1.0,
        print(x,L))
        );

    .. code-block:: maxima

        x f
        -0.1 -10.0
        -0.01 -100.0
        -0.001 -1000.0
        -1.0*10^-4 -10000.0
        -1.0*10^-5 -100000.0
        -9.999999999999999*10^-7 -1000000.0
        -1.0*10^-7 -10000000.0
        -1.0*10^-8 -1.0*10^8
        -1.0*10^-9 -9.999999999999999*10^8
        -1.0*10^-10 -1.0*10^10

Hence we would conclude,

.. math::
    \lim_{x \to 0^+} \frac{1}{x} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x} = -\infty

and

.. math::
    \lim_{x \to 0} \frac{1}{x} \quad DNE

So there is a vertical asymptote to :math:`f(x) = \frac{1}{x}` at :math:`x = 0`.


Graphical Approach
""""""""""""""""""

#. Clear any variable names you are using.

    .. code-block:: console

        kill(f,x)

#. Input the function, syntax is below,

    .. code-block:: console

        f(x):=1/x

#. Select ``Plot > Plot 2D``, a dialog box will appear, here are the settings.
    - Expression: ``f(x)``.
    - Variable: ``x`` from :math:`-5` to 5.
    - Variable: ``y`` from :math:`-5` to 5.
    - Leave the rest of the options as they are.
    - Select OK

.. figure:: Images/Limits/Inf006.png
    :alt: y = 1/x

    :math:`f(x) = \frac{1}{x}`

Hence we would conclude,

.. math::
    \lim_{x \to 0^+} \frac{1}{x} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x} = -\infty

and

.. math::
    \lim_{x \to 0} \frac{1}{x} \quad DNE

So there is a vertical asymptote to :math:`f(x) = \frac{1}{x}` at :math:`x = 0`.

.. note::

    If we did not specify a ``y`` range Maxima would select on for us, giving us the following image.  Although it is still good enough to make our conclusions specifying the ``y`` range gives a much better plot.

    .. figure:: Images/Limits/Inf005.png
        :alt: y = 1/x

        :math:`f(x) = \frac{1}{x}`



Algebraic Approach
""""""""""""""""""

#. Clear any variable names you are using.

    .. code-block:: console

        kill(f,x)

#. Input the function, syntax is below,

    .. code-block:: console

        f(x):=1/x

#. Select ``Calculus > Find Limit``, a dialog box will appear, here are the settings.
    - Expression: ``f(x)``.
    - Variable: ``x``
    - Point: 0.
    - Direction: left
    - Leave the rest of the options as they are.
    - Select OK

#. The result will be :math:`-\infty`.

#. Select ``Calculus > Find Limit``, a dialog box will appear, here are the settings.
    - Expression: ``f(x)``.
    - Variable: ``x``
    - Point: 0.
    - Direction: right
    - Leave the rest of the options as they are.
    - Select OK

#. The result will be :math:`\infty`.

Hence we would conclude,

.. math::
    \lim_{x \to 0^+} \frac{1}{x} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x} = -\infty

and

.. math::
    \lim_{x \to 0} \frac{1}{x} \quad DNE

So there is a vertical asymptote to :math:`f(x) = \frac{1}{x}` at :math:`x = 0`.


Example: :math:`f(x) = \frac{1}{x^2}`
-------------------------------------

For this example we are interested in what is happening close to :math:`x = 0`.

Numerical Approach
^^^^^^^^^^^^^^^^^^

.. math::

    \begin{array}{l|l}
    x & \frac{1}{x^2} \\ \hline
    1 & 1 \\
    0.1 & 100.0 \\
    0.01 & 10000.0 \\
    0.001 & 1000000.0 \\
    0.0001 & 100000000.0 \\
    1.0 \cdot 10^{-5} & 10000000000.0 \\
    1.0 \cdot 10^{-6} & 1000000000000.0 \\
    1.0 \cdot 10^{-7} & 100000000000000.0 \\
    1.0 \cdot 10^{-8} & 1.0 \cdot 10^{16} \\
    1.0 \cdot 10^{-9} & 1.0 \cdot 10^{18} \\
    \end{array}

.. math::

    \begin{array}{l|l}
    x & \frac{1}{x^2} \\ \hline
    -1 & 1 \\
    -0.1 & 100.0 \\
    -0.01 & 10000.0 \\
    -0.001 & 1000000.0 \\
    -0.0001 & 100000000.0 \\
    -1.0 \cdot 10^{-5} & 10000000000.0 \\
    -1.0 \cdot 10^{-6} & 1000000000000.0 \\
    -1.0 \cdot 10^{-7} & 100000000000000.0 \\
    -1.0 \cdot 10^{-8} & 1.0 \cdot 10^{16} \\
    -1.0 \cdot 10^{-9} & 1.0 \cdot 10^{18} \\
    \end{array}

Hence we would conclude,

.. math::
    \lim_{x \to 0^+} \frac{1}{x^2} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x^2} = \infty

and hence we can write,

.. math::
    \lim_{x \to 0} \frac{1}{x^2} = \infty

So there is a vertical asymptote to :math:`f(x) = \frac{1}{x^2}` at :math:`x = 0`.

Graphical Approach
^^^^^^^^^^^^^^^^^^

Plotting the function gives us the following image,

.. figure:: Images/Limits/Inf007.png
    :alt: y = 1/x^2

    :math:`f(x) = \frac{1}{x^2}`

From the image it appears that as the *x* values get closer to 0 from either side the corresponding *y* values are increasing without bound.  This would lead us to the same conclusion,

.. math::
    \lim_{x \to 0^+} \frac{1}{x^2} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x^2} = \infty

and hence we can write,

.. math::
    \lim_{x \to 0} \frac{1}{x^2} = \infty

So there is a vertical asymptote to :math:`f(x) = \frac{1}{x^2}` at :math:`x = 0`.


GeoGebra
^^^^^^^^

#. Input the function,

    .. code-block:: console

        1/x^2

#. Follow the process outlined in the first example to determine the one-sided limits of this function as :math:`x \to 0^-` and :math:`x \to 0^+`.  The spreadsheet should produce values close to the tables above, the image should look like the following, and the above and below limit commands should both produce :math:`\infty`.  In fact, we can ask GeoGebra for the two-sided limit of this function as :math:`x \to 0`, it too will result in :math:`\infty`.

.. figure:: Images/Limits/Inf007.png
    :alt: y = 1/x^2

    :math:`f(x) = \frac{1}{x^2}`

Each method should give us the conclusion,

.. math::
    \lim_{x \to 0^+} \frac{1}{x^2} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x^2} = \infty

and hence we can write,

.. math::
    \lim_{x \to 0} \frac{1}{x^2} = \infty

So there is a vertical asymptote to :math:`f(x) = \frac{1}{x^2}` at :math:`x = 0`.


CLAE
^^^^

#. Input the function,

    .. code-block:: console

        f(x):=1/x^2

#. Follow the process outlined in the first example to determine the one-sided limits of this function as :math:`x \to 0^-` and :math:`x \to 0^+`.  The spreadsheet should produce values close to the tables above, the image should look like the following, and the left and right limit commands should both produce :math:`\infty`.  In fact, we can ask CLAE for the two-sided limit of this function as :math:`x \to 0`, it too will result in :math:`\infty`.

.. figure:: Images/Limits/Inf008.png
    :alt: y = 1/x^2

    :math:`f(x) = \frac{1}{x^2}`

Each method should give us the conclusion,

.. math::
    \lim_{x \to 0^+} \frac{1}{x^2} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x^2} = \infty

and hence we can write,

.. math::
    \lim_{x \to 0} \frac{1}{x^2} = \infty

So there is a vertical asymptote to :math:`f(x) = \frac{1}{x^2}` at :math:`x = 0`.

Maxima
^^^^^^

#. Input the function,

    .. code-block:: console

        f(x):=1/x^2

#. Follow the process outlined in the first example to determine the one-sided limits of this function as :math:`x \to 0^-` and :math:`x \to 0^+`.  The spreadsheet should produce values close to the tables above, the image should look like the following, and the left and right limit commands should both produce :math:`\infty`.  In fact, we can ask Maxima for the two-sided limit of this function as :math:`x \to 0`, it too will result in :math:`\infty`.

.. figure:: Images/Limits/Inf009.png
    :alt: y = 1/x^2

    :math:`f(x) = \frac{1}{x^2}`

Each method should give us the conclusion,

.. math::
    \lim_{x \to 0^+} \frac{1}{x^2} = \infty  \quad {\rm and} \quad  \lim_{x \to 0^-} \frac{1}{x^2} = \infty

and hence we can write,

.. math::
    \lim_{x \to 0} \frac{1}{x^2} = \infty

So there is a vertical asymptote to :math:`f(x) = \frac{1}{x^2}` at :math:`x = 0`.


Example: :math:`f(x) = \frac{1}{x^{2} + 2 x - 3}`
-------------------------------------------------

For this example we will simply look at a graphical approach.  If we plot this function we get,

.. figure:: Images/Limits/Inf010.png
    :alt: y = 1/(x^2+2x-3)

    :math:`f(x) = \frac{1}{x^{2} + 2 x - 3}`

From the image it appears that we have two vertical asymptotes, one at :math:`x = -3` and one at :math:`x = 1`. Also from the graph we can conclude the following,

.. math::
    \lim_{x \to -3^+} \frac{1}{x^{2} + 2 x - 3} = -\infty  \quad {\rm and} \quad  \lim_{x \to -3^-} \frac{1}{x^{2} + 2 x - 3} = \infty

.. math::
    \lim_{x \to 1^+} \frac{1}{x^{2} + 2 x - 3} = \infty  \quad {\rm and} \quad  \lim_{x \to 1^-} \frac{1}{x^{2} + 2 x - 3} = -\infty

GeoGebra
^^^^^^^^

To get this image in GeoGebra the syntax for the function is,

.. code-block:: console

    1/(x^2+2 x-3)

.. figure:: Images/Limits/Inf010.png
    :alt: y = 1/(x^2+2x-3)

    :math:`f(x) = \frac{1}{x^{2} + 2 x - 3}`

CLAE
^^^^

To get this image in CLAE the syntax for the function is,

.. code-block:: console

    1/(x^2 + 2*x - 3)

Note that we do not need the ``f(x):=`` definition since this was just to make the spreadsheet calculations easier.

.. figure:: Images/Limits/Inf011.png
    :alt: y = 1/(x^2+2x-3)

    :math:`f(x) = \frac{1}{x^{2} + 2 x - 3}`

If we select the function in the CAS and then select ``Algebra > Factor`` the result is,

.. math::

    \frac{1}{\left(x - 1\right) \left(x + 3\right)}

Since from this it is clear that the denominator is 0 at :math:`x = -3` and :math:`x = 1` we know something interesting is happening to the function at these points.

.. note::

    Note that in this image the software graphs vertical lines at the two asymptotes.  The asymptotes are not part of the graph only a property of the graph and hence function.

Maxima
^^^^^^

To get this image in Maxima the syntax for the function is,

.. code-block:: console

    f(x):=1/(x^2 + 2*x - 3)

.. figure:: Images/Limits/Inf012.png
    :alt: y = 1/(x^2+2x-3)

    :math:`f(x) = \frac{1}{x^{2} + 2 x - 3}`

We can factor this expression in Maxima as well using the command ``factor(f(x))``, which produces,

.. math::

    \frac{1}{\left(x - 1\right) \left(x + 3\right)}

Since from this it is clear that the denominator is 0 at :math:`x = -3` and :math:`x = 1` we know something interesting is happening to the function at these points.

Example: Einstein’s Equation
----------------------------

Einstein’s equation for the mass of a moving object is

.. math::

    m = \frac{m_0}{\sqrt{1-\frac{v^2}{c^2}}}

where :math:`m_0` is the object's mass at rest, :math:`v` is its speed, and :math:`c` is the speed of light.  From the equation it is clear that as *v* increases the denominator decreases and hence (if :math:`m_0 > 0`) the mass of the object increases.

We will look at the situation of :math:`v \to c^-` graphically and algebraically.

GeoGebra
^^^^^^^^

In GeoGebra the independent variable needs to be *x* and not *v* so we will use the expression,

.. code-block:: console

    m0/sqrt(1-x^2/c^2)

When you paste this into GeoGebra, it automatically creates sliders for m0 and c, with default values of 1.  Although *c* is not 1 it is a constant so for our purposes 1 is fine.  The image is,

.. figure:: Images/Limits/Inf013.png
    :alt: Einstein’s Equation

    Einstein’s Equation

From this we can see that

.. math::

    \lim_{v \to c^-} m = \lim_{v \to c^-} \frac{m_0}{\sqrt{1-\frac{v^2}{c^2}}} = \infty

CLAE
^^^^

In CLAE the syntax for Einstein’s equation is,

.. code-block:: console

    m0/sqrt(1-v^2/c^2)

If we wish to graph this we first need to change the variable *v* to *x*.  This can be done with ``Algebra > Evaluate``, change the Variable to ``v`` and the Expression to ``x`` and hit OK.  This will result in,

.. math::
    \frac{m_{0}}{\sqrt{1 - \frac{x^{2}}{c^{2}}}}

If we plot this CLAE will automatically create sliders for m0 and c, with default values of 1.  Although *c* is not 1 it is a constant so for our purposes 1 is fine.  The image is,

.. figure:: Images/Limits/Inf014.png
    :alt: Einstein’s Equation

    Einstein’s Equation

From this we can see that

.. math::

    \lim_{v \to c^-} m = \lim_{v \to c^-} \frac{m_0}{\sqrt{1-\frac{v^2}{c^2}}} = \infty

We can also attack this algebraically in CLAE.  Select the first input

.. math::
    \frac{m_{0}}{\sqrt{1 - \frac{v^{2}}{c^{2}}}}

Then ``Calculus > Limit``, use the variable *v*, limit point *c*, and a direction of Left. The result will be,

.. math::
    \infty \operatorname{sign}{\left(\frac{m_{0}}{\sqrt{\frac{1}{c}}} \right)}

The sign function is simply a function that is 1 if the argument is positive, :math:`-1` if the argument is negative, and 0 if the argument is 0. So the result depends on the values of :math:`m_0` and :math:`c`.  The computer algebra system in CLAE does not make any assumptions about the variables unless we tell it to.  Since we know that both :math:`m_0` and :math:`c` are positive it is clear that this sign function is 1 and the result is :math:`\infty`.  We could have told CLAE this in the limit calculation by doing the following.

Select the first input

.. math::
    \frac{m_{0}}{\sqrt{1 - \frac{v^{2}}{c^{2}}}}

Then ``Calculus > Limit``, use the variable *v*, limit point *c*, and a direction of Left. Before we click OK, click on the button at the bottom, ``Edit Variable Properties``.  Another dialog box will appear with a list of variables on the left and a bunch of selections on the right.  Click *c* and then select Positive, then select m0 and again select Positive.  Click OK and the dialog will close taking you back to the first one and the types for *c* and *m0* have changed.  Now click OK and the CAS will display a result of :math:`\infty`.

Maxima
^^^^^^

In Maxima the syntax for Einstein’s equation is,

.. code-block:: console

    f(v):=m0/sqrt(1 - v^2/c^2)

Since *m0* and *c* are constants and Maxima does not create sliders for constants in graphs, like GeoGebra and CLAE, we cannot graph this unless we substitute values for *m0* and *c*.  So if we let :math:`m_0 = 1` and :math:`c = 4` we get,

.. code-block:: console

    f(v):=1/sqrt(1 - v^2/4^2)

which we can graph.  When you do make sure that the independent variable is *v*, let *v* go from 0 to 7 and *y* from 0 to 10.

.. figure:: Images/Limits/Inf015.png
    :alt: Einstein’s Equation

    Einstein’s Equation

Showing the infinite limit.

.. math::

    \lim_{v \to c^-} m = \lim_{v \to c^-} \frac{m_0}{\sqrt{1-\frac{v^2}{c^2}}} = \infty


Example: :math:`f(x) = \ln(x)`
------------------------------

Thus far, all the vertical asymptotes were when the denominator of a function was 0.  While this is frequent we can asymptotes to functions that are not fractions ot rational expressions.  Furthermore we can have rational expressions where the denominator is 0 and not have a vertical asymptote there.  For the first situation consider the function, :math:`f(x) = \ln(x)`.  Again, we will concentrate on this graphically.

GeoGebra
^^^^^^^^

To graph this in GeoGebra we use the syntax,

.. code-block:: console

    ln(x)

which gives the image,

.. figure:: Images/Limits/Inf016.png
    :alt: y = ln(x)

    :math:`f(x) = \ln(x)`

From the graph it appears that,

.. math::
    \lim_{x \to 0^+} \ln(x) = -\infty

and hence there is a vertical asymptote at :math:`x = 0`.

CLAE
^^^^

To graph this in CLAE we can use the syntax,

.. code-block:: console

    ln(x)

or

.. code-block:: console

    log(x)

In CLAE and several other computer algebra systems ``log(x)`` represents ``ln(x)``.  Also note that the CAS workspace displays ``log(x)``.  We get the image,

.. figure:: Images/Limits/Inf017.png
    :alt: y = ln(x)

    :math:`f(x) = \ln(x)`

From the graph it appears that,

.. math::
    \lim_{x \to 0^+} \ln(x) = -\infty

and hence there is a vertical asymptote at :math:`x = 0`.


Maxima
^^^^^^

To graph this in CLAE we can use the syntax,

.. code-block:: console

    log(x)

In Maxima and several other computer algebra systems ``log(x)`` represents ``ln(x)``.  We get the image,

.. figure:: Images/Limits/Inf018.png
    :alt: y = ln(x)

    :math:`f(x) = \ln(x)`

From the graph it appears that,

.. math::
    \lim_{x \to 0^+} \ln(x) = -\infty

and hence there is a vertical asymptote at :math:`x = 0`.


Example: :math:`f(x) = \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3}`
---------------------------------------------------------------

We can have rational expressions where the denominator is 0 and not have a vertical asymptote there.  Again, we will concentrate on this graphically.  We will examine the function,

.. math::
    f(x) = \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3}

GeoGebra
^^^^^^^^

To graph this in GeoGebra we use the syntax,

.. code-block:: console

    (x^2 + 2 x + 1)/(x^2 - 2 x - 3)

which gives the image,

.. figure:: Images/Limits/Inf019.png
    :alt: (x^2+2x+1)/(x^2-2x-3)

    :math:`f(x) = \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3}`

From the graph it appears that,

.. math::
    \lim_{x \to 3^+} \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3} = \infty  \quad {\rm and} \quad \lim_{x \to 3^-} \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3} = -\infty

and hence there is a vertical asymptote at :math:`x = 3`.  It also appears that there are no other vertical asymptotes, and there are not.  It is easy to see that the denominator :math:`x^{2} - 2 x - 3 = \left(x - 3\right) \left(x + 1\right)` and hence is zero at :math:`x = 3` and :math:`x = -1` but there is no vertical asymptote at :math:`x = -1`.

Although we can factor this denominator in our heads, if we could not here is how you can use GeoGebra to do so.  Select a new cell, run the command ``Denominator(f)``, this will extract the denominator and plot it, you should see the following.  GeoGebra will also give the denominator a function name, say it was g(x).  Now select a new cell and run the command ``Factor(g)`` and it will be factored into :math:`\left(x - 3\right) \left(x + 1\right)`.

.. figure:: Images/Limits/Inf020.png
    :alt: (x^2+2x+1)/(x^2-2x-3) and x^2-2x-3

    :math:`f(x) = \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3}` and :math:`y = x^{2} - 2 x - 3`

The reason that :math:`x = -1` is not an asymptote is because there is no infinite limit at :math:`x = -1`, which is caused by the numerator also having :math:`x = -1` as a root.  If we select a new cell and run ``Simplify(f)`` we get,

.. math::
    \frac{x + 1}{x - 3}

which does not have a root of :math:`x = -1` in the denominator.

.. note::

    The original function

    .. math::
        f(x) = \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3}

    and its simplification

    .. math::
        g(x) = \frac{x + 1}{x - 3}

    are not equal.  For two functions to be equal they must be equal at all values of the variable.  These two are except at :math:`x = -1` since :math:`g(-1) = 0` and  :math:`f(-1)` is undefined.  In reality there is a hole in the graph of :math:`f(x)` at :math:`x = -1`, like,

    .. figure:: Images/Limits/Inf021.png
        :alt: (x^2+2x+1)/(x^2-2x-3)

        :math:`f(x) = \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3}`

CLAE
^^^^

To graph this in CLAE we use the syntax,

.. code-block:: console

    (x^2 + 2*x + 1)/(x^2 - 2*x - 3)

which gives the image,

.. figure:: Images/Limits/Inf022.png
    :alt: (x^2+2x+1)/(x^2-2x-3)

    :math:`f(x) = \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3}`

From the graph it appears that,

.. math::
    \lim_{x \to 3^+} \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3} = \infty  \quad {\rm and} \quad \lim_{x \to 3^-} \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3} = -\infty

and hence there is a vertical asymptote at :math:`x = 3`.  It also appears that there are no other vertical asymptotes, and there are not.  It is easy to see that the denominator :math:`x^{2} - 2 x - 3 = \left(x - 3\right) \left(x + 1\right)` and hence is zero at :math:`x = 3` and :math:`x = -1` but there is no vertical asymptote at :math:`x = -1`.

Although we can factor this denominator in our heads, if we could not here is how you can use CLAE to do so.  Select the expression and then select ``Algebra > Rational Expressions > Denominator``, this will extract the denominator, now with the denominator  selected select, ``Algebra > Factor``, the result will be :math:`\left(x - 3\right) \left(x + 1\right)`.

The reason that :math:`x = -1` is not an asymptote is because there is no infinite limit at :math:`x = -1`, which is caused by the numerator also having :math:`x = -1` as a root.  If we select the original expression and then ``Algebra > Simplify``, we get,

.. math::
    \frac{x + 1}{x - 3}

which does not have a root of :math:`x = -1` in the denominator.

.. note::

    The original function

    .. math::
        f(x) = \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3}

    and its simplification

    .. math::
        g(x) = \frac{x + 1}{x - 3}

    are not equal.  For two functions to be equal they must be equal at all values of the variable.  These two are except at :math:`x = -1` since :math:`g(-1) = 0` and  :math:`f(-1)` is undefined.  In reality there is a hole in the graph of :math:`f(x)` at :math:`x = -1`, like,

    .. figure:: Images/Limits/Inf021.png
        :alt: (x^2+2x+1)/(x^2-2x-3)

        :math:`f(x) = \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3}`


Maxima
^^^^^^

To graph this in Maxima we use the syntax,

.. code-block:: console

    f(x):=(x^2 + 2*x + 1)/(x^2 - 2*x - 3)

which gives the image,

.. figure:: Images/Limits/Inf023.png
    :alt: (x^2+2x+1)/(x^2-2x-3)

    :math:`f(x) = \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3}`

From the graph it appears that,

.. math::
    \lim_{x \to 3^+} \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3} = \infty  \quad {\rm and} \quad \lim_{x \to 3^-} \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3} = -\infty

and hence there is a vertical asymptote at :math:`x = 3`.  It also appears that there are no other vertical asymptotes, and there are not.  It is easy to see that the denominator :math:`x^{2} - 2 x - 3 = \left(x - 3\right) \left(x + 1\right)` and hence is zero at :math:`x = 3` and :math:`x = -1` but there is no vertical asymptote at :math:`x = -1`.

Although we can factor this denominator in our heads, if we could not here is how you can use Maxima to do so.  Run the command ``factor(denom(f(x)))`` and the result will be :math:`\left(x - 3\right) \left(x + 1\right)`.

The reason that :math:`x = -1` is not an asymptote is because there is no infinite limit at :math:`x = -1`, which is caused by the numerator also having :math:`x = -1` as a root.  If we select the original expression and then ``Algebra > Simplify``, we get,

.. math::
    \frac{x + 1}{x - 3}

which does not have a root of :math:`x = -1` in the denominator.

.. note::

    The original function

    .. math::
        f(x) = \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3}

    and its simplification

    .. math::
        g(x) = \frac{x + 1}{x - 3}

    are not equal.  For two functions to be equal they must be equal at all values of the variable.  These two are except at :math:`x = -1` since :math:`g(-1) = 0` and  :math:`f(-1)` is undefined.  In reality there is a hole in the graph of :math:`f(x)` at :math:`x = -1`, like,

    .. figure:: Images/Limits/Inf021.png
        :alt: (x^2+2x+1)/(x^2-2x-3)

        :math:`f(x) = \frac{x^{2} + 2 x + 1}{x^{2} - 2 x - 3}`

