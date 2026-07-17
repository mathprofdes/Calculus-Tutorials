:index:`File Options`
=====================

Clear CAS
---------

Clearing the Computer Algebra System workspace can be done by selecting ``File > Clear CAS`` from the main menu or clicking the corresponding toolbar button. Clearing the CAS will simply clear the Computer Algebra System workspace list on the left and leave the other tools alone.  Clearing the CAS, as with all the other tools does not delete the current state of the tool but simply adds a clean worksheet to the undo/redo history.  Hence, if you clear the CAS and really did not want to do so you can simply select Undo from the main menu or the corresponding toolbar button to restore the CAS to what it was before the clear operation.


Open Workspaces
---------------

Although we overuse the term workspace in this documentation, since there really are six separate workspaces incorporated in the program, saving and loading workspaces will save and load all the workspace data from each tool into a single file.  So the CAS, 2-D plots, 3-D plots, etc. will all be saved or opened.

When selecting ``File > Open Workspaces...`` from the main menu or clicking the corresponding toolbar button an open dialog box will appear allowing you to select a file (.clf).  When you open a file, each tools workspace data will be replaced with the file's contents. This really means that for each tool the file data will replace the current data of that tool but the current data for the tool is not deleted, it is still in the undo/redo history.  So you can go back to the previous by selecting Undo in the tools menu or toolbar.


Save Workspaces
---------------

When selecting ``File > Save Workspaces...`` the program will save the current data from each of the program workspaces to a file.  If no file has been saved or opened a save dialog box will appear allowing you to input a filename for the data (.clf). If a file has been saved or opened then the data is saved to the current file, thus overwriting the file's current contents.


Save Workspaces As
------------------

When selecting ``File > Save Workspaces As...`` from the main menu or clicking the corresponding toolbar button a save dialog box will appear allowing you to input a filename for the data (.clf).


Open CAS
--------

When selecting ``File > Open CAS...`` from the main menu an open dialog box will appear allowing you to select a CAS file (.clm).  When you open a file, the CAS data will replace the current data of the CAS workspace. The current data in the CAS is not deleted, it is still in the undo/redo history.  So you can go back to the previous by selecting Undo in the main menu.

Save CAS As
-----------

When selecting ``File > Save CAS As...`` from the main menu a save dialog box will appear allowing you to input a filename for the CAS data (.clm).


Print
-----

Selecting ``File > Print...`` will open a print dialog box allowing you to select a printer and printer options for printing the contents of the CAS workspace.  The print job will use the same font as is being used to display the CAS entries.  Since the expression wrapping for printing is set at 75 characters you will want to reset the font size to the default before printing, if you made any change to this.


Print Preview
-------------

Selecting ``File > Print Preview...`` will open a print preview dialog box allowing you to view the perspective print job as well as select a printer and printer options for printing the contents of the CAS workspace.  The print job will use the same font as is being used to display the CAS entries.  Since the expression wrapping for printing is set at 75 characters you will want to reset the font size to the default before printing, if you made any change to this.

.. figure:: Images/PrintPreview001.png
    :alt: Print Preview Dialog Box

    Print Preview Dialog Box

.. note::

    The CLAE program has many facilities for exporting information in forms that are easily loaded into other word processors and LaTeX IDEs.  So when creating documents or materials it is better to use these features then it is to do a workspace print.  We will cover these features in other sections of this documentation.
