:index:`Introduction`
=====================

:index:`To the User`
--------------------

The Calculus & Linear Algebra Explorer (CLAE) is a program that was developed for the quick and easy exploration of concepts usually studied in an introductory Calculus sequence and in an elementary Linear Algebra class at the college and university level.

This program was written with several goals in mind:

- **A Useful Educational Tool:** The main goal of this software package is to be a useful technology tool for learning and teaching concepts in Calculus and Linear Algebra.
- **Reduce Syntax:** Reduce the amount of syntax the user needs to know to use the software.
- **Quick Visualizations:** Make the visualization of concepts quick and easy to manipulate.
- **Ability to Investigate More Complex Situations:** Give the user the ability to investigate more complex calculations and situations.  Being able to do examples and investigations that involve calculations that would be too difficult or time-consuming to do by hand.
- **Easy Integration with Other Software:** Provide tools for exporting data and images from this software to standard document creation systems such as word processors, spreadsheets, and LaTeX editing systems.

As with any software package, this program may or may not fulfill your educational needs. It is my hope that you find this work helpful to you in your study of Calculus and Linear Algebra, and if not, that you find another application or set of applications (preferably freeware or open source) that suit your educational needs.

.. include:: ../LayoutUse.md


:index:`Software`
-----------------

This software package freely available on the web, `Download CLAE <https://github.com/mathprofdes/clae>`_


:index:`Running the Program`
----------------------------

This program can be run from the console of your operating system, through an IDE like PyCharm, or as an executable if you have downloaded a binary version or built your own executable.

:index:`Running From a Console`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

First you need to make sure that Python3 and all the program dependent packages are installed.  There are several ways to get Python up and running on your system, we will discuss the traditional Python installation.  Note that some operating systems will not allow you to install packages system-wide, or at least make it difficult, in this case you should either run the program through PyCharm or create an executable version for your system, both are discussed below.

- Download and install Python3 on your system.
- If pip is not installed with the above installation, install pip. You can check if pip is installed by running the ``pip`` command from your console.
- Install the numpy package with the ``pip install numpy`` command from your console (version 2.3.4 was used during development).
- Install the scipy package with the ``pip install scipy`` command from your console (versions 1.15.2 and 1.16.3 were used during development).
- Install the sympy package with the ``pip install sympy`` command from your console (version 1.14.0 was used during development).
- Install the Colorama package with the ``pip install colorama`` command from your console (version 0.4.6 was used during development).
- Install the OpenGL packages with the ``pip install PyOpenGL`` and ``pip install PyOpenGL_Accelerate`` commands from your console (versions 3.1.9 and 3.1.10 were used during development).
- Install the PySide6 package with the ``pip install pyside6`` command from your console (versions 6.8.3 and 6.10.0 were used during development).
- At this point you should be ready to run CLAE, from your console run the command ``python3 CLAE_App.py`` and the program should start.


:index:`Running through PyCharm`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

PyCharm is a free IDE for developing Python scripts, libraries, and applications.

First you need to make sure that Python3 and all the program dependent packages are installed.  There are several ways to get Python up and running on your system, we will discuss the traditional Python installation.

- Download and install Python3 on your system.
- If pip is not installed with the above installation, install pip. You can check if pip is installed by running the ``pip`` command from your console.
- Download and start PyCharm.
- Create a new project for CLAE, you can use a virtual environment or a system wide application if you would like.
- Copy all of the CLAE source code along with subdirectories into this project.
- PyCharm has a nice and easy interface for installing packages.  As of this writing, there is an icon in the lower left of the IDE for Python Packages, click it and the package manager will appear at the bottom of the IDE.
- Install the numpy package, use the search bar in the package manager to search for numpy. Click on numpy in the found packages, select the version you wish to install and click the install button.  Version 2.3.4 was used during development but later packages should also work, if not, you can uninstall and reinstall a previous package.
- Do the same for the other required packages:
   - Install the scipy package (versions 1.15.2 and 1.16.3 were used during development).
   - Install the sympy package (version 1.14.0 was used during development).
   - Install the Colorama package (version 0.4.6 was used during development).
   - Install the OpenGL and PyOpenGL_Accelerate packages (versions 3.1.9 and 3.1.10 were used during development).
   - Install the PySide6 package (versions 6.8.3 and 6.10.0 were used during development).

