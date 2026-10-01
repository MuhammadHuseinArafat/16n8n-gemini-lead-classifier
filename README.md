# 16n8n-gemini-lead-classifier

# Project 16: AI-Powered Lead Qualification & Sentiment Analysis Automation

## 📋 Business Problem
Sales teams often waste valuable hours manually reviewing dozens of incoming contact forms and inquiries. Inbound leads are frequently a mix of high-intent enterprise prospects ("Hot Leads") and low-intent inquiries, leading to delayed responses for critical business opportunities.

## 💡 Proposed Solution
Engineered an **AI-Driven Lead Qualification Engine** in n8n that leverages Google Gemini to automatically analyze incoming client messages, extract key business requirements, evaluate budget status, classify lead priority (Hot/Warm/Cold), and dynamically route the workflow via conditional branching.

## 🛠️ Architecture & Flow
1. **Trigger & Input:** Captures raw client inquiry text payloads via a simulated input node.
2. **AI Processing Layer (`Basic LLM Chain` + `Google Gemini`):** Uses specialized *System Prompts* to convert unstructured natural language into structured evaluation metrics (Lead Category, Budget Presence, and Requirement Summary).
3. **Conditional Routing (`IF Node`):** Automatically evaluates the AI output text to isolate high-priority prospects (*Hot Leads*) and route them to dedicated priority pipelines.

<img width="1193" height="512" alt="image" src="https://github.com/user-attachments/assets/de1535a6-7831-4b68-a3b5-410f2ae1691a" />

## 🧰 Tools & Nodes Used
- **Platform:** n8n (Self-hosted / Cloud)
- **AI Model:** Google Gemini Chat Model (`models/gemini-3-flash-preview`)
- **n8n Nodes:** 
  - Manual Trigger
  - Edit Fields (Set)
  - Basic LLM Chain
  - Google Gemini Chat Model
  - IF Node (Conditional Routing)

## 🚀 Business Value & Impact
- **Instant Response Capability:** Eliminates manual sorting delays for high-value enterprise prospects.
- **Resource Optimization:** Directs sales teams to focus strictly on qualified "Hot Leads" while automating secondary processing for others.
