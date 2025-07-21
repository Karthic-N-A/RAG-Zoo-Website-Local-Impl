# chunker/

## `RecursiveChunker` 

Hierarchical separators, overlap preserved  

- `__init__`(self, chunk_size: int = 512, chunk_overlap: int = 50)

- chunk(
    self,
    docs: List[str],
    metadata: Optional[List[Dict[str, str]]] = None
) -> List[str]

## `SemanticChunker`

Sentence-transformer similarity boundaries

- `__init__`(self, chunk_size: int = 512, chunk_overlap: int = 50)

- chunk(
    self,
    docs: List[str],
    metadata: Optional[List[Dict[str, str]]] = None
) -> List[str]

## `TokenChunker` 

Divides input texts into chunks with configurable overlaps

- `__init__`(self, chunk_size: int = 512, chunk_overlap: int = 50)

- chunk(self, docs: List[str], metadata: Optional[List[Dict[str, str]]] = None) -> List[str]
