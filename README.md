# CollatzConjecture
The Collatz conjecture is a conjecture in mathematics that concerns sequences defined as follows: start with any positive integer n. Then each term is obtained from the previous term as follows: if the previous term is even, the next term is one half of the previous term. If the previous term is odd, the next term is 3 times the previous term plus 1. The conjecture is that no matter what value of n, the sequence will always reach 1.

Collatz conjecture
From Wikipedia, the free encyclopedia
Unsolved problem in mathematics:
Does the Collatz sequence eventually reach 1 for all positive integer initial values?

Directed graph showing the orbits of small numbers under the Collatz map, skipping even numbers. The Collatz conjecture states that all paths eventually lead to 1.
The Collatz conjecture is a conjecture in mathematics that concerns sequences defined as follows: start with any positive integer n. Then each term is obtained from the previous term as follows: if the previous term is even, the next term is one half of the previous term. If the previous term is odd, the next term is 3 times the previous term plus 1. The conjecture is that no matter what value of n, the sequence will always reach 1.

The conjecture is named after Lothar Collatz, who introduced the idea in 1937, two years after receiving his doctorate.[1] It is also known as the 3n + 1 problem, the 3n + 1 conjecture, the Ulam conjecture (after Stanisław Ulam), Kakutani's problem (after Shizuo Kakutani), the Thwaites conjecture (after Sir Bryan Thwaites), Hasse's algorithm (after Helmut Hasse), or the Syracuse problem.[2][4] The sequence of numbers involved is sometimes referred to as the hailstone sequence or hailstone numbers (because the values are usually subject to multiple descents and ascents like hailstones in a cloud),[5][6] or as wondrous numbers.[7]

Paul Erdős said about the Collatz conjecture: "Mathematics may not be ready for such problems."[8] He also offered US$500 for its solution.[9] Jeffrey Lagarias stated in 2010 that the Collatz conjecture "is an extraordinarily difficult problem, completely out of reach of present day mathematics."[10]


Contents
1	Statement of the problem
2	Empirical data
3	Visualizations
4	Supporting arguments
4.1	Experimental evidence
4.2	A probabilistic heuristic
4.3	Stopping times
4.4	Lower bounds
5	Cycles
5.1	Cycle length
5.2	k-cycles
6	Other formulations of the conjecture
6.1	In reverse
6.2	As an abstract machine that computes in base two
6.2.1	Example
6.3	As a parity sequence
6.4	As a tag system
7	Extensions to larger domains
7.1	Iterating on all integers
7.2	Iterating on rationals with odd denominators
7.3	2-adic extension
7.4	Iterating on real or complex numbers
8	Optimizations
8.1	Time–space tradeoff
8.2	Modular restrictions
9	Syracuse function
10	Undecidable generalizations
11	In popular culture
12	See also
13	Further reading
14	References
15	External links
Statement of the problem

Numbers from 1 to 9999 and their corresponding total stopping time

Histogram of total stopping times for the numbers 1 to 108. Total stopping time is on the x axis, frequency on the y axis.

Histogram of total stopping times for the numbers 1 to 109. Total stopping time is on the x axis, frequency on the y axis.

Iteration time for inputs of 2 to 107.
Total Stopping Time: numbers up to 250, 1000, 4000, 20000, 100000, 500000
Total stopping time of numbers up to 250, 1000, 4000, 20000, 100000, 500000
Consider the following operation on an arbitrary positive integer:

If the number is even, divide it by two.
If the number is odd, triple it and add one.
In modular arithmetic notation, define the function f as follows:

{\displaystyle f(n)={\begin{cases}{\frac {n}{2}}&{\text{if }}n\equiv 0{\pmod {2}}\\[4px]3n+1&{\text{if }}n\equiv 1{\pmod {2}}.\end{cases}}}{\displaystyle f(n)={\begin{cases}{\frac {n}{2}}&{\text{if }}n\equiv 0{\pmod {2}}\\[4px]3n+1&{\text{if }}n\equiv 1{\pmod {2}}.\end{cases}}}
Now form a sequence by performing this operation repeatedly, beginning with any positive integer, and taking the result at each step as the input at the next.

In notation:

{\displaystyle a_{i}={\begin{cases}n&{\text{for }}i=0\\f(a_{i-1})&{\text{for }}i>0\end{cases}}}a_{i}={\begin{cases}n&{\text{for }}i=0\\f(a_{i-1})&{\text{for }}i>0\end{cases}}
(that is: ai is the value of f applied to n recursively i times; ai = fi(n)).

The Collatz conjecture is: This process will eventually reach the number 1, regardless of which positive integer is chosen initially.

If the conjecture is false, it can only be because there is some starting number which gives rise to a sequence that does not contain 1. Such a sequence would either enter a repeating cycle that excludes 1, or increase without bound. No such sequence has been found.

The smallest i such that ai < a0 is called the stopping time of n. Similarly, the smallest k such that ak = 1 is called the total stopping time of n.[3] If one of the indexes i or k doesn't exist, we say that the stopping time or the total stopping time, respectively, is infinite.

The Collatz conjecture asserts that the total stopping time of every n is finite. It is also equivalent to saying that every n ≥ 2 has a finite stopping time.

Since 3n + 1 is even whenever n is odd, one may instead use the "shortcut" form of the Collatz function:

