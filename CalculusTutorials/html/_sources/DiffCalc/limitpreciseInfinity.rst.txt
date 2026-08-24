:index:`The Precise Definition of a Limit at Infinity`
======================================================

Discussion & Definitions
------------------------

In most cases having a good intuitive understanding of the limit will be sufficient and serve you well.  If you intend to go further in mathematics and take courses in analysis the intuitive understanding will serve as a good basis but will not be sufficient. In this case you will need a formal definition.  Below we give formal or precise  definitions of the limit at infinity.  Applying these algebraically can be tricky and we will not do any of these examples.  We will use dynamic software to visualize the definition to put some meaning to all the mathematics.  The big step here is to make the terms "approach" and "gets close to" precise, in essence, quantify these intuitive concepts.

.. admonition:: Definition: Precise Definition of a Limit at Infinity

    - Let :math:`f(x)` be a function defined on the interval :math:`(c, \infty)`.  Then *the limit of f(x) as x approaches* :math:`\infty` *is L*, denoted,

    .. math::

        \lim_{x \to \infty} f(x) = L

    If for every :math:`\epsilon > 0`, there exists an :math:`N`, such that if :math:`x > N`, then :math:`|f(x) - L| < \epsilon`.


    - Let :math:`f(x)` be a function defined on the interval :math:`(-\infty, c)`.  Then *the limit of f(x) as x approaches* :math:`-\infty` *is L*, denoted,

    .. math::

        \lim_{x \to -\infty} f(x) = L

    If for every :math:`\epsilon > 0`, there exists an :math:`N`, such that if :math:`x < N`, then :math:`|f(x) - L| < \epsilon`.



Example: Visualizing the Limit at InfinityDefinition
----------------------------------------------------

We will concentrate on the definition of the limit at infinity, the limit at minus infinity is similar.  Since these visualize better with dynamic software packages we will be using just GeoGebra and CLAE.  For these examples we will use the function, :math:`f(x) = 1+\frac{\sin(x)}{x}`.  The limit will be assumed to be 1.  So we will go through the definition to show, or visualize,

.. math::
    \lim_{x \to \infty} 1+\frac{\sin(x)}{x} = 1


GeoGebra
^^^^^^^^

The hardest part is the understanding of this portion of the definition.

If for every :math:`\epsilon > 0`, there exists an :math:`N`, such that if :math:`x > N`, then :math:`|f(x) - L| < \epsilon`.

Taking this step by step starting at the beginning, given an :math:`\epsilon > 0`, we need to find an :math:`N` so that for *x* values larger than this :math:`|f(x) - L| < \epsilon`.  The statement :math:`|f(x) - L| < \epsilon` means :math:`-\epsilon < f(x) - L < \epsilon` which in turn means :math:`L-\epsilon < f(x) < L + \epsilon`.  So if we put this all together, if we put an :math:`\epsilon` interval around our limit *L* then we can go out far enough along the *x* axis so that all the *y* values are within this interval.  We need to do this for all possible :math:`\epsilon > 0`.  Let's set up the visualization.

#. Input the function,

    .. code-block:: console

        1 + sin(x)/x

#. Set up a slider for :math:`\epsilon`, call it *p* since *e* is the Euler constant (2.718281828...).  Type ``p`` in a cell and hit Enter.

#. Input the :math:`L-\epsilon < f(x) < L + \epsilon` by inputting the two formulas below,

    .. code-block:: console

        1 - p

    .. code-block:: console

        1 + p

.. figure:: Images/Limits/PDInf001.png
    :alt: y = 1+ sin(x)/x with epsilon bound lines.

    :math:`f(x) = 1+\frac{\sin(x)}{x}` with :math:`\epsilon` bound lines.

Change the slider settings to go from 0 to 0.1 with an increment of 0.001.  Zoom in a bit and set the slider to 0.06, you should see,

.. figure:: Images/Limits/PDInf002.png
    :alt: y = 1+ sin(x)/x with epsilon bound lines.

    :math:`f(x) = 1+\frac{\sin(x)}{x}` with :math:`\epsilon` bound lines.

From the picture it appears that from 20 on the function is between the two horizontal lines, so our *N* for :math:`\epsilon = 0.06` is 20.  We are not done yet, this has to be possible for all :math:`\epsilon > 0`.  Although we cannot show this for every case we will go a couple more steps to get the feel that it is possible.  Move the slider down to 0.03, we see the following,

.. figure:: Images/Limits/PDInf003.png
    :alt: y = 1+ sin(x)/x with epsilon bound lines.

    :math:`f(x) = 1+\frac{\sin(x)}{x}` with :math:`\epsilon` bound lines.

