# Setup und Installation

## Voraussetzungen

Bevor du beginnst, stelle sicher, dass folgende Tools installiert sind:

### Git installieren
Git wird benötigt, um das Repository zu klonen. Falls noch nicht installiert:
- **Installationsanleitung:** [The Turing Way - Git Installation](https://book.the-turing-way.org/reproducible-research/vcs/vcs-git-install.html)
- **Windows:** [Git für Windows](https://gitforwindows.org/)
- **macOS:** `brew install git` oder über [git-scm.com](https://git-scm.com/)
- **Linux:** `sudo apt install git` (Ubuntu/Debian) oder entsprechende Distribution

### Python und Conda installieren
Conda wird für das Umgebungsmanagement empfohlen:
- **Installationsanleitung:** [The Turing Way - Conda Installation](https://book.the-turing-way.org/reproducible-research/renv/renv-package.html)
- **Miniconda (empfohlen):** [miniconda.org](https://docs.conda.io/en/latest/miniconda.html)
- **Anaconda (vollständig):** [anaconda.com](https://www.anaconda.com/products/distribution)

## Lokale Installation

### 1. Repository klonen

```bash
git clone https://github.com/lamalab-org/rag-tutorial.git
cd rag-tutorial
```

### 2. Python-Umgebung einrichten

Wir empfehlen die Verwendung einer virtuellen Umgebung:

```bash
# Mit conda (empfohlen)
conda create -n rag-tutorial python=3.9
conda activate rag-tutorial

# Oder mit venv (falls kein conda verfügbar)
python -m venv rag-tutorial
source rag-tutorial/bin/activate  # Linux/Mac
# oder
rag-tutorial\Scripts\activate  # Windows
```

### 3. Abhängigkeiten installieren

```bash
pip install -r requirements.txt
```

### 4. Jupyter Notebook starten

```bash
jupyter notebook tutorial.ipynb
```

## API-Schlüssel konfigurieren

### OpenAI API

1. Erstelle einen Account bei [OpenAI](https://platform.openai.com/)
2. Generiere einen API-Schlüssel
3. Erstelle eine `.env`-Datei im Projektverzeichnis:

```bash
# .env
OPENAI_API_KEY=your_openai_api_key_here
```

### Alternative Provider

Das Tutorial unterstützt verschiedene LLM-Provider über LiteLLM:

#### Groq (Kostenlos)
```bash
# .env
GROQ_API_KEY=your_groq_api_key_here
```

#### Cohere (Kostenlos mit Limits)
```bash
# .env
COHERE_API_KEY=your_cohere_api_key_here
```

#### Anthropic Claude
```bash
# .env
ANTHROPIC_API_KEY=your_anthropic_api_key_here
```

Eine komplette Übersicht aller unterstützten Provider findest du in der [LiteLLM Dokumentation](https://docs.litellm.ai/docs/providers).

## PDF-Dokumente vorbereiten

1. Erstelle einen Ordner `data/` im Projektverzeichnis
2. Lege deine PDF-Dateien in diesen Ordner
3. Alternativ kannst du die bereitgestellten Beispiel-PDFs im `static/pdfs/` Ordner verwenden

## Troubleshooting

### Häufige Probleme

**Problem:** `ModuleNotFoundError: No module named 'fitz'`
**Lösung:** Installiere PyMuPDF:
```bash
pip install PyMuPDF
```

**Problem:** API-Schlüssel nicht gefunden
**Lösung:** Stelle sicher, dass die `.env`-Datei im richtigen Verzeichnis liegt und korrekt formatiert ist.

**Problem:** Jupyter Notebook startet nicht
**Lösung:** Installiere Jupyter:
```bash
pip install jupyter
```

### Weitere Hilfe

Bei Problemen kannst du:
- Ein Issue auf [GitHub](https://github.com/lamalab-org/rag-tutorial/issues) erstellen
- Die [Jupyter Dokumentation](https://docs.jupyter.org/en/latest/) konsultieren
- Die [The Turing Way](https://book.the-turing-way.org/) für allgemeine Hilfe zu reproduzierbarer Forschung konsultieren

## Nächste Schritte

Nachdem du alles eingerichtet hast, kannst du mit dem [Tutorial](tutorial.ipynb) beginnen!