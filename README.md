# csci-shu220-homework-2-solved
**TO GET THIS SOLUTION VISIT:** [CSCI-SHU220 Homework 2 Solved](https://www.ankitcodinghub.com/product/csci-shu220-solved-3/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;133621&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSCI-SHU220 Homework 2  Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
This assignment has in total 70 base points and 10 extra points, and the cap is 70. Bonus questions are indicated using the ⋆ mark.

Please specify the following information before submission:

Problem 1: Packing heavy unit intervals [15 pts]

Suppose we are given a set P = {x1,…,xn} of n points on the x-axis and a positive integer k. We say an interval on the x-axis is k-heavy if it contains at least k points in P. We consider left-open right-closed unit intervals, i.e., intervals of the form I = (a,b] where b − a = 1 (for convenience, below we simply call them unit intervals). Our goal is to find a maximum number of k-heavy unit intervals on the x-axis that are disjoint from each other. For example, if and k = 1, then one optimal solution is I1 = (−1.6,−0.6], I2 = (−0.6,0.4], I3 = (0.5,1.5], which consists of three disjoint k-heavy unit intervals (note that the optimal solution is not necessarily unique). Design a greedy algorithm HeavyInt(n,P,k) to solve this problem, which should output the set of intervals you find. First describe your greedy strategy and prove its correctness. Then implement your algorithm by giving the pseudocode. Your algorithm is supposed to run in O(n) time, assuming the points in P have already been sorted in the left-right order.

Solution. Please write down your solution to Problem 1 here.

Intuition of the algorithm: First, for P = {x1,…,xn}, choose the smallest t1(t1 ≥ k) such that xt1+k−1 − xt1 &lt; 1. Take (xt1+k−1 − 1,xt1+k−1] as I1 = (a1,b1].

Repeat the process for P2 = {xl,…,xn} such that xl is the smallest element in P that is larger than b1. Take t2 ≥ l such that xt2+k−1 − xt2 &lt; 1, then let a2 = max(b1,xt2+k−1 − 1), I2 = (a2,a2 + 1]. Note we are choosing the smallest non-conflicting interval with this strategy.

Repeat until for some Pc+1 that we can no longer find tc+1 such that xtc+k−1 − xtc &lt; 1. Then the total number of intervals is c.

Proof of correctness: . Assume the intervals chosen by this greedy algorithm are Ig1,Ig2,…,Igc, we want to show for any j ∈ {0,1,…,c}, ∃ an optimal solution that contains Ig1,…,Igj.

When j = 0, an optimal solution doesn’t have to contain any intervals among Ig1,…,Igc, so this statement is true. Now, assume for some j, ∃ an optimal solution that contains Ig1,…,Igj. Assume the j + 1th chosen interval in this optimal solution is Ix, if we replace Ix with Igj+1, by definition, Igj+1 is the interval with the smallest right end after choosing Ig1,…,Igj, hence the right end of Igj+1 is smaller than that of Ix. In other words, replacing Ix with Igj+1 doesn’t interfere the selection of the subsequent intervals. The modified solution is still optimal.

By induction, when j = c, ∃ an optimal solution that contains Ig1,…,Igc. By definition, after making this selection, we can no longer choose another interval, hence this optimal solutions is {Ig1,…,Igc}, and the greedy algorithm is optimal. Python implementation:

def HeavyInt(n, P, k ): t = 0

intervals = [ ] while t + k − 1 &lt; n:

while t + k − 1 &lt; n and P[ t + k − 1] − P[ t ] &gt;= 1:

t += 1

if t + k − 1 &lt; n: if len( intervals ) &gt; 0:

l e f t = max( intervals [ −1][1] , P[ t + k − 1] − 1) else :

l e f t = P[ t + k − 1] − 1

intervals . append (( left , l e f t + 1))

while t + k − 1 &lt; n and P[ t ] &lt;= intervals [ −1][1]:

t += 1

return intervals

Problem 2: Sorting with arbitrary swaps [10+10+10⋆ pts]

Given an array A[1…n] of distinct numbers, we want to sort it in increasing order. However, we are only allowed to change A by swapping two elements (not necessarily) in A. Specifically, we are provided an oracle Swap. If we call Swap(i,j), then A[i] and A[j] will be swapped in A.

(a) Design a simple algorithm that sorts A by calling the Swap oracle at most n − 1 times. Describe the basic idea and give the pseudocode, and analyze the number of oracle calls. Your algorithm is supposed to run in O(nlogn) time (and call Swap at most n − 1 times), assuming each oracle call takes O(1) time.

(b) Next, we consider the problem of sorting A using minimum number of calls of the Swap oracle. Prof. Greed gives the following greedy algorithm for this problem. Let #Inv(A) denote the number of inversions in A. The algorithm simply repeats the following step until A is sorted: find indices i,j ∈ {1,…,n} such that swapping A[i] and A[j] makes #Inv(A) decrease the most, and then call Swap(i,j). Give a counterexample for which this algorithm fails to give an optimal solution (and briefly argue why it is a counterexample). To get the full credit, your example should make the algorithm fail no matter how it breaks the ties.

(c⋆) Design an algorithm that sorts A using minimum number of Swap calls. Describe the basic idea and give the pseudocode. Prove the correctness of your algorithm (i.e., it successfully sorts A and the number of Swap calls used is minimum). Your algorithm is supposed to run in O(n2) time or faster.

Solution. Please write down your solution to Problem 2 here.

(a) Basic idea: We first use a quick-sort-like algorithm to obtain the rank of each element in A, which takes O(nlogn) time; then we make at most n − 1 swaps to directly put each element in its correct position, which takes O(n) time.

Pseudocode:

def simpleSort (n, A):

rank = {} def SWAP( i , j ):

A[ i ] , A[ j ] = A[ j ] , A[ i ] def indexer (A, add , rank ):

if len(A) == 0: return

pivot = random . choice (A) L = [ ]

R = [ ] for each in A:

if each &lt; pivot :

L. append( each ) elif each &gt; pivot :

R. append( each ) rank [ pivot ] = add + len(L)

indexer (L, add , rank) indexer (R, add + len(L) + 1 , rank)

indexer (A, 0 , rank)

def swapSort(n, A):

swap cnt = 0 for i in range(n − 1):

while i != rank [A[ i ] ] : swap( i , rank [A[ i ] ] )

swap cnt += 1

print( swap cnt )

swapSort(n, A)

Analysis of number of oracle calls: After obtaining the rank of all of the elements, for each swap, we put at least 1 element in place and will never put one element was already in place out of place. Therefore, in at most n − 1 swaps, we will put n − 1 elements in place, so the remaining one element will also be in place. In other words, all n elements will be in place after n − 1 calls, so the number of times we call oracle swap is at most n − 1.

(b) A counter example: A = [6,5,1,3,2,4].

Illustration: Assume ∃i &lt; j such that A[i] &gt; A[j], if we swap A[i] and A[j], the decrease of #Inv is equal to 1 + |{k|i &lt; k &lt; j,A[j] &lt; A[k] &lt; A[i]}|. Therefore, in order to make #Inv decrease the most, we should swap 6 and 2 in the first place (#Inv decreases by 3). However, sorting the swapped array A′ = [2,5,1,3,6,4] takes at least 5 swaps, so in total it takes 6 swaps to sort this array with the greedy algorithm.

Alternatively, this array can be sorted by swapping 2 and 5 in the first place(#Inv decreases by 2), and sorting the swapped array A′ = [6,2,1,3,5,4] takes only 3 steps ([6,2,1,3,5,4] → [1,2,6,3,5,4] → [1,2,3,6,5,4] → [1,2,3,4,5,6]), so in total it only takes 4 swaps to sort this array. Therefore, in this case, the greedy algorithm is not optimal.

(c) We apply exactly the same algorithm in 2(a) and show it’s optimal in terms of # swaps.

Analysis of minimum number of swaps: We define a ”cycle” as follows: Ci = {Ai1,…,Aiki}, idx(a) as the actual index of a in A, rank(a) as the rank of a in A, then rank(Ai1) = idx(Ai2),…, rank(Aiki−1) = idx(Aiki),rank(Aiki) = idx(Ai1). Any unsorted array A can be decomposed into several cycles. Any swap between the elements in two cycles is meaningless because it will not put any element in place or increase the number of cycles. Therefore, the number of swaps needed to sort A is equal to the sum of the number of swaps needed to sort each cycle.

Next, we prove by induction that in order to sort a cycle with |Ci| = ki, we need to perform at least ki − 1 swaps. For ki = 2, we have Ci = {Ai1,Ai2}, where rank(Ai1) = idx(Ai2),rank(Ai2) = idx(Ai1), we only need to swap Ai1 and Ai2. Hence we need to make 1 = 2 − 1 swap to sort this cycle.

Assume for |Ci| = k, we need to make k − 1 swaps to make the cycle sorted. For |Ci| = k + 1, any swap within the array will only put at most 1 element in place. Consider making a swap that puts one element in place (swap Aij and Aij+1), now we have idx(Aij) = rank(Aij), and rank(Aij−1) = idx(Aij+1),rank(Aij+1) = idx(Aij+2). In other words, we obtained an element in place and a new cycle Ci′ with |Ci′| = k, which takes at least k − 1 swaps to sort. Hence |Ci| takes at least k steps to sort.

Finally, we prove that our algorithm obtains this optimal solution. For each i, our algorithm keeps swapping A[i] and A[rank(Ai)] if i ̸= rank(A[i]). This is equivalent to swap Aij and Aij+1 where

Aij,Aij+1 ∈ C, rank(Aij) = idx(Aij+1) Consequently, we have Aij+1 at place i and rank(Aij+1) = idx(Aij+2) and rank(Aij−1) = idx(Aij+1). Therefore, when at last i = rank(A[i]), we finish sorting a cycle C with |C| − 1 swaps. For any sorted cycle C, we have i = rank(Ai) for all Ai ∈ C and will not swap at all. Therefore, this algorithm sorts A with only ΣC(|C|−1) = n−#cycles swaps, which is optimal.

Pseudocode: See 2(a).

Problem 3: Longest doubling subsequence [15 pts]

Recall that an array (or sequence) A of real numbers is doubling if A[i] ≥ 2A[i − 1] for all i ≥ 2 (thus any array of length 1 is doubling). Given an array A, we want to find a longest subsequence of A that is doubling. For example, if A = [7,1,3,8,2,4,5,6,9], then a longest doubling subsequence of A is be [1,2,4,9], which is of length 4. Design an algorithm LDS(n,A) that returns a longest doubling subsequence A′ of the array A (where n is the size of A). Describe the basic idea of your algorithm and give the pseudocode. Briefly justify its correctness and analyze its time complexity. Your algorithm should run in O(n2) time or faster.

Solution. Please write down your solution to Problem 3 here.

Intuition of algorithm: We define the maximum length of a subsequence ending at Ai as Li. Pi =

{i1,…,ik} such that ∀j ∈ Pi,j &lt; i,2Aj ≤ Ai. Let Li = maxj∈Pi(Lj) + 1, previ = argminj∈Pi(Lj). After we obtain all Li for ∀i ∈ {1,2,…,n}, we say that the maximal length of any LDS is maxi∈{1,…,n}Li, and the corresponding LDS is obtained by checking previ recursively.

Pseudocode:

def LDS(n, A):

length = [ ]

last = [ ]

length . append(1) last . append(None)

for i in range(1 , n ): max len = 0

tmp = None for j in range(0 , i ):

if length [ j ] &gt; max len and A[ i ] &gt;= 2 ∗ A[ j ] :

max len = length [ j ]

tmp = j length . append(max len + 1)

last . append(tmp)

tail = length . index (max( length ))

res = [ ]

while tail != None: res . append(A[ tail ])

tail = last [ tail ]

return res [:: −1]

Proof of correctness: Assume an optimal solution ending at Ai contains {Ai1,…,Aj,Ai}, then {Ai1,…,Aj} is an optimal solution that ends at Aj. Therefore, in order to obtain the optimal solution that ends at Ai, we only need to retrieve the best solution among the optimal solutions at ends at Ai1,…,Aik, where ∀j ∈ {i1,…,ik},j &lt; i,2Aj ≤ Ai.

Time complexity analysis: For any i, we need to check j = 1,…,i − 1 to see if 2Aj ≤ Ai and the optimal solution that ends at Aj. For each j, the checking time is O(1); for j = 1,…,i − 1, the total time is O(n); for i = 1,2,…,n, the total time is O(n2). Hence the time complexity of this algorithm is O(n2).

Problem 4: Removing the numbers optimally [20 pts]

Given a sequence of (positive) numbers, we want to remove the numbers from the sequence one by one. When removing one number x, we gain a score equal to l2xr2 where l is the number to the left of x in the current sequence (l = 1 if x is the leftmost number in the current sequence) and r is the number to the right of x in the current sequence (r = 1 if x is the rightmost number in the current sequence). For example, suppose the given sequence is (2,9,12,3). If we remove 12 first, the score we gain is 92 × 12 × 32 = 8748, and the sequence becomes (2,9,3). Now if we remove 9 from the sequence, then the score is 22 × 9 × 32 = 324, and the sequence becomes (2,3). Next if we remove 3, then the score is 22 × 3 × 12 = 12, and the sequence becomes (2). Finally we remove 2, and the score is 12 × 2 × 12 = 2. The total score we gain is 8748 + 324 + 12 + 2 = 9086. Our goal is to find an order to remove the numbers from the given sequence such that the total score we gain is maximized. Formally, design an algorithm Remove(n,A) where A is an array of n positive numbers; the algorithm returns the maximum total score we can gain if the given sequence is A (for convenience, you are not required to return the optimal order for removing the numbers). Describe the basic idea of your algorithm and give the pseudocode. Briefly justify its correctness and analyze its time complexity. Your algorithm should run in O(n3) time or faster.

Solution. Please write down your solution to Problem 4 here.

Idea of the algorithm: In the first place, we augment the array A to a new array B, B =

(1,A1,…,An,1) = (B1,B2,…,Bn+1,Bn+2). We need to remove B2,…,Bn+1, and the score obtained by removing Bj is equal to Bj2−1 · Bj · Bj2+1 for any j ∈ {2,…,n + 1}.

Now, let 1 ≤ l &lt; r ≤ n + 2. Consider the optimal score obtained after removing all elements in

{Bl+1,…,Br−1} f(l,r). Suppose the last element we remove from {Bl+1,…,Br−1} is Bk where l &lt; k &lt; r, then the optimal score can be represented as:

f(l,r) = maxk{f(l,k) + f(k,r) + Bl2 · Bk · Br2}

The boundary case is that if r − l = 2, f(l,r) = Bl2 · Bl+1 · Br2.

Pseudocode:

def Remove(n, A):

memory = {} def helper (B, l , r ):

if memory. get (( l , r ) , 0) &gt; 0:

return memory[( l , r )] if r − l == 2:

return B[ l ] ∗∗ 2 ∗ B[ l + 1] ∗ B[ r ] ∗∗ 2

maxn = 0

for i in range( l + 1 , r ):

tmp = helper (B, l , i ) + helper (B, i , r ) + B[ l ] ∗∗ 2 ∗ B[ i ] ∗ B[ r ] ∗∗ 2

if tmp &gt; maxn: maxn = tmp memory[( l , r )] = maxn

return maxn

B = [1] + A + [1]

helper (B, 0 , n + 1) return memory[(0 , n + 1)]

Justification of correctness: We prove by induction that this algorithm gives the optimal result. When n = 1, f(1,3) = B2 = A1, this algorithm gives the best result.

Assume when n = 1,2,…,k, this algorithm gives the optimal result. When n = k + 1, we know in A = {A1,…,Ak+1}, we must choose one element Aj to remove at the last, and the score obtained is equivalent to the score obtained by removing A1,…,Aj−1(denote as L) + the score by removing Aj+1,…,An(denote as R)+Aj, where the first part and the second part are independent of each other, and Aj is not dependent on L and R(but L and R are dependent on Aj). Therefore, max(L,R,Aj){L + R + Aj} = maxAj{maxAj{L} + maxAj{R} + Aj}, where by our assumption, maxAj{L} and maxAj{R} can be obtained by our algorithm. Therefore when n = k+1, the global optimal can also be obtained by this algorithm. By induction, this algorithm works for ∀n ∈ N∗.

Analysis of time complexity: In this algorithm, we need to traverse all the possible l,r,k without redundancy, where l &lt; r &lt; k. The number of all possible combinations (l,k,r) is equal to

). The time complexity for each combination is O(1), hence the time

complexity is O(n3).
