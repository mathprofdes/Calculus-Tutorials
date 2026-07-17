:index:`Piecewise Expression Input`
===================================

:index:`The Piecewise Function Input Dialog Box`
------------------------------------------------

In most computer algebra systems inputting a piecewise defined function uses rather lengthy syntax, SymPy is no exception.  So to make these easier for the user we created a special dialog box for this purpose.  Select ``Edit > Input Piecewise Defined Function...`` from the main menu or its corresponding toolbar button to open the piecewise function input dialog box.

.. figure:: Images/Piecewise001.png
    :alt: Piecewise Function Input Dialog Box

    Piecewise Function Input Dialog Box


Dialog Use & Options
--------------------

To use the dialog, select the number of expressions, or pieces, the function is broken down into.  In the expression column input any valid expression, see the :doc:`../CLAE/syntax` for details on expressions.  In the corresponding Domain column, input the logical expression to be tested for that expression.  The syntax on the logical expressions is below.  Once all the entries are filled out click OK and the expression will be loaded into the CAS workspace.

With a piecewise defined expression the domains do not need to be mutually exclusive.  The way it is read is that the first logical expression is tested, if the result is true the first expression is evaluated and the result is returned as the function value.  If the first domain condition is false then the second condition is checked, if true the second expression is evaluated and result returned.  This continues until a valid domain is found.  When inputting the domains you can leave the last one blank and it will be interpreted as an "otherwise" entry (displayed as True).


:index:`Piecewise Function Domain Logical Syntax`
-------------------------------------------------

Basic Domain Expressions
^^^^^^^^^^^^^^^^^^^^^^^^

The basic domain expressions are single binary logical operators.

- ``>`` for greater than.
- ``>=`` for greater than or equal to.
- ``<`` for less than.
- ``<=`` for less than or equal to.
- ``==`` for equal to.
- ``!=`` for not equal to.

For example,

- ``x > 3``
- ``y <= 5``
- ``x*2*y-1 > 0``


Logical Expression Connectors
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Logical expressions can be combined with the standard connectors of and, or, and not.  The and connector is done with ``&``, or is done with ``|`` and not is done with ``~``. Also, each basic logical expression needs to be in parentheses.

For example,

- ``(x > -2) & (x <= 5)``
- ``(x < -2) | (x >= 5)``
- ``~(x > 2)``

You can do more combinations and you can nest logical expressions.

.. note::

    One thing that is a little surprising, especially for those who know a bit of Python programming, is that the syntax of ``-2 < x <= 5`` is not supported.  That expression needs to be written as ``(x > -2) & (x <= 5)``.

Basic Example
^^^^^^^^^^^^^

For a basic example, say we input the following into the dialog box,

.. figure:: Images/Piecewise004.png
    :alt: Piecewise Function Input Example

    Piecewise Function Input Example

This will create the function,

.. math::

    \begin{cases} x^{2} & \text{for}\: x \geq -2 \wedge x \leq 3 \\\sin{\left(x \right)} & \text{for}\: x < 0 \\\ln{\left(x \right)} & \text{otherwise} \end{cases}

If we plot this function we get the following graph.

.. figure:: Images/Piecewise005.png
    :alt: Piecewise Function Graph

    Piecewise Function Graph

Note that although we defined this expression to be :math:`\sin(x)` for :math:`x < 0` the function only evaluates to :math:`\sin(x)` for :math:`x < -2` since the first expression is true for :math:`-2 <= x <= 3`.  Also, the :math:`\ln(x)` piece is defaulted to otherwise.

Example of a Domain Restriction
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We can also use a piecewise expression to do a simple domain restriction.  For example, if we use a single expression ``x^2`` and the domain ``(x >= -2) & (x <= 3)``,

.. figure:: Images/Piecewise006.png
    :alt: Piecewise Function Domain Restriction

    Piecewise Function Domain Restriction

This comes into the CAS as,

.. math::

    \begin{cases} x^{2} & \text{for}\: x \geq -2 \wedge x \leq 3 \end{cases}

and if we graph it we get the following image.

.. figure:: Images/Piecewise002.png
    :alt: Domain Restriction Graph

    Domain Restriction Graph


.. note::

    Notice on the above example that the endpoints are not enhanced like we usually do when displaying a piecewise defined expression.  This enhancement is not built into the program but if you are creating an image for a professional document or for a quiz or exam you can manually add these in using a point set object.  For example,

    .. figure:: Images/Piecewise003.png
        :alt: Domain Restriction Graph Enhanced

        Domain Restriction Graph Enhanced


Menu and Tool Options
---------------------

The dialog does have a few editing options, many of these have corresponding toolbar buttons.

File Menu
^^^^^^^^^

- **Select All:**  Selects all the cells in the expression editing area.

- **Copy Selected:** Copies the selected cells to the clipboard in a tab-delimited format that can be pasted into most spreadsheets.

- **Copy All:** Copies all the cells to the clipboard in a tab-delimited format that can be pasted into most spreadsheets.

- **Paste:** Pastes the clipboard contents into the editing grid.  It is assumed that the data is in tab-delimited format.

- **Trim Cells:** This removes the leading and trailing whitespace characters from each cell.

- **Clear All:** This clears the grid contents.


View Menu
^^^^^^^^^

- **Adjust Column Widths:** This will set the column widths to a size that fits the data in the table.

- **Adjust Row Heights:** This will set the row heights to a size that fits the data in the table.

- **Adjust Row and Column Sizes:** This will set the column widths and row heights to a size that fits the data in the table.

- **Reset Row and Column Sizes:** This resets the column widths and row heights to the original width and height.

- **Increase Font Size:** This increases the font size of the table.

- **Decrease Font Size:** This decreases the font size of the table.

- **Reset Font Size:** This resets the font size of the table.

