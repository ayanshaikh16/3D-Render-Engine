**🧊 Java Software 3D Renderer**

A software-based 3D rendering engine built from scratch in Java, without using OpenGL, JavaFX 3D, or external graphics libraries. This project demonstrates the full 3D rendering pipeline implemented manually, including transformations, rasterization, depth buffering, and lighting.


**✨ Features**

3D vertex transformations using custom matrix math

Interactive camera rotation (heading & pitch) via sliders

Triangle rasterization using barycentric coordinates

Z-buffer (depth buffer) for correct hidden-surface removal

Per-face normal calculation

Lambert-style shading based on face orientation

Gamma-corrected color shading

Fully CPU-based rendering (no GPU acceleration)


**🧠 Rendering Pipeline Overview**

This renderer follows a classic graphics pipeline:

Model Definition

Geometry defined as vertices and triangles

Transformations

Rotation via custom 3×3 matrices

User-controlled heading (Y-axis) and pitch (X-axis)

Normal Calculation

Face normals computed using cross products

Normals normalized for lighting calculations

Lighting

Simple diffuse shading using the Z component of the normal

Two-sided lighting (no back-face culling)

Rasterization

Triangles rasterized using barycentric coordinates

Per-pixel depth interpolation

Z-Buffering

Depth testing ensures correct triangle visibility

Final Image Output

Rendered into a BufferedImage

Displayed using Java Swing



**🎮 Controls**

Horizontal Slider – Rotate object around the Y-axis (heading)

Vertical Slider – Rotate object around the X-axis (pitch)

The scene updates in real time as sliders are adjusted.



**🧩 Technologies Used**

Java

Java Swing

BufferedImage

Custom linear algebra (no math libraries)

**📂 Project Structure**
DemoViewer.java


Key components inside the file:

Vertex – 3D point representation

Triangle – Triangle primitive with color

Matrix3 – 3×3 matrix math for transformations

Software rasterizer + z-buffer

Lighting and shading logic



**🚀 How to Run**

Clone the repository:
git clone https://github.com/your-username/your-repo-name.git


Compile and run:
javac DemoViewer.java
java DemoViewer

Use the sliders to rotate the 3D object.


**🧪 Current Scene**

A tetrahedron composed of four colored triangular faces

Faces are shaded based on orientation relative to the camera

Correct depth ordering ensured by z-buffering

