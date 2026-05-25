# Location Intelligence ADK Agent with MCP Servers 
![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Google ADK](https://img.shields.io/badge/Google-ADK-green)
![Gemini](https://img.shields.io/badge/Gemini-3.1_Pro-orange)
![MCP](https://img.shields.io/badge/MCP-Integrated-purple)
![BigQuery](https://img.shields.io/badge/BigQuery-Analytics-blue)

Built an AI-powered bakery intelligence agent using Google ADK, BigQuery, Google Maps, MCP servers, and Gemini 3.1 Pro.

---

# Introduction

This project demonstrates how to build a multi-tool AI agent capable of combining:

- BigQuery analytics
- Google Maps intelligence
- MCP server integrations
- Gemini reasoning

The agent helps analyze bakery business opportunities using:

- demographic analysis
- foot traffic intelligence
- competitor pricing
- sales forecasting
- location-based reasoning

This implementation was built locally using Google ADK and MCP architecture.

---

# Features

- Google ADK based agent orchestration
- MCP server integration
- BigQuery analytics agent
- Google Maps intelligence tools
- Gemini-powered reasoning
- SQL execution workflows
- Multi-tool orchestration
- Context-aware responses
- Handles unsupported queries gracefully

---

# Technologies Used

- Google ADK
- Gemini 3.1 Pro
- MCP
- BigQuery
- Google Maps API
- Python
- Cloud Shell

---

# Project Structure

```text
launchmybakery/
├── data/
├── adk_agent/
│   └── mcp_bakery_app/
│       ├── agent.py
│       ├── tools.py
│       └── .env
├── setup/
└── cleanup/
```

---

# Prerequisites

Requirements:

- Google Cloud Project
- Billing Enabled
- Web Browser
- Basic terminal knowledge

---

# Setup Google Cloud

## Create or Select a Project

1. Open Google Cloud Console
2. Create or select a project
3. Enable billing

---

# Start Cloud Shell

Activate Cloud Shell from the top-right corner.

Verify authentication:

```bash
gcloud auth list
```

Verify active project:

```bash
gcloud config get project
```

Export project ID:

```bash
export PROJECT_ID=$(gcloud config get project)
```

---

# Clone Repository

```bash
git clone https://github.com/google/mcp.git
```

Navigate to project:

```bash
cd mcp/examples/launchmybakery
```

---

# Authenticate

Authenticate with Google Cloud:

```bash
gcloud auth application-default login
```

If the session exceeds 60 minutes, re-authenticate.

---

# Configure Environment & BigQuery

Run environment setup:

```bash
chmod +x setup/setup_env.sh
./setup/setup_env.sh
```

This script:

- enables APIs
- creates `.env`
- configures Maps API key

Setup BigQuery:

```bash
chmod +x ./setup/setup_bigquery.sh
./setup/setup_bigquery.sh
```

This script creates:

- Cloud Storage bucket
- BigQuery dataset
- required tables

---

# Verify Dataset in BigQuery

Dataset:

```text
mcp_bakery
```

Tables created:

- demographics
- bakery_prices
- sales_history_weekly
- foot_traffic

---

# Install ADK

Create virtual environment:

```bash
python3 -m venv .venv
```

Activate environment:

```bash
source .venv/bin/activate
```

Install ADK:

```bash
pip install google-adk==1.28.0
```

Navigate to agent directory:

```bash
cd adk_agent/
```

---

# MCP Tool Configuration

## Maps MCP Toolset

Used for:

- place search
- competition analysis
- route calculations
- location intelligence

## BigQuery MCP Toolset

Used for:

- SQL execution
- sales analytics
- demographic analysis
- forecasting

---

# Agent Definition

The agent uses Gemini 3.1 Pro for reasoning and tool orchestration.

Capabilities:

- BigQuery reasoning
- Maps reasoning
- unified business intelligence
- multi-tool execution workflows

---

# Run the Agent

Navigate to:

```bash
cd adk_agent/
```

Start ADK web server:

```bash
adk web --allow_origins 'regex:https://.*\.cloudshell\.dev'
```

Expected output:

```text
ADK Web Server started
http://127.0.0.1:8000
```

---

# Open ADK UI

Option 1:

```text
http://127.0.0.1:8000
```

Option 2:

Use Cloud Shell Web Preview and expose port `8000`.

---

# Example Prompts

## Competition Analysis

```text
Search for bakeries in that zip code to see if the market is saturated.
```

## Premium Pricing

```text
Find the maximum price for a Sourdough Loaf in the LA Metro area.
```

## Revenue Forecast

```text
Forecast December 2025 revenue using historical sales data.
```

## Logistics Validation

```text
Find the nearest Restaurant Depot and ensure drive time is under 30 minutes.
```

---

# Screenshots
<img width="3830" height="1507" alt="Firefly" src="https://github.com/user-attachments/assets/beda5bc1-acad-465c-9f66-0234d770a318" />
<img width="3040" height="1140" alt="ec9e6bf168cf426799f85be64adc19b8" src="https://github.com/user-attachments/assets/ad0d1b13-7254-4a8a-ae1a-02d4e1a9f147" />


## MCP Workflow & Tool Orchestration

Shows the ADK execution graph with MCP tool calls and SQL execution flow.

```md
![Workflow](screenshots/workflow.png)
```

---

## Unsupported Query Handling

The agent correctly identifies unsupported geography requests and explains dataset limitations instead of hallucinating responses.

```md
![Query Validation](screenshots/query-validation.png)
```

---

# Observations

The agent demonstrates:

- multi-step reasoning
- SQL tool execution
- structured workflow orchestration
- dataset-aware responses
- rejection of unsupported queries
- integration of external intelligence systems

---

# Cleanup

Run cleanup script:

```bash
chmod +x ../cleanup/cleanup_env.sh
./../cleanup/cleanup_env.sh
```

Removes:

- BigQuery datasets
- Cloud Storage buckets
- API keys

---

# Key Learnings

- Infrastructure automation using setup scripts
- MCP integrations with ADK
- Multi-tool AI orchestration
- Location intelligence workflows
- Dataset-aware reasoning
- Business intelligence with Gemini

---

# Conclusion

This project demonstrates how AI agents can combine:

- enterprise analytics
- real-world mapping intelligence
- business forecasting
- competitive analysis

using:

- MCP
- Gemini
- BigQuery
- Google Maps
- Google ADK

---

# Certifications & Event Participation

This project was built as part of the AI Agent Builder ecosystem and hands-on ADK + MCP learning initiatives.

## Build with AI Agent Builder Camp Certificate

<img width="590" height="412" alt="image" src="https://github.com/user-attachments/assets/dc7e7a0c-b867-4d45-adf8-1cf2bc68f7d2" />


---

## Build with AI 2026 Attendee Badge

<img width="1453" height="700" alt="Screenshot from 2026-05-25 21-39-22" src="https://github.com/user-attachments/assets/1649380d-3b6f-42d8-8279-4c9b39dd7d40" />


---

These programs focused on:

- AI agent development
- Google ADK workflows
- MCP integrations
- Gemini-powered reasoning systems
- Multi-tool orchestration
- Real-world AI applications
