# Sorting: Making Order from Chaos

This reference covers the computer science of sorting and how it applies to organizing physical objects, digital information, sports tournaments, and even social hierarchies. The book's core insight: sorting is far more expensive than most people assume, and deciding when NOT to sort is often the most important sorting decision.

## The Fundamental Law: Scale Hurts

Unlike most human activities, sorting suffers from what economist J.C. Hosken first identified in 1955 as "steep diseconomies of scale." In business, larger operations typically achieve lower per-unit costs. But in sorting, the per-unit cost rises as volume increases. Sorting a shelf of 100 books takes more than twice as long as sorting two shelves of 50 books each—because each item has more positions it could go.

This has a counterintuitive implication: the most efficient way to sort is often to sort less. Do laundry more frequently to reduce each batch size. Don't alphabetize your bookshelf if you can visually scan it in 10 seconds. Don't file your emails into folders when search takes 2 seconds.

### Case 1: Danny Hillis's Sock-Sorting Nightmare

Before he invented the Connection Machine supercomputer and founded Thinking Machines Corporation, Danny Hillis was an MIT undergraduate horrified by his roommate's sock-sorting method. The roommate would pull one sock from the clean laundry hamper, then randomly pull another. If it matched, great. If not, he tossed it back and tried again. For 10 pairs of socks, this takes an average of 110 pulls just to create all 10 pairs.

Hillis's own approach? He doesn't sort socks at all—he buys identical socks so any two match. This is the radical solution: eliminate the sorting problem entirely. For most of us, the practical lesson is: do laundry more often. Going from 14 days between washes to 13 saves 28 pulls. Going from 14 to 7 would reduce sorting overhead by a factor of 4.

### Case 2: The Preston Sort Center—Linear Time Sorting

The King County Library System's Preston Sort Center in Washington processes 85,000 books per day through a conveyor belt system with bar code scanners and 96 destination bins. This is Bucket Sort in pure action: instead of sorting books into full alphabetical order, it sorts them by destination branch. The sorting happens in O(n) time (linear), because each book is simply diverted into one of a fixed number of bins based on where it needs to go.

The New York Public Library's BookOps facility runs a similar system, and the two have a friendly rivalry for the "National Library Sorting Champion" title—with the title going back and forth since 2011.

UC Berkeley student Jordan Ho, a chemistry major and star sorter at the Doe and Moffitt Libraries (52 miles of bookshelves), demonstrates the human version: "I know from experience that there's a lot of 3500s, so I want to look for any books that are below 3500 and rough-sort those out." He uses Bucket Sort to get groups of ~25 books, then uses Insertion Sort within each group. Total time for a cart of 150 books: under 40 minutes.

### The Noise Problem: Why Bubble Sort Beats Mergesort in Real Life

Conventional computer science despises Bubble Sort (O(n²)). The legendary *Sorting and Searching* textbook declares it has "no apparent redeeming features." But University of New Mexico professor Dave Ackley's research on "robustness" reveals a surprising truth: when comparators are noisy (i.e., when comparisons can be wrong, as in sports), Bubble Sort's inefficiency becomes a feature.

Mergesort, the standard O(n log n) champion, is brittle: a single early error can permanently misplace items. Bubble Sort, moving items only one position at a time, is robust—an error only costs one position. The most noise-tolerant algorithm is Comparison Counting Sort (O(n²)), which compares each item to every other—exactly like a sports league's regular season.

Dean Oliver, pioneer of basketball analytics (the first person to publish a book on advanced basketball statistics), realized that basketball outcomes have so much noise that the postseason (Single Elimination, effectively Mergesort) is far less reliable than the regular season (Round Robin, effectively Comparison Counting Sort). The championship is chancy; the divisional standing is truth.

### Sorting in Nature: Pecking Orders

Biologist Christof Neumann studies dominance hierarchies in macaques. The term "pecking order" comes from chickens, where debeaking (removing the beak) actually INCREASES aggression because it removes the animals' ability to settle dominance through controlled fights—the sorting procedure breaks down.

University of Wisconsin–Madison's Jessica Flack argues that dominance hierarchies are fundamentally "information hierarchies." The computational burden of tracking who ranks where grows with group size. This explains why large-scale human societies require cardinal metrics (money, GDP, age) rather than ordinal comparisons (fights, duels). A race is fundamentally different from a fight—and it's what makes civilization possible.

### Practical Takeaways

- **Sort in small batches**: More frequent, smaller sorting sessions beat marathon organizing.
- **Bucket first, then sort**: Group by rough category before fine-sorting. 10 buckets of 10 items each is far faster than 1 set of 100.
- **Search usually beats sort**: For digital items, searching is almost always faster than organizing. For physical items, the break-even depends on how often you search.
- **Know your comparators**: If your comparisons are noisy (tastes, opinions, sports outcomes), use robust algorithms. If your comparisons are clean (numbers, dates, alphabetical), use efficient algorithms like Mergesort.
- **Cardinal beats ordinal**: When you can assign a numerical measure to everyone, you can skip pairwise comparisons entirely. This is how money, grades, and rankings make large-scale sorting possible without conflict.

---

*Source: "Algorithms to Live By" (2016), Chapter 3: Sorting, and field visits/interviews with Jordan Ho, Michael Trick, Jessica Flack, and Dave Ackley.*
