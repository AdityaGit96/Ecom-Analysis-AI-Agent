# E_LENS — E-commerce Analysis AI Agent

AI-powered e-commerce data analysis system built with **LangGraph, LangChain, and Google Gemini**.

E_LENS turns natural-language questions into data analysis, visualizations, insights, and reports through a multi-agent workflow.

## Features

- 🤖 Multi-agent AI analysis
- 📊 Automated EDA, correlation & feature analysis
- 🔎 SQL-based analysis workflows
- 💡 AI-generated insights
- 📈 Visualization generation
- 📝 Automated PDF reports
- 👤 Human-in-the-loop approvals
- 🔍 LangSmith tracing & session logging

## Architecture

```text
User
  ↓
Orchestrator
  ↓
┌─────────────┬─────────────┬─────────────┐
│ FE Agent    │ SQL Agent   │ Insight Agent│
└─────────────┴─────────────┴─────────────┘
                 ↓
           Report Agent
                 ↓
          Final Analysis
Tech Stack

AI: LangGraph, LangChain, Google Gemini, LangSmith
Data: Pandas, NumPy, scikit-learn, LightGBM
App: Python, Streamlit, FastAPI
Storage: SQLite, SQLAlchemy
Reports: ReportLab, WeasyPrint

Run
git clone https://github.com/AdityaGit96/Ecom-Analysis-AI-Agent.git
cd Ecom-Analysis-AI-Agent

pip install -r requirements.txt

python main.py --file data/sample/ecommerce_sample.csv
Example
"Find variables most correlated with revenue"

→ Analyze data
→ Calculate correlations
→ Return results
→ Generate insights
Project Structure
src/
├── agents/
├── tools/
├── streamlit/
├── graph.py
├── state.py
└── human_in_the_loop.py
License

MIT
