:index:`Process Manager`
========================

Computer Algebra System Processes
---------------------------------

Computer algebra systems are notoriously slow.  The amount of calculations needed to do exact arithmetic as well as symbolic manipulation are far greater than approximating results, especially if it is using system hardware to do it.  Hence there are some operations that could take a long time to complete.  For example, large simplifications, integration, matrix operations on large matrices, etc.  If we did not do these calculations in separate processes the program user interface would stop functioning while the calculation was being done.

When any option in the Algebra, Calculus, Matrix, or Vector menus is invoked a separate process from the one the main program is running in is spawned, the operation is given to that other process to complete.  When the calculation is finished the separate process sends the result back to the main and the result is placed in the CAS workspace.  You may notice a little pause when you input an expression or apply a calculation to an entry, this is due to the spawning of the separate process.

The con to this is that you do get a hesitation on operations that would be otherwise nearly instantaneous.  The pro to this is that long calculations do not lock up the program and you can continue working while the process is running.  The status bar displays the number of processes that are currently running if there are any.  If you close that program while a process is running the program will end the process.

The Process Manager
-------------------

Although you do not need to do this, you can cancel a running process using the Process Manager.  There is no harm in allowing one of these background processes to keep running as you work. The exception would be if you have several running at the same time it will take up your system resources.  In most cases the operations will not be lengthy and the processes will finish in a reasonable amount of time, many times before you even have the chance to do another operation.

If you do wish to stop a process select ``Edit > Process Manager`` from the main menu.  At this point the process manager dialog box will appear.

.. figure:: Images/ProcessManager001.png
    :alt: Process Manager Dialog Box

    Process Manager Dialog Box

All currently running processes will be listed in the list in the center of this dialog.  From our example, there is a simplification process that is currently running.  Each line in this list is a separate calculation that is running in the background.  The first number is just the process ID and is not needed by the user, after that, the human-readable description of the calculation is given.  To stop the process simply select the process you wish to stop by clicking it in the list, then select ``Stop Selected Calculation``.  To close the dialog box and keep all calculations running select ``Continue All Calculations``.

You can only stop one process at a time, so to stop several of them you need to back into the manager.  Also, if a process finishes while you have this dialog box open the process result be loaded into the CAS workspace and it will not matter if you select to stop or not stop the process, your selection will be ignored since the process is no longer active.
