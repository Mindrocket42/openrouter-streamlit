## This README is based on Mindrocket's "Clueless Coder" standard

### Reasons for Fork
- dependencies in requirements.txt 'frozen' to allow repo to age gracefully
- improved README

### PREREQUISITES

##### - Python 3.11.10

##### - OpenRouter Account

##### - VSCode & Dev Containers are optional and only of value if you want to tinker with code

### If you aren't up and running in 15 minutes, WALK AWAY. OpenRouter Playground is a lot less painful

- If you are comfortable working with venv's, use Option 1
- If you don't see the point of venv's, use Option 2
- Option 3 and Docker. If you know, you know. If you don't know, AVOID

### Important Notices

#### Devcontainer
/.devcontainer/devcontainer.json has deliberately been misnamed ".devcontainer.json". This is to avoid VSCode or Docker launching Devcontainer for a user unfamiliar with the purpose and functionality of Devcontainers.
To use, rename the filename to "devcontainer.json"

#### Defaults
/shared/constants.py contains default OpenRouter settings including default LLMs.


```mermaid
graph TD
    A[Start] --> B[Ensure Git is installed]
    B --> C[Go to working directory]
    C --> D[Clone repo: git clone &lt;repo-url&gt;]
    D --> E{Choose setup option}
    
    E -->|Option 1: Conda/venv| F[Prerequisites:<br>1. Anaconda or Python installed<br>2. Familiarity with command line]
    F --> G[cd into subdirectory]
    G --> H[Create venv:<br>conda create -n myenv python=3.11.10<br>or<br>python -m venv myenv]
    H --> I[Activate venv:<br>conda activate myenv<br>or<br>myenv\Scripts\activate Windows<br>source myenv/bin/activate Unix]
    I --> J[pip install -r requirements.txt]
    J --> K[Ensure Streamlit is installed:<br>pip install streamlit]
    K --> L[streamlit run filename.py]
    
    E -->|Option 2: VSCode + Devcontainer| M[Prerequisites:<br>1. VSCode installed<br>2. Remote-Containers extension in VSCode]
    M --> N[Open repo folder in VSCode]
    N --> O[Ensure .devcontainer folder exists in repo]
    O --> P[Use command palette: Ctrl+Shift+P]
    P --> Q[Select 'Remote-Containers: Reopen in Container']
    Q --> R[Wait for container to build and start]
    
    E -->|Option 3: Docker| S[Prerequisites:<br>1. Docker installed and running<br>2. Familiarity with command line]
    S --> T[cd into subdirectory]
    T --> U[Ensure Dockerfile exists in repo]
    U --> V[docker build -t my-app .]
    V --> W[docker run -p 8501:8501 my-app]
    W --> X[Access app at http&colon;//localhost&frasl;8501]
    
    L --> Y[Access Streamlit app in web browser]
    R --> Z[Follow any additional setup instructions in VSCode terminal]
    X --> AA[End]
    Y --> AA
    Z --> AA

    style A fill:#f9f,stroke:#333,stroke-width:2px,color:#000
    style E fill:#bbf,stroke:#333,stroke-width:2px,color:#000
    style AA fill:#bfb,stroke:#333,stroke-width:2px,color:#000
```


## 🔀 OpenRouter + Streamlit Example App

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/mindrocket42/openrouter-streamlit?quickstart=1)

Starter examples for building LLM apps with Streamlit and [OpenRouter](https://openrouter.ai), using [OpenRouter OAuth PCKE](https://openrouter.ai/docs#oauth).


### Reasons for Fork
- requirements.txt is frozen to allow repo to age gracefully
- improved README

## Overview of the App

OpenRouter is a single access point, cost centre and API standard in a landscape of a growing number of LLMs. This repo is a minimum working example of using a single API to access multiple language models, including [OpenAI's o1-mini and o1-preview, Anthropic's Claude, Google's Gemini and many more](https://openrouter.ai/docs#models).

Current examples include:

- Chatbot
- File Q&A
- Langchain Quickstart
- Langchain PromptTemplate
- LangChain Search (requires a Serper.dev API key)

## Demo App

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://openrouter-42.streamlit.app/)

## Running the code

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
streamlit run Chatbot.py
```

## Setting API keys

Not needed! 
- Click the **Connect OpenRouter** button on the sidebar on the left and your API key will be auto-applied using an [OAuth PKCE flow](https://openrouter.ai/docs#oauth).
- If using LangChain search, enter your Serper API key in the field provided (also on the sidebar on the left of the screen