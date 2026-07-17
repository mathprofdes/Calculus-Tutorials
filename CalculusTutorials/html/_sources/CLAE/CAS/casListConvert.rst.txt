:index:`Convert List`
=====================

This submenu contains options for doing some list conversions as well as converting lists to matrices.

Flatten List
------------

This will take a list of lists and flatten it to a single list of entries with no list nesting.

For example, if our list is

.. math::

    \left[ 2, \  \left[ 3, \  4, \  5\right], \  \left[ a, \  b, \  c, \  \left[ d, \  e\right], \  f\right], \  \left[ x, \  \left[ y, \  z\right]\right]\right]

this option will produce,

.. math::

    \left[ 2, \  3, \  4, \  5, \  a, \  b, \  c, \  d, \  e, \  f, \  x, \  y, \  z\right]

Flat List to Matrix by Row
--------------------------

This option will take a flat list (no nesting) and create a matrix from the entries going across the rows.  When selected, a dialog box will appear asking for the number of columns.  The new matrix will have that number of columns and the list entries will populate each row to the end and then start a new row.  Any matrix entries that are missing will be replaced with 0s.

For example, if our list is,

.. math::

    \left[ 2, \  3, \  4, \  5, \  a, \  b, \  c, \  d, \  e, \  f, \  x, \  y, \  z\right]

and we select 4 for our columns the result will be,

.. math::

    \left[\begin{array}{cccc}2 & 3 & 4 & 5\\a & b & c & d\\e & f & x & y\\z & 0 & 0 & 0\end{array}\right]

Note that if the list is not flat this option will flatten the list before it converts the list to a matrix.  So had we started with the list,

.. math::

    \left[ 2, \  \left[ 3, \  4, \  5\right], \  \left[ a, \  b, \  c, \  \left[ d, \  e\right], \  f\right], \  \left[ x, \  \left[ y, \  z\right]\right]\right]

we would have gotten the same result.

Flat List to Matrix by Column
-----------------------------

This option will take a flat list (no nesting) and create a matrix from the entries going down the columns.  When selected, a dialog box will appear asking for the number of rows.  The new matrix will have that number of columns and the list entries will populate each row to the end and then start a new row.  Any matrix entries that are missing will be replaced with 0s.

For example, if our list is,

.. math::

    \left[ 2, \  3, \  4, \  5, \  a, \  b, \  c, \  d, \  e, \  f, \  x, \  y, \  z\right]

and we select 4 for our rows the result will be,

.. math::

    \left[\begin{array}{cccc}2 & a & e & z\\3 & b & f & 0\\4 & c & x & 0\\5 & d & y & 0\end{array}\right]

Note that if the list is not flat this option will flatten the list before it converts the list to a matrix.  So had we started with the list,

.. math::

    \left[ 2, \  \left[ 3, \  4, \  5\right], \  \left[ a, \  b, \  c, \  \left[ d, \  e\right], \  f\right], \  \left[ x, \  \left[ y, \  z\right]\right]\right]

we would have gotten the same result.

.. math::

    \left[\begin{array}{cccc}2 & a & e & z\\3 & b & f & 0\\4 & c & x & 0\\5 & d & y & 0\end{array}\right]

List of Lists to Matrix by Row
------------------------------

This option will take a list of lists and convert it to a matrix using the list elements as rows.  If the list element is not a list the program will see it as a list with one element.  Also if the list element is a nested list it will be flattened before converted to a row of the matrix.  The size of the matrix is determined by the sizes of the list elements.  The number of rows is the number of list elements and the number of columns is the largest length of the nested lists (after flattening).  Any empty matrix entries are replaced by 0s.

For example, if our list is,

.. math::

    \left[ 2, \  \left[ 3, \  4, \  5\right], \  \left[ a, \  b, \  c, \  \left[ d, \  e\right], \  f\right], \  \left[ x, \  \left[ y, \  z\right]\right]\right]

then this option produces,

.. math::

    \left[\begin{array}{cccccc}2 & 0 & 0 & 0 & 0 & 0\\3 & 4 & 5 & 0 & 0 & 0\\a & b & c & d & e & f\\x & y & z & 0 & 0 & 0\end{array}\right]

List of Lists to Matrix by Column
---------------------------------

This option will take a list of lists and convert it to a matrix using the list elements as columns.  If the list element is not a list the program will see it as a list with one element.  Also if the list element is a nested list it will be flattened before converted to a column of the matrix.  The size of the matrix is determined by the sizes of the list elements.  The number of columns is the number of list elements and the number of rows is the largest length of the nested lists (after flattening).  Any empty matrix entries are replaced by 0s.

For example, if our list is,

.. math::

    \left[ 2, \  \left[ 3, \  4, \  5\right], \  \left[ a, \  b, \  c, \  \left[ d, \  e\right], \  f\right], \  \left[ x, \  \left[ y, \  z\right]\right]\right]

then this option produces,

.. math::

    \left[\begin{array}{cccc}2 & 3 & a & x\\0 & 4 & b & y\\0 & 5 & c & z\\0 & 0 & d & 0\\0 & 0 & e & 0\\0 & 0 & f & 0\end{array}\right]

