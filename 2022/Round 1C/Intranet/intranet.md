Problem
Apricot Rules LLC is developing a new simplified networking protocol and wants to show off their routing algorithm. In their design, a network consists of M
machines numbered from 1
to M
, and each pair of machines is connected by a direct link. Each of the links is given a unique integer priority value between 1
and (M×(M−1)/2)
and each machine routes traffic according to those priorities.

Unfortunately, the routing algorithm is too aggressive and will route all traffic from a machine through the highest priority link connected to it. This may make some groups of machines isolated from others.

Formally, we say that a machine m
uses a link ℓ
if (and only if) ℓ
is the highest priority link connected to m
. We also say that a link is active if it is used by at least one of the two machines it connects. Given the link priorities, the original network becomes partitioned into disjoint intranets. Two machines belong to the same intranet if and only if there is some path between them using only active links.

Example with 2 intranets. Active edges are (1, 2) and (3, 4) with weights 6 and 5 respectively. Example with 1 intranet. Active edges are (1, 2), (2, 3), and (3, 4) with weights 6, 5, and 4 respectively.

For example, as seen in the left image above, only the links with priorities 6
and 5
are active. This creates two disjoint intranets. However, in the example on the right, three links are active, which results in one intranet consisting of all 4
machines.

As part of the quality assurance team at Apricot Rules LLC, you are investigating the extent of the problem. You are interested in knowing the probability of there being exactly K
intranets if the priorities are assigned uniformly at random from among the (M×(M−1)/2)!
ways of doing so.

Input
The first line of the input gives the number of test cases, T
. T
test cases follow. Each test case is described in a single line containing two integers M
and K
: the number of machines and the target number of intranets, respectively.

Output
For each test case, output one line containing Case #x
: y
, where x
is the test case number (starting from 1) and y
is the sought probability computed modulo the prime 109+7
(1000000007
), which is defined precisely as follows. Represent the probability as as an irreducible fraction p/q
(with p
and q
being non-negative integers that minimize p+q
). Then, y
must equal p⋅q−1mod109+7
⁠, where q−1
is the modular multiplicative inverse of q
with respect to the modulus 109+7
. It can be shown that under the constraints of this problem, such a number y
always exists and is unique.

Limits
Memory limit: 1 GB.
1≤T≤50
.
1≤K≤M/2
.
Test Set 1 (Visible Verdict)
Time limit: 20 seconds.
2≤M≤50
.
Test Set 2 (Hidden Verdict)
Time limit: 60 seconds.
2≤M≤5×105
.
Sample
Sample Input
save_alt
content_copy
3
5 2
5 1
6 3
Sample Output
save_alt
content_copy
Case #1: 428571432
Case #2: 571428576
Case #3: 47619048
In Sample Case #1, consider the following situation. Let's call M=5
machines 1,2,3,4,5
and denote the link connecting machine a
and machine b
by (a,b)
. Assume that the priorities of links (1,2),(1,3),(1,4),(1,5),(2,3),(2,4),(2,5),(3,4),(3,5),(4,5)
are 9,8,7,6,5,4,3,2,1,10
, respectively. Then machines 1
and 2
use link (1,2)
, machine 3
uses link (1,3)
, and machines 4
and 5
use link (4,5)
. Thus three links (1,2),(1,3),(4,5)
are active, and there are two intranets {1,2,3}
and {4,5}
. Since K=2
, this situation counts the answer.

Intranets sample case #1 example. 5 nodes with active edges (1, 2), (1, 3), and (4, 5) having weights 9, 8, and 10 respectively.

We can find that there are 1555200
ways to assign the priorities to have exactly 2
intranets among 10!=3628800
ways, so the probability is 3/7
.

In Sample Case #2, the probability is 4/7
.

In Sample Case #3, the probability is 1/21
.
