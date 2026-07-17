:index:`Space Curves`
=====================

Options for space curves are the calculation of unit tangent, normal, and binormal vectors as well as curvature, torsion, and curve to surface projection calculations.

:index:`Unit Tangent`
---------------------

This returns the unit tangent vector of a space curve.  When you select this option a dialog will open asking the user to input the variable to use.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

This option works for vectors in both 2 and 3 dimensions.

For example, say we wanted the unit tangent vector for :math:`\left[ t^{2}, \  t^{3}\right]`, selecting this option would return,

.. math::
    \left[\begin{array}{c}\frac{2 t}{\sqrt{9 t^{4} + 4 t^{2}}}\\\frac{3 t^{2}}{\sqrt{9 t^{4} + 4 t^{2}}}\end{array}\right]

As another example, say we wanted the unit tangent vector for the twisted cubic :math:`\left[t,  t^{2}, \  t^{3}\right]`, selecting this option would return,

.. math::
    \left[\begin{array}{c}\frac{1}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\\\frac{2 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\\\frac{3 t^{2}}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\end{array}\right]

Note that the output is as a column vector.

:index:`Unit Normal`
---------------------

This returns the unit normal vector of a space curve.  When you select this option a dialog will open asking the user to input the variable to use.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

This option works for vectors in both 2 and 3 dimensions.

For example, say we wanted the unit normal vector for :math:`\left[ t^{2}, \  t^{3}\right]`, selecting this option would return,

.. math::
    \left[\begin{array}{c}\frac{\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2}\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2}}}}{\sqrt{\left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2}\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2}}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2}\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2}}}\right)^{2}}}\\\frac{\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2}\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2}}}}{\sqrt{\left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2}\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2}}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2}\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2}}}\right)^{2}}}\end{array}\right]

which simplifies to

.. math::
    \left[\begin{array}{c}- \frac{3 \sqrt{t^{2} \left(9 t^{2} + 4\right)}}{\sqrt{\frac{9 t^{2} + 4}{729 t^{6} + 972 t^{4} + 432 t^{2} + 64}} \left(81 t^{4} + 72 t^{2} + 16\right)}\\\frac{2 \sqrt{t^{2} \left(9 t^{2} + 4\right)}}{t \sqrt{\frac{9 t^{2} + 4}{729 t^{6} + 972 t^{4} + 432 t^{2} + 64}} \left(81 t^{4} + 72 t^{2} + 16\right)}\end{array}\right]


As another example, say we wanted the unit normal vector for the twisted cubic :math:`\left[t,  t^{2}, \  t^{3}\right]`, selecting this option would return,

.. math::
    \left[\begin{array}{c}\frac{- 18 t^{3} - 4 t}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}} \sqrt{\frac{\left(- 18 t^{3} - 4 t\right)^{2}}{\left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}\\\frac{\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}}{\sqrt{\frac{\left(- 18 t^{3} - 4 t\right)^{2}}{\left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}\\\frac{\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}}{\sqrt{\frac{\left(- 18 t^{3} - 4 t\right)^{2}}{\left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}\end{array}\right]

which simplifies to

.. math::
    \left[\begin{array}{c}\frac{t \left(- 9 t^{2} - 2\right)}{\sqrt{\frac{81 t^{8} + 117 t^{6} + 54 t^{4} + 13 t^{2} + 1}{729 t^{12} + 972 t^{10} + 675 t^{8} + 280 t^{6} + 75 t^{4} + 12 t^{2} + 1}} \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}}\\\frac{1 - 9 t^{4}}{\sqrt{\frac{81 t^{8} + 117 t^{6} + 54 t^{4} + 13 t^{2} + 1}{729 t^{12} + 972 t^{10} + 675 t^{8} + 280 t^{6} + 75 t^{4} + 12 t^{2} + 1}} \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}}\\\frac{3 t \left(2 t^{2} + 1\right)}{\sqrt{\frac{81 t^{8} + 117 t^{6} + 54 t^{4} + 13 t^{2} + 1}{729 t^{12} + 972 t^{10} + 675 t^{8} + 280 t^{6} + 75 t^{4} + 12 t^{2} + 1}} \left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}}\end{array}\right]

Note that the output is as a column vector.


:index:`Unit Binormal`
----------------------

