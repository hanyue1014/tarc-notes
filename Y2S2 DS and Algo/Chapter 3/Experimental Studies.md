## Steps
1. Implement the algorithms
2. Experiment, run the program on various inputs, record the time spent during execution
	- Java: `System.currentTimeMillis()` gives you the current time in millisecond, figure out the rest ;)

## Attention!
- To get the general dependence of running time against the size and structure of input -> run independent experiments on different test inputs with different sizes
- Visualise results -> plot the performance of each run
	- x as input size `n`
	- y as running time `t`
	- This provides intuition regarding relationship between problem size and execution time
- Make statistical analysis to find the best fit function that maps the input size to the experimental data
- To be meaningful, good sample inputs and test enough of them

## Challenges
- Difficult to be **compared directly**
	- Unless experiments performed in same hardware & software environment
- Can only be done on a **limited set of test inputs**
	- Running times of inputs not included in the experiment is left out (those inputs might be important)
 - Algorithm must be **fully implemented** to test
