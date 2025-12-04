dec 3

This produces N random numbers from a standard normal distribution:
Z∼N(0,1)
Z∼N(0,1)
Why normal distribution?

Because empirical finance discovered:

    daily returns of stocks behave (approximately) normally

    Brownian motion uses normal increments

    randomness in many natural systems follows normal distributions

This goes back to the Central Limit Theorem, meaning that small random influences accumulate into a Gaussian distribution.

dSt​=μSt​dt+σSt​dWt​

Meaning:

If 
Z
Z is positive → stock goes up

If 
Z
Z is negative → stock goes down

Larger 
σ
σ (volatility) → more extreme moves


4 dec

antithetic variates: “Can we design a smarter estimator that has the same expectation but lower variance, without just increasing N?”

this is done by taking the covariance of each calculation and averaging it. 
so by taking Z and -Z, and averaging it, we get a smaller variance that we 
can deal with. 



Figure X compares the standard deviation of the Monte Carlo estimator error for the basic and antithetic methods. Both estimators exhibit the expected 
O(N−1/2)
O(N
−1/2
) convergence, forming approximately straight lines on the log–log scale. However, the antithetic estimator consistently achieves a noticeably lower variance across all sample sizes. This confirms that pairing 
Z
Z with 
−Z
−Z introduces negative covariance that reduces the overall variance of the estimator. In practical terms, antithetic variates achieve the same accuracy as basic Monte Carlo with roughly 2–4 times fewer samples, depending on the region.....