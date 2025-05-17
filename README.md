# n8n Workflow #11 – Water Quality Assessment with GPT-4

## 💧 Objective
This workflow analyzes freshwater quality data from a Google Sheet, processes it via GPT-4, and sends the result as a structured email.

## 🧾 Parameters processed per site
- Date and sampling location
- Water temperature
- pH (acidity/basicity)
- Conductivity (mineralization level)
- Dissolved oxygen (mg/L)

## 🧠 GPT-4 Interpretation
The model provides for each measurement point:
- A comment on water temperature and its implication
- Interpretation of pH, conductivity, and oxygen levels
- A global quality assessment of the water
- A synthesis of all points analyzed

## 🔧 Workflow Steps
1. `Manual Trigger` — Executes workflow manually
2. `Google Sheets` — Reads ecological parameters (one row per site)
3. `Code` — Formats the rows into a single JSON block (array of samples)
4. `OpenAI` — Interprets the structured data using GPT-4
5. `Gmail` — Sends the synthesized analysis by email (text format)

## 📁 Files included
- `My_workflow_11.json` — n8n native export
- `Workflow_11.txt` — Functional description and comments
- `README.md` — This file

## 🛠️ Tools used
- Google Sheets API
- OpenAI API (GPT-4)
- Gmail (OAuth2)

## 📄 License
Demonstration and educational use only.
