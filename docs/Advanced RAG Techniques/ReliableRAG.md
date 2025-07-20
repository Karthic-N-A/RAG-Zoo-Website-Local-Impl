# ReliableRAG

This is reliable RAG
```python title="Reliable RAG" linenums="1"
from rag_src.Complete_RAG_Pipeline import ReliableRAG
from rag_src.llm import OpenAILLM
from rag_src.embedder import OpenAIEmbedder

llm = OpenAILLM(model="gpt-4")
embedder = OpenAIEmbedder(model_name="text-embedding-3-small")
reliable_rag = ReliableRAG(
    llm=llm,
    embeddor=embedder,
    docdir="./documents"
)

response = reliable_rag.run("Explain the principles of quantum entanglement")
print(f"Reliable RAG Response: {response}")
```
