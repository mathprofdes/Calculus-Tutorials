String Conversion Options
=========================

UPPERCASE
---------

Converts the selected text to uppercase.  For example,

.. code-block:: console

    The Text Editor is a simple text and numeric manipulation tool.

is converted to

.. code-block:: console

    THE TEXT EDITOR IS A SIMPLE TEXT AND NUMERIC MANIPULATION TOOL.

lowercase
---------

Converts the selected text to lowercase.  For example,

.. code-block:: console

    The Text Editor is a simple text and numeric manipulation tool.

is converted to

.. code-block:: console

    the text editor is a simple text and numeric manipulation tool.



Capitalize
----------

Capitalizes each word in the selected text. For example,

.. code-block:: console

    The Text Editor is a simple text and numeric manipulation tool.

is converted to

.. code-block:: console

    The Text Editor Is A Simple Text And Numeric Manipulation Tool.

Remove All Whitespace
---------------------

Removes all whitespace characters from the selected text, including whitespace between non-whitespace characters.  For example,

.. code-block:: console

    The Text    Editor is a simple

    text and             numeric


    manipulation   tool           .

is converted to

.. code-block:: console

    TheTextEditorisasimpletextandnumericmanipulationtool.

Whitespace to Single Spaces
---------------------------

Replaces all whitespace character sequences with a single space character. For example,

.. code-block:: console

    The Text    Editor is a simple

    text and             numeric


    manipulation   tool           .

is converted to

.. code-block:: console

    The Text Editor is a simple text and numeric manipulation tool .


Remove Whitespace Per Line
--------------------------

Removes all whitespace characters from the selected text, including whitespace between non-whitespace characters line by line. For example,

.. code-block:: console

    The Text    Editor is a simple

    text and             numeric


    manipulation   tool           .

is converted to

.. code-block:: console

    TheTextEditorisasimple

    textandnumeric


    manipulationtool.


Remove Punctuation
------------------

Removes all punctuation characters from the editor text. For example,

.. code-block:: console

    The Text Editor, is a simple text, and numeric manipulation tool!

is converted to

.. code-block:: console

    The Text Editor is a simple text and numeric manipulation tool

Remove Numbers
--------------

Removes all numeric characters from the editor text. For example,

.. code-block:: console

    Most computer programming languages treat integers such as 4 as
    being different from real numbers such as 4.000000004.

is converted to

.. code-block:: console

    Most computer programming languages treat integers such as  as
    being different from real numbers such as ..

Remove All Non-Letters
----------------------

Removes all characters that are not alphabetic characters. For example,

.. code-block:: console

    Written using engineering notation the imaginary part is written
    with a j suffix, e.g. 3 + 1j.

is converted to

.. code-block:: console

    Written using engineering notation the imaginary part is written
    with a j suffix eg   j


Split (Spaces to Line Breaks)
-----------------------------

Converts each space to a line break. For example,

.. code-block:: console

    The Text Editor   is a simple text   and numeric manipulation tool.

is converted to

.. code-block:: console

    The
    Text
    Editor


    is
    a
    simple
    text


    and
    numeric
    manipulation
    tool.

Join (Line Breaks to Spaces)
----------------------------

Converts each line break to a space. For example,

.. code-block:: console

    The
    Text
    Editor


    is
    a
    simple
    text


    and
    numeric
    manipulation
    tool.

is converted to

.. code-block:: console

    The Text Editor   is a simple text   and numeric manipulation tool.


Remove Blank Lines
------------------

Removes all blank lines from the editor text. For example,

.. code-block:: console

    The

    Text
    Editor


    is
    a
    simple
    text


    and
    numeric

    manipulation
    tool.

is converted to

.. code-block:: console

    The
    Text
    Editor
    is
    a
    simple
    text
    and
    numeric
    manipulation
    tool.

Remove Multiple Blank Lines
---------------------------

Converts multiple blank lines to a single blank line. For example,

