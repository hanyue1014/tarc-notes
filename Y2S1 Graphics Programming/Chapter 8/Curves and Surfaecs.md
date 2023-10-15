Topic: [[Y2S1 Graphics Programming]]

## Splines
- Used in graphics to represent smooth curves and surfaces
- Use small set of control points (knots) and a function that generates a curve through those points
- Allow creation of complex smooth shapes without needing to manipulate many short line segments or polygons at a cost of a little extra computation time

### Why Splines
- Have more compact representation than a set of polygons
- Provide scalable geometric primitives
- Provide smoother and more continuous primitives than straight lines and planar polygons
- Simpler, faster, more accurate animation and collision detection
- Save memory for model storage, increase memory cache efficiency

## Types of Curves and Surfaces
- [[Explicit]]
- [[Implicit]]
- [[Parametric]]


## Continuity
- Continuity of a curve at a breakpoint describes how the curves meet at the break point
- No continuity
	- Curves do not meet at all
- C0 continuity
	- Endpoints of two curves meet with positional continuity only
	- May be a sharp point at where they meet
- C1 continuity
	- Curves have identical tangents at the break point
	- Curve join smoothly
	- Also have positional continuity
- C2 continuity
	- Curves have identical curvature at the breakpoint
	- Curvature continuity implies both tangential and positional continuity
