# embedder/

## `OpenAIEmbedder` 
1 536-D or 3 072-D via /v1/embeddings 

- `__init__`(self, model_name: str = "text-embedding-3-small", api_key: str = None)

- embed(
    self,
    texts: List[str],
    mode: Literal["query", "document"] = "document"
) -> List[List[float]]

## `GeminiEmbedder` 
Google GenAI multimodal embeddings

- `__init__`(self, model_name: str = "models/embedding-001", api_key: str = None)

- embed(
    self,
    texts: List[str],
    mode: Literal["query", "document"] = "document"
) -> List[List[float]]
