# indexer/

## `ChromaDBIndexer` 

DuckDB-backed, metadata queries

- `__init__`(
    self,
    collection_name: str = "rag_documents",
    persist_directory: str = "./chroma_index"
)
- index(
    self,
    embeddings: List[List[float]],
    documents: List[str],
    metadata: Optional[List[Dict[str, Any]]] = None
) -> None
- reset(self) -> None
- persist(self) -> None

## `WeaviateIndexer` 

Cloud HNSW, schema enforcement

- `__init__`(
    self,
    weaviate_url: str,
    api_key: Optional[str] = None,
    class_name: str = "DocumentChunk",
    recreate_schema: bool = True
)
- index(
    self,
    embeddings: List[List[float]],
    documents: List[str],
    metadata: Optional[List[Dict[str, Any]]] = None
) -> None
- reset(self) -> None
- persist(self) -> None

## `FAISS` is the default indexer