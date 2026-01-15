<div align="center">

# Hola, I'm Tom Stehling 👋
### Software Engineer | AI Agent Architect | Language Tech Enthusiast

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org)
[![Vue.js](https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D)](https://vuejs.org)

I build systems that bridge the gap between **Generative AI** and **structured pedagogical logic**. My focus is on developing AI Agents grounded by Knowledge Graphs to solve complex problems—starting with language acquisition.

---

## 🚀 Featured Project: AnkiXParlaI

**Status:** Implementation (Active Development)  
**Current Sprint:** Multi-agent state-machine logic & FSRS integration

### 🧠 The Core: Spanish Grammar Knowledge Graph
A custom Knowledge Graph serving as the "source of truth" for AI agents, preventing hallucination through Relational Graph Modeling.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./grounding_graph.png">
  <source media="(prefers-color-scheme: light)" srcset="./grounding_graph.png">
  <img alt="Spanish Grammar Knowledge Graph" src="./grounding_graph.png" width="90%">
</picture>

---

## 🛠️ Agent Architecture & Orchestration

Utilizing a **custom state-machine coordination layer** to manage handoffs between specialized agents, ensuring deterministic transitions and robust error handling.

```mermaid
%%{init: { 'theme': 'dark', 'themeVariables': { 'mainBkg': '#0d1117', 'primaryColor': '#1f6feb', 'primaryTextColor': '#c9d1d9', 'primaryBorderColor': '#30363d', 'lineColor': '#8b949e', 'tertiaryColor': '#161b22' } } }%%
graph TD
    User((User)) -->|Spanish Input| Gateway[API Gateway - FastAPI]
    Gateway -->|Context Retrieval| KG[(Knowledge Graph)]
    
    subgraph AI Agent Swarm ["Custom State-Machine Coordination Layer"]
        Validator[Grammar Validator Agent]
        KG -->|Retrieve Rules| Validator
        Validator -->|Check Input| Tutor[Conversational Tutor Agent]
        Tutor -->|Grounded Response| Proposer[Flashcard Proposer Agent]
    end
    
    Proposer -->|New Card Proposal| User
    Tutor -->|Natural Response| User
    
    subgraph Persistence & SRS
        SRS[FSRS Scheduler] -->|Calculate Intervals| DB[(PostgreSQL)]
        User -->|Grade Card| SRS
    end

    style AI Agent Swarm fill:#161b22,stroke:#1f6feb,color:#c9d1d9
```

</div>

### 🔍 Agentic RAG: How it works
*   **Retrieval:** identifies verb lemmas and grammatical structures from user input.
*   **Grounding:** The **Validator Agent** fetches "Learning Hacks" and rules from the PostgreSQL Knowledge Graph.
*   **Validation:** The agent compares the user's input against these rules to identify specific pedagogical errors.
*   **Feedback:** The **Tutor Agent** synthesizes a grounded response while the **Proposer Agent** generates targeted flashcards.

---

### 🧰 Technical Toolbox
*   **Languages:** Python (FastAPI, SQLAlchemy), TypeScript (Vue 3, Node.js), Go
*   **AI/LLM:** Gemini API, OpenAI, Agentic Workflows, Prompt Engineering
*   **Data:** PostgreSQL (Relational/JSONB), Knowledge Graph Design
*   **DevOps:** Docker, GCP (Cloud Run, Cloud Build), Git/CI-CD

---

### 📫 Let's Connect!
*   **GitHub:** [ankixparlaibackend](https://github.com/tomstehling/ankixparlaibackend) | [ankixparlaifrontend](https://github.com/tomstehling/ankixparlaifrontend)
*   **Project Site:** [ankixparlai.com](https://ankixparlai.com) (In Development)

<div align="center">
  <br/>
  <i>Created with the help of my personalized AI engineering agent.</i>
</div>