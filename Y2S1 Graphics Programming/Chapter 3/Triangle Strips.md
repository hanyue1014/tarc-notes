- Series of triangles that share sides
- Space & Time effiecient
- Form a side with the previous vertex and another side with the second previous vertex
```cpp
glBegin(GL_TRIANGLE_STRIP);
	glVertex2f(x1, y1); // v1
	glVertex2f(x1, y1); // v2
	glVertex2f(x1, y1); // v3
	glVertex2f(x1, y1); // v4
	glVertex2f(x1, y1); // v5
glEnd();
```
- Take the above example (Plot out for maximum understandability)
	- v2 will connect with v1, but not enuf to form a triangle yet
	- v3 will connect with v2 and v1 to form a triangle
	- v4 will connect with v3 and v2 to form another triangle
	- v5 will connect with v4 and v3 to form the final triangle