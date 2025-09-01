# 📄 PDF Analyzer – Agentic Research & Reporting System

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


Real-World Use Cases of PDF Analyzer:

Academic Research & Literature Review
Problem: Manually reading hundreds of papers is time-consuming and overwhelming.
Upload a research paper → get a technical breakdown + executive summary in minutes
Compare findings across multiple studies using standardized outputs
Example: A neuroscience PhD student uses PDF Analyzer to process 20+ fMRI studies, extracting methodologies and results into structured summaries — cutting literature review time by 70%. 

Medical & Pharmaceutical Research
Problem: Keeping up with new clinical trials, drug studies, or medical breakthroughs is nearly impossible.
Analyze clinical trial reports, whitepapers, or journal articles
Extract key outcomes, dosages, side effects, and limitations
Generate plain-English summaries for non-specialists (e.g., hospital administrators)

Competitive Intelligence & Market Analysis
Problem: Competitors publish technical whitepapers or patents you need to understand — fast.
Ingest competitor research, patents, or technical blogs
Identify innovation trends, tech advantages, or R&D directions
Turn dense documents into executive briefings for leadership

Education & Corporate Training
Problem: Turning academic content into teachable material takes effort.
Convert research papers into teaching summaries or lecture notes
Break down complex topics (e.g., machine learning, economics) into digestible insights
Use executive summaries as student reading guides
