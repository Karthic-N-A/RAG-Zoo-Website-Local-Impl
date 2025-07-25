# query_transformer/

## `QueryDecomposer` 

- breaks down a complex user query into simpler sub-questions

- Parameters (with default vals and types) for class object:
    ```python
    * llm
    * verbose: bool = False
    ```

- Functions:
    ```py
    * transform(self, query: str) -> List[str]
    ```

## `HyDe` 

- Does HyDE

- Parameters (with default vals and types) for class object:
    ```python
    * llm
    * include_original: bool = True
    ```

- Functions:
    ```py
    * transform(self, query: str) -> List[str]
    ```

## `MultiQuery` 

- generates multiple reformulated queries from the original input query

- Parameters (with default vals and types) for class object:
    ```python
    * llm
    ```

- Functions:
    ```py
    * transform(self, query: str, n: int = 5) -> List[str]
    ```

## `LLMWebQueryTransformer` 

- transforms a user query into a more web-search-optimized version using an LLM.

- Parameters (with default vals and types) for class object:
    ```python
    * llm: BaseLLM
    ```

-  Functions:
    ```py
    * transform(self, query: str) -> List[str]
    ```
