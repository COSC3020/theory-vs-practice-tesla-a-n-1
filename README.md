# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

    + If constant factors are ignored, the asymptotic analysis could be MUCH different
      than the actual runtime of the algorithm. For example, 500(O(n)) would be a lot
      slower than the expected O(n) that the analysis showed.
    + Lower order terms being ignored
    + Various implementation factors of algorithms can effect how efficient the algorithm
        performs. If there isn't much memory to work with or if the language used has

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  + Given the asymptotic complexity of a binary search is O(log n) and
  + If the 1,000 element binary tree takes 5 seconds to search through
  + The number of operations for 1,000 element BT would be about O(log(1,000))
      or 9.9657 operations
  + Then we do the same for if there were 10,000 elements O(log(1,000))
      or 13.2877 operations
  + After that we take 13.2877/9.9657 to get 1.33
  + 1.33(5 seconds) approximates to 6.665 seconds for a 10,000 element BT search

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.
