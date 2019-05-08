---
layout: post
title: PCA step by step in Python
---

Step 1. Generating 3-dimensional sample data
400 3-Dimensional samples stem from two different classes, where one half (i.e., 200) samples of our data set are labeled ω1 (class 1) and the other half ω2 (class 2).

import numpy as np

np.random.seed(0)

mu_vec1 = np.array([-6,6,6]) #mean m1
cov_mat1 = np.array([[0.3,1.0,1.0],[1.0,9.0,1.0],[1.0,1.0,9.0]]) #covariance matrix
class1_sample = np.random.multivariate_normal(mu_vec1, cov_mat1, 200).T
assert class1_sample.shape == (3,200)

mu_vec2 = np.array([6,6,6]) #mean m2
cov_mat2 = np.array([[0.3,1.0,1.0],[1.0,9.0,1.0],[1.0,1.0,9.0]]) #covariance matrix
class2_sample = np.random.multivariate_normal(mu_vec2, cov_mat2, 200).T
assert class2_sample.shape == (3,200)
