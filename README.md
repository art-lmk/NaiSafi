# Green & Clean Nairobi — RAG Analytics Chatbot (n8n)

An automated conversational analytics workflow built in **n8n** for Nairobi's **Green & Clean** environmental program[cite: 1]. It translates natural-language questions into structured data queries, executes deterministic JavaScript calculations to prevent LLM hallucinations, and synthesizes concise, data-backed responses[cite: 1].

## Key Features
- **AI Query Interpretation:** Uses **Claude Haiku** to map user questions to the appropriate dataset, metric, and date range[cite: 1].
- **Multi-Sheet Data Routing:** Dynamically queries five operational Google Sheets datasets (*Greening Initiative*, *Sensitization Programs*, *Waste Collection*, *Truck Allocation vs. Waste Loads*, and *Environment Activities by Ward*)[cite: 1].
- **Deterministic Math Engine:** Performs all aggregations, breakdowns, and filtering in JavaScript before passing ground-truth figures to the LLM[cite: 1].
- **Automated Chart Generation:** Builds dynamic QuickChart visualizations for rankings, trends, and category breakdowns[cite: 1].
- **Response Synthesis:** Uses **Claude Sonnet** to generate objective, third-person executive summaries[cite: 1].
- **Automated GitHub Backup:** Self-updating workflow branch that automatically commits workflow JSON updates to this repository upon save[cite: 2].

## Repository Structure
- `workflows/green-clean-nairobi-chatbot.json` — Exported n8n workflow definition (auto-synced via n8n Trigger)[cite: 2].
