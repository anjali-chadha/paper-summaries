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
8. Character n-grams outperform word n-grams. Why?
      * Higher robustness to spelling variation of char-n -grams, especially common in expletives
9. Choosing a threshold score for indicating an attack\
      * Pick a point that strikes a balance between precision and recall on evaluation data
10. Comments analysed of registered users and anonymised users.
      * Does mask of anonymity makes people more aggressive(toxic)?
      * As per the study, anonymous contributions are more likely to be an attack
      * However, overall they contribute less than half of attacks.
11. Attacks variation with the quantity of a user's contribution?
      * User's activity level - comments made on the platform.
      * Almost half of all attacks are made by users with an activity level below 5.
      
      
      
