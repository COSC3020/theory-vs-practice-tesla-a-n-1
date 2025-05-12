# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

    + When constant factors are ignored, the asymptotic analysis could be MUCH different
      than the actual runtime of the algorithm. For example, 500(O(n)) would be a lot
      slower than the expected O(n) that the analysis showed.
    + Lower order terms also being ignored can impact how true the analysis represents the
        performance of an algorithm. Especially when combined with the constant factors
        also being ignored.  
    + Various implementation factors of algorithms can effect how efficient the algorithm
        performs. If there isn't much memory to work with or if the language used has
        rules with how arrays are handled.

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

    + Real time performace can differ from predicted performace when:
        - The tree could be unbalanced leading to excessive time to traverse tree. What I mean by this is the tree could have become a linked list which would mean a worst case O(n) vs. O(log n)
            With random permutations, its not likely, but as Jim Ward said in Data Structures, if elements were put in in sorted or almost sorted order, the tree would become very unbalanced.
            thus changing the complexity from O(log n) to O(n) which explains the jump from 6.67 seconds to 100 seconds.
        - Another reason could be due to the various positions the target could be in relative to the root of the tree. For example, if the element were close to the root in the 1,000 element tree but in a leaf node in the big 10,000 element tree, the actual path to travel on would be MUCH longer than the average case.
        - The load on the laptop's memory increased compared to when the smaller tree was run or the 1,000 element tree fit in the memory left and the 10,000 element tree. This would cause a slowdown for the larger tree and not the smaller tree if there were a memory threshold that could fit 1,000 elements but not 10,000 elements and it had to resort to other hardware to process the extra data.



[Asymptotic Complexity](https://www.sciencedirect.com/topics/computer-science/asymptotic-complexity)

[Binary Tree Basics](https://en.wikipedia.org/wiki/Binary_search_tree)

This submission was based off last semester's submission

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
