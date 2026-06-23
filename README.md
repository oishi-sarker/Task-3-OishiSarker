# DecodeLabs AI Matchmaker: Tech Stack Recommender

An intelligent, data-driven career recommendation engine built using an **Input-Process-Output (IPO) architecture**. The system converts raw, unstructured user career preferences and skill tags into a high-dimensional vector space using **TF-IDF Vectorization** and scores matches using geometric **Cosine Similarity** arrays.

---

## 🚀 Core Architectural Features

- **Automated Data Ingestion:** Reads structured job description profiles dynamically from a flat-file database schema (`raw_skills.csv`).
- **Mathematical Alignment Engine:** Computes an angular distance metric (Cosine Similarity) between user profile clusters and job requirements to deliver length-invariant ranking coefficients.
- **Cold-Start Fallback Strategy:** Built-in programmatic guardrail that intercepts empty user vectors to surface global trending pathways instead of breaking the matrix calculations.
- **Isomorphic Optimization:** Limits output vectors to a strict Top-3 presentation format to eliminate user choice overload.

---

## 🛠️ How It Works (The Core Pipeline)

```text
[ INPUT LAYER ]     --> User enters 3 primary technical skills or interests
                            ↓
[ PROCESSING LAYER ] --> Text merged with database arrays
                     --> TF-IDF Matrix Weight Matrix Transformation
                     --> Cosine Similarity Math computes angular distance 
                            ↓
[ OUTPUT LAYER ]    --> Dataset sorted descending & truncated to Top 3 Matches (%)
```

1. **TF-IDF Vectorization (Term Frequency-Inverse Document Frequency):** Evaluates user inputs against standard career paths. It rewards unique technical keywords (e.g., `tensorflow`, `kubernetes`) while down-weighting generic tokens.
2. **Cosine Similarity Calculations:** Instead of looking at simple substring matches, it treats skills as directional coordinates on a multi-dimensional grid. It calculates the geometric angle between your profile and the career roles, ensuring highly accurate matching regardless of short or long word descriptions.

---

## 📂 Project Directory Structure

```text
DecodeLabs_Project3/
│
├── .venv/                  # Local isolated environment binaries
├── raw_skills.csv          # Structured skill vocabulary database
├── recommender.py          # Primary application execution script
└── README.md               # Production architecture documentation
```

---

## 📦 System Installation & Setup

Follow these exact steps to deploy, configure, and execute the algorithm on your local machine:

### 1. Clone the Workspace & Navigate
```bash
git clone https://github.com/oishi-sarker/Task-3-OishiSarker
```

### 2. Configure Your Python Virtual Environment
```powershell
# Create the local isolated environment folder
python -m venv .venv

# Activate environment (Windows PowerShell)
& c:/Users/MY/OneDrive/Desktop/DecodeLabs_Project3/.venv/Scripts/Activate.ps1

# Activate environment (macOS/Linux)
source .venv/bin/activate
```

### 3. Install Vector Science Dependencies
Ensure your environment is active `(.venv)` and install the required processing libraries:
```bash
pip install pandas scikit-learn
```

---

## 💻 Execution & Verification

Run the primary application runner module inside your terminal:
```bash
python recommender.py
```

### Profile Test Case Validation
When prompted by the terminal pipeline interface, stream the following sample parameters:
- **Skill 1:** `python`
- **Skill 2:** `machine learning`
- **Skill 3:** `pandas`

#### Expected Mathematical Output Matrix:
```text
==================================================
           RECOMMENDED TECH STACKS (TOP 3)       
==================================================
 RANK 1 | Data Scientist
        -> Angular Match Alignment: 55.28%
--------------------------------------------------
 RANK 2 | Backend Developer
        -> Angular Match Alignment: 10.84%
--------------------------------------------------
 RANK 3 | DevOps Engineer
        -> Angular Match Alignment: 0.00%
==================================================
Execution complete. Ready for commercial-grade graduation.
==================================================
```

---
*Developed as part of the DecodeLabs AI Engineering Curriculum.*
