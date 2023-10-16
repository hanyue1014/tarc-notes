- Encloses an area and is filled by default
- Polygons have front & back face
- By default OpenGL sets polygon's front face anti clockwise
```cpp
GL_POLYGON
```

## Polygon Restrictions
- Must be ***SIMPLE***
- Must be ***CONVEX (Internal angle < $180^{\circ}$)***
- Why restriction
	- Non-convex & non-simple polygons are expensive to render
		- Becuz convexity and simplicity is expensive to test

## Tessellation (In this course)
- Subdividing concave polygons or polygons with intersecting edges into multiple convex polygons