# Green & Clean Nairobi — RAG Analytics Chatbot (n8n)

An automated conversational analytics workflow built in **n8n** for Nairobi's **Green & Clean** environmental program. It translates natural-language questions into structured data queries, executes deterministic JavaScript calculations to prevent LLM hallucinations, and synthesizes concise, data-backed responses.

## Key Features
- **AI Query Interpretation:** Uses **Claude Haiku** to map user questions to the appropriate dataset, metric, and date range.
- **Multi-Sheet Data Routing:** Dynamically queries five operational Google Sheets datasets (*Greening Initiative*, *Sensitization Programs*, *Waste Collection*, *Truck Allocation vs. Waste Loads*, and *Environment Activities by Ward*).
- **Deterministic Math Engine:** Performs all aggregations, breakdowns, and filtering in JavaScript before passing ground-truth figures to the LLM.
- **Automated Chart Generation:** Builds dynamic QuickChart visualizations for rankings, trends, and category breakdowns.
- **Response Synthesis:** Uses **Claude Sonnet** to generate objective, third-person executive summaries.
- **Automated GitHub Backup:** Self-updating workflow branch that automatically commits workflow JSON updates to this repository upon save.

## Repository Structure
- `workflows/green-clean-nairobi-chatbot.json` — Exported n8n workflow definition (auto-synced via n8n Trigger).

  
# Automated n8n-to-GitHub Version Control Pipeline #
A self-updating CI/CD workflow branch built in n8n that monitors workflow save and activation events
-dynamically fetches the latest workflow JSON definition via the n8n REST API, 
- formats the structure
-  automatically commits timestamped backups directly to a GitHub repository without interrupting live user chat sessions
