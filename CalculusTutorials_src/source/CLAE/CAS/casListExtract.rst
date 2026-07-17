:index:`Extract from List`
==========================

This submenu has several options for extracting and reordering list elements.

Extract Entry from List
-----------------------

This option is for extracting a single element from a list of elements.  When selected, a dialog box will open asking the user to input the position of the entry to extract.  The counting starts at 1, so 1 is the first element, 2 the second and so on.

Extract All List Entries
------------------------

This option extracts all the entries from a list but leaves the nested lists intact.

For example, if your list is

.. math::

    \left[ 2, \  \left[ 3, \  4, \  5\right], \  \left[ a, \  b, \  c, \  \left[ d, \  e\right], \  f\right], \  \left[ x, \  \left[ y, \  z\right]\right]\right]

This option will load the following new entries into the CAS workspace.

.. math::

    2


.. math::

    \left[ 3, \  4, \  5\right]

.. math::

    \left[ a, \  b, \  c, \  \left[ d, \  e\right], \  f\right]

.. math::

    \left[ x, \  \left[ y, \  z\right]\right]

Reorder List by Pattern
-----------------------

This option extracts entries from a list according to a pattern of position numbers, the result is another list.  When selected a dialog box will appear asking for the entry pattern.  The pattern is simply a list of row numbers separated by at least one space. For example, the pattern ``1 3 5 2`` will extract entries 1, 3, 5, and 2 in that order and create a new list with those 4 elements.  This has the added bonus of being able to rearrange and to duplicate the entries of a list.  For example, if the list has 3 entries then ``1 3 2`` will interchange entries 2 and 3.  Also, ``1 3 3 2 1`` will duplicate entry 3 for the new entries 2 and 3 and put a duplicate of entry 1 at the end.

For example, if the list is,

.. math::

    \left[ a, \  b, \  c, \  x, \  y, \  z\right]

So if we used the pattern 1 3 5 2 we would get,

.. math::

    \left[ a, \  c, \  y, \  b\right]

and if we used the pattern 1 3 3 2 1 we would get,

.. math::

    \left[ a, \  c, \  c, \  b, \  a\right]

Reverse List
------------

This option simply reverses the order of the list elements.

For example, the list,

.. math::

    \left[ 1, \  2, \  3, \  \left[ a, \  b\right], \  c, \  \left[ x, \  y, \  z\right]\right]

would be reversed to ,

.. math::

    \left[ \left[ x, \  y, \  z\right], \  c, \  \left[ a, \  b\right], \  3, \  2, \  1\right]

Extract Sublist Range
---------------------

Ths option extracts a range of elements from a list and returns the sublist of those elements.  When selected a dialog box will appear asking the user for the beginning and ending index of the sublist range.


Extract Pattern from Nested List
--------------------------------

This option extracts elements from a nested list.  If you have a list of lists and wish ti extract an element from an inner list this tool allows you to do that quickly.  When selected, a dialog box will appear asking for the extraction pattern.  The pattern is a sequence of positions, the first is the position of an inner list, the second is the position of a list within it, and so on until the position of the element you wish to extract.  Each number in the sequence should be separated by at least one space.

For example, if your list is

.. math::

    \left[ 2, \  \left[ 3, \  4, \  5\right], \  \left[ a, \  b, \  c, \  \left[ d, \  e\right], \  f\right], \  \left[ x, \  \left[ y, \  z\right]\right]\right]

If we use the pattern 2 3 we get

.. math::

    5

If we use the pattern 3 4 we get

.. math::

    \left[ d, \  e\right]


If we use the pattern 3 4 1 we get

.. math::

    d


If we use the pattern 1 we get

.. math::

    2

