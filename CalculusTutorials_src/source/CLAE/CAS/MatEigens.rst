:index:`Eigenvalues and Eigenvectors`
=====================================

This submenu of options includes operations useful in examining the concepts of Eigenvalues and Eigenvectors.

:index:`xI - A`
---------------

This option returns the matrix ``xI - A`` for a square matrix A.  When invoked the program will ask the user to input the variable to use for the independent variable ``x``.

For example, say we have the matrix,

.. math::
    \left[\begin{array}{ccc}8 & -10 & -5\\2 & 17 & 2\\-9 & -18 & 4\end{array}\right]

Then the ``xI - A`` matrix is,

.. math::
    \left[\begin{array}{ccc}x - 8 & 10 & 5\\-2 & x - 17 & -2\\9 & 18 & x - 4\end{array}\right]

Say we have the matrix,

.. math::
    \left[\begin{array}{cccc}9 & -4 & -2 & -4\\-56 & 32 & -28 & 44\\-14 & -14 & 6 & -14\\42 & -33 & 21 & -45\end{array}\right]

Then the ``xI - A`` matrix is,

.. math::
    \left[\begin{array}{cccc}x - 9 & 4 & 2 & 4\\56 & x - 32 & 28 & -44\\14 & 14 & x - 6 & 14\\-42 & 33 & -21 & x + 45\end{array}\right]

.. note::

    Some linear algebra textbooks use ``xI - A`` and some use ``A - xI``, since these are simply a negative of each other, if you want ``A - xI`` just take the result of ``xI - A``, say it is in R7 and put ``-R7`` into the CAS input bar to take the negative and hence obtain ``A - xI``.

    .. math::
        \left[\begin{array}{cccc}9 - x & -4 & -2 & -4\\-56 & 32 - x & -28 & 44\\-14 & -14 & 6 - x & -14\\42 & -33 & 21 & - x - 45\end{array}\right]

:index:`Characteristic Polynomial`
----------------------------------

This option returns the Characteristic Polynomial of the square matrix A, as defined by :math:`|xI - A|`. When invoked the program will ask the user to input the variable to use for the independent variable ``x``.

For example, say we have the matrix,

.. math::
    \left[\begin{array}{ccc}8 & -10 & -5\\2 & 17 & 2\\-9 & -18 & 4\end{array}\right]

Then the characteristic polynomial for this matrix is, :math:`x^{3} - 29 x^{2} + 247 x - 507`.

Say we have the matrix,

.. math::
    \left[\begin{array}{cccc}9 & -4 & -2 & -4\\-56 & 32 & -28 & 44\\-14 & -14 & 6 & -14\\42 & -33 & 21 & -45\end{array}\right]

Then the characteristic polynomial for this matrix is, :math:`x^{4} - 92 x^{3} + 3919 x^{2} + 10212 x - 621504`.


:index:`Eigenvalues`
--------------------

This option returns the eigenvalues of a matrix as a column vector.  For example, say we have the matrix,

.. math::
    \left[\begin{array}{ccc}8 & -10 & -5\\2 & 17 & 2\\-9 & -18 & 4\end{array}\right]

Then the eigenvalues for this matrix are given as,

.. math::
    \left[\begin{array}{c}3\\13\end{array}\right]

This means that 3 and 13 are the two eigenvalues for the matrix.  Had we taken the characteristic polynomial :math:`x^{3} - 29 x^{2} + 247 x - 507` and factored it we would have gotten :math:`\left(x - 13\right)^{2} \left(x - 3\right)` which shows that the eigenvalue 3 has multiplicity 1 and the eigenvalue 13 has multiplicity 2.

Say we have the matrix,

.. math::
    \left[\begin{array}{cccc}9 & -4 & -2 & -4\\-56 & 32 & -28 & 44\\-14 & -14 & 6 & -14\\42 & -33 & 21 & -45\end{array}\right]

Then the eigenvalues for this matrix are given as,

.. math::
    \left[\begin{array}{c}13\\-12\end{array}\right]

This means that -12 and 13 are the two eigenvalues for the matrix.  Factoring the characteristic polynomial shows that both eigenvalues have multiplicity 2.


