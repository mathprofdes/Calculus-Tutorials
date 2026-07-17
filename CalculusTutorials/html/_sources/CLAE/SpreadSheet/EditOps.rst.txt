Edit Options
============

The Edit menu contains standard copy and paste options as one would expect. It also has options for creating LaTeX code, as the program was designed to do, and export to specialized formats.

One non-standard user interface here is the existence of two paste options, Paste and Paste from Clipboard and two different copy options for spreadsheet values, Copy Values and Copy Values as Tab Delimited.  The reason for the two different paste options is to have one that will copy and paste grid information internally as to use cell references and one that will copy and paste to an external spreadsheet program. In general, use Copy Formulas, Copy Values, and Paste when you are copying and pasting from this spreadsheet back into this spreadsheet.  Use Copy Values as Tab Delimited and Paste from Clipboard when you are copying or pasting to and from an external spreadsheet program.  There are numerous other copies designed to be used with external programs.

Copy Formulas
-------------

This copies the formulas of the selected cells to the internal clipboard.  Use this if you want cell references to update on a paste, as is common in standard spreadsheets.  Note that this copy uses an internal clipboard to store the information for the paste command, not the system clipboard.

Copy Values
-----------

This copies the values of the selected cells to the internal clipboard.  Use this if you want to remove the cell references and just paste the cell values. Note that this copy uses an internal clipboard to store the information for the paste command, not the system clipboard..

Paste
-----

Pastes the contents of the clipboard into the grid at the currently selected position.  It is assumed that the data on the clipboard is form either the Copy Formulas or the Copy Values option.  If what is being pasted at the current position needs more space, rows or columns, the content of the paste will be trimmed to a size that fits the spreadsheet, no extra rows or columns will be added to the spreadsheet interface. This spreadsheet is a fixed size. Note that this paste uses the internal clipboard to retrieve the information, use the Paste from Clipboard option to load in the values from an external clipboard.

When pasting in some copied cells the program will paste the block of cells at each location that is currently selected when the paste is initiated.  So if there is only one cell selected when Paste is selected the copied block will be pasted one time at that position.  If a block of 3 rows and 4 columns is selected there will be 12 pastes of the copied data, one using each of the selected positions as the paste target for the copied block.

Copy Values as Tab Delimited
----------------------------

This copies the values of the selected cells to the system clipboard.  Use this if you want to load the cell values into an external spreadsheet program.

Paste from Clipboard
--------------------

Pastes the contents of the system clipboard into the grid at the currently selected position.  It is assumed that the data on the clipboard is in tab-delimited form, a standard format for spreadsheets. If what is being pasted at the current position needs more space, rows or columns, the content of the paste will be trimmed to a size that fits the spreadsheet, no extra rows or columns will be added to the spreadsheet interface. This spreadsheet is a fixed size.

Load to CAS
-----------

This loads the currently selected cells into the CAS of the program.  If a single cell is selected the value of that cell will be loaded as an expression, if a block of cells are selected then the values of the cells in that block will be loaded into the CAS as a matrix.

Copy as LaTeX
-------------

This copies the values of the selected cells to the system clipboard in LaTeX syntax.  If only one cell is selected the copy will be just that cell's expression.  If a block of cells are selected then the copy will be a matrix of the selected cells.

Special LaTeX Copy
------------------

This submenu of options will copy the selected cells to special LaTeX array and matrix formats.

Copy to Array Environment
^^^^^^^^^^^^^^^^^^^^^^^^^

This mode has options for column alignment, a table border, and several options for division lines between rows and columns. These are the same as with the longtable and tabular options. There are also options to include the arraystretch renew command and a decoration, that is include brackets, parenthesis, or vertical bars around the matrix.  Since this will most likely be a displayed formula for your document the code is automatically placed into display math mode.

.. code-block:: latex

    \[
    \left[
    \begin{array}{lll}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{array}
    \right]
    \]

Which would result in the following matrix.

.. math::

    \left[
    \begin{array}{lll}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{array}
    \right]


Copy to Matrix Environment
^^^^^^^^^^^^^^^^^^^^^^^^^^

This option requires the amsmath package to be used. There are options the arraystretch renew, and to include bracket, parenthesis, or vertical bar decorations around the matrix.  Since this will most likely be a displayed formula for your document the code is automatically placed into display math mode.

.. code-block:: latex

    % Package: \usepackage{amsmath}

    \[
    \left[
    \begin{matrix}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{matrix}
    \right]
    \]

Which would result in the following matrix.

.. math::

    \left[
    \begin{matrix}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{matrix}
    \right]


Copy to Special Matrix Environment
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

All of these option will require the amsmath package to be used. When the special matrix option is selected the user will have the option of exporting to a pmatrix, bmatrix, vmatrix, or Vmatrix. The only other option is to include the arraystretch renew command. Since this will most likely be a displayed formula for your document the code is automatically placed into display math mode.

With pmatrix selected, a simple example of the code would look like,

.. code-block:: latex

    % Package: \usepackage{amsmath}

    \[
    \begin{pmatrix}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{pmatrix}
    \]

