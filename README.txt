Cpp-Gtk3-GL33-Scene02

   +-------------------------------------------------------+
   |   Dieses Programm wird für den Rechner  Jetson Nano   |
   |   bereitgestellt. Die Verwendung des Programms auf    |
   |   ähnlichen Rechnern könnte möglich sein, falls die   |
   |   im Makefile genannten Programmbibliotheken          |
   |   vorhanden sind.                                     |
   +-------------------------------------------------------+

Hilfmittel:  Gtk-3, GLM, OpenGL 3.3 Core Profil, Widget GtkGLArea.

Erforderliche Pakete:

   sudo apt-get install libglm-dev libglm-doc
   sudo apt-get install libgtkmm-3.0-dev 


Dieses in C++ geschriebene Programm verwendet OpenGL 3.3 Core Profile
mit Gtk3. Für die Berechung der Projektionsmatrix werden Hilfsmittel
aus GLM verwendet.

Die Shader werden aus Dateien gelesen, die im Verzeichnis ./res
bereitgestellt werden. Die Versorgung des Shaderprogramms ist ebenfalls
in einem separaten Modul implementiert.

Die Vertex Buffer Objects des Szeneobjekts werden in einem
Vertex Array Object zusammengefasst.  (VAOs stehen ab OpenGL 3.0
zur Verfügung.)

Die unveränderlich bleibenden Geometriedaten des Szeneobjekts
(Gitter und Texturkoordinaten) werden nur einmal berechnet.
Die veränderlichen Geometriedaten (Verticees, Vertexnormalen)
werden immer dann neu berechnet, wenn sich der Animationsparameter
geändert hat.
=======================================================================

Compilierung:

   make

Programmausführung:

    ./demo

2016-04-04, 2020-09-14, 2022-04-24