{\displaystyle f(n)={\begin{cases}{\frac {n}{2}}&{\text{if }}n\equiv 0{\pmod {2}},\\[4px]{\frac {3n+1}{2}}&{\text{if }}n\equiv 1{\pmod {2}}.\end{cases}}}{\displaystyle f(n)={\begin{cases}{\frac {n}{2}}&{\text{if }}n\equiv 0{\pmod {2}},\\[4px]{\frac {3n+1}{2}}&{\text{if }}n\equiv 1{\pmod {2}}.\end{cases}}}
This definition yields smaller values for the stopping time and total stopping time without changing the overall dynamics of the process.
Empirical data
For instance, starting with n = 12, one gets the sequence 12, 6, 3, 10, 5, 16, 8, 4, 2, 1.

The number n = 19 takes longer to reach 1: 19, 58, 29, 88, 44, 22, 11, 34, 17, 52, 26, 13, 40, 20, 10, 5, 16, 8, 4, 2, 1.

The sequence for n = 27, listed and graphed below, takes 111 steps (41 steps through odd numbers, in italics), climbing as high as 9232 before descending to 1.

27, 82, 41, 124, 62, 31, 94, 47, 142, 71, 214, 107, 322, 161, 484, 242, 121, 364, 182, 91, 274, 137, 412, 206, 103, 310, 155, 466, 233, 700, 350, 175, 526, 263, 790, 395, 1186, 593, 1780, 890, 445, 1336, 668, 334, 167, 502, 251, 754, 377, 1132, 566, 283, 850, 425, 1276, 638, 319, 958, 479, 1438, 719, 2158, 1079, 3238, 1619, 4858, 2429, 7288, 3644, 1822, 911, 2734, 1367, 4102, 2051, 6154, 3077, 9232, 4616, 2308, 1154, 577, 1732, 866, 433, 1300, 650, 325, 976, 488, 244, 122, 61, 184, 92, 46, 23, 70, 35, 106, 53, 160, 80, 40, 20, 10, 5, 16, 8, 4, 2, 1 (sequence A008884 in the OEIS)
Collatz5.svg
Numbers with a total stopping time longer than that of any smaller starting value form a sequence beginning with:

1, 2, 3, 6, 7, 9, 18, 25, 27, 54, 73, 97, 129, 171, 231, 313, 327, 649, 703, 871, 1161, 2223, 2463, 2919, 3711, 6171, ... (sequence A006877 in the OEIS).
The starting values whose maximum trajectory point is greater than that of any smaller starting value are as follows:

1, 2, 3, 7, 15, 27, 255, 447, 639, 703, 1819, 4255, 4591, 9663, 20895, 26623, 31911, 60975, 77671, 113383, 138367, 159487, 270271, 665215, 704511, ... (sequence A006884 in the OEIS)
Number of steps for n to reach 1 are

0, 1, 7, 2, 5, 8, 16, 3, 19, 6, 14, 9, 9, 17, 17, 4, 12, 20, 20, 7, 7, 15, 15, 10, 23, 10, 111, 18, 18, 18, 106, 5, 26, 13, 13, 21, 21, 21, 34, 8, 109, 8, 29, 16, 16, 16, 104, 11, 24, 24, ... (sequence A006577 in the OEIS)
The starting value having the largest total stopping time while being

less than 10 is 9, which has 19 steps,
less than 100 is 97, which has 118 steps,
less than 1000 is 871, which has 178 steps,
less than 104 is 6171, which has 261 steps,
less than 105 is 77031, which has 350 steps,
less than 106 is 837799, which has 524 steps,
less than 107 is 8400511, which has 685 steps,
less than 108 is 63728127, which has 949 steps,
less than 109 is 670617279, which has 986 steps,
less than 1010 is 9780657630, which has 1132 steps,[11]
less than 1011 is 75128138247, which has 1228 steps,
less than 1012 is 989345275647, which has 1348 steps,
less than 1013 is 7887663552367, which has 1563 steps,
less than 1014 is 80867137596217, which has 1662 steps,
less than 1015 is 942488749153153, which has 1862 steps,
less than 1016 is 7579309213675935, which has 1958 steps,
less than 1017 is 93571393692802302, which has 2091 steps and
less than 1018 is 931386509544713451, which has 2283 steps.[12]
These numbers are the lowest ones with the indicated step count, but not necessarily the only ones below the given limit. As an example, 9780657631 has 1132 steps, as does 9780657630.

The starting values having the smallest total stopping time with respect to their number of digits (in base 2) are the powers of two since 2n is halved n times to reach 1, and is never increased.

Visualizations

Directed graph showing the orbits of the first 1000 numbers.

 

The x axis represents starting number, the y axis represents the highest number reached during the chain to 1. This plot shows a restricted y axis: some x values produce intermediates as high as 2.7×107 (for x = 9663)

 

The tree of all the numbers having fewer than 20 steps (click to enlarge).

Supporting arguments
Although the conjecture has not been proven, most mathematicians who have looked into the problem think the conjecture is true because experimental evidence and heuristic arguments support it.

Experimental evidence
As of 2020, the conjecture has been checked by computer for all starting values up to 268 ≈ 2.95×1020. All initial values tested so far eventually end in the repeating cycle (4;2;1) of period 3.[13]

This computer evidence is not sufficient to prove that the conjecture is true for all starting values. As in the case of some disproved conjectures, like the Pólya conjecture, counterexamples might be found when considering very large numbers.

However, such verifications may have other implications. For example, one can derive additional constraints on the period and structural form of a non-trivial cycle.[14][15][16]

A probabilistic heuristic
If one considers only the odd numbers in the sequence generated by the Collatz process, then each odd number is on average 
3
/
4
 of the previous one.[17] (More precisely, the geometric mean of the ratios of outcomes is 
3
/
4
.) This yields a heuristic argument that every Hailstone sequence should decrease in the long run, although this is not evidence against other cycles, only against divergence. The argument is not a proof because it assumes that Hailstone sequences are assembled from uncorrelated probabilistic events. (It does rigorously establish that the 2-adic extension of the Collatz process has two division steps for every multiplication step for almost all 2-adic starting values.)