:index:`Eigenvalues with Multiplicities`
----------------------------------------

This option returns a matrix with two columns.  The first column are the eigenvalues and the second column are the multiplicities for each eigenvalue.  For example, say we have the matrix,

.. math::
    \left[\begin{array}{ccc}8 & -10 & -5\\2 & 17 & 2\\-9 & -18 & 4\end{array}\right]

Then the eigenvalues and multiplicities for this matrix are given as,

.. math::
    \left[\begin{array}{cc}3 & 1\\13 & 2\end{array}\right]

Which shows that the eigenvalue 3 has multiplicity 1 and the eigenvalue 13 has multiplicity 2.

Say we have the matrix,

.. math::
    \left[\begin{array}{cccc}9 & -4 & -2 & -4\\-56 & 32 & -28 & 44\\-14 & -14 & 6 & -14\\42 & -33 & 21 & -45\end{array}\right]

Then the eigenvalues and multiplicities for this matrix are given as,

.. math::
    \left[\begin{array}{cc}13 & 2\\-12 & 2\end{array}\right]

This means that -12 and 13 are the two eigenvalues for the matrix and they both have multiplicity 2.


:index:`Eigenvectors`
---------------------

This option returns a lot of information, not just Eigenvectors.  The result of this option is a list of lists, each of the inner lists is the eigenvalue, its multiplicity, and then a list containing a basis for the eigenspace associated with that eigenvalue.  For example, say we have the matrix,

.. math::
    \left[\begin{array}{ccc}8 & -10 & -5\\2 & 17 & 2\\-9 & -18 & 4\end{array}\right]

Then this option returns,

.. math::
    \left[ \left[ 3, \  1, \  \left[ \left[\begin{array}{c}\frac{5}{9}\\- \frac{2}{9}\\1\end{array}\right]\right]\right], \  \left[ 13, \  2, \  \left[ \left[\begin{array}{c}-2\\1\\0\end{array}\right], \  \left[\begin{array}{c}-1\\0\\1\end{array}\right]\right]\right]\right]

So for the eigenvalue 3, it has multiplicity 1 and a basis to its eigenspace is

.. math::
    \left[\begin{array}{c}\frac{5}{9}\\- \frac{2}{9}\\1\end{array}\right]

and for the eigenvalue 13, it has multiplicity 2 and a basis to its eigenspace is

.. math::
    \left[ \left[\begin{array}{c}-2\\1\\0\end{array}\right], \  \left[\begin{array}{c}-1\\0\\1\end{array}\right]\right]

that is,

.. math::
    \left\{ \left[\begin{array}{c}-2\\1\\0\end{array}\right], \  \left[\begin{array}{c}-1\\0\\1\end{array}\right]\right\}


Say we have the matrix,

.. math::
    \left[\begin{array}{cccc}9 & -4 & -2 & -4\\-56 & 32 & -28 & 44\\-14 & -14 & 6 & -14\\42 & -33 & 21 & -45\end{array}\right]

Then this option gives as,

.. math::
    \left[ \left[ -12, \  2, \  \left[ \left[\begin{array}{c}\frac{2}{7}\\1\\1\\0\end{array}\right], \  \left[\begin{array}{c}0\\-1\\0\\1\end{array}\right]\right]\right], \  \left[ 13, \  2, \  \left[ \left[\begin{array}{c}- \frac{1}{2}\\0\\1\\0\end{array}\right], \  \left[\begin{array}{c}\frac{1}{3}\\- \frac{4}{3}\\0\\1\end{array}\right]\right]\right]\right]

