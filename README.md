# 🔀 OpenRouter + Streamlit Example App

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/mindrocket42/openrouter-streamlit?quickstart=1)

Starter examples for building LLM apps with Streamlit and [OpenRouter](https://openrouter.ai), using [OpenRouter OAuth PCKE](https://openrouter.ai/docs#oauth).

## Prerequisites
- Openrouter Account

## Changes
- requirements.txt changed to install older versions of;
    - openai
    - streamlit
    - langchain

## Overview of the App

This app showcases a growing collection of OpenRouter minimum working examples, using a single API to access multiple language models, including [OpenAI GPT, Anthropic Claude, Google Gemini and many more](https://openrouter.ai/docs#models).

Current examples include:

- Chatbot
- File Q&A
- Langchain Quickstart
- Langchain PromptTemplate
- LangChain Search

## Demo App

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://openrouter-42.streamlit.app/)

## Running the code

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
streamlit run Chatbot.py
```

## Getting API keys

Not needed! Click the **Connect OpenRouter** button and your API key will be auto-applied using an [OAuth PKCE flow](https://openrouter.ai/docs#oauth).
