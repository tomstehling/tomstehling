# Hola, I'm Tom Stehling 👋

```mermaid
%%{init: { 'theme': 'dark', 'themeVariables': { 'mainBkg': '#0d1117', 'primaryColor': '#0d1117', 'primaryTextColor': '#c9d1d9', 'primaryBorderColor': '#30363d' } } }%%
graph TD
    Header["<br/><h3>Software Engineer | AI Agent Architect</h3>I build systems that bridge the gap between <b>Generative AI</b> and <b>structured pedagogical logic</b>.<br/>Currently developing AI Agents grounded by Knowledge Graphs to solve complex problems.<br/><br/>🚀 <b>Featured Project: AnkiXParlaI</b><br/>Status: Implementation (Active Development)<br/>Focus: Multi-agent state-machine logic & FSRS integration<br/><br/>"]
    style Header fill:#0d1117,stroke:#30363d,stroke-width:2px,color:#c9d1d9
```

### 🧠 The Core: Spanish Grammar Knowledge Graph
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./grounding_graph.png">
  <source media="(prefers-color-scheme: light)" srcset="./grounding_graph.png">
  <img alt="Spanish Grammar Knowledge Graph" src="./grounding_graph.png" width="100%">
</picture>

### 🛠️ Agent Architecture & Orchestration
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

### 🔍 Agentic RAG in Action: A Walkthrough
```mermaid
%%{init: { 'theme': 'dark', 'themeVariables': { 'mainBkg': '#0d1117', 'primaryColor': '#0d1117', 'primaryTextColor': '#c9d1d9', 'primaryBorderColor': '#238636' } } }%%
graph TD
    RAG["<br/><b>1. Retrieval:</b> System identifies verb lemmas and grammatical structures from input.<br/><b>2. Grounding:</b> Validator Agent fetches 'Learning Hacks' and rules from the PostgreSQL Knowledge Graph.<br/><b>3. Validation:</b> Agent compares input against retrieved pedagogical rules to identify errors.<br/><b>4. Feedback:</b> Tutor Agent synthesizes response while Proposer Agent generates targeted cards.<br/><br/>"]
    style RAG fill:#0d1117,stroke:#238636,stroke-width:2px,color:#c9d1d9
```

---

## 🧰 Technical Toolbox

*   **Languages:** Python (FastAPI, SQLAlchemy), TypeScript (Vue 3), Go
*   **AI/LLM:** Gemini API, OpenAI, Agentic Workflows, Prompt Engineering
*   **Data:** PostgreSQL (Relational/JSONB), Knowledge Graph Design
*   **DevOps:** Docker, GCP (Cloud Run, Cloud Build), CI-CD

---

## 📫 Let's Connect!

*   **GitHub:** [ankixparlaibackend](https://github.com/tomstehling/ankixparlaibackend) | [ankixparlaifrontend](https://github.com/tomstehling/ankixparlaifrontend)
*   **Project Site:** [ankixparlai.com](https://ankixparlai.com) (In Development)

---
*Created with the help of my personalized AI engineering agent.*