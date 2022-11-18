# 나중에 노트로 싹 정리 코드까지

# Tokenize
- preprocessing
  - re
## SpaCy
- tokenizer
- stop words
- lemmatization
## NLTK
- stemming

# Count base Representation
- BoW
## CountVectorizer
## Tfidf
### Similarity
cosine, knn

# Distributed Representation
- Onehot Encoding
- Embedding

## Word2Vec (using gensim)
- CBoW
- Skip gram

### Keras
- Embedding layer with pretrained Word2Vec(gensim) model
tokenize fit_on_texts -> texts_to_sequences -> pad_sequences -> model
pretrained Word2Vec model -> embedding_matrix -> Embedding_layer
