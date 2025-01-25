# Organizational Chart

```mermaid
graph TD
  A[Customer] --> B[Project Management]
  A --> C[User]

  B --> D[Requirements Analysts / Business Analysts]
  B --> E[Designers and Developers]
  B --> F[Testers]
  B --> G[Quality]
  B --> H[Change Management]
  B --> I[Tech Support]

  subgraph SCM_Team_Org
    J1[SCM Manager] --> J2[SCM Librarian]
    J1 --> J3[SCM Toolsmith]
  end

  subgraph SCM_Team_Project
    K1[SCM Manager]
    K1 --> K2[SCM Toolsmith]
    K1 --> K3[SCM Librarian]
  end

  B --> SCM_Team_Org
  B --> SCM_Team_Project

  subgraph CCB[Configuration Control Board]
    L1[CCB Leader (Chair)] --> L2[CCB Members]
    L1 --> L3[CCB Screener]
    L1 --> L4[CCB Recorder]
    L1 --> L5[Impact Analysis Team]
    L2 --> M1[Subject Matter Experts (SMEs)]
    L2 --> M2[Customer/User Representative]
    L2 --> M3[Management-Level Personnel]
    L2 --> M4[Project Manager / Stakeholders]
    L2 --> M5[Configuration Management & QA Personnel]
  end

  B --> CCB

  %% Additional Role
  A --> N[Client Efforts Coordinator]
  N --> B
  N --> C