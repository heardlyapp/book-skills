> Source: The Computer Always Wins, Chapter 1 "Guess Wrong Answers" & Chapter 2 "The Road Not Taken" & Chapter 3 "One Step at a Time" & Chapter 4 "Whose Turn Is It Anyway?"

# Core Framework: Algorithmic Thinking, Puzzles, and Strategies

The central idea of this book: every puzzle and strategy game can be understood through a small set of core algorithmic patterns. Once you recognize the pattern, the solution approach follows naturally.

## Binary Search (Elimination Algorithm)

The simplest and most powerful algorithm. Given a sorted list, start in the middle. If your guess is wrong, eliminate the half that cannot contain the answer. Repeat. With each guess, you halve the search space. The key insight: **elimination is more powerful than selection.** Instead of trying to guess the right answer, focus on eliminating wrong answers as fast as possible.

> **Case: The Number Guessing Game** (Chapter 1): Lichtman asks: guess a number from 1 to 10, but you'll be told "too high" or "too low." Most people guess randomly. Binary search starts at 5. An incorrect 5 leaves an average of just 4.1 remaining options — better than guessing 7 (4.5 remaining). With numbers 1 to 1,024, binary search guarantees a win in at most 10 guesses. This scalability — adding one extra guess per doubling of the search space — is why computers can search billions of items instantly.
>
> **Key takeaway:** Elimination beats selection. The best first guess isn't the one most likely to be right — it's the one that eliminates the most possibilities when wrong.

> **Case: Wordle and the "Wrong" Word** (Chapter 1): Lichtman reduces Wordle to a smaller 18-word game and demonstrates a shocking result: the best first guess is often a word that CANNOT be the right answer. The word "there" is not in the 18-word bank, but it's a better first guess than any word in the bank because it eliminates more possibilities. A human player would never guess "there" — but an optimal algorithm does. The full 2,315-word Wordle database: a purely random elimination strategy solves Wordle in under 5 guesses for a third of words, and under 7 guesses for all but 187.
>
> **Key takeaway:** Algorithmic thinking often contradicts intuition. The computer's best strategy may feel wrong to a human — but it works.

## Recursion and Backtracking

When a problem involves exploring possibilities (mazes, sudoku, Eight Queens), the solution is recursion: a function that calls itself on smaller versions of the same problem. Backtracking is recursion with undo: try a move, see if it leads to a solution, and if not, undo it and try another.

> **Case: The Maze and the Ice Cream Line** (Chapter 2): Lichtman introduces recursion through a vivid metaphor: counting the number of people ahead of you in an ice cream line by asking the person in front of you to count the people ahead of THEM. Each person solves the same problem on a smaller input. The person at the front returns 0. That lets the second person return 1. And so on, back to you. The same pattern solves mazes. And shockingly, the EXACT SAME recursive function that solves a maze also solves sudoku — just with different helper functions.
>
> **Key takeaway:** Recursion is a universal problem-solving pattern. Once you learn to think recursively, you can solve an entire class of otherwise-intractable problems.

## Breadth-First vs Depth-First Search

The choice between exploring broadly (breadth-first) or deeply (depth-first) determines whether you find the shortest path (BFS) or any path quickly (DFS).

> **Case: Word Ladder from BOLD to HOPE** (Chapter 3): Lichtman builds all two-word ladders from BOLD (BOLD-HOLD, BOLD-TOLD), then all three-word ladders, and so on. The first winning path found is guaranteed to be the shortest. But the cost is staggering: with 4,000 words and depth 10, BFS would need 25+ billion nine-word options. DFS would find a path faster but might find a comically long one (GOOD to CODE via hood-hook-look-lock-dock-duck-dusk-dust-bust-bush-busy-bury-burn-born-corn-core, then CODE).
>
> **Key takeaway:** Choose BFS when path length matters (navigation, networking). Choose DFS when finding ANY path quickly is the goal (puzzles, constraint satisfaction).

## Minimax: The Heart of Game AI

For turn-based two-player games, the computer assumes its opponent is perfect. It explores all possible moves, evaluates each resulting position from both perspectives, and picks the move that maximizes its minimum guaranteed outcome.

> **Case: The Nim Game** (Chapter 4): Nim is simple: take 1 or 2 coins; whoever takes the last coin wins. A computer using minimax doesn't need to know the mathematical strategy (XOR sum). It discovers it by brute force — playing out every possible sequence of moves. This is the fundamental insight: computers don't "understand" games. They explore trees. And for games with small trees (tic-tac-toe, Nim), this brute-force approach is perfect.
>
> **Key takeaway:** Computers don't win by being smarter than humans. They win by being more thorough. A computer considers thousands of branches that a human would never bother to examine.

---

[One specific, immediate action the user can take right now.]

---

*Generated by [Heardly App](https://www.heard.ly) — turning books into knowledge you can Listen and Execute.*
