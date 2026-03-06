# llm-postprocess

<img width="800" height="1024" alt="Image" src="https://github.com/user-attachments/assets/034654a3-0e93-401a-b267-293059cfa6de" />


Notebook-basierte Evaluation von Whisper-Transkripten und LLM-Postprocessing
mit Fokus auf semantische Ähnlichkeit und Konsistenz (Embeddings),
inklusive Plots und Gegenexperimenten zur Analyse der Modellstabilität.

## Projektidee
Dieses Repository untersucht, wie verschiedene LLMs ASR-Transkripte (z. B. aus Whisper) nachbearbeiten/umformulieren
und wie **konsistent** diese Änderungen über unterschiedliche Domänen hinweg sind (medizinisch vs. nicht-medizinisch).

Die Analyse basiert auf:
- **Embeddings** (semantische Ähnlichkeit): Bedeutungsebene via mehrere Embedding-Backends


## Repository-Struktur
- `Gegenexperiment/` – Gegenexperimente für nicht-medizinische Texte
- `elab_request/` – Export/Abholung von Experimenten & Transkripten (z. B. aus eLab) als JSON für die Analyse
- `embedding/` – Embedding-basierte Similarity- und Distanz-Berechnung sowie Modellvergleiche
- `plots/` – generierte Abbildungen für Reporting
- `temperature_experiments/` – Analyse der Auswirkung verschiedener Temperatur-Parameter auf die Konsistenz und Stabilität der Outputs des MedGemma-Modells
- `extended_analysis/` – zusätzliche Experimente und vertiefende Auswertungen

## Daten / Large-Files
Alle Parquet-Dateien werden ausgeschlossen, damit das Repo schlank bleibt und GitHub-Dateigrößenlimits nicht überschritten werden.
Diese Dateien werden separat über **Zenodo** bereitgestellt.
