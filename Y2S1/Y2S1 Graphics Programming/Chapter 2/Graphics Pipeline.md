Topic: [[Y2S1 Graphics Programming]]

# 3D Graphics
- 3D == 3 Dimensional
	- Got **width, height, depth**
- Representing 3D in computer graphics
	- Actually 2D images on a flat computer screen (ofc loll) that provides the illusion of depth
 - [[Projection]]
	- [[Isometric Projection]]

# Graphics Pipeline
1. [[Vertex Processor]]
2. [[Clipper And Primitive Assembler]]
3. [[Rasterization]]
4. [[Fragment Processor]]
```
(Input: Vertices) -> Vertex Processor -> Primitive Assembler -> Rasterization -> Fragment Processor -> (Output: Pixels)
```

# Programmable Graphics Pipeline
- Not rlly a focus in this course
- Why important -> more details can be rendered
- Programmable vertex processor
	- Hardware unit to run computer graphic vertex programs
- Programmable fragment processor
	- Unit that runs computer graphic fragment programs
%%After reading above 2 sentence I be like ***HUH***%%