- At this point you should be ready to run CLAE, click the start button in the main toolbar at the top right of the IDE.


:index:`Running a Binary`
^^^^^^^^^^^^^^^^^^^^^^^^^

If you downloaded a binary file from the web, it should be a relatively large single file. You should be able to simply double-click this file from your file manager and the program will start.  Your system does not need to have any packages installed and in fact it does not even need to have Python installed, everything is in this single file (which is why it is so large).  You can copy this file to any place on your computer and in fact you can even put it on a thumb drive and run it on any system with the same operating system.  Note that since the file is large there is a lot to load before the program starts, so it may take several seconds for the program to load, especially off a thumb drive.

If you did not download a binary, or if one does not exist, you can run the program using the above methods or create your own executable file.  This is optional and you do not need to know anything about Python programming to do this.  For details, read the next section.

:index:`Building an Executable Version`
---------------------------------------

To build an executable file for your system,

- Download and install Python3 on your system.
- If pip is not installed with the above installation, install pip. You can check if pip is installed by running the ``pip`` command from your console.
- Download and start PyCharm.
- Create a new project for CLAE, use a virtual environment for this. Note that a system wide application will over-install packages.
- Copy all of the CLAE source code along with subdirectories into this project.
- PyCharm has a nice and easy interface for installing packages.  As of this writing, there is an icon in the lower left of the IDE for Python Packages, click it and the package manager will appear at the bottom of the IDE.
- Install the numpy package, use the search bar in the package manager to search for numpy. Click on numpy in the found packages, select the version you wish to install and click the install button.  Version 2.3.4 was used during development but later packages should also work, if not, you can uninstall and reinstall a previous package.
- Do the same for the other required packages:
   - Install the scipy package (versions 1.15.2 and 1.16.3 were used during development).
   - Install the sympy package (version 1.14.0 was used during development).
   - Install the Colorama package (version 0.4.6 was used during development).
   - Install the OpenGL and PyOpenGL_Accelerate packages (versions 3.1.9 and 3.1.10 were used during development).
   - Install the PySide6 package (versions 6.8.3 and 6.10.0 were used during development).
   - Install the pyinstaller package.

- In the lower left of the IDE there is an icon to view the Terminal, click it and you will get a terminal screen at the bottom of the IDE.  Note, do not use the Python Console here, use the Terminal.
- Run the following command in the terminal, ``pyinstaller -F CLAE_App.py``, this will configure the installer and produce several new subdirectories as well as a new file ``CLAE_App.spec``.
- Open the ``CLAE_App.spec`` file in PyCharm.
- Do the following edits to this file, note that these edits are case sensitive:
   - Change the datas line to ``datas=[('icons','icons'), ('fonts','fonts'), ('Help', 'Help')],``
   - Change the console line to ``console=False,``
- Run the following command in the terminal, ``pyinstaller CLAE_App.spec``.
- In the ``dist`` subdirectory that was created by pyinstaller there should be a single file ``CLAE_App`` which is the executable program.


:index:`Development Tools`
--------------------------

This software was developed in Python using the PySide6, numpy, scipy, sympy and pyqtgraph packages.

- **PySide6:** `<https://pypi.org/project/PySide6/>`_
- **numpy:** `<https://numpy.org/>`_
- **scipy:** `<https://scipy.org/>`_
- **sympy:** `<https://www.sympy.org/en/index.html>`_
- **pyqtgraph:** `<https://www.pyqtgraph.org/>`_


This User's Guide was created using the Sphinx documentation package built with the PyData Sphinx Theme.  The mathematical expressions were created with the MathJax extension to Sphinx.

- **Sphinx:** `<https://www.sphinx-doc.org/>`_
- **PyData Sphinx Theme:** `<https://pydata-sphinx-theme.readthedocs.io/en/stable/index.html>`_
- **MathJax:** `<https://www.mathjax.org/>`_


:index:`Copyright`
------------------

| Copyright © 2026 Don Spickler
| This software is distributed under the GNU General Public License version 3.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version. This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details http://www.gnu.org/licenses/.
