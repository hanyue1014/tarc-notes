- Perturb the normal vector without having to make any changes to the shape
- Like can show depth in the 3D model (some place appears to be dented, some appears to be raised)

## Height Map
- Texture storing the surface height information
- Normal vectors at each pixel is calculated via the height map

## Normal Map
- Texture storing normal information
- Use normal from normal map instead of interpolated vertex normals to compute light color

## How it works
- Perturb the normal vectors before shading calculation
- Fake small displacements above or below the real surface
- Surface don't really change, but the shading makes it look like it