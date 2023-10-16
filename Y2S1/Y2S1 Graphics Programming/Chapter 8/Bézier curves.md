- Defined as a function of a set of control points and basis functions
- Suggested using the same 4 data points with the cubic interpolating curve to approximate the derivatives
- de Casteljau algorithm
	- Recursive method to evaluate polynomials
- Widely used in CAD

## General Formula
- t is the fraction (or progress) of traversing from one point to another (eg P0 -> P1)
![[bezierCurve1.png]]
![[bezierCurve2.png]]

## de Casteljau Algorithm
- My understanding
- Instead of making all in one line like the general formula, use a recursive way to calculate the concerned points first

### Degree 1 (n = 2)
- Line segment
- Defined by 2 points
![[animationLinearBezierCurve.gif]]

### Degree 2 (n = 3)
- Quadratic
- Defined by 3 points
![[animationQuadraticBezierCurve.gif]]

### Degree 3 (n = 4)
- Cubic
- Defined by 4 points
![[animationCubicBezierCurve.gif]]

### Degree 4 (n = 5)
![[animationQuarticBezierCurve.gif]]

### Degree n
```
while (n > 0) {
	for (i = 0 to n-1)
		Pi = ((1 - t) * Pi + t) + (t * P(i+1))
	n--
}
return P0
```

## Limitations
- No local control
	- Changes to any control points will change every point along the curve
- Limited amount of flexibility