This returns the unit binormal vector of a space curve.  When you select this option a dialog will open asking the user to input the variable to use.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

This option only works for vectors in 3 dimensions.  Since the binormal vector is the cross product of the tangent and normal vectors it does not make sense in a 2-dimensional setting.

For example, say we wanted the unit binormal vector for the twisted cubic :math:`\left[t,  t^{2}, \  t^{3}\right]`, selecting this option would return,

.. math::
    \left[\begin{array}{c}- \frac{3 t^{2} \left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)}{\sqrt{9 t^{4} + 4 t^{2} + 1} \sqrt{\frac{\left(- 18 t^{3} - 4 t\right)^{2}}{\left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}} + \frac{2 t \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)}{\sqrt{9 t^{4} + 4 t^{2} + 1} \sqrt{\frac{\left(- 18 t^{3} - 4 t\right)^{2}}{\left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}\\\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{2} \sqrt{\frac{\left(- 18 t^{3} - 4 t\right)^{2}}{\left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}} - \frac{\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}}{\sqrt{9 t^{4} + 4 t^{2} + 1} \sqrt{\frac{\left(- 18 t^{3} - 4 t\right)^{2}}{\left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}\\- \frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{2} \sqrt{\frac{\left(- 18 t^{3} - 4 t\right)^{2}}{\left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}} + \frac{\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}}{\sqrt{9 t^{4} + 4 t^{2} + 1} \sqrt{\frac{\left(- 18 t^{3} - 4 t\right)^{2}}{\left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}\end{array}\right]

which simplifies to

.. math::
    \left[\begin{array}{c}\frac{3 t^{2}}{\sqrt{\frac{81 t^{8} + 117 t^{6} + 54 t^{4} + 13 t^{2} + 1}{729 t^{12} + 972 t^{10} + 675 t^{8} + 280 t^{6} + 75 t^{4} + 12 t^{2} + 1}} \left(9 t^{4} + 4 t^{2} + 1\right)}\\\frac{3 t \sqrt{\frac{81 t^{8} + 117 t^{6} + 54 t^{4} + 13 t^{2} + 1}{729 t^{12} + 972 t^{10} + 675 t^{8} + 280 t^{6} + 75 t^{4} + 12 t^{2} + 1}} \left(- 9 t^{4} - 4 t^{2} - 1\right)}{9 t^{4} + 9 t^{2} + 1}\\\frac{\sqrt{\frac{81 t^{8} + 117 t^{6} + 54 t^{4} + 13 t^{2} + 1}{729 t^{12} + 972 t^{10} + 675 t^{8} + 280 t^{6} + 75 t^{4} + 12 t^{2} + 1}} \left(9 t^{4} + 4 t^{2} + 1\right)}{9 t^{4} + 9 t^{2} + 1}\end{array}\right]

:index:`TNB`
------------

This returns the unit tangent, normal, and binormal vectors of a space curve as a list of three vectors.  Since this includes the binormal vector this option only works with 3-dimensional vectors.  When you select this option a dialog will open asking the user to input the variable to use.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

As a simpler example than the ones above, lets find the TNB frame for the helix, :math:`[\cos(t), \sin(t), t]`.  Selecting this option gives us the result,

.. math::
    \left[ \left[\begin{array}{c}- \frac{\sin{\left(t \right)}}{\sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}\\\frac{\cos{\left(t \right)}}{\sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}\\\frac{1}{\sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}\end{array}\right], \  \left[\begin{array}{c}- \frac{\cos{\left(t \right)}}{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}} \sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}\\- \frac{\sin{\left(t \right)}}{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}} \sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}\\0\end{array}\right], \  \left[\begin{array}{c}\frac{\sin{\left(t \right)}}{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}} \left(\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1\right)}\\- \frac{\cos{\left(t \right)}}{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}} \left(\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1\right)}\\\frac{\sin^{2}{\left(t \right)}}{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}} \left(\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1\right)} + \frac{\cos^{2}{\left(t \right)}}{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}} \left(\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1\right)}\end{array}\right]\right]

which simplifies to

