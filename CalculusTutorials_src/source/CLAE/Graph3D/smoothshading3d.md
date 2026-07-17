
Smooth shading is when each triangle that defines a surface is colored in a way that makes the surface seem smooth.  This mode does look better, but it requires between three and eight times the calculations as non-smooth shading.  For example, the surface defined by the function :math:`z = f(x, y) = x^{2} - y^{2}` with smooth shading on is pictured below,

.. figure:: Images/SmoothShade001.png
    :alt: Smooth Shading On

    Smooth Shading On

and the same surface with smooth shading off is pictured below.

.. figure:: Images/SmoothShade002.png
    :alt: Smooth Shading Off

    Smooth Shading Off

In general, you will want to keep smooth shading on unless you are doing some animations of the surface that are attached to sliders.  In this case turning smooth shading off will significantly increase the animation speed. 
