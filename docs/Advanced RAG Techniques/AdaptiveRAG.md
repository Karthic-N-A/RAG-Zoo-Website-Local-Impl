# AdaptiveRAG

This is Adaptive RAG
```python title="Adaptive RAG" linenums="1"
from rag_src.Complete_RAG_Pipeline import AdaptiveRAG
from rag_src.llm import OpenAILLM
from rag_src.embedder import OpenAIEmbedder
llm = OpenAILLM(model="gpt-4")
embedder = OpenAIEmbedder(model_name="text-embedding-3-small")

adaptive_rag = AdaptiveRAG(
    llm=llm,
    embeddor=embedder,
    docdir="./documents"
)

response = adaptive_rag.run("What are different perspectives on AI ethics?")
print(f"Adaptive RAG Response: {response}")
```