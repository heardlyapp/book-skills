# Game Theory, Randomness, and the Minds of Others

This reference covers two interrelated themes from *Algorithms to Live By*: game theory (how to make decisions when others are also deciding) and randomness (when to intentionally leave things to chance). The book's key insight is that many of life's hardest problems involve strategic interaction and irreducible uncertainty—and the optimal response often involves deliberately not being fully in control.

## Game Theory: The Science of Strategic Interaction

### The Prisoner's Dilemma and the Origins of Cooperation

The Prisoner's Dilemma was devised in 1950 by Merrill Flood and Melvin Dresher at the RAND Corporation (Flood, incidentally, also popularized the traveling salesman problem and may have coined the term "software"). The setup: two prisoners are interrogated separately. If both stay silent, each gets 1 year. If one confesses and implicates the other, the confessor goes free while the other gets 10 years. If both confess, each gets 5 years.

Individually rational choice (confess) leads to a collectively worse outcome (5 years each) than mutual cooperation (1 year each). But when the game is repeated indefinitely, something remarkable emerges: cooperation becomes rational. The tit-for-tat strategy (start by cooperating, then mirror your opponent's last move) dominated Robert Axelrod's famous computer tournaments of the 1980s, and it remains the single most robust strategy for any repeated interaction.

### Case 1: Isaac Haxton and the Poker Hierarchy

Isaac Haxton is one of the world's best heads-up, no-limit hold 'em cash game players. His world reveals game theory in its purest form: "In some ways the most important skill as a professional poker player is to be able to evaluate how good you are. If you're anything short of the very best poker player in the world, you can be pretty much assured of going broke if you are endlessly willing to play people better than you."

Haxton describes a self-organizing hierarchy where players sit at tables and better players displace worse ones—exactly like the dominance hierarchies in macaque troops studied by Christof Neumann. "I'm one of the top heads-up, no-limit hold 'em players in the world," Haxton says, "and in my head I have a fairly specific ranking of who I think the twenty or so best players are, and I think each of them has a similar ranking in their mind."

When these rankings disagree, they play. When they agree, no game happens—the weaker player simply vacates the seat. This is sorting theory applied to a live, voluntary, money-driven system.

### Case 2: John Nash and Traffic Jams

John Nash's equilibrium concept (which won him the 1994 Nobel Prize) explains why individually rational choices can produce collectively disastrous outcomes. Nash equilibrium is the state where no single player can improve their outcome by changing their strategy alone.

The classic example: everyone chooses the fastest route to work. Individually rational. But when everyone does it, the fastest route becomes congested and nobody gains. Yet no single driver can improve by switching to a slower route. This is why traffic jams exist—they're a Nash equilibrium. The only solution is coordination (carpool lanes, congestion pricing, public transit) or randomizing strategies.

## Randomness: When to Leave It to Chance

One of the book's most counterintuitive findings is that randomness is often the optimal strategy—even when you could choose deliberately.

### Case 3: Soccer Penalty Kicks

In soccer penalty kicks, statistical analysis shows that 94% of goals are scored in the top corners of the goal. Yet 90% of kicks still go to the goalkeeper's natural side. Why? Because players prefer to feel "in control" rather than randomizing. But game theory says that goalkeepers and kickers should randomize: if a kicker always goes left, the goalkeeper can anticipate. By randomizing the direction (even occasionally kicking to the center, which has lower success rate), the kicker becomes unpredictable and improves overall conversion rates.

The same principle applies to rock-paper-scissors, poker bluffing, and military strategy. When your opponent can study your patterns, deterministic strategies are exploitable. Randomness is protection against exploitation.

### Case 4: The Traveling Salesman Problem and Relaxation

The Traveling Salesman Problem (TSP)—find the shortest route visiting n cities—is NP-hard. No efficient algorithm guarantees the optimal solution. But by "relaxing" constraints (allowing reused cities, calculating minimum spanning trees), you can get a provably good approximation.

This directly applies to life: when a problem is too hard to solve perfectly, relax one constraint. Can't plan the perfect career path? Relax the constraint that you must know your destination. Can't find the perfect apartment? Relax the constraint of perfect location. Relaxation turns intractable problems into solvable ones.

### Practical Takeaways

- **In repeated interactions, start cooperatively**: Tit-for-tat is robust. Forgiveness (occasionally cooperating after a defection) can be even better in noisy environments.
- **When you can be studied, randomize**: In any competitive situation where patterns can be exploited, add randomness to your strategy.
- **For tie-breaking, toss a coin**: When two options seem equally good, flipping a coin isn't abdicating responsibility—it's optimal. You'll never wonder "what if."
- **When stuck on a hard problem, relax a constraint**: The perfect is the enemy of the good. Find one assumption you can drop and see what becomes possible.
- **Pay attention to the structure of networks**: Six degrees of separation works because of hub nodes, not because everyone knows everyone. Build relationships with connectors, not just peers.
- **Auctions have a winner's curse**: If you win a competitive auction, you likely overpaid. Always shade your bid below your true valuation.

---

*Source: "Algorithms to Live By" (2016), Chapters 9 (Randomness), 10 (Networking), and 11 (Game Theory), and interviews with Isaac Haxton, Christof Neumann, and Michael Trick.*
