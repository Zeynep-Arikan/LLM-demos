# 📚Project Description 
This project demonstrates how to build a simple yet powerful text retrieval system that allows users to ask questions and receive answers based on the content of a local text file.
It combines OpenAI embeddings for semantic understanding of text, FAISS for fast similarity-based search, and LangChain for chaining together document loading, chunking, vectorization, and retrieval into a cohesive pipeline.

## 🔍 What is OpenAI Embeddings?
Embeddings are numerical representations of text — they convert words, phrases, or entire documents into fixed-length vectors (arrays of numbers) that capture the semantic meaning of the input.
Machines don’t understand text the way humans do. To compare, search, or retrieve similar content, text must be converted into something a model can mathematically work with — that’s where embeddings come in.
<pre>
from langchain_openai import OpenAIEmbeddings

embedding_model = OpenAIEmbeddings(model="text-embedding-ada-002")
embedding = embedding_model.embed_query("What is artificial intelligence?")

</pre>

## 🔍 What is FAISS?
**FAISS (Facebook AI Similarity Search)** is an open-source library developed by Facebook AI Research. It allows for efficient **similarity search** over high-dimensional vectors. Faiss is a library for efficient similarity search and clustering of dense vectors.

Langchainjs supports using Faiss as a vectorstore that can be saved to file. It also provides the ability to read the saved file from Python's implementation.

## 🧰 Technologies Used

| Tool      | Purpose                                      |
|-----------|----------------------------------------------|
| LangChain | For orchestration and pipelines              |
| FAISS     | Vector storage and similarity search         |
| OpenAI    | Text embeddings (`text-embedding-ada-002`)   |
| Python    | Project language                             |


## 🔗 REFERENCES
- https://js.langchain.com/v0.1/docs/integrations/vectorstores/faiss
- https://platform.openai.com/docs/guides/embeddings

  ## 📘 Türkçe AÇıklama
Metin tabanlı bir soru-cevap sistemi oluşturmak için FAISS'i kullandık. FAISS, metin tabanlı soru-cevap sistemimizde, kullanıcı sorularına en alakalı cevapları hızlı ve verimli bir şekilde bulmak için kullandığımız bir araçtır. Metinleri vektörlere dönüştürerek, bu vektörleri indeksleyerek ve benzerlik araması yaparak, sistemin doğru ve hızlı cevaplar vermesini sağlar.Metin parçaları OpenAIEmbeddings kullanılarak sayısal vektörlere dönüştürüldü.AISS, bu vektörleri hızlı bir şekilde aranabilir bir indeks yapısı içinde organize etti. Bu, benzerlik aramalarını hızlandırmak için önemlidir.Kullanıcı bir soru sorduğunda, soru da bir vektöre dönüştürülür ve FAISS indeksi kullanılarak en benzer metin parçaları bulur.
