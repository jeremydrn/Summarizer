An extractive summarizer that works on a generic input text using unsupervised methods (no pretraining required).
The general idea is to use a semantic vector space to represent each sentence in the text, then use the PageRank algorithm to select those sentences that are most representative of the entire text.
Due to the time-complexity limitations of PageRank, it is not feasible to run over an arbitrarily long book. Other researchers have also noted that long texts tend to shift topics, so multiple windows are beneficial theoretically as well as practically. 
We experimented mainly on various types of vectorization (Bag-of-Words, GLOVE, Word2Vec; in order of effectiveness). Word2Vec (embeddings created over the input text) was most effective, and ran relatively quickly due to the relatively small dimensionality of the semantic vector space.