# Laplace-smoothing
Laplace smoothing is a way of dealing with the problem of sparse data. Simply put, no matter how extensive the training set used to implement a NLP system, there will be always be legitimate English words that can be thrown at the system that it won't recognize. This creates a large number of zero-probabilities produced by a bare bones bigram (or unigram) probability algorithm.

Laplace smoothing is a simplified technique of cleaning data and shoring up against sparse data or innacurate results from our models. While a regular bigram probability computation will take the count of the number of bigrams in the set over the total occurrences of the target word, count(WORDn-1, WORDn) / count(WORDn-1). With Laplace smoothing, we augment this equation by adding 1 to the numerator to discount the 0 values and adding the total number of word types in the vocabulary (V) to the denominator, count(WORDn-1, WORDn) + 1 / count(WORDn-1) + V.

While somewhat useful, Laplace smoothing is one of the simpler smoothing algorithms and is not known for generating highly accurate results. For an example of better smoothing algorithms, see the Good-Turing smoothing algorithm.
