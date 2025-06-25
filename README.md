# n8n Workflow #11 – Water Quality Assessment with GPT-4

## 💧 Objective
This workflow analyzes freshwater quality data from a Google Sheet, processes it using GPT-4, and sends the results in the form of a structured email report.

## 🧾 Parameters processed per site
- Sampling date and location
- Water temperature
- pH (acidity/basicity)
- Conductivity (mineral content)
- Dissolved oxygen (mg/L)

## 🧠 GPT-4 Interpretation
The model generates, for each sampling point:
- A comment on water temperature and its ecological relevance
- An analysis of pH, conductivity, and oxygen levels
- A global water quality diagnosis
- A synthesis summarizing all analyzed points

## 🔧 Workflow Steps
1. `Manual Trigger` — Launches the workflow manually
2. `Google Sheets` — Reads environmental parameters from a spreadsheet (one row per site)
3. `Code` — Formats rows into a single structured JSON object
4. `OpenAI` — Processes the data using GPT-4 and a structured prompt
5. `Gmail` — Sends the final interpretation by email

## 📁 Project Structure (with comments)
```
final_report_En_Fr/                        # 📬 Example outputs of the workflow
├── final_mail_with_automatic_report.docx     # Automatic email in English with structured GPT response
└── Mail final avec interprétation.jpg        # Same output (French), final email preview as image

Workflow_screenshot_and_description/      # 🖼️ Technical and visual documentation of the workflow
├── Workflow 11.jpg                           # Screenshot of the n8n workflow
├── My_workflow_11.json                       # Native JSON export of the scenario
└── Workflow_11_principles_Fr_En.txt         # Summary of principles (bilingual notes)
```

## 🌍 Related Project (field application)
This workflow is the **analytical counterpart** to a real-world, field-based project:
👉 [AI_Assisted_Lake_Ecology (GitHub)](https://github.com/Jerome-openclassroom/AI_Assisted_Lake_Ecology)

That repository shows how real chemical and physical water sampling are performed and interpreted in practice.  
Feel free to refer to it for concrete applications in ecological contexts.

## 🛠️ Tools used
- Google Sheets API
- OpenAI GPT-4
- Gmail (OAuth2)
- n8n (automation)

## 📄 License
For educational and demonstrative use only.
