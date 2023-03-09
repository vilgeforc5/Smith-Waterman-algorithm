# Smith-Waterman-algorithm
Python implementation of Smith–Waterman algorithm  

Used to determine the set of regions between two strings of nucleic acid sequences or sequences by comparing segments of all possible lCancel changesengths and optimize the measure of similarity.

Composition of three parts:

1) Determination of the substitution matrix (estimates, weights - other variants of the name) and the penalty scheme for the gap. The substitution matrix assigns each pair a positivity or non-match. Typically, matches are rated high, and inconsistencies are rated low. The gap penalty function determines the cost of points for opening or expanding a gap. It is proposed that the scoring system is chosen depending on the purpose of the study.
(this is the matrix function in the algorithm).


2) Score each element from left to right, top in the matrix, considering the results of substitutions (diagonal scores, this is done recursively in the down algorithm) or gap additions (horizontal and vertical scores). If none of the ratings is positive, this element is assigned 0.

(this is the back_func function in the algorithm)

3) Reverse move. In this process, segments are generated that cover the statistics of the collectors.
(this is included in back_func)

In the code, the alg function ties all these three dots together so they work together.
