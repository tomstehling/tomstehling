<div align="center">

# 👋 Hi, I'm Tom — CS MSc student from Kiel/Germany
### Software Engineer | Tech Enthusiast  | Applied AI 
Currently exploring agentic systems  🤖⚡
Open to collaborations on MCP or agentic tools!

---

## 🚀 Current Project: AnkiXParlaI
# 🚨 TRY HERE ➡️ [![AnkixParlAI Banner](https://img.shields.io/badge/🚀_ANKIXPARLAI.COM-f97316?style=for-the-badge&logo=appveyor&logoColor=white)](https://ankixparlai-frontend-380281608527.europe-southwest1.run.app/login)

Want an ultra personalized language teacher? Try out my prototype! (english-spanish)



### 🧠 The Architecture

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./architecture.png">
  <source media="(prefers-color-scheme: light)" srcset="./architecture.png">
  <img alt="Agent Architecture" src="./architecture.png" width="90%">
</picture>

The duality of an adaptive learning system: The system continuously asseses the students knowledge to build an accurate model, that is then used to provide an optimal next learning step. 

## 🧭 Relational Graph Modeling

To get a ultra personalized learning experience, the system uses a dynamic curriculum. To ensure factual accuracy the agent uses a Knowledge Graph to base its decitions and actions on correct data. This prevents hallucinations and supports long term goal cohearence. The graph is based on current language pedagogy principles thus leveraging the knowledge of decades of language learning.
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


</div>



### 🧰 Technical Toolbox
*   **Languages:** Python (FastAPI, SQLAlchemy), TypeScript (Vue)
*   **AI/LLM:** OpenRouter integration, Context Engineering, Agent Loops
*   **Data:** PostgreSQL (Relational/JSONB), NetworkX
*   **DevOps:** Docker, GCP (Cloud Run, Cloud Build), Git/CI-CD

---

### 📫 Let's Connect!
*   **GitHub:** [ankixparlaibackend](https://github.com/tomstehling/ankixparlaibackend) | [ankixparlaifrontend](https://github.com/tomstehling/ankixparlaifrontend)
*   **Project Site:** [![AnkixParlAI Banner](https://img.shields.io/badge/🚀_ANKIXPARLAI.COM-f97316?style=for-the-badge&logo=appveyor&logoColor=white)](https://ankixparlai-frontend-380281608527.europe-southwest1.run.app/login) (In Development)


