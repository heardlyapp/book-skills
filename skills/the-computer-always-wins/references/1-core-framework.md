> Source: The Computer Always Wins, Chapter 1 "Guess Wrong Answers" & Chapter 4 "Whose Turn Is It Anyway?"

# Core Framework: Search Trees and Minimax

The heart of game AI — and many computer algorithms — is the search tree. The computer maps out all possible moves, then all possible responses, then all possible counter-responses, building a tree of possibilities. Then it evaluates which branches lead to winning outcomes.

## Binary Search: The Simplest Powerful Algorithm

Before search trees, Lichtman introduces binary search: given a sorted list, start in the middle. If your guess is too high, eliminate the top half. If too low, eliminate the bottom half. Repeat. With each guess, you cut the remaining possibilities in half. Finding a word in a 1,000-page dictionary takes at most 10 guesses.

> **Case: The Number Guessing Game** (Chapter 1): Lichtman presents a simple game: guess a number between 1 and 100. Most people guess randomly. Binary search starts at 50. "Higher." Next: 75. "Lower." Next: 62 or 63. Within 7 guesses, you’ve found any number between 1 and 100. This is not just a party trick — it’s the same algorithm used in database indexing, debugging code, and searching sorted data.
> **Key takeaway:** Binary search is exponentially efficient. Doubling the search space adds only one extra guess. This scalability is why computers can search billions of items instantly.

## Minimax and the Game Tree

For turn-based games, the computer uses minimax: assume your opponent will make the best possible move for them (which is the worst possible move for you). Then choose the move that maximizes your minimum guaranteed outcome. The computer explores all possible moves, evaluates each resulting position, and picks the one with the highest guaranteed score.

> **Case: The Nim Game** (Chapter 4, "Whose Turn Is It Anyway?"): Nim is a simple game where players take turns removing objects from piles. The winning strategy depends on a mathematical property called the XOR sum. A computer using minimax can learn this strategy by exploring the game tree — without knowing the math. It discovers the winning positions through brute-force search, then exploits them perfectly.
> **Key takeaway:** Computers often outperform humans not by being smarter but by being more thorough. The computer explores thousands of positions that a human wouldn’t even consider. Thoroughness beats cleverness in many domains.

The elegance of binary search is that it works regardless of the size of the data. Searching a list of 10 items or 10 million items uses the same logic. The only difference is how many steps it takes. This scalability is what makes computers powerful - they apply the same simple logic at enormous scale without breaking a sweat.


The magic of algorithms is that simple rules produce intelligent behavior. A child can understand binary search in five minutes. That same algorithm powers Google, Amazon, and every database in the world. Learning algorithms is learning how to think at scale.

The simplicity and power of binary search demonstrates why algorithms are so valuable. A method that a child can understand in minutes powers the most sophisticated search systems in the world. This is the beauty of computer science: simple ideas, enormous impact.
