:index:`Factorizations`
=======================

There are many matrix factorizations for matrices but most of them are studied in advanced courses in linear algebra.  Here we look at a few factorizations that are more common for introductory linear algebra classes.

:index:`LU Decomposition`
-------------------------

This option does an LU decomposition of the selected matrix :math:`A` and returns the two matrices L and U as two separate entries in the CAS workspace.  In some cases a permutation matrix P will also be returned.  If a P matrix is returned then :math:`PA = LU`, and if no P matrix is returned then :math:`A = LU`.  We will look at a few examples, in each case you can multiply the L and U matrices to see we get back to the original.

The LU decomposition of

.. math::
    \left[\begin{array}{ccc}8 & -10 & -5\\2 & 17 & 2\\-9 & -18 & 4\end{array}\right]

gives us,

.. math::
    L = \left[\begin{array}{ccc}1 & 0 & 0\\\frac{1}{4} & 1 & 0\\- \frac{9}{8} & - \frac{3}{2} & 1\end{array}\right]
    \qquad
    U = \left[\begin{array}{ccc}8 & -10 & -5\\0 & \frac{39}{2} & \frac{13}{4}\\0 & 0 & \frac{13}{4}\end{array}\right]

The LU decomposition of

.. math::
    \left[\begin{array}{ccccc}1 & -5 & 5 & -10 & -3\\-5 & -6 & -7 & -10 & 6\\-9 & -6 & 4 & -6 & 9\end{array}\right]

gives us,

.. math::
    L = \left[\begin{array}{ccc}1 & 0 & 0\\-5 & 1 & 0\\-9 & \frac{51}{31} & 1\end{array}\right]
    \qquad
    U = \left[\begin{array}{ccccc}1 & -5 & 5 & -10 & -3\\0 & -31 & 18 & -60 & -9\\0 & 0 & \frac{601}{31} & \frac{84}{31} & - \frac{99}{31}\end{array}\right]

The LU decomposition of

.. math::
    \left[\begin{array}{ccc}1 & -5 & -9\\-5 & -6 & -6\\5 & -7 & 4\\-10 & -10 & -6\\-3 & 6 & 9\end{array}\right]

gives us,

.. math::
    L = \left[\begin{array}{ccccc}1 & 0 & 0 & 0 & 0\\-5 & 1 & 0 & 0 & 0\\5 & - \frac{18}{31} & 1 & 0 & 0\\-10 & \frac{60}{31} & \frac{84}{601} & 1 & 0\\-3 & \frac{9}{31} & - \frac{99}{601} & 0 & 1\end{array}\right]
    \qquad
    U = \left[\begin{array}{ccc}1 & -5 & -9\\0 & -31 & -51\\0 & 0 & \frac{601}{31}\\0 & 0 & 0\\0 & 0 & 0\end{array}\right]

.. note::
    In some cases the rows of a matrix need to be permuted in order to complete the LU decomposition.  In these cases this option will return a third, permutation, matrix P such that :math:`PA = LU`.  For example, if we start with the matrix,

    .. math::
        \left[\begin{array}{ccc}0 & 4 & 3\\-4 & -6 & -3\\3 & 3 & 1\end{array}\right]

    the LU decomposition returns the three matrices,

    .. math::
        L = \left[\begin{array}{ccc}1 & 0 & 0\\0 & 1 & 0\\- \frac{3}{4} & - \frac{3}{8} & 1\end{array}\right]
        \qquad
        U = \left[\begin{array}{ccc}-4 & -6 & -3\\0 & 4 & 3\\0 & 0 & - \frac{1}{8}\end{array}\right]
        \qquad
        P = \left[\begin{array}{ccc}0 & 1 & 0\\1 & 0 & 0\\0 & 0 & 1\end{array}\right]

    multiplying we have,

    .. math::
        \left[\begin{array}{ccc}1 & 0 & 0\\0 & 1 & 0\\- \frac{3}{4} & - \frac{3}{8} & 1\end{array}\right]
        \left[\begin{array}{ccc}-4 & -6 & -3\\0 & 4 & 3\\0 & 0 & - \frac{1}{8}\end{array}\right]
        = \left[\begin{array}{ccc}0 & 1 & 0\\1 & 0 & 0\\0 & 0 & 1\end{array}\right]
        \left[\begin{array}{ccc}0 & 4 & 3\\-4 & -6 & -3\\3 & 3 & 1\end{array}\right]
        = \left[\begin{array}{ccc}-4 & -6 & -3\\0 & 4 & 3\\3 & 3 & 1\end{array}\right]


:index:`LDU Decomposition`
--------------------------

