:index:`Convert Matrix`
=======================

These conversions are to change a matrix into various list structures.


Matrix to Flat List by Row
--------------------------

A flat list is one that is not a nested list structure.  This option will convert the matrix to a single list going across the rows.

For example, if we have the matrix,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

This option will create the following list,

.. math::

    \left[ 1, \  4, \  7, \  2, \  5, \  8, \  3, \  6, \  9\right]


Matrix to Flat List by Column
-----------------------------

A flat list is one that is not a nested list structure.  This option will convert the matrix to a single list going down the columns.

For example, if we have the matrix,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

This option will create the following list,

.. math::

    \left[ 1, \  2, \  3, \  4, \  5, \  6, \  7, \  8, \  9\right]


Matrix to List by Rows
----------------------

This option will convert the list to a list of lists.  The nested lists are the rows of the matrix in list form.

For example, if we have the matrix,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

This option will create the following list,

.. math::

    \left[ \left[ 1, \  4, \  7\right], \  \left[ 2, \  5, \  8\right], \  \left[ 3, \  6, \  9\right]\right]


Matrix to List by Columns
-------------------------

This option will convert the list to a list of lists.  The nested lists are the columns of the matrix in list form.

For example, if we have the matrix,

.. math::

    \left[\begin{array}{ccc}1 & 4 & 7\\2 & 5 & 8\\3 & 6 & 9\end{array}\right]

This option will create the following list,

.. math::

    \left[ \left[ 1, \  2, \  3\right], \  \left[ 4, \  5, \  6\right], \  \left[ 7, \  8, \  9\right]\right]
