# LangChain & LLM Backend: From Basics to Project 🚀

Welcome to the **LangChain & LLM Backend: From Basics to Project** repository. This codebase serves as a comprehensive, structured path starting from foundational Python development, building asynchronous RESTful APIs using FastAPI, establishing robust database architectures with SQLAlchemy, integrating local and cloud Large Language Models (LLMs) via Ollama and LangChain, and culminating in a full-stack, state-of-the-art E-Commerce application.

This repository is ideal for learning how to orchestrate advanced AI workflows, implement Retrieval-Augmented Generation (RAG) pipelines, build intelligent multi-agent setups, and couple them with modern web applications.

---

## 📂 Project Architecture

```directory
.
├── python_basics/          # Foundational Python scripts & interactive CLI applications
├── FastAPI/                 # RESTful APIs, JWT Auth systems, and task/blog managers
├── ollama/                  # Local LLM integrations, Streamlit chatbot, and local AI agents
├── langchain/               # Advanced LLM orchestration, RAG pipelines, and LangServe APIs
└── ECommerce/               # Full-Stack E-Commerce store (FastAPI backend + React frontend)
```

---

## 🛠️ Detailed Component Directory

### 🐍 1. Python Basics (`python_basics/`)
A collection of essential script implementations focusing on clean Python syntax, control flow, data structures, and CLI interfaces.
* **Key Programs**:
  * [student_record_system.py](file:///Users/abhishekduggal/Desktop/Projects/langchain-llm-backend-Basics-To-Project/python_basics/student_record_system.py): Interactive CLI application managing student profiles.
  * [todo.py](file:///Users/abhishekduggal/Desktop/Projects/langchain-llm-backend-Basics-To-Project/python_basics/todo.py) & [calculator.py](file:///Users/abhishekduggal/Desktop/Projects/langchain-llm-backend-Basics-To-Project/python_basics/calculator.py): Functional utilities showcasing dictionary manipulations and basic validation.
  * [marksDict.py](file:///Users/abhishekduggal/Desktop/Projects/langchain-llm-backend-Basics-To-Project/python_basics/marksDict.py), [ListPrograms.py](file:///Users/abhishekduggal/Desktop/Projects/langchain-llm-backend-Basics-To-Project/python_basics/ListPrograms.py), and word/number counters.

---

### ⚡ 2. FastAPI & Backend Fundamentals (`FastAPI/`)
Production-grade RESTful backend architectures demonstrating modern API development practices.
* **Authentication (`FastAPI/Authentication/`)**: A secure JWT authentication layer featuring user registration, bcrypt password hashing, and token-based protected endpoints.
* **Task Management (`FastAPI/TaskManagement/`)**: CRUD API system utilizing Pydantic models for request/response validation.
* **Database integrations (`FastAPI/database/`)**: Relational database operations leveraging SQLAlchemy with SQLite databases for structured data management:
  * **Blog Engine**: A relational CRUD application matching users with posts.
  * **Notes Manager**: A simple backend organizer utilizing persistent storage.

---

### 🦙 3. Local LLM Integration with Ollama (`ollama/`)
Utilizing local model servers to run AI systems entirely offline or in resource-restricted environments.
* **Chatbot Interface**: [chatbot.py](file:///Users/abhishekduggal/Desktop/Projects/langchain-llm-backend-Basics-To-Project/ollama/chatbot.py) offers a smooth web interface built with **Streamlit** interfacing with local Llama/Mistral models.
* **AI Agents (`ollama/Aiagent/`)**:
  * [agentOllama.ipynb](file:///Users/abhishekduggal/Desktop/Projects/langchain-llm-backend-Basics-To-Project/ollama/Aiagent/agentOllama.ipynb): Initial setups running prompt-based autonomous executions.
  * [newsOllama.ipynb](file:///Users/abhishekduggal/Desktop/Projects/langchain-llm-backend-Basics-To-Project/ollama/Aiagent/newsOllama.ipynb) & [plannerOllama.ipynb](file:///Users/abhishekduggal/Desktop/Projects/langchain-llm-backend-Basics-To-Project/ollama/Aiagent/plannerOllama.ipynb): Multi-step planning agents leveraging local models for targeted processing.
* **Rest API integration**: Interacting with local model APIs programmatically in `restapi.ipynb` and `API/`.

---

### 🔗 4. Advanced LLM Orchestration with LangChain (`langchain/`)
Productionizing AI agent pipelines and context-aware context retrieval architectures.
* **Retrieval-Augmented Generation (RAG) (`langchain/rag/`)**: Fully functional RAG implementation in [simplerag.ipynb](file:///Users/abhishekduggal/Desktop/Projects/langchain-llm-backend-Basics-To-Project/langchain/rag/simplerag.ipynb) using:
  * Document loaders (`pypdf`, `beautifulsoup4`)
  * Text splitters (`RecursiveCharacterTextSplitter`)
  * Vector stores (**ChromaDB** & **FAISS**)
  * Embedding models (Google GenAI / Ollama)
* **LangServe & APIs (`langchain/API/`)**:
  * [app.py](file:///Users/abhishekduggal/Desktop/Projects/langchain-llm-backend-Basics-To-Project/langchain/API/app.py) & [client.py](file:///Users/abhishekduggal/Desktop/Projects/langchain-llm-backend-Basics-To-Project/langchain/API/client.py): Exposing LangChain chains as FastAPI endpoints using LangServe.
* **Tool Calling & Agents (`langchain/toolscalling/` & `langchain/ai_agent/`)**:
  * Implementing structured LLM outputs, automated function/API calling (e.g., currency conversion), and building agent loops (`planner.ipynb`, `news.ipynb`).

---

### 🛒 5. End-to-End E-Commerce Application (`ECommerce/`)
A full-stack, seed-ready e-commerce store mapping complex database relationships (Users, Products, Orders, and OrderItems) with an interactive frontend.
* **Backend (`FastAPI`)**:
  * Asynchronous endpoints managing real-time stock deductions, order placements, total amount auto-calculation, and seeding initial catalogs.
* **Frontend (`React + Vite`)**:
  * A modern web client interface communicating with the FastAPI endpoints, handling items and state management.

---

## ⚡ Tech Stack & Libraries Used

* **Programming Language**: Python 3.10+
* **Web Frameworks**: FastAPI, Streamlit, Uvicorn, LangServe
* **AI & LLM Orchestration**: LangChain, LangChain Core, LangChain Community, Ollama, LangChain Google GenAI
* **Database & Vector Stores**: SQLAlchemy, ChromaDB, FAISS
* **Frontend**: React, Vite, TailwindCSS (for E-commerce UI)
* **Security & Auth**: PyJWT / python-jose, Passlib (Bcrypt)

---

## ⚙️ Quick Start Guide

### 1. Prerequisites & Environment Setup
Clone the repository and prepare a Python virtual environment:
```bash
git clone https://github.com/Aduggal1163/langchain-llm-backend-Basics-To-Project.git
cd langchain-llm-backend-Basics-To-Project
python3 -m venv venv
source venv/bin/activate
```

### 2. Installing Dependencies
Install packages for the backend and AI models:
```bash
# For main AI & LLM development
pip install -r ollama/requirements.txt

# For FastAPI systems
pip install -r FastAPI/requirements.txt
```

### 3. Setting Up Ollama
To run the local models, make sure you have [Ollama](https://ollama.com/) installed and running:
```bash
# Pull your model of choice (e.g., llama3 or mistral)
ollama pull llama3
```

### 4. Running the E-Commerce Application
To spin up the E-Commerce app:
* **Backend**:
  ```bash
  cd ECommerce
  pip install -r requirements.txt
  python main.py
  ```
  *(API will be available at `http://localhost:8000`. You can seed database values using `POST /seed`)*

* **Frontend**:
  ```bash
  cd frontend
  npm install
  npm run dev
  ```

---

## 📌 GitHub Pin Descriptions

Here are curated descriptions optimized for your GitHub profile pins depending on the specific focus you want to project:

### Option 1: AI & Full-Stack Developer Focus (Recommended)
> 🚀 Full-stack developer roadmap from Python basics & FastAPI (JWT Auth, SQLite DBs) to advanced LLM orchestration. Includes local LLMs (Ollama), LangChain agents, RAG pipelines (Chroma/FAISS), and a React + FastAPI E-commerce project.

### Option 2: AI & LLM Engineering Focus
> 🔗 Multi-agent setups, RAG pipelines, and API integrations with LangChain and local Ollama models. Features custom tool-calling notebooks, Streamlit chatbots, LangServe web APIs, and production-ready FastAPI endpoints.

### Option 3: Backend & Python Developer Focus
> ⚡ Complete backend journey building RESTful systems with FastAPI, secure database relationships with SQLAlchemy, JWT Auth, and custom AI plugins. Culminates in a full-stack React and SQLite-powered E-commerce application.
