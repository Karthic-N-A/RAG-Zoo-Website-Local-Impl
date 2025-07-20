# query_transformer/

## `QueryDecomposer` 
- breaks down a complex user query into simpler sub-questions
    * `__init__`(self, llm, verbose: bool = False)
    * transform(self, query: str) -> List[str]

## `HyDe` 
- does HyDE
    * `__init__`(self, llm, include_original: bool = True)
    * transform(self, query: str) -> List[str]

## `MultiQuery` 
- generates multiple reformulated queries from the original input query
    * `__init__`(self, llm)
    * transform(self, query: str, n: int = 5) -> List[str]

## `LLMWebQueryTransformer` 
- transforms a user query into a more web-search-optimized version using an LLM.
    *  `__init__`(self, llm: BaseLLM)
    * transform(self, query: str) -> List[str]
