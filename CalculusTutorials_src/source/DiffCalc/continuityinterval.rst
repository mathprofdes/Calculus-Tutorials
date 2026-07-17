:index:`Continuity on an Interval`
==================================

Discussion & Definitions
------------------------

Simply stated, a function :math:`f(x)` is continuous on an interval if it is continuous at every point in the interval, if an endpoint is included in the interval then we require the appropriate one-sided continuity. Specifically,

.. admonition:: Definition: Continuous on an Interval

    #. If the interval is an open interval, :math:`(a, b)` then :math:`f(x)` must be continuous at all points in the interval. This also holds if either *a*, *b*, or both are :math:`-\infty` or :math:`\infty` respectively.
    #. If the interval is a closed interval, :math:`[a, b]` then :math:`f(x)` must be continuous at all points in :math:`(a, b)`, continuous from the right at *a*, and continuous from the left at *b*.
    #. If the interval is a half open and half closed, :math:`(a, b]` then :math:`f(x)` must be continuous at all points in :math:`(a, b)` and continuous from the left at *b*.  The same is true if *a* is :math:`-\infty`.
    #. If the interval is a half open and half closed, :math:`[a, b)` then :math:`f(x)` must be continuous at all points in :math:`(a, b)` and continuous from the right at *a*. The same is true if *b* is :math:`\infty`.

Refer to the sections :doc:`continuity` and :doc:`continuityoneside` for details on how to use GeoGebra, CLAE, and Maxima to verify continuity and one-sided continuity at a point.


Example: :math:`f(x) = \sqrt{x}`
--------------------------------

:math:`f(x) = \sqrt{x}` is continuous on the interval, :math:`[0, \infty)`.

.. figure:: Images/Continuity/Int001.png
    :alt: sqrt(x)

    :math:`f(x) = \sqrt{x}`

Example: :math:`f(x) = \sqrt{4-x^2}`
------------------------------------

:math:`f(x) = \sqrt{4-x^2}` is continuous on the interval, :math:`[-2, 2]`.

.. figure:: Images/Continuity/Int002.png
    :alt: sqrt(4-x^2)

    :math:`f(x) = \sqrt{4-x^2}`


Example: :math:`f(x) = \ln(x)`
------------------------------

:math:`f(x) = \ln(x)` is continuous on the interval, :math:`(0, \infty)`.

.. figure:: Images/Continuity/Int003.png
    :alt: ln(x)

    :math:`f(x) = \ln(x)`


Example: :math:`f(x) = \tan(x)`
-------------------------------

:math:`f(x) = \tan(x)` is continuous on the union of intervals, :math:`(-\pi/2 + k\pi, \pi/2 + k\pi)`, where :math:`k \in \mathbb{Z}`.

.. figure:: Images/Continuity/Int004.png
    :alt: tan(x)

    :math:`f(x) = \tan(x)`

