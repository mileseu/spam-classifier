# spam-classifier

This project utilises a supervised learning based classifier to determine whether a given email is spam or ham.  
  
We are given a training set consisting of 1000 emails and 55 columns. The first column is the response variable and describes whether a message is spam 1 or ham 0. The remaining 54 columns are features used to build the classifier. These features correspond to 54 different keywords (such as "money", "free", and "receive") and special characters. A feature has the value 1 if the keyword appears in the message and 0 otherwise.  
  
  
We are going to use an algorithm called Naïve Bayes. Naive Bayes classifiers are a collection of classification algorithms based on Bayes’ Theorem. It is not a single algorithm but a family of algorithms where all of them share a common principle, i.e. every pair of features being classified is independent of each other.  
  
Bayes’ Theorem finds the probability of an event occurring given the probability of another event that has already occurred.  
  
Now, with regards to our dataset, we can apply Bayes’ theorem in following way:  
We can think of a histogram when looking at all the words in an email, using this we can calculate the probability of seeing each word, given it was spam or ham.  
Calculating the probabilities in an example email, we can see the likelihood of whether the message is spam or ham  
The naive assumption to the Bayes’ theorem, is independence among the features, all words orders are treated the same  
A couple tricks we use on implementation is using log probabilities to avoid underflow and laplace smoothing to avoid 0 occurance keywords  


