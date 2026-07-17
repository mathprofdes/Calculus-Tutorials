:index:`Matrix Spaces`
======================

These options return bases sets for the three matrix spaces usually covered in an introductory linear algebra class, the Null Space, Column Space, and Row Space.

:index:`Null Space`
-------------------

This option returns a basis for the Null Space of a matrix as a list of vectors.  For example, given the matrix,

.. math::
    \left[\begin{array}{ccccc}-10 & 0 & 8 & 7 & -2\\-4 & 8 & -1 & 4 & 3\\6 & 6 & -1 & -3 & 1\end{array}\right]

the Null Space option will return,

.. math::
    \left[ \left[\begin{array}{c}\frac{185}{278}\\- \frac{24}{139}\\- \frac{6}{139}\\1\\0\end{array}\right], \  \left[\begin{array}{c}\frac{21}{139}\\- \frac{34}{139}\\\frac{61}{139}\\0\\1\end{array}\right]\right]

:index:`Column Space`
---------------------

This option returns a basis for the Column Space of a matrix as a list of vectors.  For example, given the matrix,

.. math::
    \left[\begin{array}{ccccccc}50 & 150 & -1863 & 0 & 3526 & 0 & -12691\\292 & 876 & 3700 & -180 & -7668 & 36 & 28700\\0 & 0 & -81 & 1 & 157 & 0 & -573\\-70 & -210 & -21285 & 295 & 41375 & -59 & -150724\\7 & 21 & 2169 & -30 & -4216 & 6 & 15358\end{array}\right]

the Column Space option will return,

.. math::
    \left[ \left[\begin{array}{c}50\\292\\0\\-70\\7\end{array}\right], \  \left[\begin{array}{c}-1863\\3700\\-81\\-21285\\2169\end{array}\right], \  \left[\begin{array}{c}0\\-180\\1\\295\\-30\end{array}\right], \  \left[\begin{array}{c}0\\36\\0\\-59\\6\end{array}\right]\right]

Note that the reduced echelon form for this matrix is

.. math::
    \left[\begin{array}{ccccccc}1 & 3 & 0 & 0 & -4 & 0 & 7\\0 & 0 & 1 & 0 & -2 & 0 & 7\\0 & 0 & 0 & 1 & -5 & 0 & -6\\0 & 0 & 0 & 0 & 0 & 1 & -9\\0 & 0 & 0 & 0 & 0 & 0 & 0\end{array}\right]

:index:`Row Space`
------------------

This option returns a basis for the Row Space of a matrix as a list of vectors.  For example, given the matrix,

.. math::
    \left[\begin{array}{ccccccc}50 & 150 & -1863 & 0 & 3526 & 0 & -12691\\292 & 876 & 3700 & -180 & -7668 & 36 & 28700\\0 & 0 & -81 & 1 & 157 & 0 & -573\\-70 & -210 & -21285 & 295 & 41375 & -59 & -150724\\7 & 21 & 2169 & -30 & -4216 & 6 & 15358\end{array}\right]

the Row Space option will return,

.. math::
    \left[ \left[\begin{array}{ccccccc}50 & 150 & -1863 & 0 & 3526 & 0 & -12691\end{array}\right], \  \left[\begin{array}{ccccccc}0 & 0 & 728996 & -9000 & -1412992 & 1800 & 5140772\end{array}\right], \  \left[\begin{array}{ccccccc}0 & 0 & 0 & -4 & 20 & 145800 & -1312176\end{array}\right], \  \left[\begin{array}{ccccccc}0 & 0 & 0 & 0 & 0 & -109495199200 & 985456792800\end{array}\right]\right]

and if you prefer these as column vectors you can transpose the list to

.. math::
    \left[ \left[\begin{array}{c}50\\150\\-1863\\0\\3526\\0\\-12691\end{array}\right], \  \left[\begin{array}{c}0\\0\\728996\\-9000\\-1412992\\1800\\5140772\end{array}\right], \  \left[\begin{array}{c}0\\0\\0\\-4\\20\\145800\\-1312176\end{array}\right], \  \left[\begin{array}{c}0\\0\\0\\0\\0\\-109495199200\\985456792800\end{array}\right]\right]

Note that the reduced echelon form for this matrix is

.. math::
    \left[\begin{array}{ccccccc}1 & 3 & 0 & 0 & -4 & 0 & 7\\0 & 0 & 1 & 0 & -2 & 0 & 7\\0 & 0 & 0 & 1 & -5 & 0 & -6\\0 & 0 & 0 & 0 & 0 & 1 & -9\\0 & 0 & 0 & 0 & 0 & 0 & 0\end{array}\right]

