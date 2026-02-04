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
<img width="1915" height="939" alt="PLTR Analysis 1" src="https://github.com/user-attachments/assets/6ed2e1d4-a92a-420e-9e42-b97201acd1c5" />

<img width="1914" height="936" alt="PLTR Analysis 2" src="https://github.com/user-attachments/assets/b4fd700d-607b-4954-9fc9-08daffc983e0" />

<img width="1919" height="933" alt="PLTR Analysis 3" src="https://github.com/user-attachments/assets/2b84f698-2495-4828-a3d2-2aa46c86cc28" />


### 2. The Valuation Model (Code Snippet)
<img width="1840" height="957" alt="DCF Code Logic" src="https://github.com/user-attachments/assets/58710264-6bb4-435f-ad7c-13ba8960df76" />


### 3. Final Investment Memo
<img width="742" height="868" alt="Screenshot 2026-02-04 233030" src="https://github.com/user-attachments/assets/2b9c6c45-5a13-4b52-bdc0-dcbc5781fa79" />

<img width="697" height="862" alt="Screenshot 2026-02-04 233102" src="https://github.com/user-attachments/assets/7e7ba819-89e5-4752-a357-e912a6ccc6e4" />

<img width="554" height="871" alt="Screenshot 2026-02-04 233207" src="https://github.com/user-attachments/assets/46d931b1-8506-41c8-bdcc-b7b644655597" />


## 🛠️ Tech Stack

* Core Logic: Python 3.10+

* Data Analysis: Pandas, NumPy

* Web Framework: FastAPI (Microservices backend)

* AI/ML: OpenAI API (Context-aware prompting)

* Reporting: WeasyPrint (PDF generation)

* Data Source: [Yahoo Finance, AlphaVantage]
