
You can find these options under both the Matrix submenu and the Vector submenu, they are identical.  The options were included in both simply as a convenience.

:index:`Gram-Schmidt`
---------------------

This option returns the result of the Gram-Schmidt process on either a matrix or a set of vectors. If the input is a matrix it treats the columns of the matrix as vectors and the result is a set of vectors that are the result of the Gram-Schmidt process.  If the input is a set of vectors, the result, as with the matrix, is also a set of vectors.  For example, say we start with, 

.. math::
    \left[\begin{array}{ccc}10 & -4 & -3\\7 & -3 & -10\\-1 & 4 & -9\end{array}\right]

the result of this process is, 

.. math::
    \left[ \left[\begin{array}{c}10\\7\\-1\end{array}\right], \  \left[\begin{array}{c}\frac{1}{3}\\\frac{1}{30}\\\frac{107}{30}\end{array}\right], \  \left[\begin{array}{c}\frac{303}{77}\\- \frac{10908}{1925}\\- \frac{606}{1925}\end{array}\right]\right]

Note that if we had started with 

.. math::
    \left[ \left[\begin{array}{c}10\\7\\-1\end{array}\right], \  \left[\begin{array}{c}-4\\-3\\4\end{array}\right], \  \left[\begin{array}{c}-3\\-10\\-9\end{array}\right]\right]

we would get the same result.  

:index:`Normalized Gram-Schmidt`
--------------------------------

This option returns the result of the Gram-Schmidt process, with the vectors normalized, on either a matrix or a set of vectors. If the input is a matrix it treats the columns of the matrix as vectors and the result is a set of vectors that are the result of the normalized Gram-Schmidt process.  If the input is a set of vectors, the result, as with the matrix, is also a set of vectors.  For example, say we start with, 

.. math::
    \left[\begin{array}{ccc}10 & -4 & -3\\7 & -3 & -10\\-1 & 4 & -9\end{array}\right]

the result of this process is, 

.. math::
    \left[ \left[\begin{array}{c}\frac{\sqrt{6}}{3}\\\frac{7 \sqrt{6}}{30}\\- \frac{\sqrt{6}}{30}\end{array}\right], \  \left[\begin{array}{c}\frac{\sqrt{462}}{231}\\\frac{\sqrt{462}}{2310}\\\frac{107 \sqrt{462}}{2310}\end{array}\right], \  \left[\begin{array}{c}\frac{5 \sqrt{77}}{77}\\- \frac{36 \sqrt{77}}{385}\\- \frac{2 \sqrt{77}}{385}\end{array}\right]\right]

Note that if we had started with 

.. math::
    \left[ \left[\begin{array}{c}10\\7\\-1\end{array}\right], \  \left[\begin{array}{c}-4\\-3\\4\end{array}\right], \  \left[\begin{array}{c}-3\\-10\\-9\end{array}\right]\right]

we would get the same result.  
