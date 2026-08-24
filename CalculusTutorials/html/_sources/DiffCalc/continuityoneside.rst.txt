:index:`One-Sided Continuity`
=============================

Discussion & Definitions
------------------------

The only difference between one-sided continuity and continuity is that instead of the criteria that a two-sided limit exists we are only concerned with a one-sided limit.  We recap the definition of continuity, which you can consider two-sided continuity, from the last section.

.. admonition:: Definition: Continuous at a Point

    A function :math:`f(x)` is *continuous at a point a* if and only if the following three conditions are satisfied:

    #. :math:`f(a)` is defined.
    #. :math:`\displaystyle \lim_{x \to a} f(x)` exists
    #. :math:`\displaystyle \lim_{x \to a} f(x) = f(a)`


For the definitions of one-sided continuity we simply change the two-sided limit into a one-sided limit.

.. admonition:: Definition: Continuous From the Left at a Point

    A function :math:`f(x)` is *continuous from the left at a point a* if and only if the following three conditions are satisfied:

    #. :math:`f(a)` is defined.
    #. :math:`\displaystyle \lim_{x \to a^-} f(x)` exists
    #. :math:`\displaystyle \lim_{x \to a^-} f(x) = f(a)`

.. admonition:: Definition: Continuous From the Right at a Point

    A function :math:`f(x)` is *continuous from the right at a point a* if and only if the following three conditions are satisfied:

    #. :math:`f(a)` is defined.
    #. :math:`\displaystyle \lim_{x \to a^+} f(x)` exists
    #. :math:`\displaystyle \lim_{x \to a^+} f(x) = f(a)`


Example: :math:`f(x) = \sqrt{x}`
--------------------------------

GeoGebra
^^^^^^^^

Input the function with either,

.. code-block:: console

    sqrt(x)

or

.. code-block:: console

    x^(1/2)

The graph of the function is shown below.

.. figure:: Images/Continuity/OneSide001.png
    :alt: sqrt(x)

    :math:`f(x) = \sqrt{x}`

The function is clearly not defined for :math:`x < 0`, at least not in the real number system.  It is possible that this function is continuous from the right at :math:`x = 0`, and it is.  We will verify this algebraically.

Although we can do this in our heads we can also use GeoGebra to evaluate ``f(0)`` and the result is 0.  So the first criteria is satisfied.

Taking the right hand limit, ``LimitAbove`` in GeoGebra we get the result of 0.  Recall that you select a new cell and type in ``limit``, select ``LimitAbove``, put in ``f`` as the function and 0 as the limit point and  GeoGebra returns 0.

This verifies that :math:`f(x) = \sqrt{x}` is continuous from the right at :math:`x = 0`.

CLAE
^^^^

Input the function with either,

.. code-block:: console

    sqrt(x)

or

.. code-block:: console

    x^(1/2)

The graph of the function is shown below.

.. figure:: Images/Continuity/OneSide002.png
    :alt: sqrt(x)

    :math:`f(x) = \sqrt{x}`

The function is clearly not defined for :math:`x < 0`, at least not in the real number system.  It is possible that this function is continuous from the right at :math:`x = 0`, and it is.  We will verify this algebraically.

Although we can do this in our heads we can also use CLAE to evaluate ``f(0)`` and the result is 0.  So the first criteria is satisfied.

Taking the right hand limit, CLAE gives the result of 0.  Recall that you select the function, select ``Calculus > Limit``, variable *x*, limit point 0, and direction is Right.

This verifies that :math:`f(x) = \sqrt{x}` is continuous from the right at :math:`x = 0`.

Maxima
^^^^^^

Input the function with either,

.. code-block:: console

    kill(all);
    f(x):=sqrt(x)

or

.. code-block:: console

    kill(all);
    f(x):=x^(1/2)

The graph of the function is shown below.

.. code-block:: console

    wxplot2d([f(x)], [x,-1,8], [y,-5,5])

.. figure:: Images/Continuity/OneSide003.png
    :alt: sqrt(x)

    :math:`f(x) = \sqrt{x}`

