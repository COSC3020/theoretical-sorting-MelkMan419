[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/9YUeXH71)
# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

If this claim was actually true I would expect to see the run time be $O(n)$ for any data set I put in regardless of how it was previously sorted or what they had in them, where n is the number of inputs.

Verificiation:
Choose a variety of input lists, including already sorted lists, reverse sorted lists, lists with duplicate elements, random lists, and lists with special patterns.
Vary the size of the input lists from small to large to observe the algorithm's behavior across different scales. Evaluate the algorithm's performance on edge cases, such as extremely large input lists, lists with nearly identical elements, or lists with a specific structure that might challenge the sorting process.

Conclusion:
Not possible, an algorithm can sort arbitrary elements in O(n) time based on comparisons of two elements at a time contradicts the lower bound of the comparison-based sorting problem.
Comparison-Based Sorting Lower Bound:
The comparison-based sorting lower bound establishes that any comparison-based sorting algorithm must perform at least $\Omega(nlogn)$ because every comparison based sorting algorithm MUST be able to generate all permuations of a list, the number of which is $n!$. If it doesn't do this, then it cant be sorting correctly. Therefore this algorithm cannot be sorting correctly if it is $O(n)$. 
