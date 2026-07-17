
Dialog Use & Options
^^^^^^^^^^^^^^^^^^^^

To use the dialog, select the number of points, input any valid expression, that does not contain the set of independent variables (``x``, ``t``, and ``y`` in 2D and ``x``, ``y``, ``z``, ``p``, ``t``, ``u``, and ``v`` in 3D), into each of the cells, see the :doc:`syntax` page for details on expressions.  Note that any blank cells will be replaced with 0 and any blank points (both the x and y cells for the point are empty) are ignored.  Once all the entries are filled out click OK and the set will be added to the plot.


Menu and Tool Options
^^^^^^^^^^^^^^^^^^^^^

The dialog does have a few editing options, many of these have corresponding toolbar buttons.

File Menu
"""""""""

- **Select All:**  Selects all the cells in the expression editing area.

- **Copy Selected:** Copies the selected cells to the clipboard in a tab-delimited format that can be pasted into most spreadsheets.

- **Copy All:** Copies all the cells to the clipboard in a tab-delimited format that can be pasted into most spreadsheets.

- **Paste:** Pastes the clipboard contents into the editing grid.  It is assumed that the data is in tab-delimited format.

- **Fill Selected Cells with Text:** When this option is selected a dialog box will appear allowing the user to input text that will fill all the currently selected cells.

- **Apply Function to Selected Cells:** When this option is selected a dialog box will appear allowing the user to input a function and the variable for substitution that will be applied to all currently selected cells.  The function can be any valid  expression including workspace entries, see the :doc:`syntax` page for details on expressions. The variable is the variable of the expression that each of the selected cell values will be substituted into.  The program will do easy simplifications and evaluations but will not do a full simplify on the new expressions.

- **Trim Cells:** This removes the leading and trailing whitespace characters from each cell.

- **Undo:** Undoes the last edit.

- **Redo:** Redoes the last edit.

- **Clear All:** This clears the grid contents.

View Menu
"""""""""

- **Adjust Column Widths:** This will set the column widths to a size that fits the data in the table.

- **Adjust Row Heights:** This will set the row heights to a size that fits the data in the table.

- **Adjust Row and Column Sizes:** This will set the column widths and row heights to a size that fits the data in the table.

- **Reset Row and Column Sizes:** This resets the column widths and row heights to the original width and height.

- **Increase Font Size:** This increases the font size of the table.

- **Decrease Font Size:** This decreases the font size of the table.

- **Reset Font Size:** This resets the font size of the table.

