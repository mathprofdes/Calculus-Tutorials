:index:`Other Conversions/Extractions`
======================================

This set of options are for converting other data types to lists or for extracting data from other data types.  While we have tried to convert data to expressions, lists, and matrices, there are times you may encounter other outputs.  In these cases this set of options should allow you to manipulate the  CAS entries to do what you need to do.  For an overview of the data types see :doc:`casDataTypes`.  Also for equations, you can extract the left and right hand sides of the equations using options in the Algebra menu.

Convert Sets and Tuples to Lists
--------------------------------

This option converts a set or tuple to a list.

For example, say we have the following set that was the result of an advanced solver,

.. math::

    \left\{\frac{3}{2} - \frac{\sqrt{11} i}{2}, \frac{3}{2} + \frac{\sqrt{11} i}{2}\right\}

If we select this option we get the same entries but in a list,

.. math::

    \left[ \frac{3}{2} + \frac{\sqrt{11} i}{2}, \  \frac{3}{2} - \frac{\sqrt{11} i}{2}\right]

Extract Set Contents
--------------------

This option will extract each element of a set and load them in as separate CAS items.

For example, say we have the following set that was the result of an advanced solver,

.. math::

    \left\{\frac{3}{2} - \frac{\sqrt{11} i}{2}, \frac{3}{2} + \frac{\sqrt{11} i}{2}\right\}

If we select this option we get the entries as separate items in the CAS,

.. math::

    \frac{3}{2} + \frac{\sqrt{11} i}{2}

.. math::

    \frac{3}{2} - \frac{\sqrt{11} i}{2}

Convert Dictionary Keys to List
-------------------------------

You will not see dictionaries very often in the CAS but if you do this item will extract all the keys and create a list from them.

For example, say we have the following dictionary which was the result of ``factorint(123456)``,

.. math::

    \left\{ 2 : 6, \  3 : 1, \  643 : 1\right\}

This option will produce,

.. math::

    \left[ 2, \  3, \  643\right]

Convert Dictionary Values to List
---------------------------------

You will not see dictionaries very often in the CAS but if you do this item will extract all the values and create a list from them.

For example, say we have the following dictionary which was the result of ``factorint(123456)``,

.. math::

    \left\{ 2 : 6, \  3 : 1, \  643 : 1\right\}

This option will produce,

.. math::

    \left[ 6, \  1, \  1\right]

Convert Dictionary Key/Values to List of Lists
----------------------------------------------

You will not see dictionaries very often in the CAS but if you do this item will extract all the key/value pairs and create a list of key/value pairs lists from them.

For example, say we have the following dictionary which was the result of ``factorint(123456)``,

.. math::

    \left\{ 2 : 6, \  3 : 1, \  643 : 1\right\}

This option will produce,

.. math::

    \left[ \left[ 2, \  6\right], \  \left[ 3, \  1\right], \  \left[ 643, \  1\right]\right]

