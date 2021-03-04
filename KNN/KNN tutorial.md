## 1. Algorithm
### 1.1 Intuition
- The principle behind nearest neighbor methods is to find a predefined number of training samples closest in distance to the new point, and predict the label from these. 
- Despite its simplicity, nearest neighbors has been successful in a large number of classification and regression problems, including handwritten digits and satellite image scenes. Being a non-parametric method, it is often successful in classification situations where the decision boundary is very irregular.
### 1.2 Mathematics
- Step 1: $D(x,x_i)$ to every training example $x_i$;
- Step 2: select $k$ closest instances $x_{i1},...,x_{ik}$ and their labels $y_{i1},...,y_{ik}$;
- Step 3: output the class y which is the mode of $y_{i1},...,y_{ik}$.
### 1.3 Choosing k
- k has strong effect on kNN performance:
  - large value: everything classified as the most probable class;
  - small value: highly variable, unstable deicision boundary.
- Set the validation set, draw the learning rate (x-->k, y-->validation error), pick k that gives a ```reasonably good``` generalization performance.
### 1.4 Distance measures
- The measure of distances has strong effect on performance as well:
  - Minkowski distance (p-norm):
  $$ D(x,x') = \sqrt[p]{\sum_d \left|x_d - x'_d\right|^p} $$
    - 1) $p = 2$: Euclidean
    - 2) $p = 1$: Manhattan
    <p align="center">
    <img src="images/knn2.jpg" width="300" height="300" alt="knn2" align=center>
    - 3) $p -> \infty$: $\underset{d}{\text{max}}\left|x_d-x'_d\right|$
    - 4) $p -> 0$: number of non-zero differences
    $$ D(x,x') = \sum_d 1_{x_d\not=x'_d} $$
  - Custom distance measures
## 2. Decision boundary
- Voronoi tesselation
  - partitions space into regions
  - boundary: points at the same distance from two different training examples
<p align="center">
<img src="images/KNN1.jpg" width="300" height="300" alt="knn" align=center>

## 3. Examples/Applications

## 4. Extensions
### 4.1 Parzen Windows and Kernels
### 4.2 K-D trees
### 4.3 Inverted list examples
### 4.4 Locality-Sensitive hashing

## 5. Practical issues

## 6. Pros and cons