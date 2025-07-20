# retriever/

## `FusionRetriever` 

Retrieves and gives a combined set of top documents from multiple retrieval methods or query variants.

* `__init__`(self, retriever: BaseRetriever, top_k: int = 5)
* expand_query(self, query: str) -> List[str]
* retrieve(self, query: str) -> List[Dict[str, Any]]

## `ReRankingRetriever` 

Retrieves and gives top k documents

* `__init__`(self, index_path = "default_index", model_name = "all-MiniLM-L6-v2", reranker_model_name="BAAI/bge-reranker-large",
initial_top_n:int = 20)
* rerank(self, query: str, docs:List[Dict[str, Any]], k:int =5) -> List[Dict[str, Any]]
* retrieve(self, query:str, k:int =5) -> List[Dict[str, Any]]:

## `NeighborhoodContextRetriever` 

Graph-aware context expansion

*  `__init__`(self, base_retriever: BaseRetriever, all_documents: List[Dict[str, Any]], num_neighbors: int = 1, chunk_overlap: int = 20)
* retrieve(self, query: str) -> List[Dict[str, Any]]  

## `ExplainableRetriever` 

Retrieves and gives token-limited text chunks from documents, optionally enriched with metadata.

* `__init__`(self, retriever: BaseRetriever, top_k: int = 5)
* generate_explanation(self, query: str, document: str) -> str
* retrieve(self, query: str) -> List[Dict[str, Any]]

---

# web_retriever/

## `DuckDuckGoWebRetriever` 

Retrieves stuff via DuckDuckGo

* `__init__`(self, max_results: int = 5)
* retrieve(self, query: str) -> List[TextNode]

## `SerpAPIWebRetriever` 

Retrieves stuff via SerpAPI

* `__init__`(self, api_key: str = None, max_results: int = 5)
* retrieve(self, query: str) -> List[TextNode]

## `TavilyWebRetriever` 

Retrieves stuff via TavilyAPI

*  `__init__`(self, api_key: str = None, max_results: int = 5)
* retrieve(self, query: str) -> List[TextNode]

## `HybridWebRetriever` 

Attempts retrieval via a combination of the above three

* `__init__`(
    self, tavily: Optional[BaseWebRetriever] = None, serpapi: Optional[BaseWebRetriever] = None, duckduckgo: Optional[BaseWebRetriever] = None, max_results: int = 5,
)
* _deduplicate(self, nodes: List[TextNode]) -> List[TextNode]
* retrieve(self, query: str) -> List[TextNode]
