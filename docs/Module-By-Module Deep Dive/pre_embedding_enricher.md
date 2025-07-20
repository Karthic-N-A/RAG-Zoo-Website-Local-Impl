# pre_embedding_enricher/

## `MetadataInjector` 

Adds metadata (like title, author, timestamp) to each document. Metadata is provided as a dictionary indexed by document position

* `__init__`(self, metadata: dict)
* enrich(self, docs: List[str]) -> List[str]

## `QAPairGenerator` 

Converts documents into question–answer pairs using an LLM. Helpful for improving grounding and context awareness

* `__init__`(self, llm)
* enrich(self, docs: List[str]) -> List[str]

## `TopicTagger` 

Uses the LLM to classify each document's topic.Appends the topic as a tag to the beginning of each doc.

* `__init__`(self, llm)
* enrich(self, docs: List[str]) -> List[str]
