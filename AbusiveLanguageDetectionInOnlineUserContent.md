## [Abusive Language Detection in Online User Content](http://gdac.uqam.ca/WWW2016-Proceedings/proceedings/p145.pdf)
1. For dete3cting abusive languages, most commercial methods use
    * Blacklists
    * Regular Expressions
2. Anecdotes of Facebook, Robin Williams (Twitter) and online abuse
3. Abusive language is a catch-all term.
    * Detecting profanity
    * Hate Speech towards a particular ethnic group
4. The author's technique beats the deep learning approach
5. Authors introduces a new dataset
6. Why is this task difficult?
    * More than simple keyword spotting. Obfuscation of words
    * Sarcasm
7. Different previous works tackled different aspects of abusive language; define the term differently
; applying it to specific online domains - Twitter or online forumns.
8. Earlier works used n-gram; manually developed regex
9. Using blacklist not always helpful, as some blacklists words might not be abusive in the proper
context.
10. Supervised classfication aprroach - Using SVM with features including n-grams
11. Another approach can be to spell-correct and normalize noisy text before feature extraction.
12. Dataset used - 
    * Comments extracted from YaHoo Finance and News (Yahoo Webscope program)
    * WWW2015 dataset
13. Features used by the authors. Main four classes
    * N-grams  
    * Linguistic
    * Syntactic
    * Distributional Semantics - word2vec, pretrained, comment2vec
14. Preprocessing of the data - 
    * normalizing numbers
    * replacing very long unknown words with the same token
    * Replacing repeated punctuation with the same token
15.  N-grams features
     * Character n-grams (3 to 5 characters, including spaces)
     * Token unigrams, bigrams
16. Linguistic features
     * Use of prexisting hate lists to explicitly look for inflammatory words
     * Also looking for elements of non-abusive language such as the use of politeness words.
     * Multiple features used -
         * Length of comment, average length of word, number of tokens with non-alpha characters in the middle
         * Number of politeness words
         * Number of unknown words as compared to a dictionary of English words (for meansuring uniqueness and any misspelligng)
         * Number of insult and hate blacklist words
         * Number of modal words (to measure heding and confidence of speaker)
17. Syntactic features
      * Use of natural language parsing.
      * Derive features from ClearNLP dependency parser
      * Features-
            * POS tags, dependency relations, 
      * Motivation is to capture long range dependencies between words which n-grams may not be able to do
      * eg *Jews are lower class pigs.*
            * n-grams will fail to detect this as toxic comment
            * Dependency parser would generate a tuple **are-Jews-pigs**
            * where Jews and pigs are children of are.
18. Distributional Semantics Features - Uses three types of embedding-derived features
      * Based on averaging the word embeddings of all words in the comment
      * Nowadays, concept of embeddings has been extended beyond words to a number of text segments,
      including phrases, sentences and paragraphs, entities and documents. 
      * This paper used embeddings of comments
            * Comment2vec
            * While word vectors contribute to predict the next word in comments,
            * comment vectors contribute to predict the next word given many contexts sampled from the comment.
            * Every comment is mapped to a unique vector in a matrix representing comments 
            * And every word is mapped to a unique vector in a matrix representing words.
            * Then comment vectors and word vectors are concatenated to predict the next word in a context.
            * The probablity distirbution of observing a word depends not only on the fixed number of surrounding
            words, but also depends on the specific comment.
            * Represent each comment by a dense low-dimnesional vector which is trained to predict
            words in the comment and overcomes the weaknesses of word embeddings solely.
            * Embeddings trained using skip-bigram model with window size of 10  
19. Measures used -
      * Recall 
      * Precision
      * F-score
      * AUC
