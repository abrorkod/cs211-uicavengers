- **NetID:** akodi3
- **Major:** CS
- **Question that I chose from the memoization exercise:** Ways to Reach the n'th Stair
- **Link to the question article:** https://www.geeksforgeeks.org/problems/count-ways-to-reach-the-nth-stair-1587115620/1
- **My solution:**


```
int countWays(int n) {
	// Base cases
	if (n <= 1)
		return 1;
	
	int prev2 = 1;
	int prev1 = 1;
	int current = 0;
	
	for (int i = 2; i <= n; i++) {
		current = prev1 + prev2;
		prev2 = prev1;
		prev1 = current;
	}
	
	return current;
}
```