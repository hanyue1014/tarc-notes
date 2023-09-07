-  Objects are not scaled with distance
- They appear as the same size regardless of how far or near they are from the camera
- Projects perpendicular to projection plane
- Viewing volume is rectangular parallelepiped
- Multiview
	- Usually form front, top, side views

## Advantage
	- Preserve both distances and angles
	- Shapes preserved
	- Can be used for measurement
		- Building plan
		- Manuals

## Disadvantage
	- Cannot see what object really looks like (many surfaces hidden from view)
	- We often add isometric
	- Does not provide "realistic" view or sense of 3D form

## Projection Matrix
- TBH yinggai wont come out in exam, lecturer also just touch n go nia
- All $x_e, y_e, z_e$ components are linearly mapped to NDC
- Scale rectangular volume to a cube -> move to origin -> use linear relationship
$$
\left[{ \begin{array}{cccc} 
	\frac{2}{(r-l)} & 0 & 0 & -\frac{r+l}{r-l} \\
	0 & \frac{2}{t-b} & 0 & -\frac{t+b}{t-b} \\
	0 & 0 & \frac{-2}{f-n} & -\frac{f+n}{f-n} \\
	0 & 0 & 0 & 1
\end{array}} \right]
$$
- Maybe will out eh is this nia
```cpp
glOrtho(left, right, bottom, top, near, far);
```
