## 📚 Project Description
In this project, I took a text file (example content from Wikipedia), split it into small chunks, and converted these chunks into vector representations using Cohere's embed-english-v2.0 embedding model.
The resulting vectors were stored in a Chroma vector database, and I built a retriever that can return the most relevant text chunks for a given user question.

## 🤖 Language Model (LLM)
For the question-answering process, I used Cohere’s command-r language model.
This model not only generates high-quality responses but also includes a built-in hallucination grader, which helps reduce the risk of incorrect or made-up answers.

<pre>llm = ChatCohere(model="command-r", temperature=0)</pre>

## 🧠 Embedding Model
To transform the text into vector form, I used Cohere’s embed-english-v2.0 embedding model.

<pre>embd = CohereEmbeddings(model="embed-english-v2.0")</pre>


## 📘 Türkçe açıklama
Bu projede bir metin dosyasını (örnek olarak Wikipedia'dan alınmış içerik) küçük parçalara bölüp, bu parçaları Cohere’ın embed-english-v2.0 embedding modeli ile vektörlere dönüştürüldü.
Bu vektörleri Chroma veri tabanına kaydettim ve bir retriever oluşturarak, kullanıcı sorularına en uygun içerik parçalarını bulabilen bir yapı kuruldu.
Soru-cevap işlemlerinde Cohere’ın command-r dil modeli kullanıldı.
Bu model, gelişmiş cevaplar üretmenin yanı sıra, halüsinasyon kontrolü yapan yerleşik bir "grader" da içerir. Bu sayede modelin uydurma cevap verme olasılığı azaltılmış olur.
Metni sayısal vektörlere dönüştürmek için Cohere’ın embed-english-v2.0 modeli kullanıldı.
