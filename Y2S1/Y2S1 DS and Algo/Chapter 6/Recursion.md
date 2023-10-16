Topic: [[Y2S1 DS and Algo]]

- Problem solving process that breaks a problem into identical but smaller problems
- Eventually a smallest problem will be reached where there is a direct solution
	- Where that solution can solve the previous problems
	- Andd the original solution is solved
- Alternative to iteration

## Terminology
- [[Recursion]]
- [[Recursion Definition]]
- [[Stopping Case]]
- [[Recursive Case]]
- [[Recursive Algorithms]]
- [[Recursive Method]]

## Principles
- Must have one or more stopping cases (aboh infinite loop and cause stackoverflow nia lo)

## Tracing Recursion
- [[Box Trace]]

## General Recursive Method Implementation Structures
```
Stop case and recursive case have different actions
if (stop case)
	solve problem
else
	recurse on itself and solve smaller version of problem

Stop case and recursive case have common action or stop case have no action
if (recursive case)
	recurse on self and solve smaller version of problem
```

## Advantages
- Recursive implementation can be significantly simpler and easier to understand than iterative implementation
- Takes advantage of repetitive structure in many problems
	- Can avoid complex case analysis and nested loops

## Tail Recursion
- Last action performed by a [[Recursive Method]] is a recursive call
- This method is usually a straightforward repetition that can be done more efficiently with iteration

## Mutual Recursion
- Indirect recursion
- Method A call method B  -> method B call method A -> ...
- Difficult to understand and trace