This option does an LDU decomposition of the selected matrix :math:`A` and returns the three matrices L, D, and U as three separate entries in the CAS workspace.  In this factorization, :math:`L` has 1s on the main diagonal, :math:`U` has 1s (or 0s) on the main diagonal, and :math:`D` is a diagonal matrix.  In some cases a permutation matrix P will also be returned.  If a P matrix is returned then :math:`PA = LDU,` and if no P matrix is returned then :math:`A = LDU.`  We will look at a few examples, in each case you can multiply the L, D, and U matrices to see we get back to the original.

The LDU decomposition of

.. math::
    \left[\begin{array}{ccc}9 & 10 & -1\\0 & -6 & -8\\-6 & 4 & 9\end{array}\right]

is

.. math::
    \left[\begin{array}{ccc}1 & 0 & 0\\0 & 1 & 0\\- \frac{2}{3} & - \frac{16}{9} & 1\end{array}\right]
    \qquad
    \left[\begin{array}{ccc}9 & 0 & 0\\0 & -6 & 0\\0 & 0 & - \frac{53}{9}\end{array}\right]
    \qquad
    \left[\begin{array}{ccc}1 & \frac{10}{9} & - \frac{1}{9}\\0 & 1 & \frac{4}{3}\\0 & 0 & 1\end{array}\right]

The LDU decomposition of

.. math::
    \left[\begin{array}{ccccc}3 & -10 & 4 & 0 & 10\\6 & 7 & 2 & 8 & -6\\-4 & -4 & 9 & 9 & -8\end{array}\right]

is

.. math::
    \left[\begin{array}{ccc}1 & 0 & 0\\2 & 1 & 0\\- \frac{4}{3} & - \frac{52}{81} & 1\end{array}\right]
    \qquad
    \left[\begin{array}{ccc}3 & 0 & 0\\0 & 27 & 0\\0 & 0 & \frac{283}{27}\end{array}\right]
    \qquad
    \left[\begin{array}{ccccc}1 & - \frac{10}{3} & \frac{4}{3} & 0 & \frac{10}{3}\\0 & 1 & - \frac{2}{9} & \frac{8}{27} & - \frac{26}{27}\\0 & 0 & 1 & \frac{1145}{849} & - \frac{920}{849}\end{array}\right]

The LDU decomposition of

.. math::
    \left[\begin{array}{ccc}4 & 9 & 1\\7 & -1 & -2\\10 & -9 & -7\\10 & -2 & 5\\-9 & 0 & 2\\10 & -8 & -8\end{array}\right]

is

.. math::
    \left[\begin{array}{cccccc}1 & 0 & 0 & 0 & 0 & 0\\\frac{7}{4} & 1 & 0 & 0 & 0 & 0\\\frac{5}{2} & \frac{126}{67} & 1 & 0 & 0 & 0\\\frac{5}{2} & \frac{98}{67} & - \frac{535}{164} & 1 & 0 & 0\\- \frac{9}{4} & - \frac{81}{67} & \frac{19}{164} & 0 & 1 & 0\\\frac{5}{2} & \frac{122}{67} & \frac{3}{2} & 0 & 0 & 1\end{array}\right]
    \qquad
    \left[\begin{array}{cccccc}4 & 0 & 0 & 0 & 0 & 0\\0 & - \frac{67}{4} & 0 & 0 & 0 & 0\\0 & 0 & - \frac{164}{67} & 0 & 0 & 0\\0 & 0 & 0 & 1 & 0 & 0\\0 & 0 & 0 & 0 & 1 & 0\\0 & 0 & 0 & 0 & 0 & 1\end{array}\right]
    \qquad
    \left[\begin{array}{ccc}1 & \frac{9}{4} & \frac{1}{4}\\0 & 1 & \frac{15}{67}\\0 & 0 & 1\\0 & 0 & 0\\0 & 0 & 0\\0 & 0 & 0\end{array}\right]


:index:`Fraction Free LU Decomposition`
---------------------------------------

This option does a fraction-free LU decomposition of the selected matrix, :math:`A`. It returns 4 matrices, :math:`P`, :math:`L`, :math:`D`, and :math:`U`, such that :math:`PA = L D^{-1} U`. For example, the fraction free LU decomposition of

.. math::
    \left[\begin{array}{ccc}8 & -10 & -5\\2 & 17 & 2\\-9 & -18 & 4\end{array}\right]

gives us,

.. math::
    P = \left[\begin{array}{ccc}1 & 0 & 0\\0 & 1 & 0\\0 & 0 & 1\end{array}\right]
    \qquad
    L = \left[\begin{array}{ccc}8 & 0 & 0\\2 & 156 & 0\\-9 & -234 & 1\end{array}\right]
    \qquad
    D = \left[\begin{array}{ccc}8 & 0 & 0\\0 & 1248 & 0\\0 & 0 & 156\end{array}\right]
    \qquad
    U = \left[\begin{array}{ccc}8 & -10 & -5\\0 & 156 & 26\\0 & 0 & 507\end{array}\right]

