# Arhan Analytics: Automated Quantitative Valuation Engine

> **Note:** This is a proprietary commercial project currently in pre-launch. This repository serves as a technical showcase of the architecture and capabilities. The source code is private but can be demonstrated via a live walkthrough upon request.

## 🚀 Overview
**Arhan Analytics** is a high-performance quantitative analysis tool designed to automate the equity valuation process. It bridges the gap between rigid financial modeling and generative AI, reducing the time required to produce a comprehensive investment memo from hours to seconds.

Unlike standard screeners, this engine performs raw calculations from primary financial statements to derive **Intrinsic Value** using fundamental models, coupled with an AI agent that synthesizes a qualitative investment thesis.

## ⚡ Key Features

### 1. Automated DCF Engine
* **Data Ingestion:** Fetches 5-year historical financial data (Income Statement, Balance Sheet, Cash Flow) via API.
* **Logic:** Implements a dynamic **Discounted Cash Flow (DCF)** model that calculates:
    * Free Cash Flow to Firm (FCFF)
    * Weighted Average Cost of Capital (WACC) with adjustable beta and risk-free rates.
    * Terminal Value using Gordon Growth Model.
* **Output:** Generates a precise Intrinsic Value per share and a "Margin of Safety" percentage.

### 2. AI Financial Analyst (LLM Integration)
* Integrates a Large Language Model (LLM) agent to act as a junior analyst.
* **Context Awareness:** The agent is fed the raw quantitative outputs (ratios, growth rates, margins) rather than generic text.
* **Analysis:** Generates natural language commentary on:
    * Revenue Growth Trajectory
    * Solvency & Liquidity Risks
    * Competitive Moat Analysis
    * Market Sentiment Summary

### 3. Professional Reporting Pipeline
* **PDF Generation:** Automates the creation of institutional-grade PDF investment memos.
* **Visualization:** Embeds dynamically generated charts (Revenue vs. Net Income, Margin Trends) directly into the report.

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

### 1. Dashboard/User Interface
<img width="1919" height="932" alt="Screenshot 2026-02-03 190851" src="https://github.com/user-attachments/assets/767e1bf6-bfc4-4d58-88ce-ccd32471b805" />

<img width="1919" height="936" alt="Screenshot 2026-02-03 190901" src="https://github.com/user-attachments/assets/ce748906-1995-4ec5-9945-f6590a9620a4" />

### 2. The Valuation Model (Code Snippet)
<img width="1840" height="957" alt="DCF Code Logic" src="https://github.com/user-attachments/assets/58710264-6bb4-435f-ad7c-13ba8960df76" />


### 3. Final Investment Memo


![NTNX Memo 1](https://github.com/user-attachments/assets/280e3e40-8b1c-474a-8b53-37d69290a8be)

![NTNX Memo 2](https://github.com/user-attachments/assets/df65c1ca-2f9c-4c69-9607-9f746aee5421)

![NTNX Memo 3](https://github.com/user-attachments/assets/9b4f0659-1c05-4a97-99ac-724578bce6d0)



## 🛠️ Tech Stack

* Core Logic: Python 3.10+

* Data Analysis: Pandas, NumPy

* Web Framework: FastAPI (Microservices backend)

* AI/ML: OpenAI API (Context-aware prompting)

* Reporting: WeasyPrint (PDF generation)

* Data Source: [Yahoo Finance, AlphaVantage]