Stopping times
As proved by Riho Terras, almost every positive integer n has a finite stopping time.[18] In other words, almost every Collatz sequence reaches a point that is strictly below its initial value. The proof is based on the distribution of parity vectors and uses the central limit theorem.

In 2019, Terence Tao considerably improved this result by showing, using logarithmic density, that almost all Collatz orbits are descending below any given function of the starting point, provided that this function diverges to infinity, no matter how slowly. Responding to this work, Quanta Magazine wrote that Tao "came away with one of the most significant results on the Collatz conjecture in decades."[19][20]

Lower bounds
In a computer-aided proof, Krasikov and Lagarias showed that the number of integers in the interval [1,x] that eventually reach 1 is at least equal to x0.84 for all sufficiently large x.[21]

Cycles
In this part, consider the shortcut form of the Collatz function

{\displaystyle f(n)={\begin{cases}{\frac {n}{2}}&{\text{if }}n\equiv 0{\pmod {2}},\\[4px]{\frac {3n+1}{2}}&{\text{if }}n\equiv 1{\pmod {2}}.\end{cases}}}{\displaystyle f(n)={\begin{cases}{\frac {n}{2}}&{\text{if }}n\equiv 0{\pmod {2}},\\[4px]{\frac {3n+1}{2}}&{\text{if }}n\equiv 1{\pmod {2}}.\end{cases}}}
A cycle is a sequence (a0, a1, ..., aq) of distinct positive integers where f(a0) = a1, f(a1) = a2, ..., and f(aq) = a0.

The only known cycle is (1,2) of period 2, called the trivial cycle.

Cycle length
The length of a non-trivial cycle is known to be at least 17087915.[15] In fact, Eliahou (1993) proved that the period p of any non-trivial cycle is of the form

{\displaystyle p=301994a+17087915b+85137581c}{\displaystyle p=301994a+17087915b+85137581c}
where a, b and c are non-negative integers, b ≥ 1 and ac = 0. This result is based on the continued fraction expansion of 
ln 3
/
ln 2
.

A similar reasoning that accounts for the recent verification of the conjecture up to 268 leads to the improved lower bound 114208327604 (or 186265759595 without the "shortcut"). This lower bound is consistent with the above result, since 114208327604 = 17087915 × 361 + 85137581 × 1269.

k-cycles
A k-cycle is a cycle that can be partitioned into 2k contiguous subsequences: k increasing sequences of odd numbers alternating with k decreasing sequences of even numbers.[16] For instance, if the cycle consists of a single increasing sequence of odd numbers followed by a decreasing sequence of even numbers, it is called a 1-cycle.

Steiner (1977) proved that there is no 1-cycle other than the trivial (1;2).[22] Simons (2004) used Steiner's method to prove that there is no 2-cycle.[23] Simons & de Weger (2005) extended this proof up to 68-cycles: there is no k-cycle up to k = 68.[16] For each k beyond 68, this method gives an upper bound for the smallest term of a k-cycle: for example, if there is a 77-cycle, then at least one element of the cycle is less than 38137×250.[16] Along with the verification of the conjecture up to 268, this implies the nonexistence of a non-trivial k-cycle up to k = 77.[13] As exhaustive computer searches continue, larger k values may be ruled out. To state the argument more intuitively: we need not look for cycles that have at most 77 circuits, where each circuit consists of consecutive ups followed by consecutive downs.

Other formulations of the conjecture
In reverse

The first 21 levels of the Collatz graph generated in bottom-up fashion. The graph includes all numbers with an orbit length of 21 or less.
There is another approach to prove the conjecture, which considers the bottom-up method of growing the so-called Collatz graph. The Collatz graph is a graph defined by the inverse relation

{\displaystyle R(n)={\begin{cases}\{2n\}&{\text{if }}n\equiv 0,1,2,3,5\\[4px]\left\{2n,{\frac {n-1}{3}}\right\}&{\text{if }}n\equiv 4\end{cases}}{\pmod {6}}.}{\displaystyle R(n)={\begin{cases}\{2n\}&{\text{if }}n\equiv 0,1,2,3,5\\[4px]\left\{2n,{\frac {n-1}{3}}\right\}&{\text{if }}n\equiv 4\end{cases}}{\pmod {6}}.}
So, instead of proving that all positive integers eventually lead to 1, we can try to prove that 1 leads backwards to all positive integers. For any integer n, n ≡ 1 (mod 2) if and only if 3n + 1 ≡ 4 (mod 6). Equivalently, 
n − 1
/
3
 ≡ 1 (mod 2) if and only if n ≡ 4 (mod 6). Conjecturally, this inverse relation forms a tree except for the 1–2–4 loop (the inverse of the 4–2–1 loop of the unaltered function f defined in the Statement of the problem section of this article).

When the relation 3n + 1 of the function f is replaced by the common substitute "shortcut" relation 
3n + 1
/
2
, the Collatz graph is defined by the inverse relation,

{\displaystyle R(n)={\begin{cases}\{2n\}&{\text{if }}n\equiv 0,1\\[4px]\left\{2n,{\frac {2n-1}{3}}\right\}&{\text{if }}n\equiv 2\end{cases}}{\pmod {3}}.}{\displaystyle R(n)={\begin{cases}\{2n\}&{\text{if }}n\equiv 0,1\\[4px]\left\{2n,{\frac {2n-1}{3}}\right\}&{\text{if }}n\equiv 2\end{cases}}{\pmod {3}}.}
For any integer n, n ≡ 1 (mod 2) if and only if 
3n + 1
/
2
 ≡ 2 (mod 3). Equivalently, 
