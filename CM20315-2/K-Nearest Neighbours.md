Here, we can determine out model's output based off the $k$ nearest neighbours to its input.
### For Classification
![[KNN.png]]
Here if $k=3$, this blue point will be classified as **<span style="color: red">red</span>**.
### For Regression
Here, you could take a *mean*, *median*, weighted average, or *closest* point as the output.
### Extrapolation
$k$-nearest neighbour doesn't perform well at all when predict
### Distance Metrics
#### Euclidean Distance
$$\sqrt{\sum_{i=0}^d(p_0^i-p_1^i)}$$
#### Manhattan Distance
#### Cosine Similarity
Co-sine of the angle between the points and the origin.
