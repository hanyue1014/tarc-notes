- Series of triangles that form around a center point (like a pizza)
- Efficient in space & time
```cpp
glBegin(GL_TRIANGLE_FAN);
	glVertex2f(x1, y1); // v1
	glVertex2f(x1, y1); // v2
	glVertex2f(x1, y1); // v3
	glVertex2f(x1, y1); // v4
	glVertex2f(x1, y1); // v5
glEnd();
```
- Take the above example (Plot out for maximum understandability)
	- v1 will be the center point
	- v2, v3, v4, v5 will connect to the center point, each forming triangles
	- v2 and v3 form a line with each other, so v1, v2, v3 is a triangle
	- v3 and v4 will form a line with each other, so v1, v3, v4 is also a triangle
	- v4 and v5 will form a line with each other, so v1, v4, v5 is also a triangle