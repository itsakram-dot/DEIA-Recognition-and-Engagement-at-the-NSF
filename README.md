<img width="2977" height="1590" alt="YYTTG IBNOJIJO" src="https://github.com/user-attachments/assets/a1586921-db24-4bb9-8480-03da6b76fea6" />
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

## How to reproduce this analysis

1. Download the 2023 FEVS public use file from [opm.gov/fevs](https://www.opm.gov/fevs/).
2. Filter to `AGENCY == "NF"` (National Science Foundation). This yields the 1,070 responses used here.
3. Convert "X" (Do Not Know) and "Y" (I do not have accessibility needs) to `NA`.
4. Open `Project Code.qmd` in RStudio. Update the `read.csv()` path at the top to point to your filtered file.
5. Knit the file to reproduce the regression tables and plots.

The raw data is not included in this repo due to file size and privacy guidelines.

## My role

I took the lead on this project. I built the composite indices from the raw OPM items, wrote the R code for cleaning and modeling, and drafted the final report and recommendations. My teammates contributed to the literature review and the final presentation.

## Data dictionary

The full OPM codebook, mapping each question (Q1–Q91) to its survey text and index grouping, is available in the repository as `OPM Codebook Open in Excel.xlsx`.
