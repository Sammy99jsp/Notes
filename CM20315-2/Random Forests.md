What if we used multiple decision trees to overcome the overfitting of any single tree? Let's consult multiple trees, which makes a forest!

This is part of a general technique called ***ensemble*** models, where lots of independent models are consulted, and we choose an answer based on the individual results — this is usually something like a majority rule method.

### Constructing a Random Forest
Choose a number $n \tilde> 100$ (about a hundred) of trees.
For each tree:
1. Create a bootstrapped dataset:
	- Select a random row from (replacing it) from the dataset, adding it to a new 'bootstrapped' dataset until you have the same number of rows of the original dataset.
2. Create the decision tree, but with a key twist:
	- Randomly select features to consider at each node.

