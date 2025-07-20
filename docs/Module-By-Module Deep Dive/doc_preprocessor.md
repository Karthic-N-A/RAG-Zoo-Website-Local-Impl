# doc_preprocessor/

## `AdvancedPreprocessor`

Advanced preprocessor that performs lowercasing, stripping blank space, unicode normalization, HTML tag removal, special character cleanup

- `__init__`(self, remove_stopwords: bool = False, language: str = "english")
- preprocess(self, docs: List[str]) -> List[str]
