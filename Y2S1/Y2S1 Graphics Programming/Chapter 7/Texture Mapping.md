Topic: [[Y2S1 Graphics Programming]]

## Foreword
- Texture mapping allows attaching images to polygons for more realistic graphics

## What is texture
- Texel == Texture pixel
	- Contains color, alpha information
- A rectangular array of pixel (texel) data
	- 1D array / texture
		- Only width info, the height is strictly 1 pixel
	- [[2D Textures|2D array / texture]]
		- Both width and height info
	- [[3D Textures|3D array / texture]]
		- Width, height and depth info
		- Also called volume texture

## Why Texture Mapping
- Cheaper to use texture mapping instead of a myriads of tiny polygons
- Limitation of Geometric Modelling
	- Although GPU can render over 10 million of polygons in a second, still insufficient for a lot of situations
		- Clouds
		- Skin
		- Grass

## Types of Mapping
- Texture Mapping
	- Use image to fill inside of polygons
	- [[2D Textures]]
- [[Environmental Maps|Environmental Mapping (Reflection Mapping)]]
- [[Bump Mapping]]

## Texture coordinates
- Specify how the texture is mapped onto a geometric object
- `glTexCoord2f(s, t)` where  0 <= s, t <= 1

## Texture wrapping mode
- Clamping is default in OpenGL
- Clamping
	- (s, t) > 1 => use 1
	- (s, t) < 0 => use 0
	- `glTexParameteri(GL_TEXTURE_2D, GL_TEXTURE_WRAP_S, GL_CLAMP)`
- Wrapping
	- (s, t) mod 1
	- `glTexParameteri(GL_TEXTURE_2D, GL_TEXTURE_WRAP_T, GL_REPEAT)`

## Texture sampling
- Major problem in texture mapping, aliasing
- Size of pixel that we try to color on screen may be smaller or larger than 1 texel
- Magnification (polygon > texture)
	- More than 1 pixel can cover a texel
- Minification (texture > polygon)
	- More than 1 texel can cover a pixel
- Solution
	- Point Sampling
		- Use value of the texel that is closest to one computed by the bilinear interpolation
		- Fastest strategy
		- `glTexParameteri(GL_TEXTURE_2D, GL_TEXTURE_MAG_FILTER, GL_NEAREST)`
		- `glTexParameteri(GL_TEXTURE_2D, GL_TEXTURE_MIN_FILTER, GL_NEAREST)`
	- Linear Filtering
		- Use weighted average of group of texels in the neighbourhood of texel determined by point sampling
		- Smoother, less aliased
		- `glTexParameteri(GL_TEXTURE_2D, GL_TEXTURE_MAG_FILTER, GL_LINEAR)`
		- `glTexParameteri(GL_TEXTURE_2D, GL_TEXTURE_MIN_FILTER, GL_LINEAR)`
	- Mipmapping
		- Deal with the minification problem
		- If object small compared to size of texel array, we do not need the original resolution of the original texel array
		- Mipmapped texture consists of a series of texture images, each one half the size of the previous image
		- Mipmap levels do not have to be square, but the halving of the dimensions continue until the last image is texel of 1x1
			- Eg, 8x2 -> 4x1 -> 2x1 -> 2x1
		- Using square set of mipmaps require about one third more memory than not using mipmaps
		- `gluBuild2DMipmaps(...)` build all the texture from given image with GLU mipmap builder
		- `glTexImage2D(...)` declare mipmap level during texture definition
