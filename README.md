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
<img width="1919" height="938" alt="GOOGL Analysis 1" src="https://github.com/user-attachments/assets/34331a1d-536a-4976-97a3-f4e714e50016" />

<img width="1917" height="943" alt="GOOGL Analysis 2" src="https://github.com/user-attachments/assets/64d0b0ae-dad8-413d-8bfd-6285d860d22b" />


### 2. The Valuation Model (Code Snippet)
<img width="1833" height="960" alt="DCF Code Logic" src="https://github.com/user-attachments/assets/cdc80743-66f5-44df-b7f7-2751070a8c90" />

### 3. Final Investment Memo
<img width="690" height="872" alt="GOOGL PDF Report 1" src="https://github.com/user-attachments/assets/d1b19053-579d-4bb9-9f92-15832796a48b" />

<img width="688" height="885" alt="GOOGL PDF Report 2" src="https://github.com/user-attachments/assets/c48181af-0849-4ec5-8be1-c7ff6f2f1d44" />

<img width="690" height="883" alt="GOOGL PDF Report 3" src="https://github.com/user-attachments/assets/9d4ecaa9-9671-481f-98f0-896930fa1241" />


## 🛠️ Tech Stack

* Core Logic: Python 3.10+

* Data Analysis: Pandas, NumPy

* Web Framework: FastAPI (Microservices backend)

* AI/ML: OpenAI API / LangChain (Context-aware prompting)

* Reporting: WeasyPrint (PDF generation)

* Data Source: [Yahoo Finance, AlphaVantage]
