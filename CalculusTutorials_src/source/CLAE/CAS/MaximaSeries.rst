:index:`Maxima: Sums and Series`
================================

Sum
---

Finds the finite or infinite sum of the expression over the given summation interval.  As always, you are using CLAE syntax and not Maxima, so :math:`\infty` is ``oo`` and :math:`-\infty` is ``-oo``.  For example, if we find the sum of :math:`4^{- n}` for *n* going from 1 to 1000 we get,

.. math::
    \frac{38271023175808484141094440039256066134077256736289840015921424560858875379745677128555316210550208997281532154632915425781570632028768511047531045205555106179709996381770760000229593049413348290476308996687828748260538487882129454649105675346822117990301665519387466269648209868541103883178721407323444227114722969661486168534126494935971352966978258833476334238902208610174002710745427097253755961105735532998465472709007259952801347386617727750513629811300697306851652594529890679720027319072210194251793475194575338509449595473144018169638425261294208391811842933607614256939321817920728283716343125}{114813069527425452423283320117768198402231770208869520047764273682576626139237031385665948631650626991844596463898746277344711896086305533142593135616665318539129989145312280000688779148240044871428926990063486244781615463646388363947317026040466353970904996558162398808944629605623311649536164221970332681344168908984458505602379484807914058900934776500429002716706625830522008132236281291761267883317206598995396418127021779858404042159853183251540889433902091920554957783589672039160081957216630582755380425583726015528348786419432054508915275783882625175435528800822842770817965453762184851149029376}

and if we find the sum of :math:`4^{- n}` for *n* going from 1 to :math:`\infty` we get, :math:`1/3.`

In general, you probably want to use the sum options under the Calculus menu instead of this one.  The one in the Calculus menu uses SymPy which recognizes a larger set of summation forms, such as alternating series and telescoping series.

Product
-------

Finds the finite or infinite product of the expression over the given interval.  As always, you are using CLAE syntax and not Maxima, so :math:`\infty` is ``oo`` and :math:`-\infty` is ``-oo``.  For example, if we find the sum of :math:`4^{- n}` for *n* going from 1 to 20 we get,

.. math::
    \frac{1}{2707685248164858261307045101702230179137145581421695874189921465443966120903931272499975005961073806735733604454495675614232576}

As with the sum, you probably want to use the product options under the Calculus menu instead of this one.  The one in the Calculus menu uses SymPy which recognizes a larger set of product forms.

Taylor Series
-------------

This option returns the Taylor polynomial for a function given a center point and degree.  When selected, a dialog box will appear asking the user for the variable, center point, and the degree of the Taylor polynomial.  For example, if we find the Taylor polynomial of :math:`\sin(x)` centered at 0, of degree 10, we get,

.. math::
    \frac{x^{9}}{362880} - \frac{x^{7}}{5040} + \frac{x^{5}}{120} - \frac{x^{3}}{6} + x