.. math::
    \left[ \left[\begin{array}{c}- \frac{\sqrt{2} \sin{\left(t \right)}}{2}\\\frac{\sqrt{2} \cos{\left(t \right)}}{2}\\\frac{\sqrt{2}}{2}\end{array}\right], \  \left[\begin{array}{c}- \cos{\left(t \right)}\\- \sin{\left(t \right)}\\0\end{array}\right], \  \left[\begin{array}{c}\frac{\sqrt{2} \sin{\left(t \right)}}{2}\\- \frac{\sqrt{2} \cos{\left(t \right)}}{2}\\\frac{\sqrt{2}}{2}\end{array}\right]\right]

:index:`Curvature`
------------------

This returns the curvature of a space curve or a function.  When you select this option a dialog will open asking the user to input the variable to use.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

This option works for vectors in both 2 and 3 dimensions as well as functions in the plane.

For example, say we wanted the curvature for :math:`\left[ t^{2}, \  t^{3}\right]`, selecting this option would return,

.. math::
    \frac{\sqrt{\left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2}\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2}}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2}\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2}}}\right)^{2}}}{\sqrt{9 t^{4} + 4 t^{2}}}

which simplifies to

.. math::
    \frac{6}{\sqrt{729 t^{6} + 972 t^{4} + 432 t^{2} + 64} \left|{t}\right|}

Say we wanted the curvature for the twisted cubic :math:`\left[t,  t^{2}, \  t^{3}\right]` is,

