Every **pair** of vertices produce a line
```cpp
glLineWidth(size);
glBegin(GL_LINES);
	glVertex2f(x1, y1);
	glVertext2f(x2, y2);
glEnd();
```