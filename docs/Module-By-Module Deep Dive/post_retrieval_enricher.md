# post_retrieval_enricher

## `DocSummarizer` 

It helps reduce the size and the noise in the retrieved context.

* `__init__`(self, llm)
* enrich(self, docs: List[str]) -> List[str]

## `SelfRerank` 

This class re-ranks the documents using the LLM

* `__init__`(self, llm, top_k: int = 5)
* enrich(self, docs: List[str]) -> List[str]

## `SemanticFilter` 

Filters out documents that are semantically dissimilar to the query using cosine similarity of embeddings.

* `__init__`(self, embedder, query_embedding, threshold: float = 0.75)
* enrich(self, docs: List[str]) -> List[str]
