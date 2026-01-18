<div align="center">

# 👋 Hi, I'm Tom — CS MSc student from Kiel/Germany
### Software Engineer | Tech Enthusiast  | Rising Applied AI Expert
Currently maxing out LLMs and exploring agentic systems.  🤖⚡
Open to collaborations on MCP or agentic tools!

---

## 🚀 Current Project: AnkiXParlaI
Want an ultra personalized language teacher? Try out my prototype! (english-spanish)
**[🌐 Live Demo](https://ankixparlai-frontend-380281608527.europe-southwest1.run.app/login)**


### 🧠 The Architecture
A custom Knowledge Graph serving as the "source of truth" for AI agents, preventing hallucination through Relational Graph Modeling.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./grounding_graph.png">
  <source media="(prefers-color-scheme: light)" srcset="./grounding_graph.png">
  <img alt="Spanish Grammar Knowledge Graph" src="./grounding_graph.png" width="90%">
</picture>

---

## 🔄 System Data Flow

A high-level overview of the ecosystem's communication architecture. Note that the **Agent Container** is isolated, communicating exclusively with the **Backend** to ensure secure and structured data handling.

```mermaid
%%{init: { 'theme': 'dark', 'themeVariables': { 'mainBkg': '#0d1117', 'primaryColor': '#1f6feb', 'primaryTextColor': '#c9d1d9', 'primaryBorderColor': '#30363d', 'lineColor': '#8b949e', 'tertiaryColor': '#161b22' } } }%%
graph LR
    subgraph Client ["Frontend"]
        Vue[Vue 3 Application]
    end

    subgraph Server ["Backend"]
        FastAPI[FastAPI Gateway]
    end

    subgraph Storage ["Database"]
        Postgres[(PostgreSQL / FSRS)]
    end

    subgraph Intelligence ["Agent Container"]
        Agent[Centralized AI Agent]
    end

    Vue <-->|REST API / JSON| FastAPI
    FastAPI <-->|SQLAlchemy / CRUD| Postgres
    FastAPI <-->|State Handoffs| Agent

    style Client fill:#161b22,stroke:#30363d,color:#c9d1d9
    style Server fill:#161b22,stroke:#1f6feb,color:#c9d1d9
    style Storage fill:#161b22,stroke:#316192,color:#c9d1d9
    style Intelligence fill:#161b22,stroke:#238636,color:#c9d1d9
```

---

## 🛠️ Agent Architecture & Orchestration

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./architecture.png">
  <source media="(prefers-color-scheme: light)" srcset="./architecture.png">
  <img alt="Agent Architecture" src="./architecture.png" width="90%">
</picture>

Utilizing a **custom state-machine** to manage the logic and transitions of the **Centralized AI Agent**, ensuring deterministic processing and robust error handling.

```mermaid
%%{init: { 'theme': 'dark', 'themeVariables': { 'mainBkg': '#0d1117', 'primaryColor': '#1f6feb', 'primaryTextColor': '#c9d1d9', 'primaryBorderColor': '#30363d', 'lineColor': '#8b949e', 'tertiaryColor': '#161b22' } } }%%
graph TD
    User((User)) -->|Spanish Input| Gateway[API Gateway - FastAPI]
    Gateway -->|Context Retrieval| KG[(Knowledge Graph)]
    
    subgraph CentralAgent ["Centralized AI Agent"]
        direction TB
        State[State Machine Logic]
        Validator[Validation Logic]
        Tutor[Tutor Logic]
        Proposer[Proposer Logic]
    end
    
    Gateway -->|Request| CentralAgent
    KG -->|Retrieve Rules| CentralAgent
    CentralAgent -->|Response / Flashcards| User
    
    subgraph Persistence & SRS
        SRS[FSRS Scheduler] -->|Calculate Intervals| DB[(PostgreSQL)]
        User -->|Grade Card| SRS
    end

    style CentralAgent fill:#161b22,stroke:#1f6feb,color:#c9d1d9
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
