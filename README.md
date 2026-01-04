graph TD
    A[Frontend: React/Next.js] -->|API Calls| B[Backend: Node.js/Express]
    B -->|Query| C[(PostgreSQL Database)]
    B -->|Auth| D[Firebase/Auth0]
