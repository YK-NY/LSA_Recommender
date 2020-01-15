# LSA_Recommender
LSA Recommender using TF-IDF
# Author: YK

•	Use the Reuters 10K article corpus raw_text_dataset.pickle (obtained from https://github.com/chrisjmccormick/LSA_Classification)
•	Create a doc2vec(doc, tfidf_vectorizer) function corresponding to a TFIDF vectorizere
	INPUTS: doc, tfidf_vectorizer
o	doc - any string
o	tfidf_vectorizer - a TfidfVectorizer instance
	OUTPUTS: vec, doc_features, doc_counts
o	vec - a vector with 𝐿2 norm of 1
o	doc_features - the features after tokenization and pre-processing
o	doc_counts - the counts of each feature in this document 
	train tfidf_vectorizer on the Reuters 10K article corpus
•	For each of the following doc strings, calculate their corresponding vectors
	doc1: "The cocoa cadabra"
	doc2: "AAPL SE"
	doc3: "bullish stocks"
	doc3: "I walked through a random forest and earned a high premium"
•	Create a recommend(vec, X_model, X_corpus) function:
	which projects any document vector onto a given X_model
o	here X_model = {X_train_tfidf, and X_train_lsa}
	and returns doc_vec, idx_top10, sim_top10, X_top10 as followsmult
o	doc_vec - the (sparse) vector of similarity scores of vec and members of X_model. This vector should be size (Dx1)
o	idx_top10: the indices of the top-10 similarity scores
o	sim_top10: the top-10 similarity scores
o	X_top10: the top-10 corpus articles most similar to the input model

Comment on output of the recommend() function for the doc vectors in the previous exersise.
o	Do you see an improvement of the LSA similarity recommendation relative to the TF-IDF similarity recommendation?
