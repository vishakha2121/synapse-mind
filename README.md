# 🧠 Synapse-Mind: AI Distributed Brain Platform

> *"Five minds. One brain. Infinite possibilities."*

## 🌟 Overview

**Synapse-Mind** is a distributed multi-model AI platform inspired by the modular architecture of the human brain. Instead of relying on a single monolithic AI model, Synapse-Mind breaks down intelligence into **5 specialized cognitive regions**. These regions collaborate under a central **Orchestrator (The Brain Stem)** to solve complex, multi-modal tasks.

This is not just another chatbot. It is a cognitive architecture simulation powered by **Google's Gemini API**, designed to route queries intelligently, just like different lobes of the human brain handle different tasks.

---

## 🧩 The 5 Brain Regions

| Region | Role | Inspired By | Powered By |
|--------|------|-------------|------------|
| 🧠 **Reasoning** | Logical deduction, step-by-step analysis, and fact-checking. | Frontal Lobe | Gemini API |
| 💾 **Memory** | Stores & recalls past interactions, user preferences, and context. | Hippocampus | SQLite + Gemini |
| 📋 **Planning** | Breaks complex goals into actionable sub-tasks and roadmaps. | Prefrontal Cortex | Gemini API |
| 💬 **Language** | Understands intent, generates natural language, and translates. | Temporal Lobe | Gemini API |
| 👁️ **Vision** | Analyzes images, extracts visual semantics, and describes scenes. | Occipital Lobe | Gemini Vision |

---

## ⚙️ How It Works (The Orchestrator Flow)

When a user submits a query (text + optional image), the flow is:

1. **Language Module** parses the input and extracts intent.
2. **Orchestrator** dynamically decides which brain regions are needed for this specific query.
3. **Memory Module** fetches relevant context from past sessions.
4. **Vision Module** activates *only if* an image is attached.
5. **Planning Module** builds a step-by-step execution plan (for complex tasks).
6. **Reasoning Module** validates logic and checks constraints.
7. **Language Module** generates the final, polished response.
8. **Memory Module** saves the entire interaction for future recall.

---

## ✨ Core Features

- 🎭 **Multi-Model Collaboration**: 5 specialized Gemini-powered modules working together.
- 🧠 **Intelligent Orchestration**: Dynamic routing engine decides which regions activate.
- 💬 **Conversational Chat Interface**: A clean, intuitive UI with real-time streaming.
- 👁️ **Multimodal Vision Support**: Upload images for scene understanding and analysis.
- 🗂️ **Session-based Memory**: Remembers context across conversations.
- 📊 **Live Brain Visualization**: Real-time animated UI showing which brain region is active (Glassmorphic UI + Framer Motion).
- 🖥️ **CPU-Friendly**: Runs entirely on Gemini's cloud API. No local GPU required.

---

## 🏗️ Tech Stack

### Backend
- **Python 3.10+**
- **FastAPI** (High-performance async REST API)
- **SQLAlchemy** (ORM)
- **SQLite** (Lightweight persistent storage)
- **Google Gemini API** (Core AI engine)
- **Pydantic** (Data validation)

### Frontend
- **React 18 + Vite**
- **TailwindCSS** (Utility-first styling)
- **Framer Motion** (Smooth animations)
- **Axios** (API communication)
- **Lucide Icons**

---

## 🚀 Quick Start & Installation (Local Setup)

### 1. Prerequisites
- Python 3.10+ installed
- Node.js (v18+) and npm installed
- Get a free **Gemini API Key** from [Google AI Studio](https://aistudio.google.com/app/apikey)

### 2. Backend Setup
```bash
# Clone the repository
git clone https://github.com/vishakha2121/synapse-mind.git
cd synapse-mind/backend

# Create a virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create a .env file and add your Gemini API key
echo "GEMINI_API_KEY=your_api_key_here" > .env
echo "DATABASE_URL=sqlite:///./synapse.db" >> .env

# Run the FastAPI server
uvicorn app.main:app --reload