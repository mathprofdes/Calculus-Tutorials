:index:`Spreadsheet`
====================

Introduction
------------

The Spreadsheet tool is not a standard spreadsheet, it is a grid of CAS type expressions, that is, SymPy expressions with the added syntax of CAS entry designations and spreadsheet cell references.  Since each cell is a CAS expression updating the cell is the same as parsing the expression and can be time consuming if there are a lot of dependencies between the cells.  For this reason we have limited the size of the grid to 50 rows and 26 columns, frankly if you need more than that you are probably using the wrong application.

This tool is useful in the construction of special matrices you may see near the end of a Linear Algebra class or if you are working with experimental data and need to do some manipulations before putting it into a matrix in the CAS.  The interface looks like a standard spreadsheet with a grid of cells.  Menu and toolbar are at the top for a few options for data manipulation.

.. figure:: Images/SSView001.png
    :alt: Spreadsheet Layout

    Spreadsheet Layout

Each cell is designated in a usual spreadsheet manner A1, A2, ..., B1, B2, ... Z50, where the letter is the column you are in and the number is the row.  These designations can be used in the cell formulas for each cell. The page on :doc:`syntax` will go into the details of expression syntax for the cells.  In most cases the syntax is the same as with the CAS with two exceptions, first, you can use cell designations in your expressions and second, if you want to use a CAS entry you use two Rs instead of one.  So if you want the CAS entry R3 in your cell expression you would use RR3 in place of R3.  The reason for the extra R is because R1, R2, ..., R50 represent cell locations.

Each cell contains a value and a formula.  When a cell is selected, its designation is seen in the cell information bar below the toolbar.  Shown below,

.. figure:: Images/SSView002.png
    :alt: Spreadsheet Cells and Cell Information

    Spreadsheet Cells and Cell Information

The first item is the cell designation, A1, A2, ... The next box contains the cell value, this is what appears in the cell unless you are editing the cell.  The third item is the cells formula, the cell formula is the expression that use user input.  These text areas are not editable, all edits are done directly in the cell you wish to edit.  To edit a cell you can simply type in the new expression, this will remove the old contents.  You can also hit ``F2`` or double-click the cell to shift into edit mode.  Note that when you do shift into edit mode the contents of the cell will change from the cell's value to the cell's formula.

When the user inputs an expression into the cell the cell designations are saved in the formula but replaced by the cell contents for the value.  If the user inputs a CAS designation, RR1, RR2, ... these are replaced with the CAS entry immediately and not left as references in the formula.  Since entries can be deleted from the CAS, it is possible that a CAS reference will be lost.

When the user copies and pastes cells from one section of the spreadsheet to another, the cell designations in the formulas are automatically updated by the vertical and horizontal shift between the upper right corner of the selected (and copied) cells and the position of the paste.  If you wish to fix a cell position in your formula and not have it update with a paste simply begin the designation with an underscore.  So for example, if you have the formula ``A1 + _A2`` in a cell and you copy and paste this cell to another location, the ``A1`` will be updated by the shift but ``_A2`` will remain ``_A2`` in the new cells and, of course, be replaced by the value of ``A2`` in the value of the cell.

Unlike the CAS, where all entries are independent to each other, the spreadsheet cells will have dependencies with each other.  Any cell that uses a cell designation in its formula will set up a dependency.  When any cell is changed the program will run through the grid and update any cells that are dependent on it.  This will cascade into another set of cells that have changed and hence the program will update those dependent cells, and so on.  Since the program will not allow circular referencing, this process will terminate but if there are a lot of dependencies the cell update may show some pause before being completed.


Quick Guides
------------

.. toctree::
    :maxdepth: 3
    :caption: Quick Guides
    :titlesonly:

    LayoutUse
    syntax
    cassyntax

Spreadsheet Options
-------------------

.. toctree::
    :maxdepth: 3
    :caption: Spreadsheet Options
    :titlesonly:

    FileOps
    EditOps
    MathOps
    ViewOps
