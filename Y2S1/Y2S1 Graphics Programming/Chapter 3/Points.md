Every vertex produces a point
```cpp
glPointSize(size);
glBegin(GL_POINTS);
	glVertex2f(x1, y1);
	glVertex2f(x2, y2);
glEnd();
```