2n − 1
/
3
 ≡ 1 (mod 2) if and only if n ≡ 2 (mod 3). Conjecturally, this inverse relation forms a tree except for a 1–2 loop (the inverse of the 1–2 loop of the function f(n) revised as indicated above).

Alternatively, replace the 3n + 1 with 
n′
/
H(n′)
 where n′ = 3n + 1 and H(n′) is the highest power of 2 that divides n′ (with no remainder). The resulting function f maps from odd numbers to odd numbers. Now suppose that for some odd number n, applying this operation k times yields the number 1 (that is, fk(n) = 1). Then in binary, the number n can be written as the concatenation of strings wk wk−1 … w1 where each wh is a finite and contiguous extract from the representation of 
1
/
3h
.[24] The representation of n therefore holds the repetends of 
1
/
3h
, where each repetend is optionally rotated and then replicated up to a finite number of bits. It is only in binary that this occurs.[25] Conjecturally, every binary string s that ends with a '1' can be reached by a representation of this form (where we may add or delete leading '0's to s).

As an abstract machine that computes in base two
Repeated applications of the Collatz function can be represented as an abstract machine that handles strings of bits. The machine will perform the following three steps on any odd number until only one 1 remains:

Append 1 to the (right) end of the number in binary (giving 2n + 1);
Add this to the original number by binary addition (giving 2n + 1 + n = 3n + 1);
Remove all trailing 0s (i.e. repeatedly divide by two until the result is odd).
Example
The starting number 7 is written in base two as 111. The resulting Collatz sequence is:

         111
        1111
       10110
      10111
     100010
    100011
    110100
   11011
  101000
 1011
10000
As a parity sequence
For this section, consider the Collatz function in the slightly modified form

{\displaystyle f(n)={\begin{cases}{\frac {n}{2}}&{\text{if }}n\equiv 0\\[4px]{\frac {3n+1}{2}}&{\text{if }}n\equiv 1\end{cases}}{\pmod {2}}.}{\displaystyle f(n)={\begin{cases}{\frac {n}{2}}&{\text{if }}n\equiv 0\\[4px]{\frac {3n+1}{2}}&{\text{if }}n\equiv 1\end{cases}}{\pmod {2}}.}
This can be done because when n is odd, 3n + 1 is always even.

If P(…) is the parity of a number, that is P(2n) = 0 and P(2n + 1) = 1, then we can define the Collatz parity sequence (or parity vector) for a number n as pi = P(ai), where a0 = n, and ai+1 = f(ai).

Which operation is performed, 
3n + 1
/
2
 or 
n
/
2
, depends on the parity. The parity sequence is the same as the sequence of operations.

Using this form for f(n), it can be shown that the parity sequences for two numbers m and n will agree in the first k terms if and only if m and n are equivalent modulo 2k. This implies that every number is uniquely identified by its parity sequence, and moreover that if there are multiple Hailstone cycles, then their corresponding parity cycles must be different.[3][18]

Applying the f function k times to the number n = 2ka + b will give the result 3ca + d, where d is the result of applying the f function k times to b, and c is how many increases were encountered during that sequence (e.g. for 25a + 1 there are 3 increases as 1 iterates to 2, 1, 2, 1, and finally to 2 so the result is 33a + 2; for 22a + 1 there is only 1 increase as 1 rises to 2 and falls to 1 so the result is 3a + 1). When b is 2k − 1 then there will be k rises and the result will be 2 × 3ka − 1. The factor of 3 multiplying a is independent of the value of a; it depends only on the behavior of b. This allows one to predict that certain forms of numbers will always lead to a smaller number after a certain number of iterations, e.g. 4a + 1 becomes 3a + 1 after two applications of f and 16a + 3 becomes 9a + 2 after 4 applications of f. Whether those smaller numbers continue to 1, however, depends on the value of a.

As a tag system
For the Collatz function in the form

{\displaystyle f(n)={\begin{cases}{\frac {n}{2}}&{\text{if }}n\equiv 0\\[4px]{\frac {3n+1}{2}}&{\text{if }}n\equiv 1.\end{cases}}{\pmod {2}}}{\displaystyle f(n)={\begin{cases}{\frac {n}{2}}&{\text{if }}n\equiv 0\\[4px]{\frac {3n+1}{2}}&{\text{if }}n\equiv 1.\end{cases}}{\pmod {2}}}

Hailstone sequences can be computed by the extremely simple 2-tag system with production rules

a → bc, b → a, c → aaa.
In this system, the positive integer n is represented by a string of n copies of a, and iteration of the tag operation halts on any word of length less than 2. (Adapted from De Mol.)

