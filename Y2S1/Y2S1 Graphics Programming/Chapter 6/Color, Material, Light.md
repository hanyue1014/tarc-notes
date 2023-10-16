Topic: [[Y2S1 Graphics Programming]]

## Color
- The spectrum of visible light
- White & Black is not color
	- White 
		- An even combination of all the colors at once
		- Reflect all wavelength of colors
	- Black
		- Absence of color
		- Absorbs all wavelength of colors

## Illumination
- When light strikes on something
	- Reflection
	- Absorption
	- Refraction
- What we see
	- The amount of light arriving at our eyes
	- Depends on
		- Light source
		- Surface property of objects

## Lighting
- Importance
	- Make graphic image more realistic
	- Make 3-dimensionality more obvious
- Basic Light
	- [[Ambient Light]]
	- [[Diffuse Light]]
	- [[Specular Light]]
	- The three types of basic light interact with the corresponding material properties
- Lighting in OpenGL
	- Enable lighting
	- Specify light source properties
		- Position
		- Type and Intensity
			- Ambient
			- Diffuse
			- Specular
		- Provide information about surface
			- [[Normal Vectors|Surface normals]]
			- [[Materials Properties and Object Shading|Material properties]]
```cpp
// enable lighting
glEnable(GL_LIGHTING)
// specify light source properties
// light is GL_LIGHX, where X can be from 0 to 8
// pname is the param of the light to adjust, normally is GL_POSITION, GL_AMBIENT, GL_DIFFUSE, GL_SPECULAR
// param is the value to the parameter, normally pointer to the first element of a GLfloat array
glLightfv(GLenum light, GLenum pname, GLfloat* param)
```
