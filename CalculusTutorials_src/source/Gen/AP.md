
:index:`The Area Problem`
-------------------------

:index:`The Statement of The Area Problem`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Just like the Tangent Problem, the Area Problem is easy to state.  The goal here is to calculate the area under a curve between two *x* values.  For example, say we wanted to calculate the area under the curve :math:`y = x^2` with *x* ranging over the interval :math:`[0, 1]`.  A graph of this is below with the area of interest shaded.

.. figure:: ../Gen/Images/AP001.png
    :alt: Area Problem Visualization

    Area Problem Visualization

:index:`Solving The Area Problem`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
 
For example, say we wanted to calculate the area under the curve :math:`y = x^2` with *x* ranging over the interval :math:`[0, 1]`.  A graph of this is below with the area of interest shaded.

.. figure:: ../Gen/Images/AP001.png
    :alt: Area Under y = x^2 ob [0, 1]

    Area Under the Curve :math:`y = x^2` on :math:`[0, 1]`

Although we will be using a specific example here the general situation is exactly the same. If this were a nice geometric object like a rectangle, triangle, trapezoid, or even a regular polygon we could apply a formula to it and have our area.  Since it is not a nice geometric object we will take a similar approach as we did with the Tangent Problem.  With the tangent problem we approximated what we wanted using objects (secant lines) that we could calculate the slope of then we let the secant lines approach the tangent line thus having the slopes of the secant lines approach the slope of the tangent line, which was our goal.  Here we will approximate the area under the curve using nice geometric objects, rectangles.  We will first use 10 rectangles to approximate this area.

.. figure:: ../Gen/Images/AP002.png
    :alt: Area Approximation Using 10 Rectangles

    Area Approximation Using 10 Rectangles

If we add up the areas of each of these rectangles we get, 0.3325 (as you can see on the image).  Obviously this is not the exact area.  If we look at the graph it is clear that there is some area above the curve overestimating the area and there is area under the curve that is missed and hence underestimating the area.  If we increase the number of rectangles to 50 we get,

.. figure:: ../Gen/Images/AP003.png
    :alt: Area Approximation Using 50 Rectangles

    Area Approximation Using 50 Rectangles

Adding up the areas here we get approximately 0.3333.  Although this is not the exact area either, there are still extra portions above the curve and missing portions below the curve, it appears to be getting closer to the area under the curve.  Finally, if we up the number of rectangles to 100, we get,

.. figure:: ../Gen/Images/AP004.png
    :alt: Area Approximation Using 100 Rectangles

    Area Approximation Using 100 Rectangles

Giving us an approximation of 0.33333, and the appearance of a better approximation.  Noticing that these approximate areas are tending to 0.33333333... we would probably take a leap of faith and say that the exact area under the curve is :math:`A = \frac{1}{3}`, which is correct.  What is more important is that we followed the same path as we did with the tangent problem.  We needed a value we could not calculate, we used an approximation to that value we could calculate, then we took the limit of the approximations to obtain the desired value. Hence, both of these problems are solved with this concept of a limit.

Let's put a few more details in here.  Start with a general function :math:`f(x)` and some rectangles.

.. figure:: ../Gen/Images/AP005.png
    :alt: Area Derivation Visualization

    Area Derivation Visualization

Although there are 10 rectangles in this image we will imagine a more general situation with *n* rectangles.  We will also forget that this is on the interval :math:`[1, 5]` and think about it being on a general interval, :math:`[a, b]`.  We first calculate the area of a single rectangle.  The width of the rectangle is the length of the interval divided by the number of rectangles, specifically the width is :math:`\Delta x = \frac{b-a}{n}`, since all the rectangles have the same width.  The height of the rectangle is the functional value at the midpoint of each sub-interval we will call this *x* value :math:`x_i` for the *i* th sub-interval. So the height is :math:`f(x_i)`.  Hence, the area of the *i* th rectangle is :math:`f(x_i) \cdot \Delta x`.  So our approximation to the area under the curve is the sum of all the rectangles, specifically, 

.. math::
    A \approx \sum_{i = 1}^n f(x_i) \cdot \Delta x

Following our example, we got better approximations by increasing the number of rectangles, :math:`n`. We can do this with an infinite limit.  

.. math::
    A = \lim_{n \to \infty} \sum_{i = 1}^n f(x_i) \cdot \Delta x

A couple terms before we move on.  The sums of rectangle areas are called **Riemann Sums** and the limit of a Riemann sum is called the **Definite Integral**.

:index:`An Example of The Area Problem`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

As an example we will go back to the familiar velocity problem, with a twist.  As a visual, we will look at our example graph from above.  In this case, let's consider the vertical axis as velocity, so in miles/hour units, and we will consider the horizontal axis to be time, in hours.  So the curve is representing the velocity of the car or motor-scooter or particle (doesn't matter)  at each moment during the trip.  So this is essentially logging the speedometer values constantly while you are driving.  

.. figure:: ../Gen/Images/AP005.png
    :alt: Velocity Verses Time Graph

    Velocity Verses Time Graph

Each rectangle area is the height times the width, so miles/hour times hours which gives us miles.  So each rectangle represents an approximation of how far the car went during the time of the sub-interval. Consequently, the Riemann sum of all the rectangles gives an approximation of the total distance traveled between times *a* and *b*.

.. math::
    D \approx \sum_{i = 1}^n f(x_i) \cdot \Delta x

So in the limit, we get the exact distance traveled between times *a* and *b*, that is, the change in the odometer during the trip.

.. math::
    D = \lim_{n \to \infty} \sum_{i = 1}^n f(x_i) \cdot \Delta x

:index:`What Does The Area Problem Mean in General`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Let's take the previous example one step further.  In the previous example our areas were distances.  A distances is a total change of velocity with respect to time.  The velocity was our *y* variable and our time was the *x* variable.  The *y* variable is our dependent variable and our *x* variable is our independent variable.  Variables represent quantities, in many cases physical quantities.  Obviously there is a relationship between the *x* and *y* variables, in the above example it was the car or motor-scooter or whatever.  So if we have a relationship between two quantities, one is an independent quantity and the other is a dependent rate quantity (dependent on the value of the independent quantity) then the Riemann sum represents an **approximate total change** and the limit of the Riemann sum represents the **total change**.

