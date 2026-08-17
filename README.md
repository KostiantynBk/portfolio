# Kostiantyn Bakulin — AI & Backend Projects Portfolio

Junior Backend / AI Automation Developer focused on Python, AI agents, external API integrations, structured LLM outputs, SQLite persistence, workflow automation, market-data processing, and VPS-based monitoring.

This portfolio contains selected projects that demonstrate practical experience with:

* Python backend logic
* OpenAI API / OpenAI Responses API
* structured outputs
* SQLite and local persistence
* external API integrations
* Playwright browser automation
* email and workflow automation
* trading research workflows
* CLI tools and terminal-based agents
* systemd / Ubuntu VPS deployment
* RAG pipelines and vector search
* retrieval evaluation and LLM-as-judge

---

## Featured Projects

### 1. Automated Research Multi-Agent System

**Repository:** https://github.com/KostiantynBk/automatedResearch
**Tech stack:** Python, OpenAI API, Structured Outputs, Pydantic, FastAPI, SQLite, argparse

Automated Research Multi-Agent System is a Python backend prototype that researches a user-provided topic and generates a structured report through a sequential pipeline of specialized AI agents.

The system separates planning, research, writing, and critique into dedicated agent roles. It uses Pydantic models and OpenAI structured outputs to keep agent responses reliable and parseable, with fallback behavior when API credentials or external services are unavailable.

**Main features:**

* Planner agent breaks a research request into clear sub-tasks and success criteria.
* Researcher agent gathers and organizes findings for each task.
* Writer agent compiles findings into a readable structured report.
* Critic agent evaluates the final report for quality, completeness, clarity, and factual grounding.
* Includes an improvement loop when the critic score is below the configured quality threshold.
* Uses Pydantic models for structured data flow between agents.
* Saves research sessions, generated reports, critic feedback, and metadata in SQLite.
* Provides both a CLI interface and FastAPI endpoints with interactive docs.
* Handles missing OpenAI API keys and API failures through deterministic fallback behavior.

**Why it matters:**

This project demonstrates practical multi-agent orchestration, role-based AI system design, structured LLM outputs, local persistence, evaluation loops, CLI/API delivery, and reliability-focused backend engineering.

---

### 2. Terminal AI Trading Research Agent

**Repository:** https://github.com/KostiantynBk/terminalTradingAgent
**Tech stack:** Python, OpenAI Responses API, SQLite, Pydantic, Binance Public Market Data API, CLI, systemd, Ubuntu VPS

Terminal AI Trading Research Agent is a terminal-based AI trading research tool that fetches crypto OHLCV market data, reads local strategy rules, stores memory in SQLite, and produces structured long, short, watch, or no-trade research decisions.

The project is designed for research and paper-trading workflows only. It does not execute real trades.

**Main features:**

* Fetches crypto OHLCV data from the Binance public market data API.
* Reads local Markdown strategy rules from files.
* Uses the OpenAI Responses API with strict structured outputs.
* Produces structured decisions including bias, confidence, entry zone, stop loss, take profit, reasoning, setup warnings, and risk notes.
* Stores market snapshots, previous decisions, agent logs, and recent symbol history in SQLite.
* Includes deterministic backtesting commands for strategy heuristics.
* Supports TP/SL simulation, timeout handling, fees, slippage, overlap controls, and JSON/Markdown backtest reports.
* Generates timestamped JSON and Markdown research reports.
* Includes Ubuntu VPS deployment preparation with a bootstrap script and systemd service.

**Why it matters:**

This project demonstrates terminal-based AI agent development, local memory management, market-data processing, structured LLM output validation, API loops, and production-style monitoring.

---

### 3. X Market Signal Monitor

**Repository:** https://github.com/KostiantynBk/copyTrading
**Tech stack:** Python, Playwright, OpenAI Responses API, Pydantic, systemd, Ubuntu VPS

X Market Signal Monitor is an AI-powered market monitoring system that watches selected X profiles and detects posts containing trading-related views, position updates, or market commentary.

The system uses browser automation, structured LLM outputs, local persistence, and duplicate-prevention logic to create an auditable monitoring workflow.

**Main features:**