.. note::
    For random matrices the eigenvalues and eigenvectors can become rather complicated, for example, if we simply change the last entry of the above matrix to 45,

    .. math::
        \left[\begin{array}{cccc}9 & -4 & -2 & -4\\-56 & 32 & -28 & 44\\-14 & -14 & 6 & -14\\42 & -33 & 21 & 45\end{array}\right]

    we get

    .. math::
        \left[ \left[ -12, \  1, \  \left[ \left[\begin{array}{c}\frac{2}{7}\\1\\1\\0\end{array}\right]\right]\right], \  \left[ 13, \  1, \  \left[ \left[\begin{array}{c}- \frac{1}{2}\\0\\1\\0\end{array}\right]\right]\right], \  \left[ \frac{91}{2} - \frac{\sqrt{7655} i}{2}, \  1, \  \left[ \left[\begin{array}{c}\frac{1}{957} - \frac{\sqrt{7655} i}{957}\\- \frac{1}{87} + \frac{\sqrt{7655} i}{87}\\\frac{7}{1914} - \frac{7 \sqrt{7655} i}{1914}\\1\end{array}\right]\right]\right], \  \left[ \frac{91}{2} + \frac{\sqrt{7655} i}{2}, \  1, \  \left[ \left[\begin{array}{c}\frac{1}{957} + \frac{\sqrt{7655} i}{957}\\- \frac{1}{87} - \frac{\sqrt{7655} i}{87}\\\frac{7}{1914} + \frac{7 \sqrt{7655} i}{1914}\\1\end{array}\right]\right]\right]\right]

    Also if we take a random 3 X 3 matrix,

    .. math::
        \left[\begin{array}{ccc}0 & 5 & 6\\-7 & 6 & 8\\5 & 8 & 6\end{array}\right]

    we get something even more complex,

    .. math::
        \left[ \left[ 4 + \left(- \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}} + \frac{71}{\left(- \frac{3}{2} - \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}}, \  1, \  \left[ \left[\begin{array}{c}\frac{266}{271} + \frac{\left(- \frac{121}{2} - \frac{121 \sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}}{813} - \frac{8 \left(4 + \left(- \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}} + \frac{71}{\left(- \frac{3}{2} - \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}}\right)^{2}}{813} + \frac{8591}{\left(- \frac{2439}{2} - \frac{2439 \sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}}\\- \frac{234}{271} + \frac{\left(-13 - 13 \sqrt{3} i\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}}{813} + \frac{5 \left(4 + \left(- \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}} + \frac{71}{\left(- \frac{3}{2} - \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}}\right)^{2}}{813} + \frac{1846}{\left(- \frac{2439}{2} - \frac{2439 \sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}}\\1\end{array}\right]\right]\right], \  \left[ 4 + \frac{71}{\left(- \frac{3}{2} + \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}} + \left(- \frac{1}{2} + \frac{\sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}, \  1, \  \left[ \left[\begin{array}{c}\frac{266}{271} + \frac{8591}{\left(- \frac{2439}{2} + \frac{2439 \sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}} - \frac{8 \left(4 + \frac{71}{\left(- \frac{3}{2} + \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}} + \left(- \frac{1}{2} + \frac{\sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}\right)^{2}}{813} + \frac{\left(- \frac{121}{2} + \frac{121 \sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}}{813}\\- \frac{234}{271} + \frac{1846}{\left(- \frac{2439}{2} + \frac{2439 \sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}} + \frac{5 \left(4 + \frac{71}{\left(- \frac{3}{2} + \frac{3 \sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}} + \left(- \frac{1}{2} + \frac{\sqrt{3} i}{2}\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}\right)^{2}}{813} + \frac{\left(-13 + 13 \sqrt{3} i\right) \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}}{813}\\1\end{array}\right]\right]\right], \  \left[ 4 + \frac{71}{3 \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}} + \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}, \  1, \  \left[ \left[\begin{array}{c}\frac{266}{271} + \frac{8591}{2439 \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}} - \frac{8 \left(4 + \frac{71}{3 \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}} + \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}\right)^{2}}{813} + \frac{121 \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}}{813}\\- \frac{234}{271} + \frac{1846}{2439 \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}} + \frac{5 \left(4 + \frac{71}{3 \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}} + \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}\right)^{2}}{813} + \frac{26 \sqrt[3]{57 + \frac{2 \sqrt{202641} i}{9}}}{813}\\1\end{array}\right]\right]\right]\right]

:index:`Eigenmatrix`
--------------------

There is really no such thing as an Eigenmatrix. This is simply a matrix whose columns are the bases vectors for the eigenspaces of all the eigenvalues to the matrix.  So when looking at diagonalizing a matrix this is the change of basis matrix to diagonalize that matrix, if it can be. For example, say we have the matrix,

