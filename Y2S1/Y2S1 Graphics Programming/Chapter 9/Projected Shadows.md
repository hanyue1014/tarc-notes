![[projectedShadow.png]]

- Fast
- Simple
- Only really good for shadow on planes
- Squish actual world geometry down to ground plane, draw it dark

## Advantages
- Easy and fast
	- Just need a projection matrix then can squish geometry to plane already

## Disadvantage
- Difficult to make it work on non-planar surfaces
- Unrealistic shadows

## Problems
- Z-buffer fighting
	- Solution 1: control depth test
		- Draw the ground, disable depth test, draw the decals, draw everything else
	- Solution 2: shift shadow geometry
		- Draw the decals normally, but shift the geometry slightly off ground
- Stencil buffer problem (shadow overflows the ground polygon)
	- Solution: stencil buffer
		- Standard openGL feature
		- Similar to depth test, done on each pixel
		- Test performed on a new fragment against the stencil buffer value, failing fragments are rejected
		- Avoids drawing the same part of the ground twice by first rendering the geometry to the stencil buffer, then draw on where the stencil is set