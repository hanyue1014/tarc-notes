## Specifying basic materials in OpenGL
- Specify material properties
	- Ambient, diffuse, specular
	- Front/back face
```cpp
glMaterialfv(GLenum face, GLenum type, GLfloat* pointer)
glMaterialf(GLenum face, GLenum type, GLfloat val)
```
## Object Shading
- Flat shaded
	- Simplest way to shade a polygon
	- Use normal associated with first vertex of a simple polygon to perform shading calculation
	- All pixel in the polygon shaded the same
	- Quick
	- Limited realism
	- `glShadeModel(GL_FLAT)`
- Gouraud Shaded
	- Color computed for each vertex via the average normal
	- Color for pixel within the polygon calculated by linear interpolation (of colors, I assume) from the vertices
	- Slower than flat
	- Smooth appearance across polygon
	- `glShadeModel(GL_SMOOTH)`
- Phong Shaded
	- Normals are provided for each vertex of a polygon
	- Normals for pixels within the polygon are calculated by linear interpolation (of normals, I assume) from the vertices
	- Color is computed for each pixel (via the normals, I assume)
	- Much slower
	- Smooth appearance and removes some artifacts