
The lines and planes options are for constructing lines in two and three dimensions and planes in three dimensions that are defined by one or two vectors or two or three points.  While it would only take a few steps to do this without these options they are included as a convenience to allow the user to produce them quickly.

:index:`Line from Vector`
-------------------------

This creates a line from vector.  Inputs can be either a single list of two or three values or a column vector with two or three rows.

Two-Dimensional Vector
^^^^^^^^^^^^^^^^^^^^^^

The input for the two dimensional vector can be a list of two values or a column vector with two rows. For example,  :math:`\left[ 1, \  2\right]` or :math:`\left[\begin{array}{c}1\\2\end{array}\right].`  When this option is invoked a dialog box will appear asking the user to specify the output type.  The output options are as follows.

Function: y = mx + b
""""""""""""""""""""

Returns the line in function form.  For example, if the input is :math:`\left[ 1, \  2\right]` or :math:`\left[\begin{array}{c}1\\2\end{array}\right]` the output is :math:`2 x`.

General: ax + by + c = 0
""""""""""""""""""""""""

Returns the line in general (implicit) form.  For example, if the input is :math:`\left[ 1, \  2\right]` or :math:`\left[\begin{array}{c}1\\2\end{array}\right]` the output is :math:`- 2 x + y` meaning :math:`- 2 x + y = 0`.

Parametric: [x(t), y(t)]
""""""""""""""""""""""""

Returns the line in parametric form using ``t`` as the parameter.  For example, if the input is :math:`\left[ 1, \  2\right]` or :math:`\left[\begin{array}{c}1\\2\end{array}\right]` the output is :math:`\left[\begin{array}{c}t\\2 t\end{array}\right].`

Matrix/Linear System
""""""""""""""""""""

Returns the line as a linear system, row matrix.  For example, if the input is :math:`\left[ 1, \  2\right]` or :math:`\left[\begin{array}{c}1\\2\end{array}\right]` the output is :math:`\left[\begin{array}{ccc}-2 & 1 & 0\end{array}\right]`, meaning :math:`- 2 x + y = 0`.


Three-Dimensional Vector
^^^^^^^^^^^^^^^^^^^^^^^^

The input for the three dimensional vector can be a list of three values or a column vector with three rows. For example,  :math:`\left[ 1, \  2, \ 3\right]` or :math:`\left[\begin{array}{c}1\\2\\3\end{array}\right].` The output will be as parametric equations with parameter ``t`` given as a three-dimensional column vector.  For example, if the input is, :math:`\left[ 1, \  2, \ 3\right]` or :math:`\left[\begin{array}{c}1\\2\\3\end{array}\right]` the output is :math:`\left[\begin{array}{c}t\\2 t\\3 t\end{array}\right].`


:index:`Line Between Two Points`
--------------------------------

This creates a line through two points.  Inputs can be either a single list of two points given in either list or matrix form, or a combination of them, or as a matrix with two columns and either two or three rows. In the matrix case, the points are taken as the columns of the matrix.

Two-Dimensional Points
^^^^^^^^^^^^^^^^^^^^^^

The input for the two dimensional points can be a list of two points given in either list or matrix form, or a combination of them, or as a matrix with two rows and two columns.  For example,  the following are all equivalent to inputting the two points, :math:`(1, 2)` and :math:`(3, 4).`

- :math:`\left[ \left[ 1, \  2\right], \left[ 3, \  4\right] \right]`
- :math:`\left[ \left[\begin{array}{c}1\\2\end{array}\right], \left[ 3, \  4\right] \right]`
- :math:`\left[ \left[ 1, \  2\right], \left[\begin{array}{c}3\\4\end{array}\right] \right]`
- :math:`\left[ \left[\begin{array}{c}1\\2\end{array}\right], \left[\begin{array}{c}3\\4\end{array}\right] \right]`
- :math:`\left[\begin{array}{cc}1 & 3\\2 & 4\end{array}\right]`

When this option is invoked a dialog box will appear asking the user to specify the output type.  The output options are as follows.

Function: y = mx + b
""""""""""""""""""""

Returns the line in function form.  For example, if the input is :math:`\left[ \left[ 1, \  2\right], \left[ 3, \  4\right] \right]` the output is :math:`x + 1`.

General: ax + by + c = 0
""""""""""""""""""""""""

Returns the line in general (implicit) form.  For example, if the input is :math:`\left[ \left[ 1, \  2\right], \left[ 3, \  4\right] \right]` the output is :math:`- 2 x + 2 y - 2` meaning :math:`- 2 x + 2 y - 2 = 0`.

Parametric: [x(t), y(t)]
""""""""""""""""""""""""

Returns the line in parametric form using ``t`` as the parameter.  For example, if the input is :math:`\left[ \left[ 1, \  2\right], \left[ 3, \  4\right] \right]` the output is :math:`\left[\begin{array}{c}2 t + 1\\2 t + 2\end{array}\right]`.