Which would result in the following matrix.

.. math::

    \begin{pmatrix}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{pmatrix}

With bmatrix selected, a simple example of the code would look like,

.. code-block:: latex

    % Package: \usepackage{amsmath}

    \[
    \begin{bmatrix}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{bmatrix}
    \]

Which would result in the following matrix.

.. math::

    \begin{bmatrix}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{bmatrix}

With vmatrix selected, a simple example of the code would look like,

.. code-block:: latex

    % Package: \usepackage{amsmath}

    \[
    \begin{vmatrix}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{vmatrix}
    \]

Which would result in the following matrix.

.. math::

    \begin{vmatrix}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{vmatrix}

With Vmatrix selected, a simple example of the code would look like,

.. code-block:: latex

    % Package: \usepackage{amsmath}

    \[
    \begin{Vmatrix}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{Vmatrix}
    \]

Which would result in the following matrix.

.. math::

    \begin{Vmatrix}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{Vmatrix}


Selected Cells to LaTeX Code
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This will take the entries in the selected cells and convert them from CAS workspace expressions (SymPy syntax) to LaTeX syntax.  So if you copied an entry or matrix (or several of these) from the CAS to the LaTeX Table Editor tool you can convert them into LaTeX syntax automatically.  For example, if our grid contained the following expressions,

.. code-block:: console

    cos(t^2)    ln(x+4)  x^2-3*x+5
    exp(x)      1/2      4/x
    sin(cos(x)) x/y^2    x^x

This option would alter the grid into the following,

.. code-block:: console

    \cos{\left(t^{2} \right)}                  \ln{\left(x + 4 \right)}  x^{2} - 3 x + 5
    e^{x}                                      \frac{1}{2}               \frac{4}{x}
    \sin{\left(\cos{\left(x \right)} \right)}  \frac{x}{y^{2}}           x^{x}


Selected Cells to LaTeX Code in Math Mode
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This will take the entries in the selected cells and convert them from CAS workspace expressions (SymPy syntax) to LaTeX syntax and put each cell into inline math mode.  So if you copied an entry or matrix (or several of these) from the CAS to the LaTeX Table Editor tool you can convert them into LaTeX syntax automatically.  For example, if our grid contained the following expressions,

.. code-block:: console

    cos(t^2)    ln(x+4)  x^2-3*x+5
    exp(x)      1/2      4/x
    sin(cos(x)) x/y^2    x^x

This option would alter the grid into the following,

.. code-block:: console

    $\cos{\left(t^{2} \right)}$                   $\ln{\left(x + 4 \right)}$   $x^{2} - 3 x + 5$
    $e^{x}$                                       $\frac{1}{2}$                $\frac{4}{x}$
    $\sin{\left(\cos{\left(x \right)} \right)}$   $\frac{x}{y^{2}}$            $x^{x}$


Copy to Longtable Environment
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The Longtable Environment and Tabular Environment have options for column alignment, a table border, and several options for division lines between rows and columns. The Column Alignment is the alignment used for all columns in the table. These can be overridden by header rows or columns. The alignment is on each column but is easily editable in the pasted LaTeX code.

The Divisions options are for the selection of common division lines in the table. If you have worked with LaTeX you know there are many more possibilities here for row and column divisions. This tool just includes some of the more common selections and if they are not exactly what is needed it should only take some minimal editing.

- Table Boarder puts a simple border around the entire table.
- Division After First Row puts a line directly below the first row.
- Division on All Rows puts a line directly below each row of the table and one at the top.
- Division After First Column puts a line directly to the right of the first column.
- Division After All Columns puts a line directly to the right of each column of the table and one at the left.

At the bottom there are options to include math mode around the contents of each cell, and to include the arraystretch renew command. If the math mode is selected, then each cell will be put into inline math mode.

There are also have options for both row and column headers. Each header type can include as many rows and columns as you wish, you can set the alignment of the headers as well as the font styles of the headers. When a cell is both a row header and a column header the attributes for the column header are used. For example,

- A table with no headers:

.. figure:: Images/Tab001.png
    :alt: A table with no headers.

- The same table with just one column header in bold:

.. figure:: Images/Tab002.png
    :alt: The same table with just one column header in bold.

- The same table with just one row header in italics:

.. figure:: Images/Tab003.png
    :alt: The same table with just one row header in italics.

- The same table with one row header in italics and one column header in bold:

.. figure:: Images/Tab004.png
    :alt: The same table with one row header in italics and one column header in bold.

A simple example of the output of this option, note the commented inclusion of the preamble package.

.. code-block:: latex

    % Package: \usepackage{longtable}

    \begin{longtable}[l]{lll}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{longtable}


Copy to Tabular Environment
^^^^^^^^^^^^^^^^^^^^^^^^^^^

The Longtable Environment and Tabular Environment have options for column alignment, a table border, and several options for division lines between rows and columns. The Column Alignment is the alignment used for all columns in the table. These can be overridden by header rows or columns. The alignment is on each column but is easily editable in the pasted LaTeX code.

