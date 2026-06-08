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

---

## Featured Projects

### 1. Terminal AI Trading Research Agent

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

### 2. X Market Signal Monitor

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

### 3. AI Email Triage & Reply Automation Agent

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

### 4. Application Process Agent

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

