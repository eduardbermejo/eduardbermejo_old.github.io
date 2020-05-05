# Forward algorithm for HMM

In this post, I will be going through the forward algorithm and the usages of this algorithm in Hidden Markov Models.

Our goal is to compute: $p(Z_{k},X_{1:k})$ where $X_{1:k}=(X_{1},...,X_{k})$

We assume we know the emission probability distribution $p(X_{k}\|Z_{k})$ and the transition probability distribution $p(Z_{k}\|Z_{k-1})$

The forward algorithm uses Dynamic Programming ro decrease computational complexity. So the first thing we need to do is to find a way to state that recursion. What we could do is explicitly add the previous hidden random variable back like so:
We know $p(Z_{k},X_{1:k})$ is the marginal distribution over the subset $(Z_{k},X_{1:k})$ and since we know that marginalization is the process of summming the joint distribution over the variable or variables being discarded. So we will make that summation explicit in order to get $Z_{k-1}$ back:

$p(Z_{k},X_{1:k})=ªsum_Z{k-1} p(Z_{k},Z_{k-1},X_{1:k}})$










