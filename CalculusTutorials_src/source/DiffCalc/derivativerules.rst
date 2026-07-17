:index:`Differentiation Rules`
==============================

Discussion & Definitions
------------------------

In most Calculus textbooks the following set of derivative formulas are usually spread across several sections and there are numerous exercises for you to become proficient in applying these rules to find derivatives of some fairly complicated functions.  We will not be going over this by hand as your textbook will do that.  With that said, differentiation rules are not just for finding a derivative by hand, these are written into computer algebra systems as part of their differentiation function code.  In fact, we can use the power of a computer algebra system to experiment and extend the basic rules learned in class.

If :math:`f(x)` and :math:`g(x)` are two differentiable functions and if *c* is a constant then we have the following differentiation rules:

Basic Rules
^^^^^^^^^^^

- :math:`\frac{d}{dx} (c) = 0`
- :math:`\frac{d}{dx} (x) = 1`
- :math:`\frac{d}{dx} (x^n) = n x^{n-1}` for *n* any real number.


Arithmetic Rules
^^^^^^^^^^^^^^^^

- :math:`\frac{d}{dx} (c f(x)) = c f'(x)`
- :math:`\frac{d}{dx} (f(x) + g(x)) = f'(x) + g'(x)`
- :math:`\frac{d}{dx} (f(x) - g(x)) = f'(x) - g'(x)`
- :math:`\frac{d}{dx} (f(x) g(x)) = f(x)g'(x) + f'(x)g(x)`
- :math:`\frac{d}{dx} \left(\frac{f(x)}{g(x)}\right) = \displaystyle \frac{g(x)f'(x) - f(x)g'(x)}{(g(x))^2}`

Chain Rule: Compositions
^^^^^^^^^^^^^^^^^^^^^^^^

- :math:`\frac{d}{dx} (f(g(x))) = f'(g(x))g'(x)`
- :math:`\displaystyle  \frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}`

Exponential & Logarithmic Rules
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- :math:`\frac{d}{dx} (e^x) = e^x`
- :math:`\frac{d}{dx} (a^x) = a^x \ln(a)`
- :math:`\frac{d}{dx} (\ln|x|) = \displaystyle \frac{1}{x}`
- :math:`\frac{d}{dx} (\log_b(x)) = \displaystyle \frac{1}{x \ln(b)}`

Trigonometric Rules
^^^^^^^^^^^^^^^^^^^

- :math:`\frac{d}{dx} (\sin(x)) = \cos(x)`
- :math:`\frac{d}{dx} (\cos(x)) = -\sin(x)`
- :math:`\frac{d}{dx} (\tan(x)) = \sec^2(x)`
- :math:`\frac{d}{dx} (\cot(x)) = -\csc^2(x)`
- :math:`\frac{d}{dx} (\sec(x)) = \sec(x)\tan(x)`
- :math:`\frac{d}{dx} (\csc(x)) = -\csc(x)\cot(x)`

Inverse Trigonometric Rules
^^^^^^^^^^^^^^^^^^^^^^^^^^^

- :math:`\frac{d}{dx} (\sin^{-1}(x)) = \displaystyle \frac{1}{\sqrt{1-x^2}}`
- :math:`\frac{d}{dx} (\cos^{-1}(x)) = \displaystyle -\frac{1}{\sqrt{1-x^2}}`
- :math:`\frac{d}{dx} (\tan^{-1}(x)) = \displaystyle \frac{1}{1+x^2}`
- :math:`\frac{d}{dx} (\cot^{-1}(x)) = \displaystyle -\frac{1}{1+x^2}`
- :math:`\frac{d}{dx} (\sec^{-1}(x)) = \displaystyle \frac{1}{x \sqrt{x^2 - 1}}`
- :math:`\frac{d}{dx} (\csc^{-1}(x)) = \displaystyle -\frac{1}{x \sqrt{x^2 - 1}}`

Hyperbolic Rules
^^^^^^^^^^^^^^^^

- :math:`\frac{d}{dx} (\sinh(x)) = \cosh(x)`
- :math:`\frac{d}{dx} (\cosh(x)) = \sinh(x)`
- :math:`\frac{d}{dx} (\tanh(x)) = \text{sech}^2(x)`
- :math:`\frac{d}{dx} (\coth(x)) = -\text{csch}^2(x)`
- :math:`\frac{d}{dx} (\text{sech}(x)) = -\text{sech}(x)\tanh(x)`
- :math:`\frac{d}{dx} (\text{csch}(x)) = -\text{csch}(x)\coth(x)`

