# YouTube Research Agent

An automated research agent that discovers relevant YouTube videos and extracts structured transcripts for downstream research workflows.

## Overview

The agent combines browser automation and the YouTube Transcript API to automate the process of discovering videos and collecting transcript data.

Given a person's name, an optional topic, and the desired number of videos, the agent:

1. Builds a targeted YouTube search query.
2. Searches YouTube using Selenium and a headless Chrome browser.
3. Extracts video metadata and identifiers.
4. Retrieves available transcripts using the YouTube Transcript API.
5. Handles missing, unavailable, or disabled transcripts.
6. Supports transcript language selection with fallback handling.
7. Produces structured research results.
8. Saves results as JSON and combined transcript text.

## Workflow

```text
Person + Topic
      ↓
Search Query Generation
      ↓
YouTube Browser Automation
      ↓
Video Discovery
      ↓
Video ID Extraction
      ↓
Transcript Retrieval
      ↓
Language & Error Handling
      ↓
Structured Results
      ↓
JSON / TXT Output
```

## Technologies

* Python
* Selenium
* Google Chrome / ChromeDriver
* YouTube Transcript API
* webdriver-manager
* JSON
* Regular Expressions

## Key Engineering Features

* Headless browser automation
* Automated browser-driver management
* Structured data extraction
* Multilingual transcript support
* Transcript fallback handling
* Exception handling for unavailable data
* Machine-readable JSON outputs
* Transcript metadata and timestamps
* Automatic browser resource cleanup

## Example Input

```text
Person: Jensen Huang
Topic: AI
Videos: 3
```

## Example Output

The agent returns structured research data containing:

* Video metadata
* Transcript text
* Transcript language
* Language code
* Generated/translated status
* Transcript length
* Snippet timestamps
* Processing statistics

## Project Structure

```text
youtube-research-agent/
├── README.md
├── requirements.txt
├── src/
│   └── youtube_transcript_agent.py
└── notebooks/
    └── Video_Transcription_Agent.ipynb
```

## Project Status

**Completed — Initial Version**

Future iterations may extend the agent with additional data sources, LLM-based analysis, summarization, evaluation, and multi-agent research workflows.
