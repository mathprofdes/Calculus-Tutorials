:index:`Maxima: Space Curves`
=============================

Unit Tangent
------------

This returns the unit tangent vector of a space curve.  When you select this option a dialog will open asking the user to input the variable to use.  This option works only for vectors 3 dimensions.  As an example, say we wanted the unit tangent vector for the twisted cubic :math:`\left[t,  t^{2}, \  t^{3}\right]`, selecting this option would return,

.. math::
    \left[ \frac{1}{\sqrt{9 t^{4} + 4 t^{2} + 1}}, \  \frac{2 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}, \  \frac{3 t^{2}}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right]


Unit Normal
-----------

This returns the unit normal vector of a space curve.  When you select this option a dialog will open asking the user to input the variable to use. This option works only for vectors 3 dimensions.  As an example, say we wanted the unit normal vector for the twisted cubic :math:`\left[t,  t^{2}, \  t^{3}\right]`, selecting this option would return,

.. math::
    \left[ \frac{- 36 t^{3} - 8 t}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}} \sqrt{\frac{\left(36 t^{3} + 8 t\right)^{2}}{4 \left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(- \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(- \frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}, \  \frac{- \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}}{\sqrt{\frac{\left(36 t^{3} + 8 t\right)^{2}}{4 \left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(- \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(- \frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}, \  \frac{- \frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}}{\sqrt{\frac{\left(36 t^{3} + 8 t\right)^{2}}{4 \left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(- \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(- \frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}\right]

which simplifies to

.. math::
    \left[ \frac{- 9 t^{3} - 2 t}{\sqrt{9 t^{4} + 4 t^{2} + 1} \sqrt{9 t^{4} + 9 t^{2} + 1}}, \  \frac{1 - 9 t^{4}}{\sqrt{9 t^{4} + 4 t^{2} + 1} \sqrt{9 t^{4} + 9 t^{2} + 1}}, \  \frac{6 t^{3} + 3 t}{\sqrt{9 t^{4} + 4 t^{2} + 1} \sqrt{9 t^{4} + 9 t^{2} + 1}}\right]


Unit Binormal
-------------

This returns the unit binormal vector of a space curve.  When you select this option a dialog will open asking the user to input the variable to use. This option works only for vectors 3 dimensions.  As an example, say we wanted the unit normal vector for the twisted cubic :math:`\left[t,  t^{2}, \  t^{3}\right]`, selecting this option would return,

.. math::
    \left[ - \frac{3 t^{2} \left(- \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)}{\sqrt{9 t^{4} + 4 t^{2} + 1} \sqrt{\frac{\left(36 t^{3} + 8 t\right)^{2}}{4 \left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(- \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(- \frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}} + \frac{2 t \left(- \frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)}{\sqrt{9 t^{4} + 4 t^{2} + 1} \sqrt{\frac{\left(36 t^{3} + 8 t\right)^{2}}{4 \left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(- \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(- \frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}, \  - \frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{2} \sqrt{\frac{\left(36 t^{3} + 8 t\right)^{2}}{4 \left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(- \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(- \frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}} + \frac{\frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} - \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}}{\sqrt{9 t^{4} + 4 t^{2} + 1} \sqrt{\frac{\left(36 t^{3} + 8 t\right)^{2}}{4 \left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(- \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(- \frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}, \  \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{2} \sqrt{\frac{\left(36 t^{3} + 8 t\right)^{2}}{4 \left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(- \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(- \frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}} + \frac{- \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}}{\sqrt{9 t^{4} + 4 t^{2} + 1} \sqrt{\frac{\left(36 t^{3} + 8 t\right)^{2}}{4 \left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(- \frac{t \left(36 t^{3} + 8 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(- \frac{3 t^{2} \left(36 t^{3} + 8 t\right)}{2 \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}\right]

which simplifies to

.. math::
    \left[ \frac{3 t^{2}}{\sqrt{9 t^{4} + 9 t^{2} + 1}}, \  - \frac{3 t}{\sqrt{9 t^{4} + 9 t^{2} + 1}}, \  \frac{1}{\sqrt{9 t^{4} + 9 t^{2} + 1}}\right]

TNB
---

This returns the unit tangent, normal, and binormal vectors of a space curve as a list of three vectors.  This option only works with 3-dimensional vectors.  When you select this option a dialog will open asking the user to input the variable to use.  As a simpler example than the ones above, lets find the TNB frame for the helix, :math:`[\cos(t), \sin(t), t]`.  Selecting this option gives us the result,

.. math::
    \left[ \left[ - \frac{\sin{\left(t \right)}}{\sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}, \  \frac{\cos{\left(t \right)}}{\sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}, \  \frac{1}{\sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}\right], \  \left[ - \frac{\cos{\left(t \right)}}{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}} \sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}, \  - \frac{\sin{\left(t \right)}}{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}} \sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}, \  0\right], \  \left[ \frac{\sin{\left(t \right)}}{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}} \left(\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1\right)}, \  - \frac{\cos{\left(t \right)}}{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}} \left(\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1\right)}, \  \frac{\sin^{2}{\left(t \right)}}{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}} \left(\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1\right)} + \frac{\cos^{2}{\left(t \right)}}{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}} \left(\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1\right)}\right]\right]

which simplifies to

.. math::
    \left[ \left[ - \frac{\sqrt{2} \sin{\left(t \right)}}{2}, \  \frac{\sqrt{2} \cos{\left(t \right)}}{2}, \  \frac{\sqrt{2}}{2}\right], \  \left[ - \cos{\left(t \right)}, \  - \sin{\left(t \right)}, \  0\right], \  \left[ \frac{\sqrt{2} \sin{\left(t \right)}}{2}, \  - \frac{\sqrt{2} \cos{\left(t \right)}}{2}, \  \frac{\sqrt{2}}{2}\right]\right]

Curvature
---------

This returns the curvature of a space curve or a function.  When you select this option a dialog will open asking the user to input the variable to use.  This option works only for vectors in 3 dimensions.  Say we wanted the curvature for the helix, :math:`[\cos(t), \sin(t), t]`.  Selecting this option gives us the result,

.. math::
    \frac{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}}{\sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}

which simplifies to 1/2.


Torsion
-------

This returns the torsion of a space curve.  This option only works with 3-dimensional vectors.  When you select this option a dialog will open asking the user to input the variable to use.  For example, the torsion of the helix, :math:`[\cos(t), \sin(t), t]` is 1/2.


