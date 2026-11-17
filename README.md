<!-- =========================================================
     👋  PROFILE HEADER
     ========================================================= -->
<h1 align="center">👋 Hi, I'm Bat!</h1>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=22&duration=3200&pause=1000&color=6E40C9&center=true&vCenter=true&width=620&lines=CS+%26+Math+%40+Ole+Miss+('27);Break+Through+Tech+AI+Studio+Fellow;Building+ML+systems+that+touch+the+real+world" alt="Typing SVG"/>
  </a>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/bat-orgil-erdenebat/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="mailto:batorgilrb@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
  </a>
  <a href="https://github.com/BatOrgil7/Resume/blob/main/Bat-Orgil_Erdenebat_Resume.pdf">
    <img src="https://img.shields.io/badge/Resume-2A9D8F?style=for-the-badge&logo=readthedocs&logoColor=white" alt="Resume"/>
  </a>
</p>

---

<!-- =========================================================
     🧭  ABOUT ME
     ========================================================= -->
## 🧭 About Me

I build machine learning systems that have to survive contact with production.

I'm a senior at the **University of Mississippi** studying Computer Science with a Data Science emphasis and a Math minor, graduating May 2027.

My longer-term interest is **embodied AI and robot learning**, which is to say the version of this problem where the model has to act, not just predict. Everything I build keeps circling the same question, which is what breaks when a model leaves the notebook.

<!-- =========================================================
     💼  FEATURED WORK
     ========================================================= -->
## 💼 Featured Work

### ⚖️ Automated Contract Review & Risk Triage · *Accenture AI Studio, Break Through Tech*

Finding the clauses that actually carry risk in commercial contracts, so a legal reviewer knows which document to open first instead of reading all of them.

