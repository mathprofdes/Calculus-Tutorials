:index:`Introduction`
=====================

To the Reader
-------------

Welcome, whether you are using these tutorials as part of a course or just using them on your own to learn Calculus, I hope you find them beneficial.

About these Tutorials
^^^^^^^^^^^^^^^^^^^^^

This set of tutorials and examples was developed as a supplement to a STEM college-level sequence in Calculus to use computer algebra system and graphing technology to visualize and explore concepts in these courses.  Although these tutorials are geared toward a STEM Calculus sequence they are certainly useful for a course or sequence in applied calculus, the instructor and student will simply need to pick and choose the sections they utilize.  The tutorials were not designed to accompany any particular textbook but be general enough to use with a multitude of texts.  With that said, I would highly recommend Calculus Volume 1, 2, and 3 by Gilbert Strang and Edwin "Jed" Herman from OpenStax, https://openstax.org.  This is an excellent series of books for a STEM college-level sequence in Calculus and has inspired much of the content and organization of this set of tutorials. Even if you are taking a course at a university and have a course text these textbooks are a great supplementary reference.

- There are many different styles of Calculus textbooks on the market, the layout of these tutorials is fairly traditional and loosely follow the style of Anton, Stewart, Thomas, and Strang, as well as a host of others too numerous to list.  Even if you are not using a traditional style textbook you can still use these tutorials, you just may need to jump around the sections a little more.

- These tutorials focus on the use of technology to help with the calculations and visualizations of the topics in Calculus.  The tutorials do discuss the mathematics of the topic but were written more as a summary of the mathematics.  For a detailed discussion of these topics and proofs of the results you should consult your textbook.

- These tutorials utilize three open-source software packages, GeoGebra, Maxima, and CLAE (Calculus and Linear Algebra Explorer), the links to download these packages are below. Not all topics use each of these packages, but they use at least one of them. There are quick start guides for GeoGebra and Maxima in these tutorials as well as the entire help system for CLAE.  More information on GeoGebra and Maxima can be found easily online, both have extensive communities of educators using these packages.

- The tutorials themselves are distributed as a self-contained website that can be run from any web server and locally on your personal computer even without an internet connection.  Simply open the main page in your favorite browser.

- The images in these tutorials were mostly created by me with the software packages being utilized.  Those that were not created by me were taken primarily from the open-source textbooks by by Gilbert Strang and Edwin "Jed" Herman and a few were taken from the internet that appeared to be public domain.

- The goals of these tutorials are:
    - Provide a technology guide for the user to better understand Calculus concepts.
    - Give the user step-by-step instructions on how to use the software packages to lessen the learning curve and provide an example-oriented approach instead of a general functional approach.
    - Give the user enough foundational skills with the technology so that they can use it for more advanced investigations and projects.

Tutorial Organization
^^^^^^^^^^^^^^^^^^^^^

These tutorials are organized into three main parts, Differential Calculus, Integral Calculus, and Multivariable Calculus, which roughly corresponds to a Calculus I, II, and III sequence at most institutions.  This makes it easier to compartmentalize the topics and navigate the site. Each part is divided into specific topics that can be selected in the left hand window.  Once a topic is selected the tutorial will be in the center window and a page navigation for that topic is displayed on the right.

.. container:: sphinx-features-three

   .. admonition:: :doc:`/DiffCalc/index`
      :class: sphinx-feature-three

      In these tutorials and examples you will concentrate on the Tangent Problem.  Specifically you will be investigating limits, continuity, derivatives, and their applications.

   .. admonition:: :doc:`/IntCalc/index`
      :class: sphinx-feature-three

      In these tutorials and examples you will concentrate on the Area Problem.  Specifically you will be investigating integration, techniques of integration,  applications of the integral, infinite sequences and series, power series; Taylor and Maclaurin series, parametric curves, and polar coordinates.

   .. admonition:: :doc:`/MultCalc/index`
      :class: sphinx-feature-three

      In these tutorials and examples you will take the Tangent Problem and the Area Problem to a higher dimension.  Specifically you will be investigating calculus applied to functions of several variables.  Topics here include vectors and vector valued functions, multivariable functions and partial derivatives, multiple integrals, and concepts from vector calculus.


How to Use these Tutorials
^^^^^^^^^^^^^^^^^^^^^^^^^^

Here is my suggestion on how you use these tutorials.  First read your textbook on the topic, work through the textbook examples and try some of the exercises.  Then go into these tutorials and select the topic you are working on, read through the discussions, and then work through the examples using the technology you have chosen.  Then go back to the exercises in your text and use the technology to help visualize the conditions of the exercise and possibly help with the calculations of the more difficult exercises.  In addition, if your textbook does not give you graphs of the functions in an example, use the technology to do so.  It may make the example clearer.


