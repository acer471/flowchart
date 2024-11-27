```mermaid
flowchart TD
    Start([Start]) --> SeedReceipt[Seed Receipt]
    SeedReceipt --> InitialInspection{Initial Inspection}
    InitialInspection -- "Rejected" --> End1([End])
    InitialInspection -- "Approved" --> Cleaning[Cleaning & Drying]
    Cleaning --> Viability{Seed Viability Testing}
    Viability -- "Failed" --> End2([End])
    Viability -- "Passed" --> Moisture{Moisture Content Analysis}
    Moisture -- "High" --> End3([End])
    Moisture -- "Low" --> Health{Seed Health Testing}
    Health -- "Failed" --> End4([End])
    Health -- "Passed" --> Accession[Accessioning & Cataloguing]
    Accession --> Storage[Storage in Genebank]
    Storage --> End5([End])
