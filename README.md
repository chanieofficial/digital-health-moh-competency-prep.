Digital Health MoH Competency Prep
A Python-based Streamlit learning platform for structured preparation for Ethiopian Ministry of Health (MoH) behavioral competency assessments. Built for the TODAY NURSE educational project.
Current features
Dashboard with learning pathway and local progress metrics
Study library covering 15 behavioral competency units grouped under Work, Human, and Result
Behavioral indicators and personal study notes
Practice questions with answer feedback and explanations
Mock examination builder
Local SQLite progress tracking
Source register and clear distinction between source examples and original practice items
Run locally
Python 3.10 or newer is recommended.
python -m venv .venv
# Windows: .venv\\Scripts\\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
streamlit run app.py
Deploy on Streamlit Community Cloud
Push the contents of this project folder to the root of your GitHub repository.
Open Streamlit Community Cloud and connect the GitHub repository.
Select app.py as the main file.
Deploy.
The app is designed to run without secrets or external API keys.
Project structure
digital-health-moh-competency-prep/
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
├── .streamlit/
│   └── config.toml
├── data/
│   ├── competencies.json
│   ├── questions.json
│   └── source_status.json
└── utils/
    └── storage.py
Reference sources and content integrity
The initial content model uses these user-provided references:
MoH Behavioral Competency Training - Edited.pptx — primary source for the competency categories, learning domains, competency descriptions, indicators, and sample questions.
222 Behavioral Competency in the Workplace (AutoRecovered).pdf — supplementary source. It describes Work, Human, and Result pillars and a 15-element behavioral framework; some labels differ from the MoH presentation.
emotional_intelligence_healthcare_masters.pptx — healthcare-focused emotional intelligence concepts, components, applications, challenges, and strategies.
Information Management Systems.pdf — uploaded source, but its text could not be extracted during this build. No content has been invented from it. Add verified information-management study material after an OCR-readable or text-based copy is available.
The app labels questions as either Source example (adapted from examples in the MoH presentation) or Original practice (newly written for practice and not an official exam question).
The original documents are not included in this ZIP. Keep them separately and only upload them to GitHub if you have permission to redistribute them.
Data and privacy
Progress and study notes are stored in a local SQLite file named progress.db.
The database is excluded from Git by .gitignore.
This first version has no login, user accounts, cloud synchronization, encryption, or multi-user access control.
Do not store personal, confidential, or identifiable employee or patient information.
On hosted deployments, local filesystem persistence may not be guaranteed across restarts or redeployments. Treat progress as temporary unless a persistent storage layer is added.
Development notes
Python + Streamlit
SQLite for local progress
JSON for editable learning content
No external services required
Disclaimer
This is an independent educational prototype, not an official Ministry of Health examination system. It does not guarantee exam outcomes. Always verify competency requirements and assessment instructions against current official MoH materials.
