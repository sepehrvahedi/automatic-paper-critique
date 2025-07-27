# 🔬 Multi-Agent Academic Paper Review System

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/release/python-380/)
[![Status: Active](https://img.shields.io/badge/Status-Active-green.svg)](https://github.com/yourusername/multi-agent-review)

## 🎯 Overview

An innovative multi-agent system that leverages **4 different LLMs** to generate comprehensive, unbiased academic paper reviews through component-based analysis and consensus ranking. This system eliminates individual model biases by extracting specific critique components and using multi-LLM consensus to identify the most valuable insights.

### 🚀 Key Innovations

- **Component-Level Granularity**: Extracts and analyzes individual strengths, limitations, and suggestions
- **Multi-LLM Consensus**: Uses 4 different models (GPT-4o Mini, Gemini 2.0 Flash, Grok 3 Mini, Qwen3-235B)
- **Bias Elimination**: Randomizes component order to prevent ranking bias
- **Quality Optimization**: Selects only top 3 components from each category via Borda count consensus
- **Complete Transparency**: Generates detailed logs and analysis files

---

## 📊 System Architecture

![System Architecture](./diagrams/Automatic%20Critique%20Diagram.png)

[//]: # (---)

[//]: # ()
[//]: # (## 🔄 Process Methodology)

[//]: # ()
[//]: # (![Methodology]&#40;./diagrams/Innovations.png&#41;)

---

## 📋 Output Files

The system generates a comprehensive review package:

| File | Description |
|------|-------------|
| `1_critique_document.md` | Final academic critique ready for submission |
| `2_ai_collaboration_reflection.md` | Meta-analysis of the AI collaboration process |
| `3_interaction_logs.txt` | Detailed step-by-step process logs |
| `component_analysis/` | Individual component rankings and analysis |
| `individual_responses/` | Raw responses from each LLM |

---

## 🔬 Detailed Process Flow

![Sequence Diagram](./diagrams/Sequence%20Diagram.png)

---

## 🏆 Acknowledgments

- NotebookLM team for document processing capabilities
- OpenAI, Google, xAI, and Alibaba for providing robust API access
- Academic review community for methodology inspiration