Checking,

.. math::
    \left[\begin{array}{ccc}8 & 0 & 0\\2 & 156 & 0\\-9 & -234 & 1\end{array}\right] \left[\begin{array}{ccc}8 & 0 & 0\\0 & 1248 & 0\\0 & 0 & 156\end{array}\right]^{-1} \left[\begin{array}{ccc}8 & -10 & -5\\0 & 156 & 26\\0 & 0 & 507\end{array}\right] = \left[\begin{array}{ccc}8 & -10 & -5\\2 & 17 & 2\\-9 & -18 & 4\end{array}\right]


:index:`QR Decomposition`
-------------------------

This option does a QR decomposition of the selected matrix, :math:`A`, and returns the two matrices Q and R as two separate entries in the CAS workspace.  The matrix :math:`U` is a  column orthogonal matrix and the matrix :math:`R` is an upper triangular matrix, and of course :math:`A = QR`.  We will look at a few examples, in each case you can multiply the Q and R matrices to see we get back to the original.

The QR decomposition of

.. math::
    \left[\begin{array}{ccc}8 & -10 & -5\\2 & 17 & 2\\-9 & -18 & 4\end{array}\right]

gives us,

.. math::
    Q = \left[\begin{array}{ccc}\frac{8 \sqrt{149}}{149} & - \frac{62 \sqrt{9089}}{9089} & \frac{3 \sqrt{61}}{61}\\\frac{2 \sqrt{149}}{149} & \frac{59 \sqrt{9089}}{9089} & \frac{6 \sqrt{61}}{61}\\- \frac{9 \sqrt{149}}{149} & - \frac{42 \sqrt{9089}}{9089} & \frac{4 \sqrt{61}}{61}\end{array}\right]
    \qquad
    R = \left[\begin{array}{ccc}\sqrt{149} & \frac{116 \sqrt{149}}{149} & - \frac{72 \sqrt{149}}{149}\\0 & \frac{39 \sqrt{9089}}{149} & \frac{260 \sqrt{9089}}{9089}\\0 & 0 & \frac{13 \sqrt{61}}{61}\end{array}\right]

The QR decomposition of

.. math::
    \left[\begin{array}{ccccc}1 & -5 & 5 & -10 & -3\\-5 & -6 & -7 & -10 & 6\\-9 & -6 & 4 & -6 & 9\end{array}\right]

gives us,

.. math::
    Q = \left[\begin{array}{ccc}\frac{\sqrt{107}}{107} & - \frac{307 \sqrt{442766}}{221383} & \frac{12 \sqrt{4138}}{2069}\\- \frac{5 \sqrt{107}}{107} & - \frac{247 \sqrt{442766}}{442766} & - \frac{51 \sqrt{4138}}{4138}\\- \frac{9 \sqrt{107}}{107} & \frac{69 \sqrt{442766}}{442766} & \frac{31 \sqrt{4138}}{4138}\end{array}\right]
    \qquad
    R = \left[\begin{array}{ccccc}\sqrt{107} & \frac{79 \sqrt{107}}{107} & \frac{4 \sqrt{107}}{107} & \frac{94 \sqrt{107}}{107} & - \frac{114 \sqrt{107}}{107}\\0 & \frac{\sqrt{442766}}{107} & - \frac{1065 \sqrt{442766}}{442766} & \frac{4098 \sqrt{442766}}{221383} & \frac{981 \sqrt{442766}}{442766}\\0 & 0 & \frac{601 \sqrt{4138}}{4138} & \frac{42 \sqrt{4138}}{2069} & - \frac{99 \sqrt{4138}}{4138}\end{array}\right]

The QR decomposition of

.. math::
    \left[\begin{array}{ccc}1 & -5 & -9\\-5 & -6 & -6\\5 & -7 & 4\\-10 & -10 & -6\\-3 & 6 & 9\end{array}\right]

gives us,