Software
--------

These tutorials were designed to use computer algebra system and graphing technology to help explore the concepts in Calculus.  There are many such systems that are available either online or for download and local installation.  We will using three that are all cross-platform, open-source, and freely available on the web, GeoGebra, Maxima (specifically wxMaxima), and CLAE (Calculus and Linear Algebra Explorer).  It is not assumed that the user is using all three of these, just one or more.  The examples in the tutorials have subsections on how to use each one (or a combination) for that example. Not all examples will use each of these packages, in some applications one or more may prove to be too cumbersome, and hence omitted.

No single software package is perfect, if there was we would use it.  A software package is simply a tool.  Every tool has a set of things it is useful for and a set of things it is not useful for.  A hammer is very good at driving nails but not so great at cutting a piece of wood.  The same is true for software packages.  We selected GeoGebra, Maxima, and CLAE since they were all cross-platform, open-source (hence free), and they complement each other in facilities, ease of use, and strengths.  It is simply like having a toolbox of different tools.

These tutorials will take the user step-by-step through the calculation and visualization commands and options in the software packages but they do not discuss the general features of the software.  There are some quick user's guides included in these tutorials to get you started.  Both GeoGebra and wxMaxima have a long development history and there are numerous resources on the web on their commands and general use.  CLAE is a new package that has a fairly extensive help system that discusses the features of the software.

.. container:: sphinx-features-three

    .. admonition:: `Download GeoGebra or use Online <http://geogebra.org/>`_
        :class: sphinx-feature-three

        GeoGebra is a dynamic mathematics software for all levels of education that brings together geometry, algebra, spreadsheets, graphing, statistics and calculus in one engine. In addition, GeoGebra offers an online platform with over 1 million free classroom resources created by our multilingual community. These resources can be easily shared through our collaboration platform GeoGebra Classroom where student progress can be monitored in real time.

    .. admonition:: `Download wxMaxima <https://wxmaxima-developers.github.io/wxmaxima/download.html>`_
        :class: sphinx-feature-three

        wxMaxima is a document based interface for the computer algebra system Maxima. wxMaxima provides menus and dialogs for many common maxima commands, autocompletion, inline plots and simple animations. wxMaxima is distributed under the GPL license.

    .. admonition:: `Download CLAE <https://github.com/mathprofdes/clae>`_
        :class: sphinx-feature-three

        CLAE (Calculus and Linear Algebra Explorer) was developed for quick calculations and explorations in an introductory STEM mathematics classes, primarily single variable and multi-variable Calculus and Linear Algebra.  It combines the SymPy computer algebra system with the PyQtGraph two and three dimensional graphics interfaces in a primarily menu-driven user interface.  It keeps the syntax to a minimum in hopes of making the learning curve as shallow as possible while maintaining the power of more general computer algebra systems.

:index:`Calculus`
-----------------

In a nutshell, Calculus is the study and quantifying of change.  If we have two quantities that are related in a way such that the change in one creates a change in the other, there are two main questions we can ask.  The first question is, what is the rate at which the dependent quantity changes as we change the independent quantity?  The second question is, what is the total change of the dependent quantity as we change the independent quantity over some interval of values?

We tend to interpret this study and quantifying of change into two graphically oriented interpretations, the Tangent Problem and the Area Problem.  The Tangent Problem answers the first question, "What is the rate at which the dependent quantity changes as we change the independent quantity?" which is at the heart of Differential Calculus.  The Area Problem answers the second question, "What is the total change of the dependent quantity as we change the independent quantity over some interval of values?" which is at the heart of Integral Calculus.

.. include:: TP.md

.. include:: AP.md


Development Tools
-----------------

This tutorial set was created using the Sphinx documentation package built with the PyData Sphinx Theme.  The mathematical expressions were created with the MathJax extension to Sphinx.  MathJax is included in the distribution of this tutorial so that the tutorials can be viewed completely off-line.  In addition, the entire website can be run on any web server, there is no need for any server-side functionality.

- **Sphinx:** `<https://www.sphinx-doc.org/>`_
- **PyData Sphinx Theme:** `<https://pydata-sphinx-theme.readthedocs.io/en/stable/index.html>`_
- **MathJax:** `<https://www.mathjax.org/>`_


Copyright
---------

| Copyright © 2026 Don Spickler
| Licensed to the public under Creative Commons
| Attribution-NonCommercial 4.0 International License

.. image:: Images/CCL_Large.png
