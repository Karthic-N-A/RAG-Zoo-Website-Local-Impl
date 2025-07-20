# evaluator/

## `RelevanceEvaluator` 

Evaluates how relevant the generated response is to the original query using the provided contexts.

- `__init__`(self, llm: BaseLLM, threshold: float = 0.7)

- evaluate(
    self,
    query: str,
    response: str,
    contexts: List[str]
) -> Dict[str, Any]

## `SegmentAttributor` 

Identifies exact segments from documents that support the generated answer

-  `__init__`(self, llm)

- locate_segments(
    self,
    query: str,
    response: str,
    docs: List[TextNode]
) -> List[Dict[str, Any]]

-  evaluate(
    self,
    query: str,
    response: str,
    contexts: List[str]
) -> Dict[str, Any]
