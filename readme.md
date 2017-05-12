<!-- This whole class takes about 1:45, depending on how long you give for exercise  -->

<!--6:00 5 minutes -->

# Merge Sort

## Objectives
*By the end of today's class, developers will be able to:*
- **Create** a merge sort algorithm in pseudocode
- **Understand** the principle of "proof by induction"

## Why Merge Sort?
Merge sort is one of the most powerful sorting algorithms that you will encounter. In fact it is the native `.sort` algorithm used in many JavaScript environments (such as [Mozilla's](https://bugzilla.mozilla.org/show_bug.cgi?id=224128)). It compares a list of elements using a "Divide and Conquer" strategy.

> What's the main purpose of sorting your data?

## How does it work?
Merge Sort works on the basic principal of dividing a list into sub-lists until your sub-lists are of length one or zero. Once your sub-lists are at that size, you merge with a neighboring sub-list. *Note, lists of size one are techinically already sorted.*

## Visualizations
![merge-sort-visualization](https://camo.githubusercontent.com/c9d3bf4590b7284596375ffa0cd98ee62699a757/68747470733a2f2f776562646f63732e63732e75616c62657274612e63612f253745686f6c74652f5432362f4c65637475726536466967362e676966)

<!--6:05 10 minutes -->

> Exercise: can we act it out?

<!--Write a random number between 1 and 100 on a piece of paper, and line up in random order along a wall of the class.  Split up until one-by-one.-->

<!--6:15 10 minutes -->

## How would I build it?

-  A `mergeSort` function may take an array, cut it in half [recursively](https://en.wikipedia.org/wiki/Recursion_(computer_science)) until it has divided the whole array into single items. At this point the recursive calls finally start returning to the function that invoked it. At this point a separate helper function, `merge`, could be called on a pair of sorted arrays merging them together (see visualization above).
-  The `merge` function takes two *sorted* arrays as parameters (an array with one element is technically sorted), looks at the the first elements of the two lists, and assembles a resulting list based on the two lists "zipped" together by pushing the lowest to highest valued elements.

## How long will it take?

We talked briefly about **Big O notation** before, which is an indication of how *long* something will take based on how *many* items we are dealing with.  Remember the **Big o notation** for binary search?

<details>
<summary>Answer</summary>
If array is sorted, `log(n)`, if array is not sorted, `n`.
</details>

Any guesses on how long **merge sort** will take?

<!--CFU Stop-and-jot answer -->

<!--6:25 5 minutes -->

## Proof by Induction

A Proof by Induction requires two steps:

1. First, we must show that our statement is true for a single `n`, in this case for `n=0`.
2. Second, we must show that *if we assume our statement is true* for `n=k`, we can show it is true for bigger numbers, usually `n=k+1`, but in this case `n=2k`.

You can think about this like a set of stepping stones across a river.  We can cross the entire river (all numbers greater than 0) as long as our first footing is sure, and we have a consistent step to the next stone every time.

Now, let's see if we can *prove* one of our earlier Big O guesses to be true with...**induction**.

<!--Use "Explanation of Merge Sort and Proofs" below for reference -->

<!--On whiteboard work through proof, but probably a good idea to do think-squad-shares for why 1 * log_2(1) == 0, the first two steps of T(2N), and what can we do with -2N and +2N at end -->

<!--Also between step 2 and 3 is a skipped step that looks like 2N(log_2(2N/2)) + 2N -->

## Drill
**Pseudocode** an implementation of `merge`.
**Pseudocode** an implementation of `mergeSort`.
**Convert** your pseudocode to Javascript.

## Resources

- [Explanation of Merge Sort and Proofs](http://www.cs.princeton.edu/courses/archive/spr03/cs226/lectures/analysis.4up.pdf)
- [Big O Cheat Sheet](http://bigocheatsheet.com/)
- [Merge Sort Video](https://www.youtube.com/watch?v=m2KOVTaAu0k)

## Licensing
All content is licensed under a CC­BY­NC­SA 4.0 license.
All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact legal@ga.co.
