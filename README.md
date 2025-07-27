<<<<<<< HEAD
# data-analyst-agent
=======
# TDS Data Analyst Agent

A generic data analyst API agent that uses LLMs to source, prepare, analyze, and visualize any data. Exposes a single POST /api/ endpoint for data analysis tasks.

## Features
- Accepts natural language data analysis tasks
- Uses LLMs to plan and execute data sourcing, analysis, and visualization
- Returns answers and plots as JSON (with base64-encoded images)

## Setup

```bash
pip install -r requirements.txt
```

## Environment Variables

Set your OpenAI API key before running:

```bash
export OPENAI_API_KEY=sk-...
```

On Windows (cmd):

```cmd
set OPENAI_API_KEY=sk-...
```

## Run Locally

```bash
uvicorn main:app --host 0.0.0.0 --port 8000
```

## API Usage

POST /api/
- Accepts a file (multipart/form-data) or raw text body with the analysis task
- Returns a JSON response with answers and plots

Example:

```bash
curl -X POST "http://localhost:8000/api/" -F "file=@question.txt"
```

## License
MIT 
>>>>>>> f9426e1 (Initial commit)
