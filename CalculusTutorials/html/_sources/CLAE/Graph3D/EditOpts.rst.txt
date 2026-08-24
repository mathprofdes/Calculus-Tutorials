Editing Options
===============

Copy Expression
---------------

Copies the expression to the clipboard in SymPy syntax.  You would use this option if you were going to copy and paste the expression back to the CAS or paste the expression into another instance of the program.   Note that a Drag-and-Drop from the graphics manager to the CAS or another instance of the program will do the same thing.


Copy Expression with Slider Values
----------------------------------

Copies the expression to the clipboard in SymPy syntax and loads the current slider values into the constants in the expression.  You would use this option if you were going to copy and paste the expression with slider values back to the CAS or paste the expression into another instance of the program.   For example, if you have the expression :math:`a \sin{\left(b x + c \right)}` in the graphics manager and have the a slider set to 3, b slider to 4 and c slider to -2, this option will copy ``3.0*sin(4.0*x - 2.0)`` to the clipboard.


Paste Expression
----------------

This will paste the contents of the clipboard into the graphics manager.  It is assumed that the clipboard contains text that is SymPy syntax for a legitimate expression.  If the program cannot parse the clipboard expression into a graphics object you will get an error.

Duplicate Object
----------------

This makes a copy of the object and creates a new graphics entry from this object.  Note that the graphics type and all the attributes of the original object are duplicated into this new object.

Duplicate Object with Slider Values
-----------------------------------

This makes a copy of the object, substituting in the current slider values, and creates a new graphics entry from this object.  Note that the graphics type and all the attributes of the original object are duplicated into this new object.  The only difference is that the constants have been replaced with the values of the sliders.

Copy Selected Object Description
--------------------------------

This copies the description of the graphics object to the clipboard.  Note that when a description id too long it is truncated with ... at the end.  This option copies the entire description even if the display of the description is truncated.

Copy Items List to Image
------------------------

This will copy the item list to an image that can be pasted into another application.  When this option is invoked a dialog box will appear asking the user to select the font for the description, the default is the font currently being used for the description, the extra padding to use for the image, and how many characters to trim the descriptions to.  When the user clicks OK the image of the item list will be sent to the clipboard.  This option would be useful to create an external legend of the graphics window.

Copy Items List to Text
-----------------------

This will copy the item list to text that can be pasted into another application. Note that the color boxes for the objects are not copied as they are in the list to image option above.

Copy Slider Values to Image
---------------------------

This will copy the slider list along with the current slider settings to an image that can be pasted into another application.  When this option is invoked a dialog box will appear asking the user to select the font for the text, the default is the font currently being used for the description, the extra padding to use for the image, and how many characters to trim the entries to.  When the user clicks OK the image of the slider value list will be sent to the clipboard.


Copy Slider Values to Text
--------------------------

This will copy the slider value list to text that can be pasted into another application.

Delete Selected Object
----------------------

This removes the selected graphics object from the plot.

Undo
----

Undoes the last edit of the graph.

Redo
----

Redoes the last edit of the graph.