The Divisions options are for the selection of common division lines in the table. If you have worked with LaTeX you know there are many more possibilities here for row and column divisions. This tool just includes some of the more common selections and if they are not exactly what is needed it should only take some minimal editing.

- Table Boarder puts a simple border around the entire table.
- Division After First Row puts a line directly below the first row.
- Division on All Rows puts a line directly below each row of the table and one at the top.
- Division After First Column puts a line directly to the right of the first column.
- Division After All Columns puts a line directly to the right of each column of the table and one at the left.

At the bottom there are options to include math mode around the contents of each cell, and to include the arraystretch renew command. If the math mode is selected, then each cell will be put into inline math mode.

There are also have options for both row and column headers. Each header type can include as many rows and columns as you wish, you can set the alignment of the headers as well as the font styles of the headers. When a cell is both a row header and a column header the attributes for the column header are used. For example,

- A table with no headers:

.. figure:: Images/Tab001.png
    :alt: A table with no headers.

- The same table with just one column header in bold:

.. figure:: Images/Tab002.png
    :alt: The same table with just one column header in bold.

- The same table with just one row header in italics:

.. figure:: Images/Tab003.png
    :alt: The same table with just one row header in italics.

- The same table with one row header in italics and one column header in bold:

.. figure:: Images/Tab004.png
    :alt: The same table with one row header in italics and one column header in bold.

A simple example of the output of this option, note the commented inclusion of the preamble package.

.. code-block:: latex

    \begin{tabular}{lll}
    1 & 4 & 7 \\
    2 & 5 & 8 \\
    3 & 6 & 9 \\
    \end{tabular}


Copy to Tabbing Environment
^^^^^^^^^^^^^^^^^^^^^^^^^^^

The Tabbing Environment has only two options, the column spacing for each column and to include math mode on each cell. The column spacing will be in points, remember 72 points to an inch. If the math mode is selected, then each cell will be put into inline math mode. A simple example of the output of this option,

.. code-block:: latex

    \begin{tabbing}
    \hspace{20pt}\=\hspace{20pt}\=\hspace{20pt}\=\kill
    1 \> 4 \> 7 \\
    2 \> 5 \> 8 \\
    3 \> 6 \> 9 \\
    \end{tabbing}


Copy as GeoGebra
----------------

The Copy as GeoGebra will formulate the grid as a GeoGebra matrix, that is { } delimited. For example, the standard grid

.. code-block:: console

    1  4  7
    2  5  8
    3  6  9

copies as

.. code-block:: console

    {{1,4,7},{2,5,8},{3,6,9}}


Copy as Maxima
--------------

The Copy as Maxima will formulate the grid as a Maxima matrix. For example, the standard grid

.. code-block:: console

    1  4  7
    2  5  8
    3  6  9

will copy as

.. code-block:: console

    matrix([1,4,7],[2,5,8],[3,6,9])


Copy as SageMath
----------------

The Copy as SageMath will formulate the grid as a SageMath matrix. For example, the standard grid

.. code-block:: console

    1  4  7
    2  5  8
    3  6  9

will copy as

.. code-block:: console

    matrix(QQ,[[1,4,7],[2,5,8],[3,6,9]])


Copy (...) Delimited
--------------------

This copies as ( ) delimited string. For example, the standard grid

.. code-block:: console

    1  4  7
    2  5  8
    3  6  9

copies as

.. code-block:: console

    ((1,4,7),(2,5,8),(3,6,9))

Copy [...] Delimited
--------------------

This copies as [ ] delimited string. For example, the standard grid

.. code-block:: console

    1  4  7
    2  5  8
    3  6  9

copies as

.. code-block:: console

    [[1,4,7],[2,5,8],[3,6,9]]

Copy {...} Delimited
--------------------

This copies as { } delimited string. For example, the standard grid

.. code-block:: console

    1  4  7
    2  5  8
    3  6  9

copies as

.. code-block:: console

    {{1,4,7},{2,5,8},{3,6,9}}


Copy <...> Delimited
--------------------

This copies as < > delimited string. For example, the standard grid

.. code-block:: console

    1  4  7
    2  5  8
    3  6  9

copies as

.. code-block:: console

    <<1,4,7>,<2,5,8>,<3,6,9>>


Copy as HTML
------------

This copies the table to HTML markup. For example, the standard grid

.. code-block:: console

    1  4  7
    2  5  8
    3  6  9

copies as

.. code-block:: html

    <TABLE BORDER=1 CELLPADDING=1 CELLSPACING=0>
    <TR>
    <TD>1</TD><TD>4</TD><TD>7</TD>
    </TR>
    <TR>
    <TD>2</TD><TD>5</TD><TD>8</TD>
    </TR>
    <TR>
    <TD>3</TD><TD>6</TD><TD>9</TD>
    </TR>
    </TABLE>

Undo & Redo
-----------

This tool also has its own undo and redo history. Every time the grid is changed the undo history is updated with the new grid. The program does not limit the number of undos that are possible.

Delete
------

This will remove the currently selected cells from the grid.  As with all edits the old data is still in the undo/redo history and can be retrieved with an undo.