Inverse Hyperbolic Rules
^^^^^^^^^^^^^^^^^^^^^^^^

- :math:`\frac{d}{dx} (\sinh^{-1}(x)) = \displaystyle \frac{1}{\sqrt{1+x^2}}`
- :math:`\frac{d}{dx} (\cosh^{-1}(x)) = \displaystyle \frac{1}{\sqrt{x^2 - 1}}`
- :math:`\frac{d}{dx} (\tanh^{-1}(x)) = \displaystyle \frac{1}{1-x^2}`
- :math:`\frac{d}{dx} (\coth^{-1}(x)) = \displaystyle \frac{1}{1-x^2}`
- :math:`\frac{d}{dx} (\text{sech}^{-1}(x)) = \displaystyle - \frac{1}{x\sqrt{1-x^2}}`
- :math:`\frac{d}{dx} (\text{csch}^{-1}(x)) = \displaystyle - \frac{1}{|x|\sqrt{x^2 + 1}}`

.. note::

    **For the readers who have studied computer science**: You will note that several of the rules (product, quotient, and chain) have derivatives on the right hand side of the equation.  So when doing a derivative by hand, one needs to find the derivatives of the smaller portions and substitute them into the right hand side to get the final answer.  In programming, this is called a recursive definition.  To take a derivative of a product you need to take the derivative of each of the factors and then combine these into the final answer.  So when building a computer algebra system, the functions that find derivatives are recursive.

    To take this one step further, for the machine to take the derivative of

    .. math::

        \left(x^3 \sin^7(x)\right)^5 \left(3x+\sin^2(x)\cos(e^x+4x^3)\right)

    The derivative function would first do a product rule, then inside that (on the left) it would need to do a chain rule then a product rule, followed by another chain rule, and finally a derivative formula.  On the right a sum rule, followed by a product rule, then chain rules, then a sum rule, and finally some formulas.  The usual way to accomplish this repetition of rules inside the execution of other rules is to have an expression function call a term function on each term, then the term function to call a factor function on each factor, then the factor function to call a power function on each power, and the power function apply a rule or call the expression function, and so on.  So this system of differentiation function code is indirectly recursive.  A similar system is built into programming language compilers and interpreters. For the interested reader you may wish to look up Backus-Naur Form and the theory of languages.


Example: Generalizing the Product Rule
--------------------------------------

These exercises are best done with either CLAE or Maxima. If you have not read the previous section, :doc:`derivativefct`, on how to do the quick derivative function in CLAE and Maxima you should do so before continuing with this example.

CLAE
^^^^

Make sure you start with an empty workspace,

Input

.. code-block:: console

    f(x)*g(x)

Take the derivative and you will get the product rule,

.. math::
    f{\left(x \right)} \frac{d}{d x} g{\left(x \right)} + g{\left(x \right)} \frac{d}{d x} f{\left(x \right)}


Input the following and take its derivative,

.. code-block:: console

    f(x)*g(x)*h(x)

Input the following and take its derivative,

.. code-block:: console

    f(x)*g(x)*h(x)*k(x)

Input the following and take its derivative,

.. code-block:: console

    f(x)*g(x)*h(x)*k(x)*m(x)

Do you notice a pattern?  What is it?

If you were given the function,

.. math::

    \sin(x) \cdot (x^2-3x+4) \cdot  \cos(x) \cdot  \ln(x) \cdot  \frac{1}{x^3} \cdot  \sqrt[3]{x}

could you write down the derivative without any intermediate steps?

Maxima
^^^^^^

Make sure you start with a new workspace,

Input

.. code-block:: console

    f(x)*g(x)

Take the derivative and you will get the product rule,

.. math::
    f{\left(x \right)} \frac{d}{d x} g{\left(x \right)} + g{\left(x \right)} \frac{d}{d x} f{\left(x \right)}

Input the following and take its derivative,

.. code-block:: console

    f(x)*g(x)*h(x)

Input the following and take its derivative,

.. code-block:: console

    f(x)*g(x)*h(x)*k(x)

Input the following and take its derivative,

.. code-block:: console

    f(x)*g(x)*h(x)*k(x)*m(x)

Do you notice a pattern?  What is it?

If you were given the function,

.. math::

    \sin(x) \cdot (x^2-3x+4) \cdot  \cos(x) \cdot  \ln(x) \cdot  \frac{1}{x^3} \cdot  \sqrt[3]{x}

could you write down the derivative without any intermediate steps?

