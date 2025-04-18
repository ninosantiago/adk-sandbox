# ADK Sandbox

This repository serves as a sandbox environment for experimenting with the Google Application Development Kit (ADK). The ADK simplifies the process of building, deploying, and managing applications on Google Cloud.

## Prerequisites

Before getting started, ensure you have the following installed:

- [Google Cloud CLI](https://cloud.google.com/sdk/docs/install)
- Python 3.11 or later
- Docker (for containerized environments)
- Virtual environment tools (`python3-venv`)

## Setup Instructions

### Prepare files and environment
```
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt

gcloud auth login
gcloud config set project [PROJECT_ID]
```

### Before running the app
```
touch multi_tool_agent/.env
```
Configure .env file
```
# If using Gemini via Google AI Studio
GOOGLE_GENAI_USE_VERTEXAI="False"
GOOGLE_API_KEY="yourkey"

# # If using Gemini via Vertex AI on Google CLoud
# GOOGLE_CLOUD_PROJECT="your-project-id"
# GOOGLE_CLOUD_LOCATION="your-location" #e.g. us-central1
# GOOGLE_GENAI_USE_VERTEXAI="True"
```

### Run app
```
adk web
```