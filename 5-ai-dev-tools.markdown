---
layout: page
title: "(5) AI dev tools"
permalink: /AI-dev-tools/
description: Last edit 26.0501
---

<br>

This section focuses on how to use AI IDEs to create AI project. The focus is on testing and learning. The focus for now is on the following AI IDEs:
- [(5.1) Cursor](/Cursor-overview/)
- [(5.2) GPT/Codex](/GPT-Codex-overview/)
- [(5.3) Claude](/Claude-dev-tools/)

<!-- <img src="/assets/ai_project_diagram_5.png" alt="drones" width="45%">  -->



<br>

## Demos (my current 26.0506 focus)

For the first 2 demos see
- Documentation: [#606\_ai_ides_.docx](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)
- Repo [602-2_D1-tool-LLM](https://github.com/terrytaylorbonn/602-2_D1-tool-LLM)


<br>

### Demo 2 jobradar_unified.py (what it does so far 26.0506)
Single app that combines:<br>
**1. Ingest —** Pulls jobs from Greenhouse (configured companies), normalizes and dedupes into MongoDB, optional LLM scoring (OpenAI primary, Anthropic fallback) with a simple cost tracker.<br>
**2. Gmail path (CLI)** — With GMAIL_* set, the same script run ingests LinkedIn-style job alerts from a Gmail label over IMAP, parses, dedupes, scores, and writes into the same jobs collection.<br>
**3. API (uvicorn jobradar_unified:app)** — FastAPI with Google OAuth (session + email allowlist) protecting job routes. Exposes health, jobs (list/detail), status updates, summary, /login / /me / /logout.<br>
**4. Digest (Step 7)** — GET /digest/preview builds the digest text without sending. POST /digest/send emails it (SMTP to Gmail by default, or Resend via DIGEST_SENDER=resend — S7e).<br>
**5. Google Doc digest (Step 7f)** — POST /digest/google-doc creates a new, timestamp-titled Google Doc in Drive with the same digest body, using OAuth tokens with Docs + drive.file scopes; optional DIGEST_DRIVE_FOLDER_ID and title prefix.
Config is env-driven (Mongo, LLM keys, Gmail, digest, Resend, Drive folder, Google OAuth secrets, etc.).<br>

<img src="/assets/job_radar_high_level.png" alt="drones" width="85%"> 

<img src="/assets/job_radar_digest_outputs.png" alt="drones" width="70%"> 

<img src="/assets/job_radar_notes.png" alt="drones" width="45%"> 


<br>

### Demo 1 Cursor / gpt-40-mini / MongoDB / n8n / index.html (26.0501)


<img src="/assets/cursor_demo1_00.png" alt="drones" width="50%"> 

Bearer token for basic security.

<img src="/assets/cursor_demo1_01.png" alt="drones" width="50%"> 

List of events in MongoDB.

<img src="/assets/cursor_demo1_02.png" alt="drones" width="65%"> 

Human language data input and resulting normalized input.

<img src="/assets/cursor_demo1_03.png" alt="drones" width="50%"> 

<img src="/assets/cursor_demo1_04.png" alt="drones" width="65%"> 

DB contents.

<img src="/assets/cursor_demo1_05.png" alt="drones" width="65%"> 

<br>

<!-- #### 2 Using Codex desktop Render plugin to manage Render.

<img src="/assets/cursor2_render.png" alt="drones" width="40%"> 

<br>  -->

26.0506 (v1 26.0428)
