# Comprehensive Seed Evaluation Flowchart in Seed Genebank

```mermaid
graph TD
    A[Start] --> B[Seed Receipt]
    B --> C[Initial Inspection]
    C -->|Accepted| D[Seed Cleaning & Drying]
    C -->|Rejected| Z[End]
    D --> E[Seed Viability Testing]
    E -->|Passed| F[Moisture Content Testing]
    E -->|Failed| E1[Second Viability Testing]
    E1 -->|Passed| F
    E1 -->|Failed| Z
    F -->|Passed| G[Seed Health Testing]
    F -->|Failed| F1[Re-Drying]
    F1 --> F2[Re-Testing]
    F2 -->|Passed| G
    F2 -->|Failed| Z
    G -->|Passed| H[Accessioning & Cataloguing]
    G -->|Failed| G1[Second Health Testing]
    G1 -->|Passed| H
    G1 -->|Failed| I[Documentation, Notification, & Disposal/Return]
    H --> J[Storage in Genebank]
    J --> Z[End]