* Uses Playwright with a saved browser session to poll selected X timelines.
* Maintains login state and extracts recent post text, timestamps, links, and media metadata.
* Uses OpenAI Responses API with structured outputs.
* Extracts tickers, companies, sectors, sentiment, confidence, rationale, and supporting evidence.
* Compares new signals against recent posts from other watched accounts.
* Identifies same-ticker and same-sector opinions.
* Persists seen posts, extracted signals, analysis logs, and generated JSON reports.
* Includes Ubuntu VPS / systemd preparation for continuous monitoring.

**Why it matters:**

This project demonstrates browser automation, AI-based signal extraction, local data persistence, auditability, continuous monitoring, and practical automation around external data sources.

---

### 4. AI Email Triage & Reply Automation Agent

**Repository:** https://github.com/KostiantynBk/emailReply
**Demo:** https://youtu.be/gN160zCNbAA
**Tech stack:** Python, OpenAI API, email integration, database logging, Google Sheets / Telegram integration

AI Email Triage & Reply Automation Agent is an AI workflow tool that classifies incoming emails, extracts important information, generates context-aware draft replies, and logs processing results.

The project is designed to simulate a business email workflow where routine messages can be processed automatically while uncertain or sensitive emails are escalated for human review.

**Main features:**

* Classifies incoming emails into categories.
* Extracts key information from the email body.
* Generates context-aware draft replies using the OpenAI API.
* Produces structured outputs such as category, priority, summary, required action, confidence score, and draft reply.
* Adds fallback logic for uncertain, sensitive, or high-priority emails.
* Marks risky or unclear emails for human review instead of handling them automatically.
* Stores processed emails, generated replies, statuses, and error logs.
* Supports external workflow integrations such as Google Sheets and Telegram notifications.

This project demonstrates practical AI workflow automation, structured LLM outputs, fallback logic, database-backed tracking, and real business process automation.

---

### 5. Application Process Agent

**Repository:** https://github.com/KostiantynBk/jobAnalysis
**Demo:** https://youtu.be/-2XxQz76ZGk
**Tech stack:** Python, OpenAI Responses API, SQLite, JavaScript

Application Process Agent is an AI-powered job application assistant that analyzes job descriptions and compares them against a predefined resume profile.

The tool helps identify matched skills, missing skills, project improvement opportunities, and generates tailored application material.

**Main features:**

* Analyzes job descriptions against a predefined resume profile.
* Supports English and Ukrainian job descriptions.
* Uses OpenAI Responses API with structured outputs.
* Extracts key requirements and role keywords.
* Identifies matched and missing skills.
* Calculates a match score.
* Suggests which project to build or improve.
* Generates tailored CV bullet points.
* Generates short application notes in the selected language.
* Stores analyzed jobs, generated CV bullets, application notes, match results, and metadata in SQLite.
* Includes a browser-based interface for pasting job descriptions, viewing analysis, copying generated text, and saving jobs.
* Includes local rule-based fallback logic if the OpenAI API key is missing or the API request fails.

**Why it matters:**

This project demonstrates AI-assisted workflow automation, structured outputs, multilingual support, SQLite persistence, browser UI development, and fallback logic.

---

### 6. Lead Processing MVP

**Repository:** https://github.com/KostiantynBk/jobTask
**Tech stack:** Python, FastAPI, OpenAI API, SQLite, Telegram Bot API, Pydantic

Lead Processing MVP is a small backend prototype for processing landing-page lead submissions after a form is sent.

The project receives JSON lead data, normalizes it, generates an AI summary, classifies the lead, stores the result in SQLite, and sends a Telegram notification when credentials are configured.

**Main features:**

* Exposes a FastAPI endpoint for receiving lead submissions.
* Parses and validates JSON request bodies with Pydantic.
* Normalizes submitted fields such as email, budget, services, timeline, and source.
* Uses the OpenAI API to generate a concise summary of the lead.
* Classifies leads as hot, warm, or cold using a transparent rule-based score.
* Stores raw payloads, normalized payloads, AI summaries, scores, classifications, and notification status in SQLite.
* Sends Telegram notifications through the Telegram Bot API when bot credentials are configured.
* Includes example payloads and clear launch instructions for local testing.

