:index:`Force Operation`
========================

The Force Operation option was initially a menu item used in the development and debugging of the program, but since it has some usefulness to the intended audience for this program we left it in the system.  It will probably not be used very often but can come in handy from time to time.

This option will take the expression and if there are any unfinished operations to perform it will attempt to complete them.  This can happen, for example, if the program returns an integral or a sum as a result.  There are other instances as well where you can try to force an operation to finish.

Example
-------

As an example, say we have the function,

.. math::
    \frac{1}{3 \sin{\left(x \right)} + 4 \cos{\left(x \right)}}

And we found the indefinite integral of this function using course techniques, that is, with the Course Techniques selector checked.  The result is,

.. math::
    \int \frac{1}{3 \sin{\left(x \right)} + 4 \cos{\left(x \right)}}\, dx

If we selected this result and then selected the Force Operation option the result will be,

.. math::
    - \frac{\ln{\left(\tan{\left(\frac{x}{2} \right)} - 2 \right)}}{5} + \frac{\ln{\left(2 \tan{\left(\frac{x}{2} \right)} + 1 \right)}}{5}

So the program finished the integral evaluation, using the full integration procedures.

Note that if we had selected the original function and did the indefinite integral, with the Course Techniques selector unchecked, the result would be the same,

.. math::
    - \frac{\ln{\left(\tan{\left(\frac{x}{2} \right)} - 2 \right)}}{5} + \frac{\ln{\left(2 \tan{\left(\frac{x}{2} \right)} + 1 \right)}}{5}


