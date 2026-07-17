:index:`Data Types`
===================

Since one of the goals of this program is to reduce the amount of "coding" and concentrate on the mathematics, we tried to reduce as much of the Python language aspects as we could.  Unfortunately we cannot eliminate all of it, but we reduced the number of the types of structures as possible.

The basic types you will need to work with are expressions, piecewise defined expressions, matrices, and lists.  The program will output other data types depending on the operation that is being done.  The program has several menu options that make it easy for you to convert one of these other types to the basic four where necessary.

Expressions
-----------

An expression is a single mathematical expression like :math:`\sin(x)` or :math:`3\ln(x+y)`.  This is the most basic object on the program and the other structures are essentially just collections of these.

Piecewise Defined Expressions
-----------------------------

An piecewise defined expression is a list of expressions each with an associated domain.  The domain is simply a logical expression that determines if the expression is to be used in the evaluation.

For example,

.. math::

    \begin{cases} x & \text{for}\: x \leq -1 \\x^{2} & \text{for}\: x < 3 \\x^{3} & \text{otherwise} \end{cases}


Matrices
--------

A matrix is a rectangular array of expressions.  A matrix has rows and columns of these entries.

For example,

.. math::

    \left[\begin{array}{ccc}1 & x & \sin{\left(t \right)}\\2 & y & 3\\3 & x y & \cos{\left(x + y \right)}\end{array}\right]

Matrices are the key structure in Linear Algebra and there are many options for manipulating matrices in the main menu of this program.

Lists
-----

A list is simply a finite sequence of expressions, matrices, piecewise expressions, or lists separated by commas and enclosed in square brackets.

For example, the following are all lists,

.. math::

    \left[ 3, \  x y, \  \cos{\left(x + y \right)}\right]

.. math::

    \left[ \left[ 1, \  2\right], \  \left[ a, \  b, \  c\right], \  \left[ 3, \  4, \  5, \  6\right], \  \left[ x, \  y, \  z\right]\right]

.. math::

    \left[ \left[\begin{array}{c}1\\2\\3\end{array}\right], \  \left[\begin{array}{c}x\\y\\x y\end{array}\right], \  \left[\begin{array}{c}\sin{\left(t \right)}\\3\\\cos{\left(x + y \right)}\end{array}\right]\right]

Note that it may be confusing in some cases, if you are working with a list of items there are commas between the entries.  For example,

.. math::

    \left[ 3, \  x y, \  \cos{\left(x + y \right)}\right]

is a list, but

.. math::

    \left[\begin{array}{ccc}3 & x y & \cos{\left(x + y \right)}\end{array}\right]

is a 1 X 3 matrix.

Lists are very easy to manipulate and the menu has several options for extracting the entries of a list to work with them.


Other Types
-----------

From time to time you will see some other data types but most of these can be changed to lists and worked with as a list.

Tuples
^^^^^^

A tuple looks exactly like a list except that it is enclosed in parentheses instead of square brackets.

For example,

.. math::

    \left( 3, \  x y, \  \cos{\left(x + y \right)}\right)

Most of the time we convert tuple output to lists before the object is entered into the CAS but there are times you will see these.  Although there is a technical difference between lists and tuples in Python, for this program they work essentially the same way.

Sets
^^^^

A set is like a mathematical set.  The notation of a set is like that of a list or tuple but enclosed in curly brackets.

For example,

.. math::

    \left\{ 3, \  x y, \  \cos{\left(x + y \right)}\right\}

Sets and lists are common outputs for solving equations.  For example, if we input the expression :math:`x^{2} - 3 x + 1` and select ``Algebra > Solve`` we get an output of

.. math::

    \left[ \frac{3}{2} - \frac{\sqrt{5}}{2}, \  \frac{\sqrt{5}}{2} + \frac{3}{2}\right]

which is a list of the two solutions to :math:`x^{2} - 3 x + 1 = 0`. If we had chosen the advanced solvers instead and selected to solve over the reals we would have obtained,

.. math::

    \left\{\frac{3}{2} - \frac{\sqrt{5}}{2}, \frac{\sqrt{5}}{2} + \frac{3}{2}\right\}

a set of the same two solutions.  The program has a menu option that will convert sets and tuples to lists.  In addition, there are menu options for extracting all the elements of a list.


Dictionaries
^^^^^^^^^^^^

From time to time you may encounter a dictionary.  A dictionary is a key/value pair of data.  As an example, type in a big number, say 70472695472659745620.  Select ``Algebra > Factor Integer`` and what you will get is,

.. math::

    \left[ \left[ 2, \  2\right], \  \left[ 5, \  1\right], \  \left[ 43, \  1\right], \  \left[ 81944994735650867, \  1\right]\right]

This is a list of lists (not a dictionary) that means

.. math::

    70472695472659745620 = 2^2 \cdot 5^1 \cdot 43^1 \cdot 81944994735650867^1

which is the prime factorization of 70472695472659745620.  If you invoke the integer factorization method directly in the input bar with ``factorint(70472695472659745620)`` you will get as a result,

.. math::

    \left\{ 2 : 2, \  5 : 1, \  43 : 1, \  81944994735650867 : 1\right\}

which means the same thing but is in dictionary form.  It is easy to spot a dictionary, just look for the colons.  When you used the menu we converted the dictionary to a list of lists under the hood.  Also, there are menu options for doing this same conversion.  If you select the dictionary version and then ``Edit > Other Conversions/Extractions > Convert Dictionary Key/Values to List of Lists`` you will get the list of list form.

Equations
^^^^^^^^^

In this program we take the approach of expressions equaling to 0 if we invoke a solve option.  That is, if we input the expression :math:`x^{2} - 3 x + 1` and select ``Algebra > Solve`` we are assuming that the equation that is being solved is :math:`x^{2} - 3 x + 1 = 0` and not :math:`x^{2} - 3 x = -1` or :math:`x^{2} = 3 x - 1`.  This is simply our convention and has pedagogical advantages. The program and SymPy solvers are quite capable of solving equations not equal to 0 and we can create them in this program but again this is syntax that is above where we need to go.  There are some cases where the output will be in equation form, for example, when solving ODEs.

For example, if we solve the ODE, (assumed equal to 0)

.. math::

    - f{\left(x \right)} + \frac{d^{2}}{d x^{2}} f{\left(x \right)} + 1

we get the output of

.. math::

    f{\left(x \right)} = C_{1} e^{- x} + C_{2} e^{x} + 1

All we really need here is the right had side of the equation.  Selecting ``Algebra > Equations > Right Hand Side`` will extract the right hand side of the equation for us.

.. math::

    C_{1} e^{- x} + C_{2} e^{x} + 1
