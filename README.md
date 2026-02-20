# Arhan Analytics: Automated Quantitative Valuation Engine

> **Note:** This is a proprietary commercial project currently in pre-launch. This repository serves as a technical showcase of the architecture and capabilities. The source code is private but can be demonstrated via a live walkthrough upon request.

## 🚀 Overview
**Arhan Analytics** is a high-performance quantitative analysis tool designed to automate the equity valuation process. It bridges the gap between rigid financial modeling and generative AI, reducing the time required to produce a comprehensive investment memo from hours to seconds.

Unlike standard screeners, this engine performs raw calculations from primary financial statements to derive **Intrinsic Value** using fundamental models, coupled with an AI agent that synthesizes a qualitative investment thesis.

## ⚡ Key Features

### 1. Automated DCF Engine

### 2. AI Financial Analyst (LLM Integration)


### 3. Professional Reporting Pipeline
* **PDF Generation:** Automates the creation of institutional-grade PDF investment memos.


## 🏗️ System Architecture

*(The system follows a modular data pipeline architecture)*

```mermaid
graph TD
    A[User Input: Ticker Symbol, WACC, Growth Rate] --> B[Data Ingestion Service]
    B --> C{Valuation Engine}
    C -->|Quantitative Data| D[DCF Model & Ratio Analysis]
    C -->|Context Vectors| E[AI Analyst Agent]
    D --> F[Report Generator]
    E --> F
    F --> G[Final Investment Memo]
```

## 📸 Sample Output

### 1. Dashboard/User Interface Snippet

<img width="1919" height="298" alt="Screenshot 2026-02-16 2154312" src="https://github.com/user-attachments/assets/d466e27c-4d86-45e9-98d9-6a137b120e1e" />
<img width="1919" height="938" alt="Screenshot 2026-02-16 215446" src="https://github.com/user-attachments/assets/0ebae63d-a295-4ccb-98a1-2b7be5eed40b" />




### Final Investment Memo Snippet


![NTNX Memo 1](https://github.com/user-attachments/assets/280e3e40-8b1c-474a-8b53-37d69290a8be)



## 🛠️ Tech Stack

* Core Logic: Python 3.10+

* Data Analysis: Pandas, NumPy

* Web Framework: FastAPI (Microservices backend)

* AI/ML: OpenAI API (Context-aware prompting)

* Reporting: WeasyPrint (PDF generation)

* Data Source: [Finance Modeling Prep (FMP), AlphaVantage]
