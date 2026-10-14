# Profile: [Your Full Name]

- **NetID:** ayass6@uic.edu
- **Major:** Computer Science
- **Question that I chose from the memoization exercise:** [Type the 
Question as listed on the Website]
- **Link to the question article:** 
[https://www.geeksforgeeks.org/problems/count-ways-to-reach-the-nth-stair-1587115620/1]
- **My solution:** */ int countWays(int n) {
    // Base cases
    if (n <= 1) return 1;
    if (n == 2) return 2;

    int prev2 = 1; // ways(1)
    int prev1 = 2; // ways(2)
    int current = 0;

    for (int i = 3; i <= n; ++i) {
        current = prev1 + prev2;
        prev2 = prev1;
        prev1 = current;
    }

    return prev1;
} */
\```

Paste your C code here. It should contain the comments you added when 
trying to solve.

\```

int countWays(int n) {
    // Base cases
    if (n <= 1) return 1;
    if (n == 2) return 2;

    int prev2 = 1; // ways(1)
    int prev1 = 2; // ways(2)
    int current = 0;

    for (int i = 3; i <= n; ++i) {
        current = prev1 + prev2;
        prev2 = prev1;
        prev1 = current;
    }

    return prev1;
}
