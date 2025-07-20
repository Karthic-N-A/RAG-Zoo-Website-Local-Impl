# CRAG

This is CRAG
```python title="CRAG" linenums="1"
from rag_src.Complete_RAG_Pipeline import CRAG
from rag_src.llm import OpenAILLM
from rag_src.embedder import OpenAIEmbedder
from rag_src.web_retriever import TavilyWebRetriever

llm = OpenAILLM(model="gpt-4")
embedder = OpenAIEmbedder(model_name="text-embedding-3-small")
web_retriever = TavilyWebRetriever(api_key="your_tavily_api_key")
crag = CRAG(
    llm=llm,
    embeddor=embedder,
    web_retriever=web_retriever,
    docdir="./documents"
)
response = crag.run("What are the latest quantum computing breakthroughs in 2024?")
print(f"CRAG Response: {response}")
```