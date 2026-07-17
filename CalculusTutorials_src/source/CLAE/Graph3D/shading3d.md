
Surface shading simply refers to how colors are being used to display the surface.  It is this color manipulation that gives the image a three-dimensional feel even though it is being viewed on a two-dimensional surface.  For different applications you may want to change the shading mode to better see the mathematical aspects of the surface. This program offers seven different shading modes or algorithms.

Shade by Camera Position
""""""""""""""""""""""""

This mode shades the surface according to the position of the camera and the curve of the surface.  The surface base color is the one selected.  The surface is rendered with a non-shiny finish and two simulated light sources, a simplified Phong shading model. For example, 

.. figure:: Images/ShadeCamera.png
    :alt: Shade by Camera Position

    Shade by Camera Position


Shade by Surface Height
"""""""""""""""""""""""

This mode shades the surface according to the height (z-value) of the surface.  In this mode the base color is not used.  The colors used are the standard rainbow ROYGBIV from top to bottom.  So the red portions are at the top and the violet portions are at the bottom.  For example, 

.. figure:: Images/ShadeSurfaceHeight.png
    :alt: Shade by Surface Height

    Shade by Surface Height

This mode would be useful if you wanted to produce a color contour map of the surface.  For example, 

.. figure:: Images/ViewOpts008.png
    :alt: Shade by Surface Height for a Color Contour Map

    Shade by Surface Height for a Color Contour Map

Shade by Camera and Surface Height
""""""""""""""""""""""""""""""""""

This mode combines the surface height algorithm with the camera position algorithm.  In this mode the base color is not used.  The colors used are the standard rainbow ROYGBIV from top to bottom and then these colors are changed in intensity to simulate two additional light sources.  For example, 

.. figure:: Images/ShadeSurfaceHeightCamera.png
    :alt: Shade by Camera and Surface Height

    Shade by Camera and Surface Height

Shade by View Height
""""""""""""""""""""

This mode shades the surface according to the height (z-value) of the surface within the viewing cube.  In this mode the base color is not used.  The colors used are the standard rainbow ROYGBIV from top to bottom but instead of this color map being applied to the minimum and maximum z-values of the surface the map is applied to the minimum and maximum z-values of the viewing cube.  For example, 

.. figure:: Images/ShadeViewHeight.png
    :alt: Shade by View Height

    Shade by View Height

Note that in this mode if we translate the image vertically the surface is at a different part of the color map and hence is shaded differently.  In surface height mode this would not happen. 

.. figure:: Images/ShadeViewHeight2.png
    :alt: Shade by View Height Translated

    Shade by View Height Translated

.. figure:: Images/ShadeViewHeight3.png
    :alt: Shade by View Height Translated

    Shade by View Height Translated

This mode would be useful if there are several surfaces using this mode in the view, then the colors can be used to compare the heights between the surfaces. 

Shade by Camera and View Height
"""""""""""""""""""""""""""""""

This mode combines the view height algorithm with the camera position algorithm.  In this mode the base color is not used.  The colors used are the standard rainbow ROYGBIV from top to bottom of the view and then these colors are changed in intensity to simulate two additional light sources.  For example, 

.. figure:: Images/ShadeViewHeightCamera.png
    :alt: Shade by Camera and View Height

    Shade by Camera and View Height

Shade by Surface Normals
""""""""""""""""""""""""

This mode shades the surface by the surface normals, vectors that are perpendicular to the surface.   In this mode the base color is not used. 

.. figure:: Images/ShadeNormals.png
    :alt: Shade by Surface Normals

    Shade by Surface Normals

This mode is useful to view aspects of surface curvature using the color changes.  It is also useful when plotting the planes defined by a linear system, it tends to make the planes easier to distinguish even when the planes are close to each other.

Shade by Camera and Normals
"""""""""""""""""""""""""""

This mode combines the surface normal algorithm with the camera position algorithm.   In this mode the base color is not used. The colors are first determined by the surface normal algorithm and then changed in intensity to simulate two additional light sources.  For example,

.. figure:: Images/ShadeNormalsCamera.png
    :alt: Shade by Camera and Normals

    Shade by Camera and Normals

