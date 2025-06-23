# Google Colab Setup

Google Colab ist eine kostenlose Plattform, die es ermöglicht, Jupyter Notebooks direkt im Browser auszuführen - ohne lokale Installation!

## Schnellstart mit Colab

### Option 1: Direkt öffnen
Klicke auf diesen Link, um das Tutorial direkt in Colab zu öffnen:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lamalab-org/rag-tutorial/blob/master/tutorial.ipynb)

### Option 2: Manuell öffnen
1. Gehe zu [Google Colab](https://colab.research.google.com/)
2. Wähle "GitHub" als Quelle
3. Gib ein: `lamalab-org/rag-tutorial`
4. Wähle `tutorial.ipynb`

## Colab-spezifische Anpassungen

### 1. Abhängigkeiten installieren
Am Anfang des Notebooks führe diese Zelle aus:

```python
# Zusätzliche Pakete für Colab installieren
!pip install python-dotenv

# Überprüfe, ob alle Pakete installiert sind
!pip list | grep -E "(pymupdf|numpy|litellm|langchain|python-dotenv)"
```

### 2. API-Schlüssel in Colab
Da du keine `.env`-Datei in Colab hochladen kannst, nutze eine der folgenden Methoden:

#### Methode 1: Colab Secrets (Empfohlen)
1. Klicke auf das Schlüssel-Symbol 🔑 in der linken Seitenleiste
2. Füge einen neuen Secret hinzu:
   - Name: `OPENAI_API_KEY`
   - Wert: dein API-Schlüssel
3. Aktiviere den Zugriff für das Notebook
4. Verwende im Code:

```python
from google.colab import userdata
import os

# API-Schlüssel aus Colab Secrets laden
os.environ['OPENAI_API_KEY'] = userdata.get('OPENAI_API_KEY')
```

#### Methode 2: Direkte Eingabe (Weniger sicher)
```python
import os
import getpass

# API-Schlüssel eingeben (wird nicht angezeigt)
api_key = getpass.getpass("Gib deinen OpenAI API-Schlüssel ein: ")
os.environ['OPENAI_API_KEY'] = api_key
```

### 3. PDF-Dateien hochladen
In Colab kannst du deine eigenen PDFs direkt hochladen:

```python
from google.colab import files
import os

# Ordner für PDFs erstellen
os.makedirs('data', exist_ok=True)

# Dateien hochladen
uploaded = files.upload()

# Hochgeladene Dateien in den data-Ordner verschieben
for filename in uploaded.keys():
    if filename.endswith('.pdf'):
        os.rename(filename, f'data/{filename}')
        print(f'PDF {filename} hochgeladen und in data/ verschoben')
```

## Colab-Vorteile

✅ **Keine lokale Installation nötig**
✅ **Kostenlose GPU/TPU-Nutzung**
✅ **Einfaches Teilen von Notebooks**
✅ **Automatische Speicherung in Google Drive**

## Colab-Nachteile

❌ **Sitzungen werden nach Inaktivität beendet**
❌ **Begrenzte Laufzeit (12 Stunden)**
❌ **Dateien gehen verloren (außer in Google Drive gespeichert)**
❌ **Internetverbindung erforderlich**

## Tipps für Colab

1. **Regelmäßig speichern:** Colab speichert automatisch, aber speichere wichtige Änderungen zusätzlich
2. **Google Drive verbinden:** Für persistente Dateispeicherung
3. **Runtime-Typ wählen:** Für dieses Tutorial reicht CPU, aber GPU kann bei großen Dokumenten helfen
4. **Keine sensiblen Daten:** Verwende keine echten API-Schlüssel in geteilten Notebooks

## Google Drive Integration

Für persistente Speicherung:

```python
from google.colab import drive
drive.mount('/content/drive')

# Arbeitsverzeichnis auf Google Drive setzen
import os
os.chdir('/content/drive/MyDrive/rag-tutorial')
```

## Nächste Schritte

Nachdem du Colab eingerichtet hast, kannst du direkt mit dem [Tutorial](tutorial.ipynb) beginnen!

Hast du Probleme? Schaue in unsere [Troubleshooting-Sektion](setup.md#troubleshooting) oder erstelle ein [GitHub Issue](https://github.com/lamalab-org/rag-tutorial/issues).