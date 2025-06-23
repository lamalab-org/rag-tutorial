# RAG Tutorial: Retrieval-Augmented Generation von Grund auf

Willkommen zu diesem umfassenden Tutorial über **Retrieval-Augmented Generation (RAG)**! 

In diesem Tutorial lernst du, wie du ein RAG-System von Grund auf aufbaust, um Fragen basierend auf wissenschaftlichen Artikeln zu beantworten. RAG kombiniert die Stärken von Retrieval- und Generierungsmodellen und ist die Grundlage für Systeme wie [PaperQA](https://arxiv.org/abs/2409.13740) oder [ScholarQA](https://scholarqa.allen.ai/chat).

## Was ist RAG?

Retrieval-Augmented Generation (RAG) ist eine Technik, die:
- Relevante Informationen aus einer Dokumentensammlung abruft (Retrieval)
- Diese Informationen nutzt, um präzise Antworten zu generieren (Generation)
- Quellen für die Antworten bereitstellt (Transparenz)

## Was lernst du in diesem Tutorial?

1. **PDF-Dokumente einlesen** und Text extrahieren
2. **Text in Chunks aufteilen** für effiziente Verarbeitung
3. **Embeddings erstellen** zur semantischen Suche
4. **Vektorstore aufbauen** für schnelle Abfragen
5. **Retrieval implementieren** um relevante Textabschnitte zu finden
6. **Antworten generieren** mit Sprachmodellen

## Voraussetzungen

- Python 3.8 oder höher
- Grundkenntnisse in Python
- Ein OpenAI API-Key (oder anderer LLM-Provider)
- PDF-Dokumente zum Testen

## Zielgruppe

Dieses Tutorial richtet sich an:
- Studierende und Forschende, die RAG-Systeme verstehen möchten
- Entwickler:innen, die eigene Frage-Antwort-Systeme bauen wollen
- Alle, die lernen möchten, wie moderne AI-Systeme funktionieren

## Setup-Optionen

Du kannst dieses Tutorial auf verschiedene Weise durchführen:

1. **[Lokale Installation](setup.md)** - Empfohlen für die vollständige Erfahrung
2. **[Google Colab](colab-setup.md)** - Schneller Einstieg ohne lokale Installation

## Autoren

Dieses Tutorial wurde von **Mara Schilling-Wilhelmi** und **Kevin Maik Jablonka** vom [LamaLab](https://lamalab.org) erstellt.

## Lizenz

Dieses Tutorial steht unter der MIT-Lizenz und kann frei verwendet und modifiziert werden.

---

Bereit loszulegen? Wähle deine bevorzugte Setup-Option und beginne mit dem Tutorial!