So an *N* of 20 no longer works since some of the function is outside the horizontal line bounds.  If we move the graph off to the right and zoom in a little we see that an *N* of 34 looks like it will do the job.

.. figure:: Images/Limits/PDInf004.png
    :alt: y = 1+ sin(x)/x with epsilon bound lines.

    :math:`f(x) = 1+\frac{\sin(x)}{x}` with :math:`\epsilon` bound lines.

One more step just to solidify the concept.  Move the slider down to 0.005.

.. figure:: Images/Limits/PDInf005.png
    :alt: y = 1+ sin(x)/x with epsilon bound lines.

    :math:`f(x) = 1+\frac{\sin(x)}{x}` with :math:`\epsilon` bound lines.

Move further off to the right, an *N* of 235 looks like it will work.

.. figure:: Images/Limits/PDInf006.png
    :alt: y = 1+ sin(x)/x with epsilon bound lines.

    :math:`f(x) = 1+\frac{\sin(x)}{x}` with :math:`\epsilon` bound lines.

This is certainly not a proof or an algebraic justification but hopefully it gives you a feel for how we gave quantified the terms "approach", "gets close to", and "increases without bound" precisely.

CLAE
^^^^

The hardest part is the understanding of this portion of the definition.

If for every :math:`\epsilon > 0`, there exists an :math:`N`, such that if :math:`x > N`, then :math:`|f(x) - L| < \epsilon`.

Taking this step by step starting at the beginning, given an :math:`\epsilon > 0`, we need to find an :math:`N` so that for *x* values larger than this :math:`|f(x) - L| < \epsilon`.  The statement :math:`|f(x) - L| < \epsilon` means :math:`-\epsilon < f(x) - L < \epsilon` which in turn means :math:`L-\epsilon < f(x) < L + \epsilon`.  So if we put this all together, if we put an :math:`\epsilon` interval around our limit *L* then we can go out far enough along the *x* axis so that all the *y* values are within this interval.  We need to do this for all possible :math:`\epsilon > 0`.  Let's set up the visualization.

#. Input the function,

    .. code-block:: console

        1 + sin(x)/x

#. Input the :math:`L-\epsilon < f(x) < L + \epsilon` by inputting the list,

    .. code-block:: console

        [1 - e, 1 + e]

#. Drag this over to the graph, it will come in as horizontal lines which is what we want.

.. figure:: Images/Limits/PDInf007.png
    :alt: y = 1+ sin(x)/x with epsilon bound lines.

    :math:`f(x) = 1+\frac{\sin(x)}{x}` with :math:`\epsilon` bound lines.

Change the slider settings to go from 0 to 0.1 with 1000 steps.  Zoom in a bit and set the slider to 0.06, you should see,

.. figure:: Images/Limits/PDInf008.png
    :alt: y = 1+ sin(x)/x with epsilon bound lines.

    :math:`f(x) = 1+\frac{\sin(x)}{x}` with :math:`\epsilon` bound lines.

From the picture it appears that from 20 on the function is between the two horizontal lines, so our *N* for :math:`\epsilon = 0.06` is 20.  We are not done yet, this has to be possible for all :math:`\epsilon > 0`.  Although we cannot show this for every case we will go a couple more steps to get the feel that it is possible.  Move the slider down to 0.03, we see the following,

.. figure:: Images/Limits/PDInf009.png
    :alt: y = 1+ sin(x)/x with epsilon bound lines.

    :math:`f(x) = 1+\frac{\sin(x)}{x}` with :math:`\epsilon` bound lines.

So an *N* of 20 no longer works since some of the function is outside the horizontal line bounds.  If we move the graph off to the right and zoom in a little we see that an *N* of 34 looks like it will do the job.

.. figure:: Images/Limits/PDInf010.png
    :alt: y = 1+ sin(x)/x with epsilon bound lines.

    :math:`f(x) = 1+\frac{\sin(x)}{x}` with :math:`\epsilon` bound lines.

One more step just to solidify the concept.  Move the slider down to 0.005.

.. figure:: Images/Limits/PDInf011.png
    :alt: y = 1+ sin(x)/x with epsilon bound lines.

    :math:`f(x) = 1+\frac{\sin(x)}{x}` with :math:`\epsilon` bound lines.

Move further off to the right, an *N* of 220 looks like it will work.

.. figure:: Images/Limits/PDInf012.png
    :alt: y = 1+ sin(x)/x with epsilon bound lines.

    :math:`f(x) = 1+\frac{\sin(x)}{x}` with :math:`\epsilon` bound lines.

This is certainly not a proof or an algebraic justification but hopefully it gives you a feel for how we gave quantified the terms "approach", "gets close to", and "increases without bound" precisely.

