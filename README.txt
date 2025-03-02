Understand and implement the attention mechanism
1. Attention in transformers
2. Self attention and masked attention

Word Embedding -> Positional Encoding -> Attention

Self Attention -> Similarity Score


In self-attention, each input token (word or subword embedding) is used to compute three different vectors:

Query vector (Q): Represents what the token is looking for.
Key vector (K): Represents the token’s content for matching with queries.
Value vector (V): Represents the actual information to be passed to the next layer.
Each of these vectors is computed using learnable weight matrices:
Q =XW(q) 
K=XW(k) 
V=XW(v) 
where:
W(q), W(k) , W(v) are learnable weight matrices that project the input into query, key, and value spaces.


Self-attention is computed as:

Attention(Q,K,V) = softmax(Q Kt/sqrt(dk)) V

Q Kt - Computes similarity scores between queries and keys.
dk - is the dimension of the key space
softmax - Converts scores into a probability distribution.
V - Weighted sum of values

softmax(similarity score) V - How much influence will each work have on final encoding of a gievn word.