**Why it matters:**

This project demonstrates a pragmatic MVP backend workflow: API input handling, JSON normalization, AI integration, lead scoring, local persistence, and external notification delivery.

---

### 7. MEDICA Business Analytics Dashboard

**Repository:** https://github.com/KostiantynBk/MEDICABusinessAnalyticsDashboard
**Tech stack:** Python, pandas, SQLite, SQL, Streamlit, Plotly, OpenAI API

MEDICA Business Analytics Dashboard is a simulated end-to-end business analytics system for a scaling medical/e-commerce company. The project combines sales, CRM, marketing, payment, refund, and customer-service data into a unified SQLite analytics layer, calculates key business KPIs, visualizes them in an interactive Streamlit dashboard, and generates automated business reports.

The project uses realistic synthetic data only, so it demonstrates a complete BI workflow without relying on private company data.

**Main features:**

* Generates synthetic business data for customers, orders, order items, products, marketing spend, CRM leads, payments, refunds, and support tickets.
* Loads all datasets into a SQLite analytics database with useful indexes.
* Calculates KPIs including revenue, gross profit, gross margin, CAC, LTV, ROAS, ROMI, CPO, conversion rate, retention, refund rate, and repeat purchase rate.
* Includes reusable SQL analysis for revenue, margin, CAC, ROAS/ROMI, CPO, conversion, retention, refunds, and profit leaks.
* Builds an interactive Streamlit dashboard with executive, marketing, CRM, product profitability, customer retention, and profit-leak analysis views.
* Generates an automated weekly Markdown business report with KPI summaries and recommendations.
* Includes optional OpenAI-powered business insight generation that uses only calculated KPI data.

**Why it matters:**

This project demonstrates practical business intelligence work: data generation, data modeling, SQL analysis, KPI design, dashboarding, reporting automation, and AI-assisted executive insights for a realistic medical e-commerce scenario.

---

### 8. Law Firm Voice Intake Agent

**Repository:** https://github.com/KostiantynBk/lawFirmVoiceIntakeAgent
**Tech stack:** Python, FastAPI, Vapi.ai, OpenAI API (gpt-4o), Pydantic, SQLite, vanilla JS

Law Firm Voice Intake Agent is a Python backend that integrates with Vapi.ai to handle inbound phone calls for a personal injury law firm. An AI agent named Alex guides callers through a structured 9-stage intake flow, automatically qualifies or disqualifies them, and logs structured lead data for attorney review.

The system is designed for Morrison & Associates, a fictional personal injury firm, and demonstrates how AI voice agents can replace manual phone screening at scale.

**Main features:**

* Handles Vapi.ai webhook events: call start, mid-call transcript turns, and end-of-call reports.
* Runs a 9-stage conversation state machine: greeting, case type, incident date, injury check, fault determination, treatment, contact capture, booking, and closing.
* Automatically detects ineligible cases based on statute of limitations (3+ years), no reported physical injury, or case type outside personal injury.
* Refers callers with non-personal-injury matters (divorce, criminal, contract) to a state bar referral line and sets outcome to REFERRED_OUT.
* Uses per-stage LLM slot extraction with structured JSON outputs to capture name, case type, incident date, injury status, fault, treatment history, phone number, and appointment slot.
* Extracts a full structured lead summary at end of call using `openai.beta.chat.completions.parse()` with a Pydantic response model.
* Persists all calls, turn-by-turn transcripts, and structured lead data in SQLite.
* Includes a single-file vanilla JS dashboard: call list with color-coded outcomes, full transcript view, and structured lead card per call. Auto-refreshes every 30 seconds.
* Conversation simulation tests cover happy path, old incident, no injury, wrong practice area, and difficult caller scenarios.

**Why it matters:**

This project demonstrates voice AI integration, multi-stage conversation orchestration, structured LLM outputs, business-rule gate checking, end-to-end lead capture, and a practical admin dashboard — all within a focused, real-world use case.

---

### 9. DocsRAG — Retrieval-Augmented Documentation Assistant

