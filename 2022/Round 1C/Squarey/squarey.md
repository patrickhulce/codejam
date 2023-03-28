Problem
Addition and squaring do not commute. That is, the square of the sum of all elements of a list of integers is not necessarily equal to the sum of the squares of those same elements. However, this is true for some lists; one example is [3,−2,6]
, because (3+(−2)+6)2=49=32+(−2)2+62
. Let us call these lists squary.

Image showing that (3 + (-2) + 6)^2 = 3^2 + (-2)^2 + 6^2.

Given a (not necessarily squary) list of relatively small integers, we want to know whether it is possible to add at least 1
and at most K
more elements such that the final list is squary. Each added element must be an integer between −1018
and 1018
, inclusive, and these do not have to be distinct from each other or from the initial list's elements.

Input
The first line of the input gives the number of test cases, T
. T
test cases follow. Each test case is described in two lines. The first line contains two integers N
and K
, the number of elements of the initial list and the maximum number of elements you may add, respectively. The second line contains N
integers E1,E2,…,EN
, representing the N
elements of the initial list.

Output
For each test case, output one line containing Case #x
: y
, where x
is the test case number (starting from 1). If it is possible to add at least 1
and at most K
elements (each an integer between −1018
and 1018
, inclusive) to the initial list such that the square of the sum of its elements equals the sum of the squares of its elements, y
should be z1 z2 … zr
, where 1≤r≤K
and the zi
values are the additional elements. If there is no way to accomplish this, y
should be IMPOSSIBLE.

Limits
Memory limit: 1 GB.
1≤T≤100
.
1≤N≤1000
.
−1000≤Ei≤1000
, for all i
.
Test Set 1 (Visible Verdict)
Time limit: 5 seconds.
K=1
.

Test Set 2 (Visible Verdict)
Time limit: 10 seconds.
2≤K≤1000
.

Sample
Note: there are additional samples that are not run on submissions down below.
Sample Input
save_alt
content_copy
4
2 1
-2 6
2 1
-10 10
1 1
0
3 1
2 -2 2
Sample Output
save_alt
content_copy
Case #1: 3
Case #2: IMPOSSIBLE
Case #3: -1000000000000000000
Case #4: 2
In Sample Case #1, we can end up with the example list given in the problem statement.

In Sample Case #2, we have to add exactly one element. If we call that element x
, the sum of the entire list is x
and its square is x2
. The sum of the squares of all elements, on the other hand, is x2+102+(−10)2=x2+200≠x2
, so the case is impossible.

In Sample Case #3, any integer in the [−1018,1018]
range is a valid answer.

In Sample Case #4, notice that the input might contain duplicate elements, and that it is valid to create even more duplicates with the elements you choose to add.

Additional Sample - Test Set 2
The following additional sample fits the limits of Test Set 2. It will not be run against your submitted solutions.
Sample Input
save_alt
content_copy
3
3 10
-2 3 6
6 2
-2 2 1 -2 4 -1
1 12
-5
Sample Output
save_alt
content_copy
Case #1: 0
Case #2: -1 15
Case #3: 1 1 1 1 1 1 1 1 1 1 1
In Case #1 of the additional samples, we are given the example list from the problem statement, which is already squary, but we need to add at least one element to it. Adding a 0
keeps the list squary.

In Case #3 of the additional samples, we present one of multiple possible valid answers. Notice that it is permissible to add fewer than K
elements; here K
is 12
but we have only added 11
elements.
