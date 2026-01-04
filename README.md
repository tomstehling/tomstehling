### Project Architecture
```mermaid
graph TD
    A[User Browser] -->|Interaction| B[React Frontend]
    B -->|REST API| C[Express Backend]
    C -->|CRUD Operations| D[(Database)]
