# 🤖 Pepper LLM To-Do List Manager

![ROS 2](https://img.shields.io/badge/ROS_2-Humble%20%7C%20Iron%20%7C%20Jazzy-22314E?style=for-the-badge&logo=ros)
![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python)
![AI & LLM](https://img.shields.io/badge/AI_%26_LLM-Integrated-FF9D00?style=for-the-badge&logo=openai)

> Questo pacchetto ROS 2 (`project_nodes`) gestisce l'interazione intelligente con il robot umanoide **Pepper**. Combina il riconoscimento facciale, l'elaborazione audio avanzata e l'integrazione con un **LLM (Large Language Model)** per permettere a Pepper di riconoscere gli utenti, interagire in modo naturale e gestire una *To-Do List* personalizzata.

---

## 🧠 Architettura del Progetto



Il sistema si appoggia al pacchetto base `pepper_nodes` per l'interfaccia hardware e aggiunge un livello di intelligenza superiore tramite i seguenti nodi principali:

* 🧩 **Orchestrator:** Il *cervello centrale* che coordina le transizioni di stato e gestisce la logica del sistema.
* 🎙️ **Audio Pipeline:** Gestisce il VAD (*Voice Activity Detection*), l'ASR (*Automatic Speech Recognition*) tramite SpeechBrain e la logica di trascrizione in tempo reale.
* 👁️ **Facial Recognition:** Utilizza la telecamera di Pepper e librerie di computer vision avanzate (es. *DeepFace*) per identificare chi sta parlando.
* 💬 **LLM Node:** Invia i prompt testuali a un modello linguistico per generare risposte conversazionali naturali e tradurre le richieste vocali in azioni sulla To-Do List.
* 🔄 **Awareness Node** *(da `pepper_nodes`)*: Gestisce il tracking visivo per far sì che Pepper mantenga il contatto visivo (*"SemiEngaged"*) con l'utente in modo fluido e umano.

---

## ⚙️ Prerequisiti e Installazione

### 1. Requisiti di Sistema
- **Framework:** ROS 2 (Humble, Iron o Jazzy)
- **Linguaggio:** Python 3.10+
- **Hardware/Rete:** Connessione di rete attiva con il robot Pepper (o un ambiente di simulazione compatibile).

### 2. Dipendenze Python
Questo progetto richiede diverse librerie di machine learning per elaborare flussi audio e video. Puoi installare rapidamente tutte le dipendenze necessarie utilizzando il file `requirements.txt`:

```bash
pip install -r requirements.txt
