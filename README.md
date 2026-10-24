# StackTrace Sloth 🦥

**Debug at your pace.**

StackTrace Sloth is a beginner-friendly AI debugging assistant that helps developers understand programming errors and find practical next steps.

## Why I Built It

Error messages can be confusing, especially when you're learning to code. I built StackTrace Sloth to make debugging less stressful by turning confusing errors into simple explanations and actionable suggestions.

## Features

- Explains programming errors in plain English.
- Identifies likely causes and suggests debugging steps.
- Provides a simple, responsive web interface.
- Uses the Gemma 3 1B model through Ollama.
- Supports local AI inference after the model has been downloaded.
- Does not execute submitted code.

## Tech Stack

- **Language:** Python
- **Backend:** FastAPI
- **AI runtime:** Ollama
- **Model:** Gemma 3 1B
- **Frontend:** HTML, CSS and JavaScript

## How It Works

1. The user pastes an error message or Python traceback.
2. The FastAPI backend sends the error text to the local Ollama API.
3. Gemma generates an explanation, identifies a likely cause and suggests debugging steps.
4. The web interface displays the response.

## Getting Started

### Prerequisites

Install [Python](https://www.python.org/downloads/) and [Ollama](https://ollama.com/).

### 1. Download the model

Open a terminal and run:

```bash
ollama pull gemma3:1b
```

### 2. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/stacktrace-sloth.git
cd stacktrace-sloth
```

Replace `YOUR_USERNAME` with your GitHub username after publishing the repository.

### 3. Create a virtual environment

```bash
python -m venv .venv
```

On Windows PowerShell, activate it:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the application

```bash
python -m uvicorn app.main:app --reload
```

Open [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser.

## Why Open-Weight AI?

Using an open-weight model gives developers more control over their AI tools and how they run.

With Gemma running locally through Ollama, error logs can be analyzed on the developer's own computer without sending them to a third-party AI API. After downloading the model, the application can perform inference without an internet connection, provided the local services are running.

Local inference still uses system resources, and model-generated suggestions may be incorrect. Always review suggested fixes before applying them.

## Current Limitations

- Currently designed to explain pasted errors and tracebacks.
- Does not automatically modify, execute or repair source code.
- Explanation quality and response time depend on the model and available hardware.

## Hacktoberfest 2026 — Week 3

**Theme:** Slow and Steady

This project explores how open-weight AI can reduce repetitive debugging effort and help developers understand errors one step at a time.

Built with Python, FastAPI, Ollama and Gemma.

## License

Add a license before publishing if you intend to make the project open source. The MIT License is one option for a small developer tool; choose it only if you want to publish under those terms.