# Extreme-Scale-course
This repository is for the PHY905(sec004) Spring 2016, Designing and building applications for Extreme-Scale System

#Notes for the lectures videos 

##Meeting 01/19/2016

###Discussions at the end of 2nd leture：

1. Why do you think the algorithm runs slowly at large sizes?
  - [my answer]I'm thinking about the read and write process. Maybe for small sizes, the memory of cache in the cpu is large enough for the work, so there's no need to go through the read and write the memory. While in the large case, the **r** and **w** are costing more and more time.
  - Caches faster than RAM, and the hard drive is the slowest. but the space in cache is limited.
  - For matrix, the computer will load a row at once, so the order of do loop is crucial to the reading and writing process of large matrix.
1. Why do you think the compiler doesn't do a better job?
	- [my answer]I do not know much about the compiler, but my guess is that if compiler does a better job, the running time should be pretty scaleable.
	- There are different options of optimizaiton for every compiler. **HPCC** recommands `-O3`, since it's the best stable optimization for most compliers.
1. What about other algorithms such as Strassen's Algorithm, and how would that algorithm change this analysis?
	- [Strassen Algorithm] (https://en.wikipedia.org/wiki/Strassen_algorithm)
		- reduce the number of operations


###Discussions at the end of 3rd leture：
1. True of False:
	- There are computers using more than one million cores today
		- TRUE: Tianhe2, over 3 million cores
	- THe Top500 benchmark predicts the performance of many applications
		- FALSE: only matrix-matrix multiply
1. What are 3 important benchmarks? What do they measure?
	- Top500: HP Linpack, solving linear equations
	- STREAM: Measure "Sustainable Memory Bandwidth"
	- RandomAccess
1. Do all benchmarks specify the specific code that must be run?
	-	RandomAccess do not have a specific code.

###Discussions in 4th lecture:
- For the tables at the beginning, what might be problem? [Hint: it's about measuring performance]
- Assume that the sustainable memory bandwidth is 12 Gbytes/second. For a DAXPY operation, what is the maximum possible performance, using the same analysis as we used for the Sparse matrix-vector multiply. 
	- DAXPY
	- Do i=1,n; y(i) = alpha * x(i) + y(i); enddo
	- What is the ratio of the performance for DAXPY and the peak performance for the processor?

###Discussions in 5th lecture:


###Questions in HW2
- [Task#2] As mentioned in the forum, the cache now is shared by multi cores, I'm not sure how much is used for the one I was running. Maybe I can find an answer from HPCC.

###About Vectorization
- Find out how to request the compiler to do the vectorization, if it's not by default
	- Do we need to tell the compiler about the stucture of the cpu so that it can vectorize the code more properly?
