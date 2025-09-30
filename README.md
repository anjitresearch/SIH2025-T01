🚀 SIH Project Repository – AI/ML-based Auto Evaluation of R&D Proposals

This repository contains the source code, data samples, and documentation for the Smart India Hackathon Problem Statement (SIH25180):
AI/ML-based Auto Evaluation of R&D Proposals for NaCCER, CMPDI Ranchi.

The system is designed to automatically evaluate R&D proposals based on:

✅ Novelty detection against existing projects

✅ Financial evaluation using funding guidelines

✅ Impact scoring (technical feasibility, industry relevance)

✅ Explainability of evaluation results

📂 Repository Structure
   SIH_Project_Repository/
│── README.md                → Project overview  
│── requirements.txt         → Python dependencies  
│── data/  
│   ├── raw/                 → Sample input proposals (CSV)  
│   └── processed/           → Cleaned proposals after preprocessing  
│── src/  
│   ├── preprocessing/       → Data cleaning scripts  
│   ├── models/              → Novelty, financial, and scoring modules  
│   └── utils/               → Explainability helpers  
│── notebooks/               → Jupyter notebooks for experiments  
│── results/                 → Sample output results (JSON)  
│── docs/                    → Documentation and project description  


⚙️ Installation

Clone or unzip the repository:

git clone <repo-url>
cd SIH_Project_Repository


Install dependencies:

pip install -r requirements.txt


(Optional) Install NLP models:

python -m spacy download en_core_web_sm

▶️ Usage
Preprocess proposals
from src.preprocessing.data_cleaning import clean_text

text = "Using AI to Improve Diagnosis Accuracy"
print(clean_text(text))

Run novelty detection
from src.models.novelty_detector import detect_novelty

result = detect_novelty("AI in healthcare for diagnosis support")
print(result)

Financial evaluation
from src.models.financial_evaluator import evaluate_financials

data = {"budget": 1000000, "expected_roi": 1.5}
print(evaluate_financials(data))

Scoring
from src.models.scoring import calculate_score

score = calculate_score(novelty=0.85, impact=0.9, roi=1.5)
print("Final Score:", score)

Explainability
from src.utils.explainability import explain_score

print(explain_score(0.92))

📊 Example Output
{
  "proposal_id": 1,
  "novelty": 0.85,
  "roi": 1.5,
  "final_score": 0.92
}

🌟 Key Features

Automated Evaluation → Reduces manual effort and biases

Transparent Scoring → Provides explainable AI-driven results

Financial Checks → Ensures compliance with S&T guidelines

Scalable → Can handle large volumes of proposals

📖 References

IEEE Xplore – AI in Proposal Evaluation Systems

ResearchGate – Machine Learning for Decision Support in R&D

Ministry of Coal (MoC) S&T Funding Guidelines
