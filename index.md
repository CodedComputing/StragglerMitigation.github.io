---
layout: default
title: About
permalink: /index.html
---

# Large-scale Coded Computing


Coded distributed matrix multiplication for straggler mitigation has received a lot of attention recently.
In coded distributed matrix multiplication, a master node wishes to compute the matrix product $$A^TB$$ with the help of several worker nodes. (As shown in the figure)
The main idea is to partition $$\mb{A}$$ and $$\mb{B}$$ into several smaller submatrices, encode the submatrices using a carefully constructed code into a redundant set of submatrices, and transmit the encoded submatrices to different worker nodes. 
The worker nodes compute the smaller matrix products and return their computation to the master node which combines the results from each worker node to produce the final result.
The code is designed such that the final result can be recovered from a subset of the submatrix products, i.e., the system is resilient to straggling workers which do not return their computation in time.


![Unsourced MAC](assets/CodedC.jpeg)

Robust algorithms for such kind of large-scale distributed matrix multiplication need to address several important factors including 

(i) resilience to straggling workers, typically measured using a recovery threshold, which is the minimum number of workers that need to return their computation; 

(ii) communication cost - the amount of information that needs to be communicated to the worker nodes; 

(iii) scalability - the numerical accuracy and implementation complexity of the distributed algorithms.