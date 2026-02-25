# 🤖 Pepper LLM To-Do List Manager

![ROS 2](https://img.shields.io/badge/ROS_2-Humble%20%7C%20Iron%20%7C%20Jazzy-22314E?style=for-the-badge&logo=ros)
![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python)
![AI & LLM](https://img.shields.io/badge/AI_%26_LLM-Integrated-FF9D00?style=for-the-badge&logo=openai)

> This ROS 2 package (`project_nodes`) manages intelligent interaction with the humanoid robot **Pepper**. It combines facial recognition, advanced audio processing, and integration with a **Large Language Model (LLM)** to allow Pepper to recognize users, interact naturally, and manage a personalized *To-Do List*.

---

## 🧠 Project Architecture



The system builds upon the base `pepper_nodes` package for hardware interfacing and adds a higher level of intelligence through the following main nodes:

* 🧩 **Orchestrator:** The *central brain* that coordinates state transitions and manages the system's logic.
* 🎙️ **Audio Pipeline:** Handles VAD (*Voice Activity Detection*), ASR (*Automatic Speech Recognition*) via SpeechBrain, and real-time transcription logic.
* 👁️ **Facial Recognition:** Utilizes Pepper's camera and advanced computer vision libraries (e.g., *DeepFace*) to identify the speaker.
* 💬 **LLM Node:** Sends text prompts to a language model to generate natural conversational responses and translate voice requests into To-Do List actions.
* 🔄 **Awareness Node** *(from `pepper_nodes`)*: Manages visual tracking so Pepper maintains eye contact (*"SemiEngaged"*) with the user in a fluid, human-like manner.

---

## ⚙️ Prerequisites and Installation

### 1. System Requirements
- **Framework:** ROS 2 (Humble, Iron, or Jazzy)
- **Language:** Python 3.10+
- **Hardware/Network:** Active network connection with the Pepper robot (or a compatible simulation environment).

### 2. Python Dependencies
This project requires several machine learning libraries to process audio and video streams. You can quickly install all necessary dependencies using the `requirements.txt` file:

```bash
pip install -r requirements.txt