.. math::
    \left[\begin{array}{ccc}8 & -10 & -5\\2 & 17 & 2\\-9 & -18 & 4\end{array}\right]

Then the "eigenmatrix" is,

.. math::
    \left[\begin{array}{ccc}\frac{5}{9} & -2 & -1\\- \frac{2}{9} & 1 & 0\\1 & 0 & 1\end{array}\right]

Say we have the matrix,

.. math::
    \left[\begin{array}{cccc}9 & -4 & -2 & -4\\-56 & 32 & -28 & 44\\-14 & -14 & 6 & -14\\42 & -33 & 21 & -45\end{array}\right]

Then the "eigenmatrix" is,

.. math::
    \left[\begin{array}{cccc}\frac{2}{7} & 0 & - \frac{1}{2} & \frac{1}{3}\\1 & -1 & 0 & - \frac{4}{3}\\1 & 0 & 1 & 0\\0 & 1 & 0 & 1\end{array}\right]

:index:`Power Method`
---------------------

The Power Method is a numerical method for finding the dominant eigenvalue, which is based on a dynamical system of successive multiplications by the original matrix.  This tool is simply here in case you wish to investigate this numerical method for approximating the eigenvalues of a matrix.

When this option is selected the program will ask the user to input the initial vector, the tolerance, and the maximum number of iterations to apply.  Once input, the program will approximate the initial matrix (to make it floating point numeric) and then do the power method on the matrix with the initial vector until two consecutive approximations of the dominant eigenvalue are within the tolerance or the maximum number of iterations is reached. The program will return a list of two items, the first is an approximation of the eigenvalue and the second is an approximation to an associated eigenvector for that eigenvalue.

For example, say we have the matrix,

.. math::
    \left[\begin{array}{ccc}-3 & -4 & -1\\-10 & -7 & -9\\3 & -7 & -5\end{array}\right]

If we apply the power method to this matrix using the default initial vector of :math:`(1, 1, 1)` we get,

.. math::
    \left[ -15.623026969768166619, \  \left[\begin{array}{c}0.36100657198531533974\\1.0\\0.55699569443627948404\end{array}\right]\right]

So the approximate dominant eigenvalue is :math:`-15.623026969768166619` and its associated eigenvector is

.. math::
    \left[\begin{array}{c}0.36100657198531533974\\1.0\\0.55699569443627948404\end{array}\right]

The actual eigenvalues to this matrix are,

