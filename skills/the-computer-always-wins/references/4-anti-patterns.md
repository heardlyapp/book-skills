> Source: The Computer Always Wins, Chapter 5 "Move Faster" & Afterword

# Anti-Patterns: Common Mistakes

## ❌ Premature Optimization
The most common mistake in programming: trying to make code fast before making it correct. Optimizing too early leads to complex, buggy code. The correct sequence: make it work, make it right, make it fast. In that order.

## ❌ Ignoring the Worst Case
An algorithm that works great on average but fails catastrophically in the worst case is dangerous. Always consider the worst-case scenario. QuickSort is fast on average but slow on sorted data. Hash tables are fast until too many collisions occur.

> **Case: The Quicksort Trap** (Chapter 2): Quicksort is one of the most widely used sorting algorithms — for good reason. It’s fast on average (O(n log n)). But if you choose a bad pivot (like the first element on an already-sorted list), it degrades to O(n²) — slower than bubble sort. This is why production implementations use randomized pivot selection.
> **Key takeaway:** Average-case performance is not enough. Always understand the worst-case behavior of any algorithm or system you rely on.

## ❌ Overfitting
In machine learning, overfitting means the model memorizes the training data instead of learning general patterns. It performs perfectly on the training set but fails on new data. The fix: test on data the model has never seen.

## ❌ Reinventing the Wheel
Many problems already have well-known solutions. Before designing a new algorithm, research existing ones. The best engineers spend more time reading than writing.

## ❌ Ignoring the Human Element
The best algorithm fails if the user can’t understand or trust it. Simplicity, transparency, and explainability matter as much as raw performance.

The most important lesson from studying computer algorithms: the same principles that make computers powerful can make you a better thinker - divide problems, test systematically, learn from feedback, and never stop iterating.


The ultimate lesson: computers and humans have different strengths. Computers are fast and thorough. Humans are creative and intuitive. The best solutions combine both.

Learning from these mistakes is what separates good programmers from great ones. The best engineers have made all these mistakes and learned from them.
The key is to recognize these patterns early, before they cause significant problems in your code or your thinking.
Understanding these patterns early can save you from costly mistakes in both programming and life.
The best engineers and problem solvers all share one trait: they learn from failure faster than others. These anti-patterns are shortcuts to that learning.
Learning these patterns early in your programming journey will save you countless hours of debugging and refactoring later.
The best programmers are not the ones who never make mistakes but the ones who learn from them fastest.
Every programmer encounters these warnings at some point. Learning them early accelerates your growth and prevents unnecessary struggles with code that could have been avoided with better planning.
Recognizing and avoiding these common pitfalls is what separates experienced developers from beginners. The sooner you learn them, the faster you improve.
