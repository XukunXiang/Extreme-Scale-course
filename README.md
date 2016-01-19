# Extreme-Scale-course
This repository is for the PHY905(sec004) Spring 2016, Designing and building applications for Extreme-Scale System

#Notes for the lectures videos

###Discussions at the end of 2nd leture：

1. Why do you think the algorithm runs slowly at large sizes?
  - I'm thinking about the read and write process. Maybe for small sizes, the memory of cache in the cpu is large enough for the work, so there's no need to go through the read and write the memory. While in the large case, the **r** and **w** are costing more and more time.
1. Why do you think the compiler doesn't do a better job?
	- I do not know much about the compiler, but my guess is that if compiler does a better job, the running time should be pretty scaleable.
1. What about other algorithms such as Strassen's Algorithm, and how would that algorithm change this analysis?
	- [Strassen Algorithm] (https://en.wikipedia.org/wiki/Strassen_algorithm)
		- reduce the number of operations