.. math::
    \left[ -5 - \frac{104}{\left(- \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \sqrt[3]{1269 + 3 \sqrt{3195663} i}} - \frac{\left(- \frac{1}{2} - \frac{\sqrt{3} i}{2}\right) \sqrt[3]{1269 + 3 \sqrt{3195663} i}}{3}, \  -5 - \frac{\left(- \frac{1}{2} + \frac{\sqrt{3} i}{2}\right) \sqrt[3]{1269 + 3 \sqrt{3195663} i}}{3} - \frac{104}{\left(- \frac{1}{2} + \frac{\sqrt{3} i}{2}\right) \sqrt[3]{1269 + 3 \sqrt{3195663} i}}, \  -5 - \frac{\sqrt[3]{1269 + 3 \sqrt{3195663} i}}{3} - \frac{104}{\sqrt[3]{1269 + 3 \sqrt{3195663} i}}\right]

which approximates to

.. math::
    \left[ -4.0888812132655636103, \  4.7119081830425869325, \  -15.623026969777023322\right]

:index:`The Inverse Power Method`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

There is not a special tool for doing the inverse power method on a matrix since one can apply the power method to a slightly altered matrix to accomplish this.  Here is the general procedure.

1. Say we guess that there is an eigenvalue close to :math:`\alpha` of a matrix *A*.
2. Form the matrix :math:`B = (A-\alpha I)^{-1}.`
3. Apply the power method to the matrix *B*. The result will be the value-vector pair :math:`[\mu, \mathbf{v}].`
4. Calculate :math:`1/\mu + \alpha,` this will be an approximation of the eigenvalue close to the initial guess of :math:`\alpha.`  Its associated eigenvector will be :math:`\mathbf{v}` without any alteration.

For example, we will use the same matrix,

.. math::
    \left[\begin{array}{ccc}-3 & -4 & -1\\-10 & -7 & -9\\3 & -7 & -5\end{array}\right]

Say we guess that there is an eigenvalue around 4.7, then the matrix :math:`B = (A-4.7 I)^{-1}` is

.. math::
    \left[\begin{array}{ccc}23.7376586741886 & -14.9506346967557 & 11.4245416078982\\-58.2980724024437 & 36.5256229431117 & -27.8796426892331\\49.4123178185228 & -30.9826046074277 & 23.5496003761162\end{array}\right]

Applying the power method to this matrix gives us the following,

.. math::
    \left[ 83.975867386628610559, \  \left[\begin{array}{c}-0.40884105951785534599\\1.0\\-0.84705528754044794651\end{array}\right]\right]

Then our approximation to the eigenvalue close to 4.7 is :math:`1/83.975867386628610559 + 4.7 = 4.7119081830425873502` and its associated eigenvector is

.. math::
    \left[\begin{array}{c}-0.40884105951785534599\\1.0\\-0.84705528754044794651\end{array}\right]


:index:`QR Method`
------------------

The QR Method is another numerical method for finding eigenvalues, which is based on the QR factorization method.  This tool is simply here in case you wish to investigate this numerical method for approximating the eigenvalues of a matrix.

When this option is selected the program will ask the user to input the number of steps of the QR algorithm to do.  Once input, the program will approximate the initial matrix (to make it floating point numeric) and then do the desired number of iterations on the matrix and finally return the result.

For example, say we have the matrix,

.. math::
    \left[\begin{array}{ccc}8 & -10 & -5\\2 & 17 & 2\\-9 & -18 & 4\end{array}\right]

Then doing 10 iterations on this matrix produces,

.. math::
    \left[\begin{array}{ccc}13.0000023363476 & 8.4783185986411 \cdot 10^{-7} & 14.0129732648145\\3.17936873001484 \cdot 10^{-6} & 13.0000011537539 & 19.0692556351194\\-1.66727527340489 \cdot 10^{-6} & -6.05033737760955 \cdot 10^{-7} & 2.99999650989854\end{array}\right]

Doing 100 iterations on the original matrix produces,

.. math::
    \left[\begin{array}{ccc}13.0 & -3.38947781723743 \cdot 10^{-15} & 14.0129809949072\\-6.20348547401211 \cdot 10^{-16} & 13.0 & 19.0692517849119\\-8.09129943668922 \cdot 10^{-64} & -2.93623036680901 \cdot 10^{-64} & 3.0\end{array}\right]

From this it appears that the eigenvalues are 3 and 13 with 13 having multiplicity 2.

As a more advanced example, say we have the following matrix,

.. math::
    \left[\begin{array}{cccccc}3 & -8 & 8 & 0 & -6 & -1\\0 & 3 & 6 & 1 & 9 & 10\\3 & 8 & -3 & 8 & 1 & 7\\-7 & -1 & -7 & 10 & 10 & -4\\-6 & -8 & -1 & -8 & -5 & -6\\-9 & 0 & 8 & 8 & -9 & 9\end{array}\right]

If we do 500 iterations of the QR method on this we get,

.. math::
    \left[\begin{array}{cccccc}16.0058278186172 & 12.1046178770684 & 8.22798196182224 & -1.60016708065307 & 0.608220377292673 & 2.30607079233788\\-12.2276527196469 & 9.29407653966238 & 6.50320446143348 & -4.95898721530967 & -0.384292732120875 & -1.61237712636443\\-4.1801826912127 \cdot 10^{-91} & -3.32167916461904 \cdot 10^{-91} & 11.2987475158688 & -7.423281460445 & -1.92791569106384 & 1.05125679281016\\-2.26507153985018 \cdot 10^{-99} & -3.63540125130923 \cdot 10^{-99} & 1.66520587934375 \cdot 10^{-7} & -14.2622718077259 & 7.32912657978935 & -3.25147547716453\\-1.66320079212229 \cdot 10^{-100} & -1.13860668857001 \cdot 10^{-99} & 8.77899143684282 \cdot 10^{-8} & -13.06945782964 & -1.50229977038175 & 9.04214459992051\\-3.43698662456677 \cdot 10^{-326} & -1.80201639585912 \cdot 10^{-326} & 9.19929895186918 \cdot 10^{-234} & -1.60788822651477 \cdot 10^{-225} & -4.39315717858831 \cdot 10^{-226} & -3.83408029604088\end{array}\right]

which shows the upper-block-diagonal form which displays two real eigenvalues and two instances of conjugate pair eigenvalues.

.. note::
    This program will find exact values for eigenvalues and eigenvectors when it can.  Since for larger matrices the characteristic polynomial may exceed degree four and hence the program may not be able to find exact eigenvalues and subsequently exact eigenvectors.  In these cases we can approximate the matrix first (to move it into a floating point matrix) and then calculate the eigenvalues and  eigenvectors.  These will, of course, be approximations.  For example, say we have the matrix (just a random 6 X 6 from the program),

    .. math::
        \left[\begin{array}{cccccc}3 & -8 & 8 & 0 & -6 & -1\\0 & 3 & 6 & 1 & 9 & 10\\3 & 8 & -3 & 8 & 1 & 7\\-7 & -1 & -7 & 10 & 10 & -4\\-6 & -8 & -1 & -8 & -5 & -6\\-9 & 0 & 8 & 8 & -9 & 9\end{array}\right]

    If we try to calculate the eigenvalues for this matrix we get,

    .. math::
        \left[\begin{array}{c}\operatorname{CRootOf} {\left(x^{6} - 17 x^{5} + 43 x^{4} + 2013 x^{3} + 21343 x^{2} - 333869 x - 1506924, 0\right)}\\\operatorname{CRootOf} {\left(x^{6} - 17 x^{5} + 43 x^{4} + 2013 x^{3} + 21343 x^{2} - 333869 x - 1506924, 1\right)}\\\operatorname{CRootOf} {\left(x^{6} - 17 x^{5} + 43 x^{4} + 2013 x^{3} + 21343 x^{2} - 333869 x - 1506924, 2\right)}\\\operatorname{CRootOf} {\left(x^{6} - 17 x^{5} + 43 x^{4} + 2013 x^{3} + 21343 x^{2} - 333869 x - 1506924, 3\right)}\\\operatorname{CRootOf} {\left(x^{6} - 17 x^{5} + 43 x^{4} + 2013 x^{3} + 21343 x^{2} - 333869 x - 1506924, 4\right)}\\\operatorname{CRootOf} {\left(x^{6} - 17 x^{5} + 43 x^{4} + 2013 x^{3} + 21343 x^{2} - 333869 x - 1506924, 5\right)}\end{array}\right]

    Not very informative, since it is simply telling us to find the 6 roots to the characteristic polynomial for the matrix, which is the program's job. If we first approximate the matrix to

    .. math::
        \left[\begin{array}{cccccc}3.0 & -8.0 & 8.0 & 0 & -6.0 & -1.0\\0 & 3.0 & 6.0 & 1.0 & 9.0 & 10.0\\3.0 & 8.0 & -3.0 & 8.0 & 1.0 & 7.0\\-7.0 & -1.0 & -7.0 & 10.0 & 10.0 & -4.0\\-6.0 & -8.0 & -1.0 & -8.0 & -5.0 & -6.0\\-9.0 & 0 & 8.0 & 8.0 & -9.0 & 9.0\end{array}\right]

    and then ask for the eigenvalues we get,

    .. math::
        \left[\begin{array}{c}-7.8822857645494 - 7.42182522224422 i\\-7.8822857645494 + 7.42182522224422 i\\-3.83408029604088 + 3.5248633986871 \cdot 10^{-63} i\\12.6499521791399 - 11.6939797501614 i\\12.6499521791399 + 11.6939797501614 i\\11.29874746686 + 6.18565873830988 \cdot 10^{-64} i\end{array}\right]

    From this we can see that there are two solutions that are "close" to being real and hence are most likely real eigenvalues.  The other four appear to be two sets of conjugate pairs, which we would expect.

