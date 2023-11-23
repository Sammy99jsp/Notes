The idea is that we want the speed of [[Heap-based Treesort]], but without creating a tree.

Heapsort does this by performing *make-heap* within the array.

Heapsort has worst-case complexity of $O(n\log n)$ (same as average-case), which is better than quick-sort's worse case $O(n^2)$. 
Though, quick-sort's best case is $O(n)$ whereas heapsort's is still $O(n\log n)$.