# 🧠 AI-Powered Financial Content Creator

A multi-agent AI system that autonomously creates, refines, and formats high-quality financial content — including blog posts and social media snippets — using real-time market data and news.

---

## 🚀 What It Does

This system uses **CrewAI agents** to automate the entire content creation pipeline:

1. **📡 Market News Monitor Agent**  
   Tracks the latest financial news based on a given subject (e.g. “US-China tariffs”), summarizing impactful headlines.

2. **📊 Data Analyst Agent**  
   Analyzes market trends and economic indicators to identify actionable insights.

3. **✍️ Content Creator Agent**  
   Generates engaging blog content and social media posts from insights provided by the above agents.

4. **🧐 Quality Assurance Agent**  
   Refines and formats the content using markdown, ensuring clarity, structure, and brand alignment.

---

## 💼 Use Case

Ideal for:
- Financial blogs and media platforms
- Automated newsletter creation
- Market intelligence publishing
- Anyone needing timely, data-driven financial content

---


## 🛠️ Tech Stack

- **CrewAI** – Multi-agent orchestration
- **LangChain / LLMs** – Natural language generation
- **YAML Configs** – Agent & task modular setup
- **Jupyter Notebook** – For testing and orchestration
- **Markdown output** – For clean blog-ready formatting

---


## 🧪 Performance Benchmarks

| Agent                      | Task Description                        | Avg Time (approx) |
|---------------------------|-----------------------------------------|-------------------|
| 📡 Market News Monitor     | Scrapes live financial news             | ~45 seconds       |
| 📊 Data Analyst Agent      | Extracts and interprets insights        | ~60 seconds       |
| ✍️ Content Creator Agent   | Generates blog + social media content   | ~75 seconds       |
| ✅ Quality Assurance Agent | Formats content in markdown             | ~30 seconds       |
| ⏱️ **Total Runtime**       | End-to-end pipeline execution           | **~3.5 minutes**  |

> 🧠 Benchmarks based on `mistral-large-latest` model and real-time web scraping.

---


## 🤖 LLM Models Used

This project uses open-weight models from [Mistral](https://mistral.ai/), accessed via the **LiteLLM** routing layer.

### 🔹 `mistral-small-latest`
- Lightweight and fast
- Best for retrieval tasks and embeddings
- Used in: `WebsiteSearchTool`, `embedder`, lightweight analysis

### 🔹 `mistral-large-latest`
- Strong reasoning and summarization capabilities
- Handles long, structured generation tasks
- Used in: All core agents (`llm=llms['large']`) — blog writing, analysis, formatting

> Both models are accessed through the `mistralai` provider with `LiteLLM`, allowing flexible switching, logging, and future fallback support.

---


## 🧪 How to Run

1. Install dependencies:

```
pip install -r requirements.txt
```
2. Set your environment variables:

```
export MISTRAL_API_KEY=your_key_here
export SERPER_API_KEY=your_key_here
```
3. Launch the notebook:
```
jupyter notebook main.ipynb
```
4. Provide your topic (e.g. "US-China tariffs") and let the agents do the rest.