The function is clearly not defined for :math:`x < 0`, at least not in the real number system.  It is possible that this function is continuous from the right at :math:`x = 0`, and it is.  We will verify this algebraically.

Although we can do this in our heads we can also use Maxima to evaluate ``f(0)`` and the result is 0.  So the first criteria is satisfied.

Taking the right hand limit,

.. code-block:: console

    limit(f(x),x,0,plus)

Maxima gives the result of 0.

This verifies that :math:`f(x) = \sqrt{x}` is continuous from the right at :math:`x = 0`.


Example: :math:`f(x) = \sqrt{4-x^2}`
------------------------------------

GeoGebra
^^^^^^^^

Input the function with either,

.. code-block:: console

    sqrt(4-x^2)

or

.. code-block:: console

    (4-x^2)^(1/2)

The graph of the function is shown below.

.. figure:: Images/Continuity/OneSide004.png
    :alt: sqrt(4 - x^2)

    :math:`f(x) = \sqrt{4-x^2}`

From what we know about root functions we know that the domain of this function is :math:`[-2, 2]`.  This function is continuous from the right at :math:`x = -2` and continuous from the left at :math:`x = -2`.  We will verify these claims.

Starting with continuity from the right at :math:`x = -2`.  Evaluate ``f(-2)`` and you should get 0.  Now do the ``LimitAbove`` command of *f* at :math:`x = -2` and you will also get 0.  This verifies that the function is continuous from the right at :math:`x = -2`.

Moving on to continuity from the left at :math:`x = 2`.  Evaluate ``f(2)`` and you should get 0.  Now do the ``LimitBelow`` command of *f* at :math:`x = 2` and you will also get 0.  This verifies that the function is continuous from the left at :math:`x = 2`.


CLAE
^^^^

Input the function with either,

.. code-block:: console

    sqrt(4-x^2)

or

.. code-block:: console

    (4-x^2)^(1/2)

The graph of the function is shown below.

.. figure:: Images/Continuity/OneSide005.png
    :alt: sqrt(4 - x^2)

    :math:`f(x) = \sqrt{4-x^2}`

From what we know about root functions we know that the domain of this function is :math:`[-2, 2]`.  This function is continuous from the right at :math:`x = -2` and continuous from the left at :math:`x = -2`.  We will verify these claims.

Starting with continuity from the right at :math:`x = -2`.  Evaluate the function at :math:`-2` and you should get 0.  Now do the right hand limit of *f* at :math:`x = -2` and you will also get 0.  This verifies that the function is continuous from the right at :math:`x = -2`.

Moving on to continuity from the left at :math:`x = 2`.  Evaluate the function at 2 and you should get 0.  Now do the left hand limit of *f* at :math:`x = 2` and you will also get 0.  This verifies that the function is continuous from the left at :math:`x = 2`.


Maxima
^^^^^^

Input the function with either,

.. code-block:: console

    kill(all);
    f(x):=sqrt(4-x^2)

or

.. code-block:: console

    kill(all);
    f(x):=(4-x^2)^(1/2)

The graph of the function is shown below.

.. figure:: Images/Continuity/OneSide006.png
    :alt: sqrt(4 - x^2)

    :math:`f(x) = \sqrt{4-x^2}`

From what we know about root functions we know that the domain of this function is :math:`[-2, 2]`.  This function is continuous from the right at :math:`x = -2` and continuous from the left at :math:`x = -2`.  We will verify these claims.

Starting with continuity from the right at :math:`x = -2`.  Evaluate``f(-2)```` and you should get 0.  Now do the right hand limit of *f* at :math:`x = -2`

.. code-block:: console

    limit(f(x),x,-2,plus)


and you will also get 0.  This verifies that the function is continuous from the right at :math:`x = -2`.

Moving on to continuity from the left at :math:`x = 2`.  Evaluate ``f(2)`` and you should get 0.  Now do the left hand limit of *f* at :math:`x = 2`

.. code-block:: console

    limit(f(x),x,2,minus)

and you will also get 0.  This verifies that the function is continuous from the left at :math:`x = 2`.

