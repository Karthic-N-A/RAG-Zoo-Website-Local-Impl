# llm/

## `SmartLLM` 

GraphRAG LLM

* `__init__`(self)
* generate(self, query: str, contexts: List[str]) -> str
  
  Lot more functios under this can be seen under graph_Rag_llm.py in llm folder

## `HuggingFaceLLMWrapper` 

HuggingFace LLM

* `__init__`(self, model_name: str = "distilbert")
* generate(self, query: str, contexts: List[str], temperature: float = 0.7) -> str

## `OpenAILLM` 

GPT-3.5-Turbo / GPT-4 / GPT-4o

*  `__init__`(self, model: str = "gpt-4")
* generate(self, query: str, contexts: List[str]) -> Union[str, dict] 

## `GroqLLM` 

Ultra-low latency Mixtral/Gemma 

*  `__init__`(self, api_key: str = None, model: str = "llama3-8b-8192" )
* generate(self, query: str, contexts: List[str]) -> Union[str, dict]

## `OllamaLLM` 

Local Llama 3, Mistral

* `__init__`(self, model: str = "mistral")
* generate(self, query: str, contexts: List[str]) -> Union[str, dict]

## `GeminiLLM` 

Google Gemini Pro / Flash

* `__init__`(self, api_key: str = None, model: str = "gemini-1.5-flash")
* generate(self, query: str, contexts: List[str]) -> Union[str, dict]