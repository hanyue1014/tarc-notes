Topic: [[Y2S1 Graphics Programming]]

# Transformation Pipeline
![[transformationPipeline.png]]

# Understanding Transformations
- Viewing
	- Position view volume in the world (set where can camera see I guess)
- Modeling
	- Position the models in the world (put the primitives in)
- Projection
	- Determine shape of viewing volume
	- [[Perspective Projection]]
	- [[Orthographic Projection]]

# OpenGL Camera
- Object and camera frames are same 
- Initially, camera is
	- At origin
	- Points in negative z direction
	- Specifies default view volume (a cube with sides of length 2, center = origin)
	- Default projection matrix is an identity
	- Default projection is Orthogonal ([[Orthographic Projection]])

## Moving Camera
- Translate camera frame
- Move all objects in the world (Translate World Frame, both also translates world frame)
```cpp
glTranslatef(...);
gluLookAt(eyeX, eyeY, eyeZ, lookX, lookY, lookZ, upX, upY, upZ); // eye{X, Y, Z} is where the camera position should be, look{X, Y, Z} is the coordinate that should be in the center of the camera, up{X, Y, Z} should actually always be 0, 1, 0 cuz we want the camera to stay upright up{X, Y, Z} is the vector pointing upwards the camera should follow
// useful reference: https://stackoverflow.com/a/7746682
```

# Projection
- Reduces dimension by one (3D -> 2D)
- Required becuz computer only can show 2D screen, must convert project 3D into 2D
- Two common projection types:
	- [[Orthographic Projection]]
	- [[Perspective Projection]]
- `GL_PROJECTION` matrix
	- Used to convert 3D to 2D
	- Used to convert eye coordinates to clip coordinates
- Clip coordinates are then transformed into Normalized Device Coordinates (NDC) by dividing w component of the clip coordinates
