:index:`Projections`
====================

This submenu of items is for the calculation of projections of a vector onto another vector or a vector onto a subspace spanned by a set of vectors.  These options can also calculate the orthogonal component of the projection.


:index:`Projection`
-------------------

This finds the projection of one vector onto another.  To find the projection, select the vector you wish to project, select this option, a dialog box will appear asking the user to input the vector to project onto using the CAS workspace designation, select this and click OK.  The program will then return the projection vector. For example, say we have the following two vectors in the CAS workspace,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{c}4\\5\\6\end{array}\right]

The projection of the first onto the second is,

.. math::
    \left[\begin{array}{c}\frac{128}{77}\\\frac{160}{77}\\\frac{192}{77}\end{array}\right]

:index:`Orthogonal Component`
-----------------------------

This finds the orthogonal component of the projection of one vector onto another.  To find the orthogonal component, select the vector you wish to project, select this option, a dialog box will appear asking the user to input the vector to project onto using the CAS workspace designation, select this and click OK.  The program will then return the orthogonal component vector. For example, say we have the following two vectors in the CAS workspace,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{c}4\\5\\6\end{array}\right]

The orthogonal component of the first onto the second is,

.. math::
    \left[\begin{array}{c}- \frac{51}{77}\\- \frac{6}{77}\\\frac{39}{77}\end{array}\right]


:index:`Projection and Component`
---------------------------------

This finds both the projection and orthogonal component vectors of the projection of one vector onto another.  To find the projection and orthogonal component, select the vector you wish to project, select this option, a dialog box will appear asking the user to input the vector to project onto using the CAS workspace designation, select this and click OK.  The program will then return the projection and orthogonal component vectors as separate entries in the CAS workspace. For example, say we have the following two vectors in the CAS workspace,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{c}4\\5\\6\end{array}\right]

The projection and orthogonal component of the first onto the second are,

.. math::
    \left[\begin{array}{c}\frac{128}{77}\\\frac{160}{77}\\\frac{192}{77}\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{c}- \frac{51}{77}\\- \frac{6}{77}\\\frac{39}{77}\end{array}\right]


:index:`Projection onto Subspace`
---------------------------------

This finds the projection of one vector onto the subspace spanned by a set of vectors.  To find the projection, select the vector you wish to project, select this option, a dialog box will appear asking the user to input the set of vectors to project onto using the CAS workspace designation, select this and click OK.  The program will then return the projection vector along with the orthogonal basis used during the calculation (obtained from the Gram-Schmidt method). The vector set to project onto can be given as a matrix (in which case the columns are used as the vector set) or as a list of vectors.  For example, say we have the following in the CAS workspace,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{cc}3 & 5\\2 & -1\\7 & 4\end{array}\right]

The projection of the first onto the space spanned by the columns of the second is,

.. math::
    \left[\begin{array}{c}\frac{593}{923}\\\frac{1340}{923}\\\frac{235}{71}\end{array}\right]

and the orthogonal basis used in the calculation is

.. math::
    \left[ \left[\begin{array}{c}3\\2\\7\end{array}\right], \  \left[\begin{array}{c}\frac{187}{62}\\- \frac{72}{31}\\- \frac{39}{62}\end{array}\right]\right]


:index:`Orthogonal Component to Subspace`
-----------------------------------------

This finds the orthogonal component of the projection of one vector onto the subspace spanned by a set of vectors.  To find the orthogonal component, select the vector you wish to project, select this option, a dialog box will appear asking the user to input the set of vectors to project onto using the CAS workspace designation, select this and click OK.  The program will then return the orthogonal component vector along with the orthogonal basis used during the calculation (obtained from the Gram-Schmidt method). The vector set to project onto can be given as a matrix (in which case the columns are used as the vector set) or as a list of vectors.  For example, say we have the following in the CAS workspace,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{cc}3 & 5\\2 & -1\\7 & 4\end{array}\right]

The orthogonal component of the first onto the space spanned by the columns of the second is,

.. math::
    \left[\begin{array}{c}\frac{330}{923}\\\frac{506}{923}\\- \frac{22}{71}\end{array}\right]

and the orthogonal basis used in the calculation is

.. math::
    \left[ \left[\begin{array}{c}3\\2\\7\end{array}\right], \  \left[\begin{array}{c}\frac{187}{62}\\- \frac{72}{31}\\- \frac{39}{62}\end{array}\right]\right]


:index:`Projection and Component to Subspace`
---------------------------------------------

This finds both the projection and orthogonal component of the projection of one vector onto the subspace spanned by a set of vectors.  To find the projection and orthogonal component, select the vector you wish to project, select this option, a dialog box will appear asking the user to input the set of vectors to project onto using the CAS workspace designation, select this and click OK.  The program will then return the projection and orthogonal component vectors along with the orthogonal basis used during the calculation (obtained from the Gram-Schmidt method). The vector set to project onto can be given as a matrix (in which case the columns are used as the vector set) or as a list of vectors.  For example, say we have the following in the CAS workspace,

.. math::
    \left[\begin{array}{c}1\\2\\3\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{cc}3 & 5\\2 & -1\\7 & 4\end{array}\right]

The orthogonal component of the first onto the space spanned by the columns of the second is,

.. math::
    \left[\begin{array}{c}\frac{593}{923}\\\frac{1340}{923}\\\frac{235}{71}\end{array}\right]
    \qquad {\rm and } \qquad
    \left[\begin{array}{c}\frac{330}{923}\\\frac{506}{923}\\- \frac{22}{71}\end{array}\right]

and the orthogonal basis used in the calculation is

.. math::
    \left[ \left[\begin{array}{c}3\\2\\7\end{array}\right], \  \left[\begin{array}{c}\frac{187}{62}\\- \frac{72}{31}\\- \frac{39}{62}\end{array}\right]\right]


.. note::
    In the above examples, the matrix

    .. math::
        \left[\begin{array}{cc}3 & 5\\2 & -1\\7 & 4\end{array}\right]

    could be replaced with,

    .. math::
        \left[ \left[\begin{array}{c}3\\2\\7\end{array}\right], \  \left[\begin{array}{c}5\\-1\\4\end{array}\right]\right]

    or

    .. math::
        \left[ \left[ 3, \  2, \  7\right], \  \left[ 5, \  -1, \  4\right]\right]
