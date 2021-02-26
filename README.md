# Sonnet-by-Machine-Learning
In this project,  we're going to train an n-gram language model that is able to "imitate" William Shakespeare's writing.

As the first step towards imitating Shakespeare's writing, you will create a function called load_data that loads his original Sonnets from ../gutenberg/THE_SONNETS.txt. This function should accomplish the following:
  1) Extract sentences from the data file.
  2) Tokenise each extracted sentence. 

Next, we need a "vocabulary" that contains all the unique tokens. Moreover, we often pad a sentence with '<s>' and '</s>' to indicate its start and end when working with n-gram language models; therefore, these two special tokens should also be included in our vocabulary.

Then, let's write a function to generate all  𝑛 -grams for each sentence. This can be accomplished in two steps:
  1) Pad each sentence with '<s>' and '</s>' for  𝑛≥2 . 
  2) Generate  𝑛 -grams on the padded sentences.

Assume we are now working with bi-grams. a bi-gram language model is essentially a first-order Markov Chain.

Now we are well positioned to start training an  𝑛 -gram language model. We can fit a language model using the MLE class from nltk.lm. It requires two inputs: a list of all  𝑛 -grams for each sentence and a vocabulary, both of which you have already written a function to build. Now it's time to put them together to work.

It'd be interesting to see how the "authenticity" of the sonnets is related to the parameter  𝑛 .
