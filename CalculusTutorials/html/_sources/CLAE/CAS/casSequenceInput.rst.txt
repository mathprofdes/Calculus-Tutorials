:index:`Sequence Input`
=======================

A sequence here is a finite list of values.  There are many instances where operating on a list will save a substantial amount of time and many of the options in this program will be applied to list entries automatically.  There are two options for creating a sequence list.

Specifying Start and Step
-------------------------

When selected, a dialog box will appear asking the user for the starting value, a step value, and the number of values to create for the list.  The start and step values can be any syntactically correct expression and may include CAS designations (e.g. ``R1``, ``R2``, etc.).

For example, a start of 3, step of 1/2 and 15 values returns the list,

.. math::
    \left[ 3, \  \frac{7}{2}, \  4, \  \frac{9}{2}, \  5, \  \frac{11}{2}, \  6, \  \frac{13}{2}, \  7, \  \frac{15}{2}, \  8, \  \frac{17}{2}, \  9, \  \frac{19}{2}, \  10\right]

For example, a start of 3, step of 0.5 and 15 values returns the list,

.. math::
    \left[ 3, \  3.5, \  4.0, \  4.5, \  5.0, \  5.5, \  6.0, \  6.5, \  7.0, \  7.5, \  8.0, \  8.5, \  9.0, \  9.5, \  10.0\right]

For example, a start of a, step of b and 10 values returns the list,

.. math::
    \left[ a, \  a + b, \  a + 2 b, \  a + 3 b, \  a + 4 b, \  a + 5 b, \  a + 6 b, \  a + 7 b, \  a + 8 b, \  a + 9 b\right]

Specifying an Interval and Number of Divisions
----------------------------------------------

This is a nice feature for creating evenly-spaced divisions in an interval.  When selected, a dialog box will appear asking the user to input the starting and ending values for the interval and the number of divisions to create.  Note that this is the number of divisions, not the number of values produced.  So if you select 10 divisions you will get a list of 11 numbers, since we include the endpoints. The start and stop values can be any syntactically correct expression and may include CAS designations (e.g. ``R1``, ``R2``, etc.).

For example, a start of 3, stop of 10, and 10 divisions returns the list,

.. math::
    \left[ 3, \  \frac{37}{10}, \  \frac{22}{5}, \  \frac{51}{10}, \  \frac{29}{5}, \  \frac{13}{2}, \  \frac{36}{5}, \  \frac{79}{10}, \  \frac{43}{5}, \  \frac{93}{10}, \  10\right]

For example, a start of a, stop of b, and 10 divisions returns the list,

.. math::
    \left[ a, \  \frac{9 a}{10} + \frac{b}{10}, \  \frac{4 a}{5} + \frac{b}{5}, \  \frac{7 a}{10} + \frac{3 b}{10}, \  \frac{3 a}{5} + \frac{2 b}{5}, \  \frac{a}{2} + \frac{b}{2}, \  \frac{2 a}{5} + \frac{3 b}{5}, \  \frac{3 a}{10} + \frac{7 b}{10}, \  \frac{a}{5} + \frac{4 b}{5}, \  \frac{a}{10} + \frac{9 b}{10}, \  b\right]
