# Harbour: Inbox Triage Assistant

An AI-powered support ticket classification and triage prototype built with reliability, structured outputs, and observability in mind. 

## Overview
**Harbour** automates incoming inbox triage by categorizing tickets using Large Language Models (LLMs). Instead of relying on raw text responses, it enforces strict schema validation, handles transient failures gracefully, and logs API usage across multiple model providers.

## Key Features
* **Multi-Provider Service Layer:** Abstracts LLM API calls to support two distinct providers, allowing seamless switching or fallback.
* **Call Logging & Observability:** Tracks request metadata, latency, token usage, and provider responses for debugging and auditing.
* **Structured Output Validation:** Enforces strict schema compliance on model responses for ticket classification.
* **Safe Retry Mechanism:** Automatically retries malformed responses or transient API errors with safe backoff boundaries.
* **Evaluation Suite:** Includes a curated evaluation dataset and report measuring classification accuracy and reliability.

## Project Structure
```text
├── src/
│   ├── service/       # Multi-provider LLM client & call logging
│   ├── triage/        # Prompt templates, schema validation & retry logic
│   └── eval/          # Evaluation runner and test dataset
├── reports/           # Mini-project 2 evaluation report & findings
└── README.md
```

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com<your-username>/harbour-inbox-triage.git
   cd harbour-inbox-triage
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure environment variables:**
   Add your API keys for both LLM providers in a `.env` file.

4. **Run the triage prototype or evaluation:**
   ```bash
   python -m src.eval.run_eval
   ```