**Repository:** https://github.com/KostiantynBk/ragAssistant 
**Tech stack:** Python, OpenAI API, Chroma, Sentence-Transformers, LangChain, FastAPI, Pydantic, SQLite

DocsRAG is a production-style RAG pipeline that answers questions over a technical-docs corpus (LangChain docs) with cited, schema-validated responses. The project benchmarks two chunking strategies and two retrieval configurations, measuring quality with a purpose-built evaluation harness and an LLM-as-judge faithfulness check.

**Main features:**

* Ingests markdown documentation into two Chroma vector database collections using two chunking strategies: recursive character splitting and markdown-header-aware splitting.
* Retrieves relevant chunks via OpenAI `text-embedding-3-small` embeddings and cosine similarity search, then optionally re-scores results with a `cross-encoder/ms-marco-MiniLM-L-6-v2` cross-encoder.
* Generates answers with `gpt-4o-mini` using a strict context-grounding prompt; every answer includes inline source citations referencing doc ID and chunk index.
* Validates all outputs with Pydantic v2: `RAGAnswer` carries the answer text, a `sources` list, a `grounded` boolean, and latency.
* Runs an agent loop using OpenAI function-calling, exposing retrieval as a `retrieve_docs` tool so the model decides when and what to retrieve.
* Evaluates all four configurations (2 chunking × 2 reranker) with an automated harness reporting Hit@1/5/10, MRR, faithfulness score, and average latency.
* Logs every query and every evaluation run to SQLite for reproducible benchmarking.
* Serves the full pipeline via a FastAPI endpoint (`POST /ask`, `GET /eval/latest`, `GET /health`).
* Includes 14 unit tests covering chunking, retrieval, reranking, and the API layer.

**Why it matters:**

This project demonstrates end-to-end RAG engineering: chunking strategy comparison, embedding-based dense retrieval, cross-encoder reranking, structured output validation, agent-loop design, and a rigorous evaluation harness — all wired together into a deployable FastAPI service.

---

5. AI Support Ticket Triage Workflow
**Tech stack:** n8n, OpenAI API, Structured Output Parser, Google Sheets, Slack, Webhook/Form triggers

AI Support Ticket Triage Workflow is a low-code AI automation pipeline built in n8n that classifies incoming support tickets, drafts context-aware replies, and routes them for automatic logging or human approval based on priority and confidence.

The system is designed to simulate a real customer-support intake process, where an AI agent handles first-pass triage and drafting while urgent or low-confidence tickets are escalated to a human before any reply goes out.

**Main features:**

* Accepts ticket submissions via a form (or webhook, for real ticketing-system integration such as Zendesk/Intercom).
* Uses an LLM classification chain with a Structured Output Parser to guarantee valid, typed JSON — including automatic re-prompting on malformed model output.
* Produces structured fields: category, priority, sentiment, one-line summary, suggested reply, and confidence score.
* Conditional routing (Switch node) sends high-priority or negative-sentiment tickets down an escalation path, distinct from routine tickets.
* Human-in-the-loop approval gate via Slack ("Send and Wait for Response") — an agent reviews and approves or rejects the AI-drafted reply before anything reaches the customer.
* Logs every processed ticket — classification, draft reply, and outcome — to Google Sheets for auditability.
* Dedicated error-handling workflow: failed LLM calls or malformed input are caught and routed to a fallback path instead of failing silently.
* Input validation step rejects or flags empty/malformed submissions before they reach the model.

**Why it matters:**

This project demonstrates practical AI-to-business-system orchestration: webhook/API integration, structured LLM output validation, conditional routing logic, human-in-the-loop review gates, and production-style error handling — built in a low-code platform (n8n) that mirrors how AI gets integrated into existing business tooling in real companies, rather than built from scratch.

---

6. Observable AI Content Pipeline
**Tech stack:** n8n, OpenAI API, Langfuse (LLM observability), Structured Output Parser, Google Sheets

Observable AI Content Pipeline is an n8n workflow that generates business content (e.g. support-article drafts or outreach copy) through an LLM step instrumented end-to-end with observability — every run is traced, timed, costed, and compared against alternate prompt variants.

The project is designed to show how an AI workflow is monitored and iterated on once it's in production, not just how it's built.

Main features:

