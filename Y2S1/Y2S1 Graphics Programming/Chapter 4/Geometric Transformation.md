Topic: [[Y2S1 Graphics Programming]]

# Basic Elements in Geometry
- [[Y2S1/Y2S1 Graphics Programming/Chapter 4/Points|Points]]
- [[Scalars]]
- [[Vectors]]
> If we only use vectors to represent coordinate system, there is no way we know where should the points be located

# Affine Spaces
%%let's hope I still rmb and understand this in the future%%
- Use [[Y2S1/Y2S1 Graphics Programming/Chapter 4/Points|Points]] + [[Vectors]] to form a frame, with the point representing origin and vectors representing the axises and their directions, denoted by $(P_0, v_1, v_2, v_3)$ where $P_0$ represents the origin point, $v_1, v_2, v_3$ represents the axises respectively
- In this case, we can say that
- For any point P(x, y, z), the position can be found by $xv_1 + yv_2 + zv_3 + P_0$
- For any vector W(i, j, k), it can be found through $iv_1 + jv_2 + kv_3$

# Homogenous Coordinates Graphics
> TBH I don't really understand this and ma boi lecturer also just touched the surface of this topic very lightly ~~perhaps to cover the fact that he does not understand this as represented in the lecture slides very well~~
> So imma find a resource online and if wanna further read I only read through
> https://www.geeksforgeeks.org/computer-graphics-homogeneous-coordinates/

# Maths behind transformation matrixes
- Don't think will come out in exam since this more like an introduction course and more towards practical side
- + my skill level can't reorganise the words into simpler terms, so if I write when I refer back I will also be confused, might as well just leave a link here
- [How Transformation Matrix Work in OpenGL](https://stackoverflow.com/a/48349423)

## TL;DR
- Translation matrix can be represented by 
	- (3D) $$
		\left[ {\begin{array}{cccc}
			1 & 0 & 0 & x \\
			0 & 1 & 0 & y \\
			0 & 0 & 1 & z \\
			0 & 0 & 0 & 1
		\end{array} } \right]
	$$
	- (2D) $$
	\left[ {\begin{array}{ccc}
		1 & 0 & x \\
		0 & 1 & y \\
		0 & 0 & 1
	\end{array} } \right]
	$$
- Scale about origin matrix can be represented by
	- (3D) $$
	\left[ {\begin{array}{cccc}
		S_x & 0 & 0 & 0 \\
		0 & S_y & 0 & 0 \\
		0 & 0 & S_z & 0 \\
		0 & 0 & 0 & 1
	\end{array} } \right]
	$$
	- (2D) $$
	\left[ {\begin{array}{cccc}
		S_x & 0 & 0 \\
		0 & S_y & 0 \\
		0 & 0 & 1
	\end{array} } \right]
	$$
- Rotation about origin
	- Rotate Z (3D) $$
	\left[ {\begin{array}{cccc}
		\cos\theta & -\sin\theta & 0 & 0 \\
		\sin\theta & \cos\theta & 0 & 0 \\
		0 & 0 & 1 & 0 \\
		0 & 0 & 0 & 1
	\end{array} } \right]
	$$
	- Rotate Z (2D) [I actually dk why diff with 3D one] $$
	\left[ {\begin{array}{cccc}
		\cos\theta & \sin\theta & 0 \\
		-\sin\theta & \cos\theta & 0 \\
		0 & 0 & 1
	\end{array} } \right]
	$$
	- Rotate X (only got effect in 3D) $$
	\left[ {\begin{array}{cccc}
		0 & 0 & 0 & 0 \\
		0 & \cos\theta & -\sin\theta & 0 \\
		0 & \sin\theta & \cos\theta & 0 \\
		0 & 0 & 0 & 1
	\end{array} } \right]
	$$
	- Rotate Y (only got effect in 3D) $$
	\left[ {\begin{array}{cccc}
		\cos\theta & 0 & \sin\theta & 0 \\
		0 & 0 & 0 & 0 \\
		-\sin\theta & 0 & \cos\theta & 0 \\
		0 & 0 & 0 & 1
	\end{array} } \right]
	$$
	- Shear in x (notes only got 2D), where + A will be the new x of the top left corner (I rmb in 3D it should be $\cot\theta$) $$
	\left[ {\begin{array}{ccc}
		1 & A & 0 \\
		0 & 1 & 0 \\
		0 & 0 & 0
	\end{array} } \right]
	$$
	- Shear in x (notes only got 2D), where + B will be the new y of the bottom right corner $$
	\left[ {\begin{array}{ccc}
		1 & 0 & 0 \\
		B & 1 & 0 \\
		0 & 0 & 0
	\end{array} } \right]
	$$
	- Reflection in origin $$
	\left[ {\begin{array}{ccc}
		-1 & 0 & 0 \\
		0 & -1 & 0 \\
		0 & 0 & 0
	\end{array} } \right]
	$$
	- Reflection in about x axis $$
	\left[ {\begin{array}{ccc}
		1 & 0 & 0 \\
		0 & -1 & 0 \\
		0 & 0 & 0
	\end{array} } \right]
	$$
	- Reflection about y axis $$
	\left[ {\begin{array}{ccc}
		-1 & 0 & 0 \\
		0 & 1 & 0 \\
		0 & 0 & 0
	\end{array} } \right]
	$$