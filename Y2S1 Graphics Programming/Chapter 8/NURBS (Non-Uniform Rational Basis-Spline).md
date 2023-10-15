- Use a sequence of weights, one for control point which control the impact of individual control points

## Non-Uniform
- Different areas along a NURBS object have different properties that affects how objects are formed
- One control vertex can have more/less control over the object than another

## Rational
- Objects defined by a mathematical formula
	- Derived from the ratio of two polynomials instead of a single summed polynomial

## Basis-Spline
- Chain series of Bézier splines with controllable degree

## Advantages
- Invariant with respect to both affine and perspective transformations
	- Save computational overhead of transforming every point along the curve
- More control over the shape of the curve
	- Ability to change weighting factor of individual control points
- Can be used to correctly draw [[Conic Sections]] (like circles)
	- How??
		- Assume we have 3 points, P0, P1, P2, with P1 as the weighted control point, with a weight factor, w (which means depends on it's width, it have different influences on how the curve is calculated)
		- When w = 0 => a straight line drawn between P0 and P2
		- When 0 < w < 1 or -1 < w < 0 => an elliptical line is drawn
		- When w = 1, a parabola is drawn
		- When w > 1, a hyperbola is drawn
		- ![[conicWithNURBS.png]]
