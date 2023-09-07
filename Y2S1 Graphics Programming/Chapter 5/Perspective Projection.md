- Mimics scaling of distance
- If near camera -> bigger
- If far from camera -> smaller
- Models how a camera will take pictures
- Parallel lines will converge at a single point (also called the vanishing point)

## Advantages
- Object further are projected smaller
- Sized objects closer to the viewer 
- Looks realistic

## Disadvantages
- Equal distance along a line are not projected into equal distances
	- Nonuniform foreshortening
- More difficult to construct by hand
```cpp
glFrustum(xmin, xmax, ymin, ymax, znear, zfar); // xmin, ymin marks the bottom left of the front pane, xmax, ymax marks the top right of the front pane, the back pane will scale in ratio with the front pane, znear & zfar must be positive
// or can say as
glFrustum(left, right, bottom, top, near, far);

// another way to set perspective projection
gluPerspective(fovy, aspect, near, far); // fovy is field of view y, it marks the angle of how big the field of view would be, in height
```

- Exam yinggai won't ask, lecturer touch and go nia
$$
\left[{\begin{array}{cccc}
	\frac{2n}{r-l} & 0 & \frac{r+l}{r-l} & 0 \\
	0 & \frac{2n}{t-b} & \frac{t+b}{t-b} & 0 \\
	0 & 0 & \frac{-(f+n)}{f-n} & \frac{-2fn}{f-n} \\
	0 & 0 & -1 & 0
\end{array}}\right]
$$