# Data Science Salary Analysis — U.S. Market

An exploratory data analysis of data science salaries in the United States, covering roles, experience levels, remote work trends, and required skills.

---

## 🎯 Project Goals

- Understand what U.S. data science roles actually pay across seniority levels
- Identify which roles and skills command the highest compensation
- Provide an honest baseline for entry-level job seekers

---

## 📊 Key Findings

### 💰 U.S. Salary Landscape
- **Overall median salary: $138,175** — with a range of $25K–$600K depending on role and seniority
- Salaries grew ~19% from 2020 ($118K median) to 2021–2022 ($140K median)

### 📈 Experience Premium
| Level | Median Salary |
|---|---|
| Entry | $90,000 |
| Mid | $118,000 |
| Senior | $147,800 |
| Executive | $224,000 |

Each level up adds roughly $30–50K in median pay.

### 🏆 Highest-Paying Roles (min. 3 listings)
| Role | Median Salary |
|---|---|
| Principal Data Scientist | $227,500 |
| Principal Data Engineer | $200,000 |
| Data Architect | $180,000 |
| Analytics Engineer | $179,850 |
| Machine Learning Engineer | $174,998 |

### 🏠 Remote Work
- **Fully remote pays the most** — $140K median vs. $130K on-site and $120K hybrid
- **74% of U.S. jobs are fully remote** (246 of 330 records), reflecting post-2020 industry norms

### 🚪 Entry-Level Reality Check
- **Entry-level U.S. median: $90,000** — 50% of roles fall between $72K and $105K
- Top entry-level roles: **ML Engineer ($131K)** › Data Scientist ($95K) › Data Engineer ($76K) ≈ Data Analyst ($76K)
- Geography matters enormously: the global entry-level median is just $56K; U.S.-only is 60% higher

### 🛠️ Must-Have Skills (Entry-Level)
1. **Python** — universal across every role
2. **SQL** — critical for analyst and engineer tracks
3. **TensorFlow / PyTorch** — expected at entry level for DS/ML roles
4. **Kubernetes** — increasingly required for ML engineering pipelines
5. **Scala** — common in data engineering (Spark ecosystem)

---

## 📁 Repository Structure

```
salary-analysis/
├── README.md
├── salary_analysis.ipynb   ← Main notebook (fully executed with outputs)
├── data/
│   ├── ds_salaries.csv     ← Primary salary dataset (real, survey-based)
│   └── ai_job_skills.csv   ← Skills dataset (synthetic, role→skill mapping only)
└── visuals/
    ├── 01_us_salary_distribution.png
    ├── 02_us_top_job_titles.png
    ├── 03_us_salary_trends.png
    ├── 04_us_remote_vs_salary.png
    ├── 05_us_entry_level_salaries.png
    ├── 06_us_top_skills.png
    └── 07_us_entry_level_skills.png
```

---

## 🗃️ Data Sources

| Dataset | Source | Type | Used For |
|---|---|---|---|
| Data Science Job Salaries | [Kaggle — ruchi798](https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries) | Real (CC0) | All salary analysis |
| Global AI Job Market 2025 | [Kaggle — bismasajjad](https://www.kaggle.com/datasets/bismasajjad/global-ai-job-market-and-salary-trends-2025) | Synthetic | Role→skill mapping only |

> The salary dataset contains 607 global records (2020–2022). This analysis filters to **330 U.S.-only records** (where both employee residence and company location are the United States) to ensure geographic comparability.

---

## 🛠️ Tech Stack

- **Python** — pandas, NumPy, matplotlib, seaborn
- **Jupyter Notebook** — fully executed with inline outputs
- **Kaggle CLI** — dataset retrieval

---

## 🚀 Run It Yourself

```bash
# Clone the repo
git clone https://github.com/pop400/salary-analysis.git
cd salary-analysis

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Download the datasets (requires Kaggle API key)
kaggle datasets download -d ruchi798/data-science-job-salaries --unzip -p data/
kaggle datasets download -d bismasajjad/global-ai-job-market-and-salary-trends-2025 --unzip -p data/
mv data/ai_job_dataset1.csv data/ai_job_skills.csv

# Launch the notebook
jupyter notebook salary_analysis.ipynb
```

---

*Built as part of a data science portfolio. See more at [github.com/pop400](https://github.com/pop400).*
