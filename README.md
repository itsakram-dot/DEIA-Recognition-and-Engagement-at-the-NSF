flowchart LR
    classDef predictor fill:#E3F2FD,stroke:#1E88E5,stroke-width:2px,color:#000000
    classDef outcome fill:#FFF3E0,stroke:#F57C00,stroke-width:2px,color:#000000

    REC["Recognition<br/>Q17, Q35, Q69"]:::predictor
    AGI["Agile Practices<br/>Q13, Q14, Q27–Q31,<br/>Q42, Q64, Q65"]:::predictor
    DEIA["DEIA Climate<br/>Q73–Q85"]:::outcome
    ENG["Engagement<br/>16 items"]:::outcome

    REC -->|"B = 0.90, R² = 0.55"| DEIA
    AGI -->|"B = 0.70, R² = 0.52"| DEIA
    REC -->|"B = 1.01, R² = 0.62"| ENG
    AGI -->|"B = 0.85, R² = 0.70"| ENG

# DEIA, Recognition, and Engagement at the NSF

A regression analysis of National Science Foundation employees, using the 2023 Federal Employee Viewpoint Survey (FEVS).

## The question

Federal agencies invest in recognition programs and agile project management. Do either of them relate to how employees perceive DEIA and how engaged they report being?

## The model

```mermaid
flowchart LR
    classDef predictor fill:#E3F2FD,stroke:#1E88E5,stroke-width:2px,color:#000000
    classDef outcome fill:#FFF3E0,stroke:#F57C00,stroke-width:2px,color:#000000

    REC["Recognition<br/>Q17, Q35, Q69"]:::predictor
    AGI["Agile Practices<br/>Q13, Q14, Q27–Q31,<br/>Q42, Q64, Q65"]:::predictor
    DEIA["DEIA Climate<br/>Q73–Q85"]:::outcome
    ENG["Engagement<br/>16 items"]:::outcome

    REC -->|"B = 0.90, R² = 0.55"| DEIA
    AGI -->|"B = 0.70, R² = 0.52"| DEIA
    REC -->|"B = 1.01, R² = 0.62"| ENG
    AGI -->|"B = 0.85, R² = 0.70"| ENG
