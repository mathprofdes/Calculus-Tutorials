:index:`Norms and Normalization`
================================

The norm and normalize options are broken down into Real and Complex domains.  If you are working with variables that are real then select the real options and if you are working with variables that are complex then select the complex options.  The type you select will determine the assumptions that are made on the variables and may affect the simplification of the results. The only norm that we wrote into this program is the 2-norm (or Euclidean Norm).

:index:`Norm (2-Norm, Real)`
----------------------------

This finds the 2-norm of the selected vector. For example, say we have the following vector,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]

its real 2-norm is, :math:`\sqrt{14}`.

Say we have the following vector,

.. math::
    \left[\begin{array}{c}x\\y\\z\end{array}\right]

its real 2-norm is, :math:`\sqrt{x^{2} + y^{2} + z^{2}}`.

:index:`Normalize (Real)`
-------------------------

This normalizes the selected vector using the real 2-norm.  For example, say we have the following vector,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]

its 2-norm normalization is, :math:`\sqrt{14}`.

.. math::
    \left[\begin{array}{c}\frac{\sqrt{14}}{14}\\\frac{\sqrt{14}}{7}\\\frac{3 \sqrt{14}}{14}\end{array}\right]

Say we have the following vector,

.. math::
    \left[\begin{array}{c}x\\y\\z\end{array}\right]

its 2-norm normalization is,

.. math::
    \left[\begin{array}{c}\frac{x}{\sqrt{x^{2} + y^{2} + z^{2}}}\\\frac{y}{\sqrt{x^{2} + y^{2} + z^{2}}}\\\frac{z}{\sqrt{x^{2} + y^{2} + z^{2}}}\end{array}\right]

:index:`Norm (2-Norm, Complex)`
-------------------------------

This finds the 2-norm of the selected vector. For example, say we have the following vector,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]

its complex 2-norm is, :math:`\sqrt{14}`.

Say we have the following vector,

.. math::
    \left[\begin{array}{c}x\\y\\z\end{array}\right]

its complex 2-norm is, :math:`\sqrt{\left|{x}\right|^{2} + \left|{y}\right|^{2} + \left|{z}\right|^{2}}`.


:index:`Normalize (Complex)`
----------------------------

This normalizes the selected vector using the 2-norm.  For example, say we have the following vector,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]

its 2-norm normalization is, :math:`\sqrt{14}`.

.. math::
    \left[\begin{array}{c}\frac{\sqrt{14}}{14}\\\frac{\sqrt{14}}{7}\\\frac{3 \sqrt{14}}{14}\end{array}\right]

Say we have the following vector,

.. math::
    \left[\begin{array}{c}x\\y\\z\end{array}\right]

its 2-norm normalization is,

.. math::
    \left[\begin{array}{c}\frac{x}{\sqrt{\left|{x}\right|^{2} + \left|{y}\right|^{2} + \left|{z}\right|^{2}}}\\\frac{y}{\sqrt{\left|{x}\right|^{2} + \left|{y}\right|^{2} + \left|{z}\right|^{2}}}\\\frac{z}{\sqrt{\left|{x}\right|^{2} + \left|{y}\right|^{2} + \left|{z}\right|^{2}}}\end{array}\right]
