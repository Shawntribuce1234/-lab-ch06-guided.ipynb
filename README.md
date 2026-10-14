Sampling for Machine Learning — Train-Test Splits
Objective
The goal of this lab was to understand how different sampling methods affect machine learning results, how data leakage happens, and why having more data doesn't always mean better accuracy.
Methodology
- Explored the Titanic dataset containing 891 passengers, using survival as the target variable.
- Compared naive and stratified train-test splits to see how each affected the distribution of survivors.
- Used StandardScaler and SimpleImputer to identify and fix data leakage by fitting only on the training data.
- Created a function called split_by_share() to split datasets using a test percentage and random seed.
- Simulated the 1936 Literary Digest polling failure using a population of 10 million voters.
- Calculated Meng's data defect correlation to measure how sampling bias affects accuracy.
- Ran 100 simulations comparing biased sampling with random sampling.
Key Findings
- Stratified sampling: I found that stratified splitting kept survival rates nearly identical between training and testing sets, while naive splitting produced larger differences.
- Data leakage: I learned that using information from the test set during preprocessing can make a model's performance look better than it actually is.
- Sampling bias: The Literary Digest simulation showed that a large biased sample could produce less accurate results than a random sample of 50,000 people.
- Data defect correlation: I found that even a small relationship between someone's likelihood of being sampled and their voting preference could lead to inaccurate estimates.
- Sample size vs. sampling method: My biggest takeaway was that collecting more data doesn't automatically improve accuracy. How the data is collected matters just as much, and sometimes even more.
Conclusion
This lab helped me understand why sampling is important in machine learning. I learned that even with millions of observations, biased data can still lead to inaccurate conclusions. I also learned why it's important to split data before preprocessing so the model doesn't accidentally learn from the test set. Overall, the biggest lesson was that a smaller, well-selected sample can be more useful than a much larger biased one.
