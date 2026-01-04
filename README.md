### Project Architecture
```mermaid
sequenceDiagram
    participant U as User (Vue.js)
    participant A as Orchestrator (Python)
    participant KG as Knowledge Graph (Neo4j/NetworkX)
    participant LLM as LLM Agent
    
    Note over U, LLM: The "Grounding" Process
    U->>A: "Why is it 'el mapa' not 'la mapa'?"
    
    rect rgb(240, 248, 255)
        Note right of A: Step 1: Intent & Entity Extraction
        A->>LLM: Parse query for grammatical concepts
        LLM-->>A: Entities: ["Gender Exceptions", "Ending -ma"]
    end
    
    rect rgb(255, 250, 240)
        Note right of A: Step 2: Graph Traversal
        A->>KG: Query: (Noun)-[EXCEPTION]->(Gender)
        KG-->>A: Return Sub-graph: 'mapa' is Greek origin exception
    end

    rect rgb(230, 255, 230)
        Note right of A: Step 3: Synthesis
        A->>LLM: System Prompt + User Query + Graph Context
        LLM-->>A: Generate explanation grounded in rules
    end
    
    A->>U: Returns explanation with specific grammar rule
