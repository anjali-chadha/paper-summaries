## [Ex Machina: Personal Attacks Seen at Scale](https://arxiv.org/pdf/1610.08914.pdf)
1. Uses a combination of ML and crowdsourcing to analyze personal attacks
on online platforms
2. Used Wikipedia Dataset
3. Treats the problem as binary text classification problem.
4. Based purely on features extracted from text.
    * Ignores author's past behavious
    * Ignores the discussion context
5. Model architectures explored in the paper:
    * Logistic Regression (LR)
    * Multi-Layer Perceptron (MLP)
6. Used Bag of Words representation based on word or character level n grams.
7. Loss function used - Cross Entropy
8. Character n-grams outperform word n-grams.
      * 
