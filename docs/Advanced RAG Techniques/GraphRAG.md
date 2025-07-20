# GraphRAG

This is GraphRAG
```python title="GraphRAG" linenums="1"
from rag_src.Complete_RAG_Pipeline import GraphRAG
from rag_src.llm import SmartLLM
from rag_src.embedder import OpenAIEmbedder

llm = SmartLLM()
embedder = OpenAIEmbedder(model_name="text-embedding-3-small")
graph_rag = GraphRAG(
    llm=llm,
    embedder=embedder,
    docdir="./documents"
)
response = graph_rag.run("What is the relationship between quantum computing and cryptography?")
print(f"Graph RAG Response: {response}")

graph_rag.visualize_graph(output_file="knowledge_graph.html")
```
