Math Options
============

The options in this submenu do some minor mathematical operations on the grid data.  More advanced operations should be done in the CAS.

Approximate Cells
-----------------

This will approximate the values of each selected cell using the default precision.  Note that the cell entries will be replaced by their approximations, including the formulas.  The old data is still in the undo/redo history and can be retrieved with an undo.

Approximate Cells to Precision
------------------------------

This will approximate the values of each selected cell to the precision the user selects in the dialog box that appears.  Note that the cell entries will be replaced by their approximations, including the formulas.  The old data is still in the undo/redo history and can be retrieved with an undo.

Evaluate Cells
--------------

This option will bring up a dialog box allowing the user to input the list of variables to be evaluated and a corresponding list of expressions or values to evaluate the variables at.  The lists are simply variables or values separated by commas.

Sum
---

This will take the sum of the selected cells.  When this option is selected a dialog box will appear asking the user to input a cell position for the result of the sum.  You may not use any cell position in the selection but may use any other cell.  If you input a position inside the selected range the program will report an error.  If you input a cell position that is already occupied the result will overwrite the contents of that cell.  The old data is still in the undo/redo history and can be retrieved if you mistype the position for the result.

Average
-------

This will take the average of the selected cells.  When this option is selected a dialog box will appear asking the user to input a cell position for the result of the average.  You may not use any cell position in the selection but may use any other cell.  If you input a position inside the selected range the program will report an error.  If you input a cell position that is already occupied the result will overwrite the contents of that cell.  The old data is still in the undo/redo history and can be retrieved if you mistype the position for the result.

Product
-------

This will take the product of the selected cells.  When this option is selected a dialog box will appear asking the user to input a cell position for the result of the product.  You may not use any cell position in the selection but may use any other cell.  If you input a position inside the selected range the program will report an error.  If you input a cell position that is already occupied the result will overwrite the contents of that cell.  The old data is still in the undo/redo history and can be retrieved if you mistype the position for the result.


Uniform Integer Range
---------------------

This will replace all selected cells with pseudo-random integers, between a user-selected lower bound and upper bound, inclusive. Numbers are generated using Python's built-in random number generator. A dialog box will open allowing the user to select the seed (starting point) of the generator, and the lower and upper bounds for the output. The seed option has a button that will allow the user to use the current time from the system clock. The output is a list of pseudo-random numbers in the specified range.

Uniform Float Range
-------------------

This will replace all selected cells with pseudo-random floats, between a user-selected lower bound and upper bound, inclusive. Numbers are generated using Python's built-in random number generator. A dialog box will open allowing the user to select the seed (starting point) of the generator, and the lower and upper bounds for the output. The seed option has a button that will allow the user to use the current time from the system clock. The output is a list of pseudo-random numbers in the specified range.

Binomial Distribution
---------------------

This will replace all selected cells with pseudo-random integers from a binomial distribution. A dialog box will open allowing the user to select the seed (starting point) of the generator, the number of trials for each value and the probability of a success. The seed option has a button that will allow the user to use the current time from the system clock. The output is the number of successes for each trial run.

Normal Distribution
-------------------

This will replace all selected cells with pseudo-random floats from a normal distribution. A dialog box will open allowing the user to select the seed (starting point) of the generator, mu and sigma. The seed option has a button that will allow the user to use the current time from the system clock.

Log Normal Distribution
-----------------------

This will replace all selected cells with pseudo-random floats from a log normal distribution. A dialog box will open allowing the user to select the seed (starting point) of the generator, mu and sigma. The seed option has a button that will allow the user to use the current time from the system clock.

Exponential Distribution
------------------------

This will replace all selected cells with pseudo-random floats from an exponential distribution. A dialog box will open allowing the user to select the seed (starting point) of the generator, and lambda. The seed option has a button that will allow the user to use the current time from the system clock.