![Contracts](https://img.shields.io/badge/510-commercial_contracts-6E40C9?style=flat-square)
![Spans](https://img.shields.io/badge/13.8K-expert_annotated_spans-6E40C9?style=flat-square)
![Categories](https://img.shields.io/badge/34-clause_categories-6E40C9?style=flat-square)
![F1](https://img.shields.io/badge/0.717_→_0.750-macro--F1-6E40C9?style=flat-square)

- Designed the **offset-preserving chunking strategy** the team's pipeline runs on — 510-token sliding windows with 128-token overlap — keeping character offsets aligned to the source text so every clause prediction stays auditable, with **97.8%** of annotated clauses intact inside a single chunk
- **Disproved the team's leading hypothesis** for classifier misses (clauses split across chunk boundaries: correlation **+0.004**, only 2% of spans split) and isolated positive training volume as the real driver (**+0.715**), redirecting the team away from a costly chunking rewrite
- Built **5-fold cross-validated threshold tuning** split by contract, scoring every training contract with a model that never saw it — lifting held-out macro-F1 from **0.717 to 0.750** with no retraining, and the weakest clause category **5x** (0.091 → 0.500)
- Showed **per-category thresholds overfit** on low-support categories (as few as 27 positive contracts) and shipped a single global cutoff instead

`Python` · `PyTorch` · `Hugging Face Transformers` · `DistilRoBERTa` · `Pandas` · `scikit-learn`

*Five-person team project on the [CUAD](https://www.atticusprojectai.org/cuad) corpus — the work above is my own commits. [Repo →](https://github.com/Break-Through-Tech/Accenture-1Q-contract-review-challenge)*

---

### 🔗 Graph Threat Intelligence Platform · *PotatoNet Co., Ltd., Seoul*

Turning raw malicious JavaScript into named attacker "families" so analysts can chase infrastructure instead of individual scripts.

![Nodes](https://img.shields.io/badge/19.4K-malicious_JS_nodes-6E40C9?style=flat-square)
![Domains](https://img.shields.io/badge/13.7K-domains-6E40C9?style=flat-square)
![Dedup](https://img.shields.io/badge/267K_→_12.4K-SimHash_LSH_dedup-6E40C9?style=flat-square)
![Accuracy](https://img.shields.io/badge/94.7%25-fault_predictor-6E40C9?style=flat-square)

- Shipped a **production graph-ETL pipeline** backfilling six months of threat data into a live Neo4j store through idempotent, rollback-tagged loads, automated as a nightly self-healing cron job
- Built a **7-signal attacker-profiling engine** clustering malicious JS via SimHash AST similarity, perceptual screenshot hashing, and shared TLS cert / IP / ASN / registrant infrastructure, using GDS **Leiden community detection**
- Diagnosed and fixed a **52K-script over-merge** caused by benign library bridges between unrelated families, cutting max family size to 476 across 334 clean clusters
- Extracted a **CNN-LSTM-Attention** fault predictor (94.7% accuracy) out of a legacy Django monolith into a clean FastAPI service on a 16-container microservices platform, with zero-downtime deploys

`Python` · `Neo4j / Cypher` · `PyTorch` · `FastAPI` · `Docker` · `Nginx` · `Gunicorn`

*Proprietary work. Happy to walk through the architecture and the debugging story.*

---

### 📂 Projects

| Project | What It Does | Tech |
| :--- | :--- | :--- |
| **[Census Income Classification](https://github.com/BatOrgil7/census-income-ml-pipeline)** 📌 | End-to-end ML pipeline on 32K+ census records. Tuned on F1 rather than accuracy to handle class imbalance, found a 3-layer Keras net beat logistic regression by only 0.02 F1 (0.70 vs 0.68), too small to justify the added complexity, so shipped the simpler interpretable model. **Audited coefficients for fairness, surfaced a discrimination risk, and recommended against lending deployment.** | `Python` `Scikit-learn` `Keras` `Pandas` |
| **[Streaming Evaluation Protocol for CSLR](https://github.com/BatOrgil7/signstream-eval)** 🔬 | A standardized evaluation protocol for streaming sign language recognition, adapting latency and stability metrics from streaming ASR and simultaneous MT to fill a gap left by offline-only benchmarks. Includes a fault-tolerant landmark extraction pipeline over PHOENIX-2014T. | `Python` `MediaPipe` `Multiprocessing` |
| **[Real-Time ASL Translation](https://github.com/BatOrgil7/ASL-Translation-Capstone)** 🤟 | Live ASL recognition from webcam input, built for interactive frame rates on consumer hardware rather than batch inference. | `Python` `TensorFlow` `OpenCV` `MediaPipe` |
| **[Multi-Modal RAG Chatbot](https://github.com/BatOrgil7/multi-modal-ai-chatbot-rag)** 🧠 | Gemini-powered agent with persistent long-term memory: a lightweight secondary model emits schema-enforced JSON add/update/delete operations over SQLite, classifying entries as semantic, procedural, or episodic and resolving contradictions in place rather than duplicating records. RAG over a document store and the memory layer, with multimodal image and document input. | `Python` `Gemini` `SQLite` `Streamlit` `Docker` |
| **[Hyntor](https://github.com/BatOrgil7/Hyntor)** 📚 | Responsible-AI study platform for web and mobile: an AI study partner with shared per-course memory, built so students get help that is scoped to their course rather than open-ended answers. | `TypeScript` `React` `AI` |
| **[CS2 Esports Statistics Tracker](https://github.com/BatOrgil7/cs2-esports-statistics-tracker)** 📊 | Normalized relational schema for pro Counter-Strike teams, players, tournaments, and match performance, designed around the queries analysts actually run. | `SQL` `Database Design` |

<sub>Also on my profile: an e-commerce storefront in TypeScript/React and a desktop note-taking app in Python.</sub>

---

<!-- =========================================================
     🛠  TECH STACK
     ========================================================= -->
## 🛠 Tech Stack

**💻 Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Cypher](https://img.shields.io/badge/Cypher-008CC1?style=for-the-badge&logo=neo4j&logoColor=white)

**🧠 ML & Computer Vision**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=for-the-badge&logo=google&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

**☁️ Infrastructure & Data**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![Neo4j](https://img.shields.io/badge/Neo4j-008CC1?style=for-the-badge&logo=neo4j&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

<!-- =========================================================
     📊  GITHUB STATS
     ========================================================= -->
## 📊 GitHub Stats

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=BatOrgil7&hide_border=true&theme=tokyonight" alt="GitHub contribution streak"/>
</p>

<!-- The two github-readme-stats cards (stats + top languages) are commented out:
     the public instance at github-readme-stats.vercel.app is currently returning
     503 DEPLOYMENT_PAUSED, so both rendered as broken images.
     To restore them, deploy your own instance (5 min, free) and swap the host:
       1. Fork https://github.com/anuraghazra/github-readme-stats
       2. Import the fork into Vercel, add env var PAT_1 = a GitHub personal access token
       3. Replace the host below with your-instance.vercel.app
<p align="center">
  <img height="165" src="https://YOUR-INSTANCE.vercel.app/api?username=BatOrgil7&show_icons=true&hide_border=true&count_private=true&include_all_commits=true&theme=tokyonight" alt="GitHub stats"/>
  <img height="165" src="https://YOUR-INSTANCE.vercel.app/api/top-langs/?username=BatOrgil7&layout=compact&hide_border=true&theme=tokyonight" alt="Top languages"/>
</p>
-->

---

<!-- =========================================================
     📫  CONNECT
     ========================================================= -->
## 📫 Connect with Me

<p align="center">
  <a href="https://www.linkedin.com/in/bat-orgil-erdenebat/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="mailto:batorgilrb@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
  </a>
</p>

<p align="center"><i>Open to conversations about embodied AI, robot learning, and anything that puts a model on real hardware.</i></p>