.. math::
    Q = \left[\begin{array}{ccc}\frac{\sqrt{10}}{40} & - \frac{109 \sqrt{1335}}{10680} & - \frac{51701 \sqrt{150661959}}{1205295672}\\- \frac{\sqrt{10}}{8} & - \frac{5 \sqrt{1335}}{712} & - \frac{3817 \sqrt{150661959}}{401765224}\\\frac{\sqrt{10}}{8} & - \frac{37 \sqrt{1335}}{2136} & \frac{63887 \sqrt{150661959}}{1205295672}\\- \frac{\sqrt{10}}{4} & - \frac{11 \sqrt{1335}}{1068} & \frac{8833 \sqrt{150661959}}{602647836}\\- \frac{3 \sqrt{10}}{40} & \frac{49 \sqrt{1335}}{3560} & \frac{16481 \sqrt{150661959}}{401765224}\end{array}\right]
    \qquad
    R = \left[\begin{array}{ccc}4 \sqrt{10} & \frac{9 \sqrt{10}}{5} & \frac{37 \sqrt{10}}{20}\\0 & \frac{2 \sqrt{1335}}{5} & \frac{1337 \sqrt{1335}}{5340}\\0 & 0 & \frac{\sqrt{150661959}}{1068}\end{array}\right]

:index:`LDL Decomposition`
--------------------------

This option does an LDL decomposition of the selected matrix :math:`A` if the matrix is symmetric.  If the matrix is not symmetric the program will return an error.  This option will return two matrices :math:`L` and :math:`D` with :math:`L D L^T = A`.  For example the LDL decomposition of

.. math::
    \left[\begin{array}{ccc}5 & 4 & 10\\4 & -4 & 1\\10 & 1 & -2\end{array}\right]

returns,

.. math::
    L = \left[\begin{array}{ccc}1 & 0 & 0\\\frac{4}{5} & 1 & 0\\2 & \frac{35}{36} & 1\end{array}\right]
    \qquad
    D = \left[\begin{array}{ccc}5 & 0 & 0\\0 & - \frac{36}{5} & 0\\0 & 0 & - \frac{547}{36}\end{array}\right]

Checking,

.. math::
    \left[\begin{array}{ccc}1 & 0 & 0\\\frac{4}{5} & 1 & 0\\2 & \frac{35}{36} & 1\end{array}\right] \left[\begin{array}{ccc}5 & 0 & 0\\0 & - \frac{36}{5} & 0\\0 & 0 & - \frac{547}{36}\end{array}\right] \left[\begin{array}{ccc}1 & \frac{4}{5} & 2\\0 & 1 & \frac{35}{36}\\0 & 0 & 1\end{array}\right] = \left[\begin{array}{ccc}5 & 4 & 10\\4 & -4 & 1\\10 & 1 & -2\end{array}\right]

:index:`Cholesky Decomposition`
-------------------------------

This option does a Cholesky-type decomposition of the selected matrix :math:`A` if the matrix is symmetric.  If the matrix is not symmetric the program will return an error.  This option will return one matrix :math:`L` with :math:`L L^T = A`.  For example the Cholesky decomposition of

.. math::
    \left[\begin{array}{ccc}5 & 4 & 10\\4 & -4 & 1\\10 & 1 & -2\end{array}\right]

returns,

.. math::
    \left[\begin{array}{ccc}\sqrt{5} & 0 & 0\\\frac{4 \sqrt{5}}{5} & \frac{6 \sqrt{5} i}{5} & 0\\2 \sqrt{5} & \frac{7 \sqrt{5} i}{6} & \frac{\sqrt{547} i}{6}\end{array}\right]

Checking,

.. math::
    \left[\begin{array}{ccc}\sqrt{5} & 0 & 0\\\frac{4 \sqrt{5}}{5} & \frac{6 \sqrt{5} i}{5} & 0\\2 \sqrt{5} & \frac{7 \sqrt{5} i}{6} & \frac{\sqrt{547} i}{6}\end{array}\right] \left[\begin{array}{ccc}\sqrt{5} & \frac{4 \sqrt{5}}{5} & 2 \sqrt{5}\\0 & \frac{6 \sqrt{5} i}{5} & \frac{7 \sqrt{5} i}{6}\\0 & 0 & \frac{\sqrt{547} i}{6}\end{array}\right] = \left[\begin{array}{ccc}5 & 4 & 10\\4 & -4 & 1\\10 & 1 & -2\end{array}\right]

as another example, the Cholesky decomposition of

.. math::
    \left[\begin{array}{ccc}25 & 15 & -5\\15 & 18 & 0\\-5 & 0 & 11\end{array}\right]

returns,

.. math::
    \left[\begin{array}{ccc}5 & 0 & 0\\3 & 3 & 0\\-1 & 1 & 3\end{array}\right]

Checking,

.. math::
    \left[\begin{array}{ccc}5 & 0 & 0\\3 & 3 & 0\\-1 & 1 & 3\end{array}\right] \left[\begin{array}{ccc}5 & 3 & -1\\0 & 3 & 1\\0 & 0 & 3\end{array}\right] = \left[\begin{array}{ccc}25 & 15 & -5\\15 & 18 & 0\\-5 & 0 & 11\end{array}\right]
