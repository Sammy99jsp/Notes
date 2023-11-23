If our model was too simple to fit the "true function", why not add more joints (hidden units)?
![[reduce-bias.png]]
Unfortunately, if we keep the number of data points the same, the variance increase quite quickly too:
![[increased-bias.png]]This variance increases because of over-fitting as our model will try to exactly fit every point in the training set (including the noisy ones!)

This phenomenon is the **bias-variance tradeoff**:
![[bias-variance-tradeoff.png]]