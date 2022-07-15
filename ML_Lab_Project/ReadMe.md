# Auto-Correct-System


### PROBLEM STATEMENT:
To make a simple auto-correct system by using NLP principles and methods.



### INTRODUCTION:
Almost everyone in this digital age carries a smartphone, it can be an Android or iOS device. Autocorrect uses natural language processing as its foundation (NLP). It is designed to fix spelling and other text-entry errors. On our smartphones, we commonly utilise autocorrect models when messaging on sites like Facebook Messenger, WhatsApp, and others. This project would be merely a Natural Language Processing application on a smaller dataset—Shakespeare.txt—and is undoubtedly not an identical replica of the smartphone we currently use.


### STEPS FOR BUILIDING AN AUTO-CORRECT MODEL:
Building an autocorrect model that corrects spelling mistakes involves the following 4 steps:

**Step 1:** Identify the misspelled word \
If a word in the text cannot be located in the dictionary, it is flagged as misspelt by the autocorrect system and needs to be corrected.


**Step 2:** Find strings that are n edit changes away \
Editing is the process of changing a string to another one.
The n denotes the edit distance, which maintains track of how many edit operations need to be performed, such 1, 2, 3, and so on. For autocorrect systems, n is usually between 1 and 3 edits.\
In other words, the edit distance is the total number of procedures that were used to modify a word. The edit operations include:
1. Splitting the words into 2 or more components: here we will use a function and it will return a tuple. Here we will be using list comprehension.
2. Delete: here we will remove a letter from the above split words.
3. Swap: here we will swap the 2 adjacent letters.
4. replace: changes one letter to another. We need letters in english so we will use ASCII.
5. insert: add a letter


**Step 3:** Filter Candidates \
We only take into account correctly spelled words from the generated candidate list so that we may contrast them with terms in the library and exclude words that don't exist. edits. 


**Step 4:** Compute the probabilities for the suggestions\
Based on the following formula, the probabilities of the words are determined: $$P(w) = \frac{C(w)}{V},$$ where 
1. P(w)- the probability of a word w.
2. C(w) - number of times (frequency) word appears in the vocabulary dictionary.
3. V - the total sum of words in the dictionary.\

The real list of words is categorised by the term that was formed as the candidate with the highest probability when the probabilities are calculated.


### LIBRARIES USED:
1. Regular expression (re)
2. Numpy (np)
3. String
4. Collections


### CONCLUSIONS:
NLP is essential for giving computers the ability to comprehend and process natural human language. This is how the autocorrect mechanism has been put into practice above.



### REFERENCES:
1. https://thecleverprogrammer.com/2020/10/04/autocorrect-with-python/
2. https://www.analyticsvidhya.com/blog/2021/11/autocorrect-feature-using-nlp-in-python/