LLM generation step wrapped with Langfuse tracing, capturing the full input/output, token usage, latency, and per-run cost.
Structured Output Parser enforces a consistent schema on generated content, with automatic re-prompting on invalid output.
A/B branch that runs two prompt variants against the same input and logs both outputs side by side for comparison.
Cost and latency metrics logged per run to Google Sheets, enabling a simple dashboard view of drift or regressions over time.
Scheduled evaluation sub-workflow that re-runs a fixed set of test inputs periodically and flags outputs that fall below a quality threshold.
Error handling routes failed generations or trace-logging failures to a fallback path rather than dropping data silently.

Why it matters:

This project demonstrates LLM observability and evaluation discipline in a low-code environment — tracing, cost/latency monitoring, and prompt A/B testing — the production-monitoring layer that most AI automation builds skip entirely, and a skill set explicitly requested across current AI-automation job listings.

7. Multi-Agent Research Desk (n8n)
**Tech stack:** n8n, OpenAI API, AI Agent nodes, Execute Workflow sub-workflows, HTTP Request / Code nodes

Multi-Agent Research Desk is an n8n workflow implementing a supervisor/router pattern: a coordinating agent decomposes an incoming query, dispatches it to specialized sub-agents built as reusable sub-workflows, and merges their outputs into a single structured brief.

The project is designed to show agent orchestration and tool-use as a visual, inspectable system rather than a single monolithic prompt.

**Main features:**

* Supervisor agent (n8n AI Agent node) receives a query and decides which specialized sub-agent(s) to invoke.
* Dedicated sub-workflows, each triggered via "Execute Workflow," act as specialized agents: a web-research agent, a data/calculation agent, and a summarizer agent.
* Cost-aware routing: simple queries are handled by a cheaper model; the supervisor escalates to a stronger model only on low-confidence outputs.
* Conflict handling when sub-agents return contradictory information — the supervisor flags disagreement rather than silently picking one answer.
* Retry logic on individual sub-agent failures before the whole run is marked failed.
* Final structured output (via Output Parser) merges sub-agent results into a single report with per-section sourcing.

Why it matters:

This project demonstrates multi-agent system design and orchestration — task decomposition, tool-calling, sub-workflow reuse, cost-aware model routing, and failure handling across agents — implemented visually in n8n, complementing the code-based multi-agent system in project #1 by showing the same architectural pattern built with low-code orchestration tooling.

## Professional Experience

### Backend Engineer — Voxum

**App Store:** https://apps.apple.com/nl/app/voxum-app/id6759362982
**Role:** Backend Engineer
**Period:** 09/2024 – 02/2026
**Type:** Remote, NDA-protected codebase

Worked as a backend engineer on Voxum, an online trading automation startup app focused on automated crypto trading strategy signals.

**High-level responsibilities:**

* Integrated external crypto market data from the Bybit API into backend workflows.
* Contributed to backend logic for processing market data and generating strategy-based trading signals.
* Worked on a strategy-builder system where users could create custom trading strategies by combining predefined tools, entry conditions, validation rules, stop-loss, and take-profit parameters.
* Supported business logic for transforming user-defined strategy configurations into structured backend workflows.
* Worked under an NDA; private codebase and internal implementation details cannot be shared.

---

## Technical Focus Areas

### AI / LLM

* OpenAI API
* OpenAI Responses API
* structured outputs
* prompt design
* LLM-based classification
* confidence scoring
* fallback logic
* rationale extraction
* AI workflow automation

### Backend / APIs

* Python backend logic
* REST API concepts
* HTTP / JSON
* external API integrations
* API polling loops
* data ingestion workflows
* workflow automation

### Databases / Storage

* SQLite
* local persistence
* audit logs
* database-backed workflow tracking
* duplicate-prevention logic
* generated JSON and Markdown reports

### Automation / Deployment

* Playwright
* browser session automation
* scheduled polling
* CLI applications
* systemd services
* Ubuntu VPS deployment

### Trading / Market Data

* Bybit API
* Binance Public Market Data API
* OHLCV data processing
* trading signal workflows
* strategy configuration logic
* TP/SL research workflows
* deterministic backtesting

---

