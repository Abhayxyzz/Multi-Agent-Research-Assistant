# 🔬 ResearchMind: Multi-Agent Research Assistant

Enter a topic and four specialized AI agents collaborate to search the web, scrape the best source, write a structured report, and critique it.

## How It Works

```
Topic → Search Agent → Reader Agent → Writer Chain → Critic Chain → Report + Feedback
```

| Step | Component | Role |
|------|-----------|------|
| 1 | **Search Agent** | Finds recent, reliable information on the topic |
| 2 | **Reader Agent** | Picks the most relevant URL and scrapes it for deeper content |
| 3 | **Writer Chain** | Drafts a structured research report from the collected material |
| 4 | **Critic Chain** | Reviews the report and returns feedback |

Search and Reader are tool-using **agents**; Writer and Critic are plain **chains** that transform text.

## Project Structure

```
├── Agents.py     # Agent and chain definitions
├── Tools.py      # Web search and scraping tools
├── Pipeline.py   # Orchestrates the 4 steps (CLI)
└── App.py        # Streamlit web UI
```

## Features

- Live pipeline view with per-agent status
- Expandable raw outputs from the Search and Reader agents
- Report rendered in Markdown, with one-click `.md` download
- Critic feedback shown alongside the report
- Runs from the terminal or the web app

## Getting Started

```bash
# 1. Clone the repo
git clone <your-repo-url>
cd <your-repo-name>

# 2. Install dependencies
pip install -r requirements.txt

# 3. Add your API keys to a .env file
# e.g. LLM key, search tool key

# 4a. Run the web app
streamlit run App.py

# 4b. Or run from the terminal
python Pipeline.py
```

## Tech Stack

Python · LangChain · Streamlit · LLM Agents · Web Search & Scraping

## Roadmap

- [ ] Feed critic feedback back to the writer for automatic revisions
- [ ] Scrape multiple sources instead of one
- [ ] Live per-step status updates in the UI

## License

MIT
