:index:`Maxima: Complex Numbers`
================================

Real Part
---------

This option extracts the real part of the complex number.  For example, for the number :math:`3 + 4 i` this option returns 3.  Also, for :math:`\sin{\left(4 + 3 i \right)}` this option returns :math:`\sin{\left(4 \right)} \cosh{\left(3 \right)}.`

Imaginary Part
--------------

This option extracts the imaginary part of the complex number.  For example, for the number :math:`3 + 4 i` this option returns 4.  Also, for :math:`\sin{\left(4 + 3 i \right)}` this option returns :math:`\cos{\left(4 \right)} \sinh{\left(3 \right)}.`

Rectangular Form
----------------

This option writes the complex number in rectangular form.  For example, for :math:`\sin{\left(4 + 3 i \right)}` this option returns :math:`\sin{\left(4 \right)} \cosh{\left(3 \right)} + i \cos{\left(4 \right)} \sinh{\left(3 \right)}.`


Polar Form
----------

This option writes the complex number in polar form.  For example, for the number :math:`3 + 4 i` this option returns :math:`5 e^{i \operatorname{atan}{\left(\frac{4}{3} \right)}}.`  Also, for :math:`\sin{\left(4 + 3 i \right)}` this option returns,

.. math::
    \sqrt{\cos^{2}{\left(4 \right)} \sinh^{2}{\left(3 \right)} + \sin^{2}{\left(4 \right)} \cosh^{2}{\left(3 \right)}} e^{i \left(- \pi + \operatorname{atan}{\left(\frac{\cos{\left(4 \right)} \sinh{\left(3 \right)}}{\sin{\left(4 \right)} \cosh{\left(3 \right)}} \right)}\right)}

Demoivre Form
-------------

Complex exponentials are converted into equivalent expressions in terms of circular functions. For example, :math:`e^{a + i b}` is converted to :math:`\left(i \sin{\left(b \right)} + \cos{\left(b \right)}\right) e^{a}.`

Exponential Form
----------------

Converts circular and hyperbolic functions to exponential form. For example, :math:`\left(i \sin{\left(b \right)} + \cos{\left(b \right)}\right) e^{a}` is converted to :math:`e^{a} e^{i b}`, which simplifies to :math:`e^{a + i b}.`


