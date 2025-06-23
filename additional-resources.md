# Weitere Ressourcen

## Erweiterte RAG-Techniken

### Hybride Suche
Kombiniere Vektor-Suche mit traditioneller Keyword-Suche für bessere Ergebnisse:
- [BM25 + Semantic Search](https://weaviate.io/blog/hybrid-search-explained)
- [Elasticsearch Hybride Suche](https://www.elastic.co/guide/en/elasticsearch/reference/current/knn-search.html)

### Verbesserungen für Produktionssysteme
- **Reranking:** Verwende spezialisierte Modelle um Ergebnisse zu verbessern
- **Query Expansion:** Erweitere Suchanfragen automatisch
- **Chunk Overlap:** Optimiere Überlappung zwischen Text-Chunks
- **Metadaten-Filtering:** Nutze Dokumenten-Metadaten für präzisere Suche

## Vektor-Datenbanken

### Open Source
- **[Chroma](https://www.trychroma.com/)** - Einfach zu verwenden, lokal oder gehostet
- **[FAISS](https://faiss.ai/)** - Von Meta entwickelt, sehr schnell
- **[Weaviate](https://weaviate.io/)** - Vollständige Vektor-Datenbank mit GraphQL
- **[Qdrant](https://qdrant.tech/)** - Rust-basiert, sehr performant

### Kommerzielle Lösungen
- **[Pinecone](https://www.pinecone.io/)** - Managed Vektor-Datenbank

## Embedding-Modelle

### Mehrsprachige Modelle
- **[multilingual-e5](https://huggingface.co/intfloat/multilingual-e5-large)** - Unterstützt 100+ Sprachen
- **[BGE-M3](https://huggingface.co/BAAI/bge-m3)** - Multilinguale, Multi-Granularität

### Wissenschaftliche Modelle
- **[SciBERT](https://huggingface.co/allenai/scibert_scivocab_uncased)** - Speziell für wissenschaftliche Texte
- **[PubMedBERT](https://huggingface.co/microsoft/BiomedNLP-PubMedBERT-base-uncased-abstract)** - Für biomedizinische Literatur

## RAG-Frameworks

### LangChain
- **[LangChain Python](https://python.langchain.com/)** - Umfassendes Framework
- **[LangChain Expression Language (LCEL)](https://python.langchain.com/docs/expression_language/)** - Für komplexe Pipelines

### LlamaIndex
- **[LlamaIndex](https://www.llamaindex.ai/)** - Fokus auf Daten-Integration

### Haystack
- **[Haystack](https://haystack.deepset.ai/)** - Von deepset, sehr flexibel

## Wissenschaftliche Paper und Tools

### Grundlagen-Paper
- **[RAG: Retrieval-Augmented Generation](https://arxiv.org/abs/2005.11401)** - Original RAG Paper
- **[Dense Passage Retrieval](https://arxiv.org/abs/2004.04906)** - DPR für bessere Retrieval

### Wissenschaftliche RAG-Systeme
- **[PaperQA](https://arxiv.org/abs/2409.13740)** - RAG für wissenschaftliche Literatur
- **[ScholarQA](https://scholarqa.allen.ai/chat)** - Allen Institute's Wissenschafts-QA

### Evaluation
- **[RAGAS](https://github.com/explodinggradients/ragas)** - Framework für RAG-Evaluation
- **[TruLens](https://www.trulens.org/)** - Evaluation und Monitoring von LLM-Apps

## Implementierungs-Beispiele

### GitHub Repositories
- **[RAG from Scratch](https://github.com/langchain-ai/rag-from-scratch)** - LangChain's Tutorial-Serie
- **[Verba](https://github.com/weaviate/Verba)** - Open Source RAG-Interface

## Nächste Schritte

Nach diesem Tutorial kannst du:

1. **Experimentiere mit verschiedenen Embedding-Modellen** - Teste, welches für deine Dokumente am besten funktioniert
2. **Verwende eine Vektor-Datenbank** - Skaliere dein System für größere Dokumentensammlungen
3. **Implementiere Evaluation** - Messe die Qualität deiner RAG-Antworten
4. **Baue eine Web-Interface** - Erstelle eine benutzerfreundliche Oberfläche mit Streamlit oder FastAPI
5. **Erweitere um Multimodal-Support** - Integriere Bilder und Tabellen aus PDFs

## Kontakt

Hast du Fragen oder Verbesserungsvorschläge? 
- **GitHub Issues:** [rag-tutorial/issues](https://github.com/lamalab-org/rag-tutorial/issues)
- **LamaLab Website:** [lamalab.org](https://lamalab.org)

Viel Erfolg beim Aufbau deines RAG-Systems! 🚀