.. code-block:: console

    The

    Text
    Editor


    is
    a
    simple
    text


    and
    numeric

    manipulation
    tool.


is converted to

.. code-block:: console

    The

    Text
    Editor

    is
    a
    simple
    text

    and
    numeric

    manipulation
    tool.


Remove Front Whitespace
-----------------------

Removes whitespace characters from the beginning of each line. Any whitespace characters at the end of the line or between non-whitespace characters are not removed. For example,

.. code-block:: console

      The Text Editor is a
             simple text and numeric
         manipulation tool.

is converted to

.. code-block:: console

    The Text Editor is a
    simple text and numeric
    manipulation tool.


Remove End Whitespace
---------------------

Removes whitespace characters from the end of each line. Any whitespace characters at the beginning of the line or between non-whitespace characters are not removed.  For example,

.. code-block:: console

    The Text Editor is a
    simple text and numeric
    manipulation tool.

is converted to

.. code-block:: console

    The Text Editor is a
    simple text and numeric
    manipulation tool.

There was trialing whitespace on each line of the original and none on the result.

Trim Lines
----------

Removes whitespace characters from the beginning and end of each line. Any whitespace characters between non-whitespace characters are not removed. For example,

.. code-block:: console

      The Text Editor is a
             simple text and numeric
         manipulation tool.

is converted to

.. code-block:: console

    The Text Editor is a
    simple text and numeric
    manipulation tool.

Convert Tabs to Spaces
----------------------

Replaces all tab characters with the desired (selected in the submenu) number of spaces (1-5).

Convert Spaces to Tabs
----------------------

Replaces all space characters with a tab character.

Replace All
-----------

Brings up a dialog box allowing the user to input target and replacement strings and will replace all occurrences of the target with the replacement. The replacement is done in a case sensitive manner.

Split At
--------

Brings up a dialog box allowing the user to input a string that will be used for splitting the selected text. The string that is split over is removed from the text and replaced with line breaks. For example, if we take the text,

.. code-block:: console

    The Text Editor is a simple text and numeric manipulation tool.

and split it at the character ``a`` we get,

.. code-block:: console

    The Text Editor is
     simple text
    nd numeric m
    nipul
    tion tool.

If we take the text,

.. code-block:: console

    The Text Editor is a simple text and numeric manipulation tool.

and split it at the string ``and`` we get,

.. code-block:: console

    The Text Editor is a simple text
     numeric manipulation tool.


Break Character Stream
----------------------

Brings up a dialog box allowing the user to select the number of characters for each line and places a line break after each block of characters of this length. There is also an option for preserving words that will put the break after the word the fills the block. So in if this option is selected there may be lines longer than the block size selected. For example, if we take the text,

.. code-block:: console

    The Text Editor is a simple text and numeric manipulation tool.

and split it at 20 characters without preserving words we get,

.. code-block:: console

    The Text Editor is a
    simple text and nume
    ric manipulation too
    l.

If we had split it at 20 characters with preserving words we get,

.. code-block:: console

    The Text Editor is a
    simple text and
    numeric manipulation
    tool.


Reformat Text
-------------

Brings up a dialog box allowing the user to select the maximum number of characters for each line and places a line break after each block of characters of this length. This automatically preserves words when possible.

For example, if we take the text,

.. code-block:: console

    The Text Editor is a simple text and numeric manipulation tool.

and reformat to 20 characters we get,

.. code-block:: console

    The Text Editor is a
    simple text and
    numeric manipulation
    tool.


Remove Double Characters
------------------------

Replaces double characters with an X between the characters.  If the double characters are XX then a Z is placed between them. This is probably not very useful in general but it does come in handy when studying classical cryptography. For example,

.. code-block:: console

    This is a test of the tool for removing double
    characters, committee, XXXX, ZZZ...

is converted to

.. code-block:: console

    This is a test of the toXol for removing double
    characters, comXmitXteXe, XZXZXZX, ZXZXZ.X.X.



