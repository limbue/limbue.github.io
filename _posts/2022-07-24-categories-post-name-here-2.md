---
title: "[포스팅 예시] 이곳에 제목을 입력하세요"
excerpt: Binary Search
	- In Binary Search, when searching in the segment from $L$ to $R$ the middle position $K=⌊(L+R)/2⌋$ is chosen for comparison. This method continuously halves the size of the search interval
		- For an array of size $N$, this process guarantees completion in $log N$ steps.
	
- Interpolation Search
	- Interpolation Position
	- $$pos(k)=시작인덱스+⌈\frac{값오프셋}{전체값범위길이}​*인덱스간격길이 ⌉$$$$pos(k) = l-1 + ⌈\frac{target(a) - S[l-1]}{S[r+1] - S[l-1]}  * (r - l+1) ⌉$$
	- $$ S[0] = 0, S[1] = 1  $$
 
	- The ratio indicating how far the $target$ is from the lowest value relative to the entire range ($arr[r+1] - arr[l-1]$)
		- $$ \frac{a-S[l-1]}{S[r+1]-S[l-1]}$$
	- Multiplying this ratio by the length of the index interval $r-l+1$ and adding it back to the starting index $l -1$ determines the expected index position where $target$ should be located within the array.
	- Interpolation Search seeks to be even faster than Binary Search. It assumes that the data elements are randomly drawn from a uniform distribution over the interval.
	- Mechanism: 
		- Instead of taking the middle position, Interpolation Search determines the expected position K of the search element A by interpolation based on the relative distance of A within the current bounds $S[l-1]$ and $S[r+1]$.
		- The formula for the interpolated position $K$ (relative to the segment start $l-1$) involves the quotient of the offset of $A$ relative to the lowest element, divided by the total size of the interval, multiplied by the number of indices in the segment $(r-l+1)$.
	- Performance (Uniform Distribution):
		- Average Case: The expected runtime is $O(log log N)$. This function grows very slowly; for example if $N$ is 1 million, $log N ≈20$, while $log log N$ is only slightly more than 4.
		- Worst case: if the data are not uniformly distributed (e.g., clustered at one end), the worst-case time complexity is $Θ(N)$.
			- $O(N)$: "In the worst case, it's no worse than N." (Correct statement)
			- $Θ(N)$: "In the worst case, it's exactly N." (More precise statement)
	- HW #3 - (a)
		- Show that interpolation search on an array of size $n$ has worst case runtime $Ω(n)$.
			- In the worst case, when data is not uniformly distributed but clustered at one end, the runtime is $Θ(n)$.
			- This can be seen as having an upper bound of $O(n)$ and a lower bound of $Ω(n)$.
			- $O(n)$: At most this much time is required. (Upper Bound)
			- $Ω(n)$: Takes at least this much time. (Lower Bound)
            - $Θ(n)$: Takes exactly this much time. (Tight Bound)

categories:
  - Categories2
tags:
  - [tag1, tag2]

permalink: /categories2/post-name-here-2/

toc: true
toc_sticky: true

date: 2022-07-24
last_modified_at: 2022-07-24
---

## 🦥 본문

본문은 여기에 ...

