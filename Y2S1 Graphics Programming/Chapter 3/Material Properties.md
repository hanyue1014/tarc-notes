Topic: [[Y2S1 Graphics Programming]]
> Any properties that determines how a geometric primitive is rendered
> Eg. Colour, Shading properties, transparency

# Colour
```cpp
glColor3f(r, g, b); // r, g, b goes from 0 -> 1
```

# Shading
- Flat shading
	- Objects always drawn with one colour, no matter how many colour assigned to the different vertices, the primitive will always be drawn with the last colour assigned to the vertex
	- `glShadeModel(GL_FLAT)`
- Smooth Shading
	- Objects are drawn with many different colours
	- `glShadeModel(GL_SMOOTH)`

# Stippling
- Add a pattern to a simple line or a filling polygon
- Uses bit patterns

## Line Stippling
- Pattern is 16 bit
```cpp
glEnable(GL_LINE_STIPPLE);
glLineStipple(1 /* bit multiplier */, 0x7733 /* pattern */);
```
- The above code will draw out a line as follows
```
0x7733 = 0b0111 0111 0011 0011 (hex to bin)
Look from back to front, 1 = draw, 0 = don't draw
so
1100 1100 1110 1110
--  --  --- --- 
is the final result

In the case of bit multiplier = 2, then multiply every bit by 2
1100 1100 1110 1110 = 11 11 00 00 11 11 00 00 11 11 11 00 11 11 11 00
Then draw
11 11 00 00 11 11 00 00 11 11 11 00 11 11 11 00
----    ----    ------  ------  
is the final result, same applies to 3, 4 and so on

PS: the line drawn is for ONE SEGMENT, if there are multiple segments, repeat the pattern
```

## Polygon Stippling
- [Very Good Example](https://stackoverflow.com/a/2316144)
- Pattern is byte array with length 128 `GLubytemask pattern[128]`
```cpp
0xff, 0x01, 0x00, 0x01,  // #########               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0x00, 0x01, 0x00, 0x01,  //         #               #       
0xff, 0x01, 0xff, 0x01,  // #########       #########       
0x00, 0x01, 0x01, 0x01,  //         #       #       #       
0x00, 0x01, 0x01, 0x01,  //         #       #       #       
0x00, 0x01, 0x01, 0x01,  //         #       #       #       
0x00, 0x01, 0x01, 0x01,  //         #       #       #       
0x00, 0x01, 0x01, 0x01,  //         #       #       #       
0x00, 0x01, 0x01, 0x01,  //         #       #       #       
0x00, 0x01, 0x01, 0x01,  //         #       #       #       
0x00, 0x01, 0x01, 0x01,  //         #       #       #       
0x00, 0x01, 0x01, 0x01,  //         #       #       #       
0x00, 0x01, 0x01, 0x01,  //         #       #       #       
0x00, 0x01, 0x01, 0x01,  //         #       #       #       
0xff, 0x00, 0xFF, 0x01,  // ########         ########       
0x00, 0x00, 0x00, 0x00,  //
0x00, 0x00, 0x00, 0x00,  //
0x00, 0x00, 0x00, 0x00   //
```
- Pattern is repeated for every 32x32 pixels drawn
- Pattern also is seen from back to front
```cpp
glEnable(GL_POLYGON_STIPPLE);
glPolygonStipple(128ByteArray);
```
