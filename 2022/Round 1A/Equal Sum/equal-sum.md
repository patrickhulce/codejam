Problem
You are given a set of distinct integers. You need to separate them into two non-empty subsets such that each element belongs to exactly one of them and the sum of all elements of each subset is the same.

An anonymous tip told us that the problem above was unlikely to be solved in polynomial time (or something like that), so we decided to change it. Now you get to decide what half of the integers are!

This is an interactive problem with three phases. In phase 1, you choose N
distinct integers. In phase 2, you are given another N
integers that are distinct from each other and from the ones you chose in phase 1. In phase 3, you have to partition those 2N
integers into two subsets, both of which sum to the same amount. All 2N
integers are to be between 1
and 109
, inclusive, and it is guaranteed that they sum up to an even number.

Input and output
This is an interactive problem. You should make sure you have read the information in the Interactive Problems section of our FAQ.

Initially, your program should read a single line containing an integer, T
, the number of test cases. Then, T
test cases must be processed.

For each test case, your program must first read a line containing a single integer N
. Then, it must output a line containing N
distinct integers A1,A2,…,AN
. Each of these integers must be between 1
and 109
, inclusive. After that, your program must read a line containing N
additional integers B1,B2,…,BN
. Finally, your program must output a line containing between 1
and 2N−1
integers from among A1,A2,…,AN,B1,B2,…,BN
: the ones chosen to be part of the first subset. The integers from A
and B
that you do not output are considered to be part of the other subset.

The next test case starts immediately if there is one. If this was the last test case, the judge will expect no more output and will send no further input to your program. In addition, all T
test cases are always processed, regardless of whether the final output from your program is correct or not.

Note: It can be shown that given the limits for this problem, there exists a sequence A1,A2,…,AN
such that any sequence B1,B2,…,BN
results in a set of 2N
integers that can be separated into two subsets with equal sums.

If the judge receives an invalidly formatted or invalid line (like outputting an unexpected number of integers, or integers out of range, or repeated integers in a line) from your program at any moment, the judge will print a single number −1
and will not print any further output. If your program continues to wait for the judge after receiving a −1
, your program will time out, resulting in a Time Limit Exceeded error. Notice that it is your responsibility to have your program exit in time to receive a Wrong Answer judgment instead of a Time Limit Exceeded error. As usual, if the memory limit is exceeded, or your program gets a runtime error, you will receive the appropriate judgment.

Limits
Time limit: 5 seconds.
Memory limit: 1 GB.
Test Set 1 (Visible Verdict)
1≤T≤100
.
N=100
.
1≤Bi≤109
, for all i
.
Bi≠Aj
, for all i,j
.
Bi≠Bj
, for all i≠j
.
For each test case, the judge will choose the Bi
s such that the sum of all 2N
integers is even.

Testing Tool
You can use this testing tool to test locally or on our platform. To test locally, you will need to run the tool in parallel with your code; you can use our interactive runner for that. For more information, read the instructions in comments in that file, and also check out the Interactive Problems section of the FAQ.

Instructions for the testing tool are included in comments within the tool. We encourage you to add your own test cases. Please be advised that although the testing tool is intended to simulate the judging system, it is NOT the real judging system and might behave differently. If your code passes the testing tool but fails the real judge, please check the Coding section of the FAQ to make sure that you are using the same compiler as us.

Download testing tool

Sample Interaction
Judge
Solution
Number of cases
2
Case 1
3
Judge gives N=3
.
5 1 3
Solution starts with {1,3,5}
.
10 4 9
Judge adds to the set to get {1,3,4,5,9,10}
.
1 10 5
Solution says to use {1,5,10}
for one subset.
This is correct because 1+5+10=16=3+4+9
.
Case 2
3
Judge gives N=3
.
5 2 3
Solution starts with {2,3,5}
.
10 8 12
Judge adds to the set to get {2,3,5,8,10,12}
.
12 8
Solution says to use {8,12}
for one subset.
This is correct because 8+12=20=2+3+5+10
.
In the sample interaction above, the solution gets all cases right and would receive a correct verdict. Notice that the value for N
does not conform to the limits for the Test Set and is used to simplify the example only. Notice that the judge could have given the solution the integers {2,7,100}
for the first case, making it impossible for the solution to find a valid partition into subsets of equal sum.