.. math::
    \frac{\sqrt{\frac{\left(- 18 t^{3} - 4 t\right)^{2}}{\left(9 t^{4} + 4 t^{2} + 1\right)^{3}} + \left(\frac{2 t \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{2}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2} + \left(\frac{3 t^{2} \left(- 18 t^{3} - 4 t\right)}{\left(9 t^{4} + 4 t^{2} + 1\right)^{\frac{3}{2}}} + \frac{6 t}{\sqrt{9 t^{4} + 4 t^{2} + 1}}\right)^{2}}}{\sqrt{9 t^{4} + 4 t^{2} + 1}}

which simplifies to

.. math::
    \frac{2 \sqrt{81 t^{8} + 117 t^{6} + 54 t^{4} + 13 t^{2} + 1}}{\sqrt{9 t^{4} + 4 t^{2} + 1} \sqrt{729 t^{12} + 972 t^{10} + 675 t^{8} + 280 t^{6} + 75 t^{4} + 12 t^{2} + 1}}

Say we wanted the curvature for the helix, :math:`[\cos(t), \sin(t), t]`.  Selecting this option gives us the result,

.. math::
    \frac{\sqrt{\frac{\sin^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1} + \frac{\cos^{2}{\left(t \right)}}{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}}{\sqrt{\sin^{2}{\left(t \right)} + \cos^{2}{\left(t \right)} + 1}}

which simplifies to 1/2.

If simply want the curvature of the function :math:`f(x) = x^2`, this would return,

.. math::
    \frac{2}{\left(4 x^{2} + 1\right)^{\frac{3}{2}}}


:index:`Torsion`
----------------

This returns the torsion of a space curve.  Since this includes the binormal vector (or cross products of derivatives of the curve) this option only works with 3-dimensional vectors.  When you select this option a dialog will open asking the user to input the variable to use.  There is also a variable assumptions selection at the bottom.  For more about variable assumptions see the discussion at the bottom of this page.  In most cases you will leave the assumptions alone (everything real) but sometimes you may need to change these.

For example, the torsion of the helix, :math:`[\cos(t), \sin(t), t]` is 1/2.

The program can calculate more complected expressions, for example, we did the torsion of the twisted cubic.  The result was very large (over 4000 columns wide) and we will not include it here.


:index:`Curve Projections onto a Surface`
-----------------------------------------

These options are for projecting a 2D curve onto a 3D function surface :math:`z = f(x, y)` and returning the space curve parametrization of the projection.  Since the CAS and graphical systems are independent of each other, this operation is purely algebraic.  It will take an expression in two variables, an ``x`` expression, a ``y`` expression, do a substitution and return a column vector of the parametrization.  Creating space curve projections is simple enough to do, these options just convenience options to save the user a few steps.  Projecting a curve onto a surface can have many visualization uses, limit paths, directional derivatives, and multiple integrals to name a few.

:index:`Project Function to Surface`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This option will project a 2D function of the form :math:`y = f(x)` onto a 3D functional surface of the form :math:`z = f(x, y)`.  When this option is invoked a dialog box will appear asking the user for the variables of the 3D function to substitute, the independent variable to use the for the space curve parametrization, and the 2D functional expression for the curve.  The program will use the independent variable for the first variable in the variable list given for the 3D function, and the 2D functional expression for the second variable in the variable list given for the 3D function.  This is all combined into a vector parametrization of the space curve.

For example, say our surface is :math:`\sin{\left(x \right)} + \cos{\left(y \right)}` and we want to project the curve :math:`y = x^2` onto the surface.  When we select this option the program will automatically see that there are two variables in the 3D surface expression and put those in automatically into the variable list.  For the independent variable we will use ``t`` (any variable could be used here but if we are going to graph the space curve the program will expect the independent variable to be ``t``).  For the function we will use ``t^2``.  Once all this is in we click OK and the result is the curve (in matrix form),

.. math::
    \left[\begin{array}{c}t\\t^{2}\\\sin{\left(t \right)} + \cos{\left(t^{2} \right)}\end{array}\right]

If we plot the surface and the curve we get the following image,

.. figure:: Images/Proj001.png
    :alt: Function Projection to Surface

    Function Projection to Surface

Removing the surface to get a better look at the curve shows,

.. figure:: Images/Proj002.png
    :alt: Function Projection to Surface, Surface Removed

    Function Projection to Surface, Surface Removed

:index:`Project Point/Direction Line to Surface`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This option will project a 2D line defined by a point on the line and a 2D direction vector onto a 3D functional surface of the form :math:`z = f(x, y)`.  When this option is invoked a dialog box will appear asking the user for the variables of the 3D function to substitute, the independent variable to use the for the space curve parametrization, the 2D point on the line, and the direction vector of the line. The program will write the line equation parametrically, use the x coordinate for the first variable in the variable list given for the 3D function, and the second coordinate for the second variable in the variable list given for the 3D function.  This is all combined into a vector parametrization of the space curve.

For example, say our surface is :math:`\sin{\left(x \right)} + \cos{\left(y \right)}` and we want to project the line through :math:`(2, -3)` in the direction :math:`(1, 3)` onto the surface.  When we select this option the program will automatically see that there are two variables in the 3D surface expression and put those in automatically into the variable list.  For the independent variable we will use ``t`` (any variable could be used here but if we are going to graph the space curve the program will expect the independent variable to be ``t``).  For the point we input the list ``2, -3`` (or ``[2, -3]``) and for the direction we input the list ``1, 3`` (or ``[1, 3]``).  Once all this is in we click OK and the result is the curve (in matrix form),

.. math::
    \left[\begin{array}{c}t + 2\\3 t - 3\\\sin{\left(t + 2 \right)} + \cos{\left(3 t - 3 \right)}\end{array}\right]

If we plot the surface and the curve we get the following image,

.. figure:: Images/Proj003.png
    :alt: Line Projection to Surface

    Line Projection to Surface

Removing the surface to get a better look at the curve shows,

.. figure:: Images/Proj004.png
    :alt: Line Projection to Surface, Surface Removed

    Line Projection to Surface, Surface Removed


:index:`Project Parametric Curve to Surface`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This option will project a 2D line defined parametrically onto a 3D functional surface of the form :math:`z = f(x, y)`.  When this option is invoked a dialog box will appear asking the user for the variables of the 3D function to substitute, the ``x`` coordinate function of the 2D parametrized curve, and the ``y`` coordinate function of the 2D parametrized curve.  Although these functions can be in any variable you should use ``t`` if you plan to plot this curve.  The program will substitute the x coordinate for the first variable in the variable list given for the 3D function, and the second coordinate for the second variable in the variable list given for the 3D function.  This is all combined into a vector parametrization of the space curve.

For example, say our surface is :math:`\sin{\left(x \right)} + \cos{\left(y \right)}` and we want to project the parametric line :math:`x = 8 \cos(t)`, :math:`y = 8 \sin(t)` onto the surface.  When we select this option the program will automatically see that there are two variables in the 3D surface expression and put those in automatically into the variable list.  For the ``x`` coordinate we will use ``8*cos(t)`` and for the ``y`` coordinate we will use ``8*sin(t)``.  Once all this is in we click OK and the result is the curve (in matrix form),

.. math::
    \left[\begin{array}{c}8 \cos{\left(t \right)}\\8 \sin{\left(t \right)}\\\sin{\left(8 \cos{\left(t \right)} \right)} + \cos{\left(8 \sin{\left(t \right)} \right)}\end{array}\right]

If we plot the surface and the curve we get the following image,

.. figure:: Images/Proj005.png
    :alt: Parametric Curve Projection to Surface

    Parametric Curve Projection to Surface

Removing the surface to get a better look at the curve shows,

.. figure:: Images/Proj006.png
    :alt: Parametric Curve Projection to Surface, Surface Removed

    Parametric Curve Projection to Surface, Surface Removed


:index:`Project Polar Curve to Surface`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This option will project a 2D line defined in polar coordinates onto a 3D functional surface of the form :math:`z = f(x, y)`.  When this option is invoked a dialog box will appear asking the user for the variables of the 3D function to substitute, the independent variable to use for the space curve parametrization and polar coordinate function :math:`r = f(t) = f(\theta)`.  Although these can be in any variable you should use ``t`` if you plan to plot this curve.  The program will first parameterize the curve in rectangular coordinates, substitute the x coordinate for the first variable in the variable list given for the 3D function, and the second coordinate for the second variable in the variable list given for the 3D function.  This is all combined into a vector parametrization of the space curve.  Note that the parametrization will be in rectangular coordinates.

For example, say our surface is :math:`\sin{\left(x \right)} + \cos{\left(y \right)}` and we want to project the polar coordinate function :math:`r = 7 \sin(t) = 7 \sin(\theta)` onto the surface.  When we select this option the program will automatically see that there are two variables in the 3D surface expression and put those in automatically into the variable list.  For the variable we will use ``t`` and for the function we input ``7*sin(t)``.  Once all this is in we click OK and the result is the curve (in rectangular and matrix form),

.. math::
    \left[\begin{array}{c}7 \sin{\left(t \right)} \cos{\left(t \right)}\\7 \sin^{2}{\left(t \right)}\\\sin{\left(7 \sin{\left(t \right)} \cos{\left(t \right)} \right)} + \cos{\left(7 \sin^{2}{\left(t \right)} \right)}\end{array}\right]

If we plot the surface and the curve we get the following image,

.. figure:: Images/Proj007.png
    :alt: Polar Curve Projection to Surface

    Polar Curve Projection to Surface

Removing the surface to get a better look at the curve shows,

.. figure:: Images/Proj008.png
    :alt: Polar Curve Projection to Surface, Surface Removed

    Polar Curve Projection to Surface, Surface Removed


.. note::

    If the 3D surface does not contain exactly 2 variables they will not be automatically populated into the variable list in the dialog box.  If there are more than three variables simply input them in (independent and dependent) order with a comma between them.  If there are fewer than 2 variables then you will need to input a dummy variable to fill in one or both of the substitution slots.  For example, say our surface was :math:`z = \sin(x)` and we want to project the polar coordinate function :math:`r = 7 \sin(t) = 7 \sin(\theta)` onto the surface.  When we select the polar projection option the program will see only one variable in the expression and leave the variables box empty. For the variables we will input ``x, y`` (or ``[x, y]``), here ``y`` is our dummy variable. For the variable we will use ``t`` and for the function we input ``7*sin(t)``.  Once all this is in we click OK and the result is the curve (in rectangular and matrix form),

    .. math::
        \left[\begin{array}{c}7 \sin{\left(t \right)} \cos{\left(t \right)}\\7 \sin^{2}{\left(t \right)}\\\sin{\left(7 \sin{\left(t \right)} \cos{\left(t \right)} \right)}\end{array}\right]

    If we plot the surface and the curve we get the following image,

    .. figure:: Images/Proj009.png
        :alt: Projection to Surface Sheet

        Projection to Surface Sheet

    Removing the surface to get a better look at the curve shows,

    .. figure:: Images/Proj010.png
        :alt: Projection to Surface Sheet, Surface Removed

        Projection to Surface Sheet, Surface Removed

Variable Assumptions
--------------------

.. include:: ../CLAE/VariableAssumptions.md


