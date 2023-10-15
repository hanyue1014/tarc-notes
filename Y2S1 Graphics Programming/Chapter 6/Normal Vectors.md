## Angle of Incidence (AoI)
- Angle at which the rays of light hit the surface
- Affects the brightness of the surface
- Can be calculated after we know the direction that each surface is facing
	- The direction is called normal of the surface

## Normal Vectors
- Unit vectors perpendicular to a surface
- Vector that points in the direction perpendicular to the tangent of a surface
- Two cases
	- Planar surface
		- Normal at different points of the surface are identical
	- Curved surface
		- Different points may have different normal
- For polygonal mesh, normal vectors are often associated with vertices, not polygon faces
	- Two types
		- Flat object: normal vectors identical
		- Smooth object: normal vectors can be different
```cpp
// use either one of these, need repeat for every vertices
glNormal3f(nx, ny, nx)
glNormal3fv(pointer_to_normal)
```