Matrix/Linear System
""""""""""""""""""""

Returns the line as a linear system, row matrix.   For example, if the input is :math:`\left[ \left[ 1, \  2\right], \left[ 3, \  4\right] \right]` the output is :math:`\left[\begin{array}{ccc}-2 & 2 & 2\end{array}\right]` meaning :math:`- 2 x + 2 y = 2`.


Three-Dimensional Points
^^^^^^^^^^^^^^^^^^^^^^^^

The input for the three dimensional points can be a list of two points given in either list or matrix form, or a combination of them, or as a matrix with three rows and two columns.  For example,  the following are all equivalent to inputting the two points, :math:`(1, 2, 3)` and :math:`(4, 5, 6).`

- :math:`\left[ \left[ 1, \  2, \ 3\right], \left[ 4, \  5, \ 6\right] \right]`
- :math:`\left[ \left[\begin{array}{c}1\\2\\3\end{array}\right], \left[ 4, \  5, \ 6\right] \right]`
- :math:`\left[ \left[ 1, \  2, \ 3\right], \left[\begin{array}{c}4\\5\\6\end{array}\right] \right]`
- :math:`\left[ \left[\begin{array}{c}1\\2\\3\end{array}\right], \left[\begin{array}{c}4\\5\\6\end{array}\right] \right]`
- :math:`\left[\begin{array}{cc}1 & 4\\2 & 5\\3 & 6\end{array}\right]`

The output will be as parametric equations with parameter ``t`` given as a three-dimensional column vector.  For example, if the input is, :math:`\left[ \left[ 1, \  2, \ 3\right], \left[ 4, \  5, \ 6\right] \right]` the output is :math:`\left[\begin{array}{c}3 t + 1\\3 t + 2\\3 t + 3\end{array}\right].`


:index:`Plane from Vectors`
---------------------------

The input can be a list of two vectors given in either list or matrix form, or a combination of them, or as a matrix with three rows and two columns.  For example,  the following are all equivalent to inputting the two points, :math:`(1, 2, 3)` and :math:`(4, 5, 6).`

- :math:`\left[ \left[ 1, \  2, \ 3\right], \left[ 4, \  5, \ 6\right] \right]`
- :math:`\left[ \left[\begin{array}{c}1\\2\\3\end{array}\right], \left[ 4, \  5, \ 6\right] \right]`
- :math:`\left[ \left[ 1, \  2, \ 3\right], \left[\begin{array}{c}4\\5\\6\end{array}\right] \right]`
- :math:`\left[ \left[\begin{array}{c}1\\2\\3\end{array}\right], \left[\begin{array}{c}4\\5\\6\end{array}\right] \right]`
- :math:`\left[\begin{array}{cc}1 & 4\\2 & 5\\3 & 6\end{array}\right]`


General: ax + by + cz + d = 0
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The output is in general (implicit) form, :math:`ax + by + cz + d = 0.` For example, if the input is, :math:`\left[ \left[ 8, \  2, \  -3\right], \  \left[ -4, \  5, \  6\right]\right]` the output is :math:`27 x - 36 y + 48 z` meaning :math:`27 x - 36 y + 48 z = 0`.

Matrix/Linear System
^^^^^^^^^^^^^^^^^^^^

Returns the line as a linear system, row matrix.  For example, if the input is, :math:`\left[ \left[ 8, \  2, \  -3\right], \  \left[ -4, \  5, \  6\right]\right]` the output is :math:`\left[\begin{array}{cccc}27 & -36 & 48 & 0\end{array}\right]` meaning :math:`27 x - 36 y + 48 z = 0`.


:index:`Plane Containing Three Points`
--------------------------------------

The input can be a list of three vectors given in either list or matrix form, or a combination of them, or as a matrix with three rows and three columns.

General: ax + by + cz + d = 0
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The output is in general (implicit) form, :math:`ax + by + cz + d = 0.` For example, if the input is, :math:`\left[ \left[ 8, \  2, \  -3\right], \  \left[ -4, \  5, \  6\right], \  \left[ 5, \  -9, \  -7\right]\right]` the output is :math:`87 x - 75 y + 141 z - 123` meaning :math:`87 x - 75 y + 141 z - 123 = 0`.

Matrix/Linear System
^^^^^^^^^^^^^^^^^^^^

Returns the line as a linear system, row matrix.  For example, if the input is, :math:`\left[ \left[ 8, \  2, \  -3\right], \  \left[ -4, \  5, \  6\right], \  \left[ 5, \  -9, \  -7\right]\right]` the output is :math:`\left[\begin{array}{cccc}87 & -75 & 141 & 123\end{array}\right]` meaning :math:`87 x - 75 y + 141 z = 123`.
