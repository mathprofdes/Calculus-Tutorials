:index:`Random Matrices`
========================

The Random Matrices options are a submenu under ``Edit > Random Matrices`` of the main program menu.

:index:`Random Integer Matrix`
------------------------------

When this option is selected a dialog box will open allowing the user to select the matrix size and the numeric bounds for the matrix entries, inclusive.  The result is a matrix of the desired size with uniformly distributed pseudo-random numbers.  The seed of the random number generator is set from the system clock.

For example, a 5 X 3 matrix with entries between 0 and 100 could be,

.. math::

    \left[\begin{array}{ccc}17 & 5 & 2\\23 & 26 & 68\\47 & 61 & 66\\51 & 61 & 84\\45 & 97 & 75\end{array}\right]

Doing the same selection again produces,

.. math::

    \left[\begin{array}{ccc}40 & 59 & 29\\82 & 100 & 11\\66 & 25 & 58\\32 & 75 & 7\\96 & 84 & 22\end{array}\right]

These are different since the seed for the generator would have changed between the matrix generations.


:index:`Random Symmetric Integer Matrix`
----------------------------------------

When this option is selected a dialog box will open allowing the user to select the matrix size (forced to be square) and the numeric bounds for the matrix entries, inclusive.  The result is a symmetric matrix of the desired size with uniformly distributed pseudo-random numbers. The seed of the random number generator is set from the system clock.

For example, a 5 X 5, with entries between :math:`-100` and 100 could be,

.. math::

    \left[\begin{array}{ccccc}-63 & 2 & 63 & 3 & 79\\2 & 33 & -1 & 57 & 28\\63 & -1 & -79 & -67 & -40\\3 & 57 & -67 & -84 & -45\\79 & 28 & -40 & -45 & -58\end{array}\right]


:index:`Random Integer Matrix with Rank`
----------------------------------------

This option is for randomly generating a matrix with a specific size and specified rank.  The way it works is that it first creates a reduced echelon form matrix of the specified rank and then performs random row operations on that matrix.  The resulting entries can become a bit large.

When this option is selected a dialog box will open allowing the user to select several options for generating the matrix.

- The number of rows and columns of the matrix.
- The desired rank of the matrix.
- The number of random row operations to do on the matrix after it is formed.
- Constant lower and upper bounds.  This numeric range is used for the entries of the original matrix and the constant multipliers for the row operations.
- The type of matrix, coefficient or augmented.
- Force a pivot to be in column 1.

The result is a matrix of the desired size and rank with uniformly distributed pseudo-random numbers. The seed of the random number generator is set from the system clock.

For example, a 5 X 7 matrix of rank 3 could be,

.. math::
    \left[\begin{array}{ccccccc}-49 & 392 & -441 & -10 & 80 & -606 & 100\\254 & -2032 & 2286 & 51 & -408 & 3107 & -469\\-392 & 3136 & -3528 & -80 & 641 & -4853 & 808\\-325 & 2600 & -2925 & -73 & 585 & -4298 & 1065\\5 & -40 & 45 & 1 & -8 & 61 & -9\end{array}\right]

If you reduce this to reduced row echelon form you get,

.. math::
    \left[\begin{array}{ccccccc}1 & -8 & 9 & 0 & 0 & 4 & 10\\0 & 0 & 0 & 1 & 0 & 1 & 5\\0 & 0 & 0 & 0 & 1 & -5 & 8\\0 & 0 & 0 & 0 & 0 & 0 & 0\\0 & 0 & 0 & 0 & 0 & 0 & 0\end{array}\right]

As was stated above, the random row operations tend to make the size of the entries rather large.


:index:`Random Floating Point Matrix`
-------------------------------------

When this option is selected a dialog box will open allowing the user to select the matrix size and the numeric bounds for the matrix entries, inclusive.  The result is a matrix of the desired size with uniformly distributed pseudo-random floating point numbers.  The seed of the random number generator is set from the system clock.

For example, a 5 X 3 matrix with entries between 0 and 100 could be,

.. math::
    \left[\begin{array}{ccc}40.7429931655636 & 31.9377144079156 & 12.7096266142081\\51.0726279216547 & 84.8672800754309 & 42.4296960261762\\47.0556275288065 & 58.3771101890111 & 4.2777694388029\\55.859433215424 & 74.357009646709 & 87.7078859801935\\94.4499803902881 & 57.3862538197089 & 20.3469321697742\end{array}\right]


:index:`Random Symmetric Floating Point Matrix`
-----------------------------------------------

When this option is selected a dialog box will open allowing the user to select the matrix size (forced to be square) and the numeric bounds for the matrix entries, inclusive.  The result is a symmetric matrix of the desired size with uniformly distributed pseudo-random numbers. The seed of the random number generator is set from the system clock.

For example, a 5 X 5, with entries between :math:`-100` and 100 could be,

.. math::

    \left[\begin{array}{ccccc}43.8667624308118 & -76.3630212378955 & -41.1401592681903 & -82.2509570841883 & 20.1140000424874\\-76.3630212378955 & 17.3864403378826 & 23.7515834591208 & 98.5733828200611 & -1.42614541677095\\-41.1401592681903 & 23.7515834591208 & 23.9623839776101 & -42.7456489319958 & 85.2633026832353\\-82.2509570841883 & 98.5733828200611 & -42.7456489319958 & -41.8736472351084 & 9.79868469552095\\20.1140000424874 & -1.42614541677095 & 85.2633026832353 & 9.79868469552095 & -36.4226027795596\end{array}\right]


:index:`Random Row Operations`
------------------------------

When this option is selected a dialog box will open allowing the user to select the number of row operations to do and the bounds on the multipliers that are used.  Note that all multipliers are integers.

For example, if we start with the matrix

.. math::

    \left[\begin{array}{ccc}5 & 6 & 10\\6 & -3 & 7\\-5 & 10 & 10\end{array}\right]

If we do 10 operations with multiplier bounds of :math:`-5` and 5 the result could be,

.. math::

    \left[\begin{array}{ccc}-3634 & 12723 & -7683\\-749 & 2623 & -1583\\-1674 & 5862 & -3538\end{array}\right]

Again, the entries can accumulate with this process.


:index:`Row Operation Pass`
---------------------------

This operation is similar to the random row operations except that a pass is considered to be operating on rows 2 - n using row 1, then rows 3 - n using row 2, etc, then using rows 1 - n-1 with row n, then rows 1 - n-2 with row n-1, etc.

For example, if we start with the matrix

.. math::

    \left[\begin{array}{ccc}5 & 6 & 10\\6 & -3 & 7\\-5 & 10 & 10\end{array}\right]

If we do a pass with multiplier bounds of :math:`-5` and 5 the result could be,

.. math::

    \left[\begin{array}{ccc}97 & 227 & 309\\58 & 138 & 186\\24 & 55 & 73\end{array}\right]


.. note::

    All random numbers in these options are being generated with a uniform distribution.  You can use other distributions to create matrices using the Spreadsheet tool for this program.