The Collatz conjecture equivalently states that this tag system, with an arbitrary finite string of a as the initial word, eventually halts (see Tag system#Example: Computation of Collatz sequences for a worked example).

Extensions to larger domains
Iterating on all integers
An extension to the Collatz conjecture is to include all integers, not just positive integers. Leaving aside the cycle 0 → 0 which cannot be entered from outside, there are a total of 4 known cycles, which all nonzero integers seem to eventually fall into under iteration of f. These cycles are listed here, starting with the well-known cycle for positive n:

Odd values are listed in large bold. Each cycle is listed with its member of least absolute value (which is always odd) first.

Cycle	Odd-value cycle length	Full cycle length
1 → 4 → 2 → 1 ...	1	3
−1 → −2 → −1 ...	1	2
−5 → −14 → −7 → −20 → −10 → −5 ...	2	5
−17 → −50 → −25 → −74 → −37 → −110 → −55 → −164 → −82 → −41 → −122 → −61 → −182 → −91 → −272 → −136 → −68 → −34 → −17 ...	7	18
The generalized Collatz conjecture is the assertion that every integer, under iteration by f, eventually falls into one of the four cycles above or the cycle 0 → 0. The 0 → 0 cycle is often regarded as "trivial" by the argument, as it is only included for the sake of completeness.

Iterating on rationals with odd denominators
The Collatz map can be extended to (positive or negative) rational numbers which have odd denominators when written in lowest terms. The number is taken to be 'odd' or 'even' according to whether its numerator is odd or even. Then the formula for the map is exactly the same as when the domain is the integers: an 'even' such rational is divided by 2; an 'odd' such rational is multiplied by 3 and then 1 is added. A closely related fact is that the Collatz map extends to the ring of 2-adic integers, which contains the ring of rationals with odd denominators as a subring.

When using the "shortcut" definition of the Collatz map, it is known that any periodic parity sequence is generated by exactly one rational.[26] Conversely, it is conjectured that every rational with an odd denominator has an eventually cyclic parity sequence (Periodicity Conjecture[3]).

If a parity cycle has length n and includes odd numbers exactly m times at indices k0 < ⋯ < km−1, then the unique rational which generates immediately and periodically this parity cycle is

{\displaystyle {\frac {3^{m-1}2^{k_{0}}+\cdots +3^{0}2^{k_{m-1}}}{2^{n}-3^{m}}}.}{\frac {3^{m-1}2^{k_{0}}+\cdots +3^{0}2^{k_{m-1}}}{2^{n}-3^{m}}}.
 

 

 

 

(1)

For example, the parity cycle (1 0 1 1 0 0 1) has length 7 and four odd terms at indices 0, 2, 3, and 6. It is repeatedly generated by the fraction

{\displaystyle {\frac {3^{3}2^{0}+3^{2}2^{2}+3^{1}2^{3}+3^{0}2^{6}}{2^{7}-3^{4}}}={\frac {151}{47}}}{\displaystyle {\frac {3^{3}2^{0}+3^{2}2^{2}+3^{1}2^{3}+3^{0}2^{6}}{2^{7}-3^{4}}}={\frac {151}{47}}}
as the latter leads to the rational cycle

{\displaystyle {\frac {151}{47}}\rightarrow {\frac {250}{47}}\rightarrow {\frac {125}{47}}\rightarrow {\frac {211}{47}}\rightarrow {\frac {340}{47}}\rightarrow {\frac {170}{47}}\rightarrow {\frac {85}{47}}\rightarrow {\frac {151}{47}}.}{\displaystyle {\frac {151}{47}}\rightarrow {\frac {250}{47}}\rightarrow {\frac {125}{47}}\rightarrow {\frac {211}{47}}\rightarrow {\frac {340}{47}}\rightarrow {\frac {170}{47}}\rightarrow {\frac {85}{47}}\rightarrow {\frac {151}{47}}.}
Any cyclic permutation of (1 0 1 1 0 0 1) is associated to one of the above fractions. For instance, the cycle (0 1 1 0 0 1 1) is produced by the fraction

{\displaystyle {\frac {3^{3}2^{1}+3^{2}2^{2}+3^{1}2^{5}+3^{0}2^{6}}{2^{7}-3^{4}}}={\frac {250}{47}}.}{\displaystyle {\frac {3^{3}2^{1}+3^{2}2^{2}+3^{1}2^{5}+3^{0}2^{6}}{2^{7}-3^{4}}}={\frac {250}{47}}.}
For a one-to-one correspondence, a parity cycle should be irreducible, i.e., not partitionable into identical sub-cycles. As an illustration of this, the parity cycle (1 1 0 0 1 1 0 0) and its sub-cycle (1 1 0 0) are associated to the same fraction 
5
/
7
 when reduced to lowest terms.

In this context, assuming the validity of the Collatz conjecture implies that (1 0) and (0 1) are the only parity cycles generated by positive whole numbers (1 and 2, respectively).

If the odd denominator d of a rational is not a multiple of 3, then all the iterates have the same denominator and the sequence of numerators can be obtained by applying the "3n + d" generalization[27] of the Collatz function

{\displaystyle T_{d}(x)={\begin{cases}{\frac {x}{2}}&{\text{if }}x\equiv 0{\pmod {2}},\\[4px]{\frac {3x+d}{2}}&{\text{if }}x\equiv 1{\pmod {2}}.\end{cases}}}{\displaystyle T_{d}(x)={\begin{cases}{\frac {x}{2}}&{\text{if }}x\equiv 0{\pmod {2}},\\[4px]{\frac {3x+d}{2}}&{\text{if }}x\equiv 1{\pmod {2}}.\end{cases}}}
2-adic extension
The function

{\displaystyle T(x)={\begin{cases}{\frac {x}{2}}&{\text{if }}x\equiv 0{\pmod {2}}\\[4px]{\frac {3x+1}{2}}&{\text{if }}x\equiv 1{\pmod {2}}\end{cases}}}{\displaystyle T(x)={\begin{cases}{\frac {x}{2}}&{\text{if }}x\equiv 0{\pmod {2}}\\[4px]{\frac {3x+1}{2}}&{\text{if }}x\equiv 1{\pmod {2}}\end{cases}}}
is well-defined on the ring ℤ2 of 2-adic integers, where it is continuous and measure-preserving with respect to the 2-adic measure. Moreover, its dynamics is known to be ergodic.[3]

Define the parity vector function Q acting on ℤ2 as

{\displaystyle Q(x)=\sum _{k=0}^{\infty }\left(T^{k}(x)\mod 2\right)2^{k}}{\displaystyle Q(x)=\sum _{k=0}^{\infty }\left(T^{k}(x)\mod 2\right)2^{k}}.
The function Q is a 2-adic isometry.[28] Consequently, every infinite parity sequence occurs for exactly one 2-adic integer, so that almost all trajectories are acyclic in {\displaystyle \mathbb {Z} _{2}}\mathbb {Z} _{2}.

An equivalent formulation of the Collatz conjecture is that

{\displaystyle Q\left(\mathbb {Z} ^{+}\right)\subset {\tfrac {1}{3}}\mathbb {Z} .}{\displaystyle Q\left(\mathbb {Z} ^{+}\right)\subset {\tfrac {1}{3}}\mathbb {Z} .}
Iterating on real or complex numbers

Cobweb plot of the orbit 10-5-8-4-2-1-2-1-2-1-etc. in the real extension of the Collatz map (optimized by replacing "3n + 1" with "
3n + 1
/
2
")
The Collatz map (with shortcut) can be viewed as the restriction to the integers of the smooth map

{\displaystyle f(z)={\frac {1}{2}}z\cos ^{2}\left({\frac {\pi }{2}}z\right)+{\frac {3z+1}{2}}\sin ^{2}\left({\frac {\pi }{2}}z\right).}{\displaystyle f(z)={\frac {1}{2}}z\cos ^{2}\left({\frac {\pi }{2}}z\right)+{\frac {3z+1}{2}}\sin ^{2}\left({\frac {\pi }{2}}z\right).}


Collatz map fractal in a neighbourhood of the real line
The iterations of this map on the real line lead to a dynamical system, further investigated by Chamberland.[29] He showed that the conjecture does not hold for positive real numbers since there are infinitely many fixed points, as well as orbits escaping monotonically to infinity. The function f has two attracting cycles of period 2, (1;2) and (1.1925...;2.1386...). Moreover, the set of unbounded orbits is conjectured to be of measure 0.

Letherman, Schleicher, and Wood extended the study to the complex plane, where most of the points have orbits that diverge to infinity (colored region on the illustration).[30] The boundary between the colored region and the black components, namely the Julia set of f, is a fractal pattern, sometimes called the "Collatz fractal".

Optimizations
Time–space tradeoff
The section As a parity sequence above gives a way to speed up simulation of the sequence. To jump ahead k steps on each iteration (using the f function from that section), break up the current number into two parts, b (the k least significant bits, interpreted as an integer), and a (the rest of the bits as an integer). The result of jumping ahead k steps can be found as:

fk(2ka + b) = 3c(b)a + d(b).
The c (or better 3c) and d arrays are precalculated for all possible k-bit numbers b, where d(b) is the result of applying the f function k times to b, and c(b) is the number of odd numbers encountered on the way.[31] For example, if k = 5, one can jump ahead 5 steps on each iteration by separating out the 5 least significant bits of a number and using:

c(0...31) = {0,3,2,2,2,2,2,4,1,4,1,3,2,2,3,4,1,2,3,3,1,1,3,3,2,3,2,4,3,3,4,5}
d(0...31) = {0,2,1,1,2,2,2,20,1,26,1,10,4,4,13,40,2,5,17,17,2,2,20,20,8,22,8,71,26,26,80,242}.
This requires 2k precomputation and storage to speed up the resulting calculation by a factor of k, a space–time tradeoff.

Modular restrictions
For the special purpose of searching for a counterexample to the Collatz conjecture, this precomputation leads to an even more important acceleration, used by Tomás Oliveira e Silva in his computational confirmations of the Collatz conjecture up to large values of n. If, for some given b and k, the inequality

fk(2ka + b) = 3c(b)a + d(b) < 2ka + b
holds for all a, then the first counterexample, if it exists, cannot be b modulo 2k.[14] For instance, the first counterexample must be odd because f(2n) = n, smaller than 2n; and it must be 3 mod 4 because f2(4n + 1) = 3n + 1, smaller than 4n + 1. For each starting value a which is not a counterexample to the Collatz conjecture, there is a k for which such an inequality holds, so checking the Collatz conjecture for one starting value is as good as checking an entire congruence class. As k increases, the search only needs to check those residues b that are not eliminated by lower values of k. Only an exponentially small fraction of the residues survive.[32] For example, the only surviving residues mod 32 are 7, 15, 27, and 31.

Syracuse function
If k is an odd integer, then 3k + 1 is even, so 3k + 1 = 2ak′ with k′ odd and a ≥ 1. The Syracuse function is the function f from the set I of odd integers into itself, for which f(k) = k′ (sequence A075677 in the OEIS).

Some properties of the Syracuse function are:

For all k ∈ I, f(4k + 1) = f(k). (Because 3(4k + 1) + 1 = 12k + 4 = 4(3k + 1).)
In more generality: For all p ≥ 1 and odd h, fp − 1(2ph − 1) = 2 × 3p − 1h − 1. (Here fp − 1 is function iteration notation.)
For all odd h, f(2h − 1) ≤ 
3h − 1
/
2
The Collatz conjecture is equivalent to the statement that, for all k in I, there exists an integer n ≥ 1 such that fn(k) = 1.

Undecidable generalizations
In 1972, John Horton Conway proved that a natural generalization of the Collatz problem is algorithmically undecidable.[33]

Specifically, he considered functions of the form

{\displaystyle {g(n)=a_{i}n+b_{i}}\;\;,{\text{where}}\;{n\equiv i{\pmod {P}}}}{\displaystyle {g(n)=a_{i}n+b_{i}}\;\;,{\text{where}}\;{n\equiv i{\pmod {P}}}}
and a0, b0,...,aP − 1, bP − 1 are rational numbers which are so chosen that g(n) is always an integer.

The standard Collatz function is given by P = 2, a0 = 
1
/
2
, b0 = 0, a1 = 3, b1 = 1. Conway proved that the problem:

Given g and n, does the sequence of iterates gk(n) reach 1?
is undecidable, by representing the halting problem in this way.

Closer to the Collatz problem is the following universally quantified problem:

Given g does the sequence of iterates gk(n) reach 1, for all n > 0?
Modifying the condition in this way can make a problem either harder or easier to solve (intuitively, it is harder to justify a positive answer but might be easier to justify a negative one). Kurtz and Simon[34] proved that the above problem is, in fact, undecidable and even higher in the arithmetical hierarchy, specifically Π0
2-complete. This hardness result holds even if one restricts the class of functions g by fixing the modulus P to 6480.[35]

In popular culture
In the movie Incendies, a graduate student in pure mathematics explains the Collatz conjecture to a group of undergraduates. She puts her studies on hold for a time to address some unresolved questions about her family's past. Late in the movie, the Collatz conjecture turns out to have foreshadowed a disturbing and difficult discovery that she makes about her family.[36][37]

See also
icon	Mathematics portal
3x + 1 semigroup
Arithmetic dynamics
Modular arithmetic
Residue-class-wise affine group
Further reading
The Ultimate Challenge: the 3x + 1 problem:
This volume,[10] edited by Jeffrey Lagarias and published by the American Mathematical Society, is a compendium of information on the Collatz conjecture, methods of approaching it and generalizations. It includes two survey papers by the editor and five by other authors, concerning the history of the problem, generalizations, statistical approaches and results from the theory of computation. It also includes reprints of early papers on the subject (including an entry by Lothar Collatz).
References
 O'Connor, J.J.; Robertson, E.F. (2006). "Lothar Collatz". St Andrews University School of Mathematics and Statistics, Scotland.
 Maddux, Cleborne D.; Johnson, D. Lamont (1997). Logo: A Retrospective. New York: Haworth Press. p. 160. ISBN 0-7890-0374-0. The problem is also known by several other names, including: Ulam's conjecture, the Hailstone problem, the Syracuse problem, Kakutani's problem, Hasse's algorithm, and the Collatz problem.
 Lagarias, Jeffrey C. (1985). "The 3x + 1 problem and its generalizations". The American Mathematical Monthly. 92 (1): 3–23. doi:10.1080/00029890.1985.11971528. JSTOR 2322189.
 According to Lagarias (1985),[3] p. 4, the name "Syracuse problem" was proposed by Hasse in the 1950s, during a visit to Syracuse University.
 Pickover, Clifford A. (2001). Wonders of Numbers. Oxford: Oxford University Press. pp. 116–118. ISBN 0-19-513342-0.
 "Hailstone Number". MathWorld. Wolfram Research.
 Hofstadter, Douglas R. (1979). Gödel, Escher, Bach. New York: Basic Books. pp. 400–2. ISBN 0-465-02685-0.
 Guy, Richard K. (2004). ""E17: Permutation Sequences"". Unsolved problems in number theory (3rd ed.). Springer-Verlag. pp. 336–7. ISBN 0-387-20860-7. Zbl 1058.11001.
 Guy, R. K. (1983). "Don't try to solve these problems". Amer. Math. Monthly. 90 (1): 35–41. doi:10.2307/2975688. JSTOR 2975688. By this Erdos means that there aren't powerful tools for manipulating such objects.
 Lagarias, Jeffrey C., ed. (2010). The Ultimate Challenge: the 3x + 1 problem. American Mathematical Society. ISBN 978-0-8218-4940-8. Zbl 1253.11003.
 Leavens, Gary T.; Vermeulen, Mike (December 1992). "3x + 1 Search Programs". Computers & Mathematics with Applications. 24 (11): 79–99. doi:10.1016/0898-1221(92)90034-F.
 Roosendaal, Eric. "3x+1 Delay Records". Retrieved 14 March 2020. (Note: "Delay records" are total stopping time records.)
 Barina, David (2020). "Convergence verification of the Collatz problem". The Journal of Supercomputing. 77 (3): 2681–2688. doi:10.1007/s11227-020-03368-x. S2CID 220294340.
 Garner, Lynn E. (1981). "On the Collatz 3n + 1 Algorithm". Proceedings of the American Mathematical Society. 82 (1): 19–22. doi:10.1090/S0002-9939-1981-0603593-2. JSTOR 2044308.
 Eliahou, Shalom (1993). "The 3x + 1 problem: new lower bounds on nontrivial cycle lengths". Discrete Mathematics. 118 (1): 45–56. doi:10.1016/0012-365X(93)90052-U.
 Simons, J.; de Weger, B. (2005). "Theoretical and computational bounds for m-cycles of the 3n + 1 problem" (PDF). Acta Arithmetica. 117 (1): 51–70. Bibcode:2005AcAri.117...51S. doi:10.4064/aa117-1-3.
 Lagarias (1985),[3] section "A heuristic argument".
 Terras, Riho (1976). "A stopping time problem on the positive integers" (PDF). Acta Arithmetica. 30 (3): 241–252. doi:10.4064/aa-30-3-241-252. MR 0568274.
 Tao, Terence (10 September 2019). "Almost all Collatz orbits attain almost bounded values". What's new. Retrieved 11 September 2019.
 Hartnett, Kevin. "Mathematician Proves Huge Result on 'Dangerous' Problem". Quanta Magazine. Retrieved 26 December 2019.
 Krasikov, Ilia; Lagarias, Jeffrey C. (2003). "Bounds for the 3x + 1 problem using difference inequalities". Acta Arithmetica. 109 (3): 237–258. arXiv:math/0205002. Bibcode:2003AcAri.109..237K. doi:10.4064/aa109-3-4. MR 1980260. S2CID 18467460.
 Steiner, R. P. (1977). "A theorem on the syracuse problem". Proceedings of the 7th Manitoba Conference on Numerical Mathematics. pp. 553–9. MR 0535032.
 Simons, John L. (2005). "On the nonexistence of 2-cycles for the 3x + 1 problem". Math. Comp. 74: 1565–72. Bibcode:2005MaCom..74.1565S. doi:10.1090/s0025-5718-04-01728-4. MR 2137019.
 Colussi, Livio (9 September 2011). "The convergence classes of Collatz function". Theoretical Computer Science. 412 (39): 5409–5419. doi:10.1016/j.tcs.2011.05.056.
 Hew, Patrick Chisan (7 March 2016). "Working in binary protects the repetends of 1/3h: Comment on Colussi's 'The convergence classes of Collatz function'". Theoretical Computer Science. 618: 135–141. doi:10.1016/j.tcs.2015.12.033.
 Lagarias, Jeffrey (1990). "The set of rational cycles for the 3x+1 problem". Acta Arithmetica. 56 (1): 33–53. doi:10.4064/aa-56-1-33-53. ISSN 0065-1036.
 Belaga, Edward G.; Mignotte, Maurice (1998). "Embedding the 3x+1 Conjecture in a 3x+d Context". Experimental Mathematics. 7 (2): 145–151. doi:10.1080/10586458.1998.10504364.
 Lagarias, Jeffrey C.; Bernstein, Daniel J. (1996). "The 3x + 1 Conjugacy Map". Canadian Journal of Mathematics. 48 (6): 1154–1169. doi:10.4153/CJM-1996-060-x. ISSN 0008-414X.
 Chamberland, Marc (1996). "A continuous extension of the 3x + 1 problem to the real line". Dynam. Contin. Discrete Impuls Systems. 2 (4): 495–509.
 Letherman, Simon; Schleicher, Dierk; Wood, Reg (1999). "The (3n + 1)-Problem and Holomorphic Dynamics". Experimental Mathematics. 8 (3): 241–252. doi:10.1080/10586458.1999.10504402.
 Scollo, Giuseppe (2007). "Looking for Class Records in the 3x + 1 Problem by means of the COMETA Grid Infrastructure" (PDF). Grid Open Days at the University of Palermo.
 Lagarias (1985),[3] Theorem D.
 Conway, John H. (1972). "Unpredictable Iterations". Proc. 1972 Number Theory Conf., Univ. Colorado, Boulder. pp. 49–52.
 Kurtz, Stuart A.; Simon, Janos (2007). "The Undecidability of the Generalized Collatz Problem". In Cai, J.-Y.; Cooper, S. B.; Zhu, H. (eds.). Proceedings of the 4th International Conference on Theory and Applications of Models of Computation, TAMC 2007, held in Shanghai, China in May 2007. pp. 542–553. doi:10.1007/978-3-540-72504-6_49. ISBN 978-3-540-72503-9. As PDF
 Ben-Amram, Amir M. (2015). "Mortality of iterated piecewise affine functions over the integers: Decidability and complexity". Computability. 1 (1): 19–56. doi:10.3233/COM-150032.
 Emmer, Michele (2012). Imagine Math: Between Culture and Mathematics. Springer Publishing. pp. 260–264. ISBN 978-8-847-02426-7.
 Mazmanian, Adam (19 May 2011). "MOVIE REVIEW: 'Incendies'". The Washington Times. Retrieved 7 December 2019.
External links
Keith Matthews' 3x + 1 page: Review of progress, plus various programs.
Distributed computing (BOINC) project that verifies the Collatz conjecture for larger values.
An ongoing distributed computing project by Eric Roosendaal verifies the Collatz conjecture for larger and larger values.
Another ongoing distributed computing project by Tomás Oliveira e Silva continues to verify the Collatz conjecture (with fewer statistics than Eric Roosendaal's page but with further progress made).
Weisstein, Eric W. "Collatz Problem". MathWorld.
Collatz Problem at PlanetMath..
Nochella, Jesse. "Collatz Paths". Wolfram Demonstrations Project.
Mathematicians Are So Close to Cracking This 82-Year-Old Riddle
Eisenbud, David (August 8, 2016). "UNCRACKABLE? The Collatz Conjecture - Numberphile". YouTube.
Eisenbud, David (August 9, 2016). "Collatz Conjecture (extra footage) - Numberphile". YouTube.
"The Simplest Math Problem No One Can Solve". YouTube. Veritasium. July 30, 2021. (featuring Alex Kontorovich [de])
Categories: ConjecturesArithmetic dynamicsInteger sequencesUnsolved problems in number theory
Navigation menu
Not logged in
Talk
Contributions
Create account
Log in
ArticleTalk
ReadMore
Search
Search Wikipedia
Main page
Contents
Current events
Random article
About Wikipedia
Contact us
Donate
Contribute
Help
Learn to edit
Community portal
Recent changes
Upload file
Tools
What links here
Related changes
Special pages
Permanent link
Page information
Cite this page
Wikidata item
Print/export
Download as PDF
Printable version
In other projects
Wikimedia Commons

Languages
Deutsch
Español
Français
한국어
हिन्दी
Italiano
Русский
Tiếng Việt
中文
25 more
Edit links
This page was last edited on 4 August 2021, at 20:06 (UTC).
Text is available under the Creative Commons Attribution-ShareAlike License; additional terms may apply. By using this site, you agree to the Terms of Use and Privacy Policy. Wikipedia® is a registered trademark of the Wikimedia Foundation, Inc., a non-profit organization.
