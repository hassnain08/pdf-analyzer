# 📄 PDF Analyzer – Autonomous Research & Reporting System

An AI-powered agentic system that reads, understands, and summarizes academic or research PDFs using **CrewAI**. This project automates document analysis with a two-agent pipeline: one for deep technical breakdown, another for executive summarization.

Built with Python and CrewAI, this system turns dense research papers into structured insights — ideal for researchers, analysts, and knowledge workers.

---

## 🚀 Overview

PDF Analyzer uses autonomous AI agents to:
1. **Analyze** a research paper section-by-section (Abstract, Methods, Results, etc.)
2. **Extract** key findings, figures, equations, and limitations
3. **Generate** a technical markdown summary
4. **Produce** an executive summary in plain English

Perfect for:
- Academic literature review
- Competitive intelligence
- Research automation
- Executive briefing generation

---

## 🧠 How It Works

### Agents
| Agent | Role | Responsibility |
|------|------|----------------|
| `researcher` | Senior PDF Research Analyst | Deep analysis of the paper, section breakdown, interpretation of visuals/tables, insight extraction |
| `reporting_analyst` | PDF Insights Reporting Analyst | Converts technical findings into a concise, accessible executive summary |

### Tasks
1. **`research_task`**  
   - Input: Raw text from a PDF (`{pdf_content}`)
   - Output: Structured technical analysis in markdown
   - Focus: Thesis, methodology, results, figures, limitations

2. **`reporting_task`**  
   - Input: Output from `research_task`
   - Output: Plain-English executive summary + bullet points
   - Final report saved to `report.md`

### Workflow
```text
PDF Text → Researcher Agent → Technical Summary → Reporting Analyst → Executive Summary (report.md)
