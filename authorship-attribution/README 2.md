# Authorship attribution tutorial

This tutorial shows a possible application of the Naive Bayes algorithm for authorship attribution. The system is first trained on five texts by four different authors (J. Austen, R. Kipling, L. Carroll and K. Grahame) and is then asked to recognise the authorship of two additional works (i.e., Jane Austen's "Emma" and Rudyard Kipling's "Kim").


## Requirements

For the first part, only the docopt package is needed to run the code from the terminal. Here is the command to install it on the system:

    sudo pip3 install docopt-ng

For the second part, the nltk library is required to download the list of English stopwords. To install it on the system, do:

    sudo pip install -U nltk


## Run the code

Experiment 1-> YES Stopwords 

For Kipling's "Kim":

    python3 attribution.py --words data/Kim.txt

   or alternatively

    python3 attribution.py --chars 3 data/Kim.txt


For Austen's "Emma":

    python3 attribution.py --words data/emma.txt

   or alternatively

    python3 attribution.py --chars 3 data/emma.txt


Experiment 2->NO stopwords

For Kipling's "Kim":

    python3 attribution2.py --words data/Kim.txt

   or alternatively

    python3 attribution2.py --chars 3 data/Kim.txt


For Austen's "Emma":

    python3 attribution2.py --words data/emma.txt

   or alternatively

    python3 attribution2.py --chars 3 data/emma.txt


Within each pair, the first alternative computes a model over words, whereas the second uses character ngrams of the size given to the system.


The output of the code shows the operations the classifier is currently performing: 
-computing prior probabilities
-calculating conditional probabilities
-returning the best 10 features with highest conditional probability for the class under consideration (i.e., the most distinctive features for each author). This gives an idea of which words / ngrams are most important for each author
-getting sorted log figures for the probability of each class. The first entry in that list is the author guessed by the system.



