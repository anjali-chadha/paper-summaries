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
        * Character n-grams (3 to 5 characters, including spaces)
        * Token unigrams, bigrams
    * Linguistic
        * Use of prexisting hate lists to explicitly look for inflammatory words
        * Also looking for elements of non-abusive language such as the use of politeness words.
        * Multiple features used -
            * Length of comment, average length of word, number of tokens with non-alpha characters in the middle
            * Number of politeness words
            * Number of unknown words as compared to a dictionary of English words (for meansuring uniqueness and any misspelligng)
            * Number of insult and hate blacklist words
            * Number of modal words (to measure heding and confidence of speaker)
    * Syntactic
    * Distributional Semantics
14. Preprocessing of the data - 
    * normalizing numbers
    * replacing very long unknown words with the same token
    * Replacing repeated punctuation with the same token
