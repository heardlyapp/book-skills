> Source: The Computer Always Wins, Chapter 5 "Move Faster" & Chapter 6 "Pruning the Tree" & Chapter 7 "Throwing Darts" & Chapter 12 "Minimizing Regret"

# Anti-Patterns: Wrong Strategies and Cognitive Traps

Algorithms fail in predictable ways. Recognizing these failure patterns is as important as knowing the algorithms themselves.

## Mistake 1: Premature Optimization

The most common error: trying to make code fast before making it correct. Lichtman shows this throughout the book — the elegantly simple recursive solution comes first, the pruning and depth-limiting comes later.

> **Case: The Quicksort Trap** (Analogy to Chapter 5-6): Quicksort is beautiful and fast on average — but choose a bad pivot (e.g., the first element on an already-sorted list) and it degrades to O(n²), slower than bubble sort. The parallel in game AI: implementing depth-limited minimax without first verifying that the base minimax works correctly guarantees bugs. The correct sequence: make it work, make it right, make it fast.
>
> **Key takeaway:** Speed without correctness is useless. Optimize only after you have a working baseline.

## Mistake 2: Ignoring the Worst Case

An algorithm that works great "on average" but fails catastrophically in the worst case is not a good algorithm — it's a dangerous one.

> **Case: The Random Wordle Solver's Blind Spots** (Chapter 1): Lichtman's random Wordle solver works well — it identifies the hidden word in under 5 guesses for a third of the 2,315-word database. But 187 words require 7 or more guesses. Is that a failure? It depends on your standards. If you're playing for fun, 7 guesses is fine. If you're building a competitive solver, those 187 words are exactly where your algorithm needs improvement. The worst case — not the average — determines whether you can claim your algorithm "wins."
>
> **Key takeaway:** Always ask: what does failure look like? How often does it happen? Is that acceptable? Average-case thinking blinds you to catastrophic edge cases.

## Mistake 3: Assuming Symmetry in Opponent Behavior

The biggest mistake humans make in games: assuming the opponent is as rational (or irrational) as you are. The computer avoids this by assuming the opponent plays optimally — but that assumption can also be wrong.

> **Case: Exploiting Human Weakness in Rock-Paper-Scissors** (Chapter 10): A computer that assumes its opponent is random will win, lose, and tie equally. A computer that tracks patterns (reluctance to repeat, favoring one move, changing after losses) can win up to 43% of games — a significant edge. The anti-pattern is assuming your opponent has no patterns. In reality, the first round of Rock-Paper-Scissors is not random — 35.4% of people play rock. The algorithm that exploits this knowledge beats the algorithm that assumes symmetry.
>
> **Key takeaway:** The assumption that opponents are random is itself a dangerous assumption. Account for real human behavior when designing competitive algorithms.

## Mistake 4: Forgetting the Base Case in Recursion

Recursive functions must have a non-recursive exit condition. Without it, the function calls itself forever — infinite recursion. This is the programming equivalent of asking "what happens if I keep going and never stop?" The answer: stack overflow.

> **Case: The Ice Cream Line Without an End** (Chapter 2): Lichtman's recursion metaphor works because the person at the front of the line can return "0" — the base case. Remove that base case, and the question "how many people are in front of me?" propagates forever. Every recursive function in this book (maze solving, sudoku, minimax) has a clear non-recursive condition: the maze exit, a filled board, a win/loss/tie. Forgetting this is the single most common bug in recursive code.
>
> **Key takeaway:** Always define the stopping condition first when designing recursion. The base case is not optional — it's the foundation.

## Mistake 5: Giving Equal Attention to All Options

The throw-darts approach (Chapter 7) treats all options equally — 50 simulations per move, regardless of whether some options are clearly terrible. The aim-darts approach (Chapter 8) improves this by allocating simulations dynamically. But both can fall into the trap of investing too much in clearly inferior paths.

> **Case: Wasting Simulations on Bad Connect Four Moves** (Chapter 9): Lichtman's MCTS Connect Four uses a CHOOSECHILD function that naturally favors promising nodes and neglects bad ones. But if the initial random seeding causes the computer to explore a terrible move first, it can waste hundreds of simulations before the CHOOSECHILD function shifts focus. The fix: prioritize checking for immediate wins and blocks before starting the simulation tree.
>
> **Key takeaway:** Don't give equal time to all options. Check the obvious best and worst moves first. Then allocate your remaining analysis budget proportionally.

## Mistake 6: Treating the Algorithm as a Black Box

The most subtle anti-pattern in the book: becoming so confident in your algorithm that you stop verifying its outputs. The neural network in Chapter 11 is explicitly called a "black box" — the programmer feeds in data and gets predictions without understanding the internal logic. This is powerful but dangerous.

> **Case: The Neural Network's Hidden Assumptions** (Chapter 11): Lichtman's neural network distinguishes random players from reluctant players in Rock-Paper-Scissors. It does this by learning weights that it discovers through trial and error. But the programmer doesn't know which features the network actually learned to use. If the training data has a hidden bias (e.g., all "random" players were generated with one seed, all "reluctant" with another), the network will learn to exploit that bias instead of the actual distinction. This is overfitting — and you can't detect it without testing on fresh data.
>
> **Key takeaway:** Black box algorithms require continuous validation. Trust but verify. Test on data the algorithm has never seen.

---

[One specific, immediate action the user can take right now.]

---

*Generated by [Heardly App](https://www.heard.ly) — turning books into knowledge you can Listen and Execute.*
