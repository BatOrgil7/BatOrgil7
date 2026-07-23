<!-- =========================================================
     👋  PROFILE HEADER
     ========================================================= -->
<h1 align="center">👋 Hi, I'm Bat!</h1>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=22&duration=3200&pause=1000&color=6E40C9&center=true&vCenter=true&width=620&lines=CS+%26+Math+%40+Ole+Miss+('27);ML+Engineering+Intern+%40+PotatoNet%2C+Seoul;Break+Through+Tech+AI+Studio+Fellow;Building+ML+systems+that+touch+the+real+world" alt="Typing SVG"/>
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

I'm a senior at the **University of Mississippi** studying Computer Science with a Data Science emphasis and a Math minor, graduating May 2027. Originally from Mongolia 🇲🇳, currently in **Seoul** as a Machine Learning Engineering Intern at **PotatoNet**, where most of my work sits between graph databases, deep learning, and the deployment plumbing that makes either one useful.

My longer-term interest is **embodied AI and robot learning**, which is to say the version of this problem where the model has to act, not just predict. Everything I build keeps circling the same question, which is what breaks when a model leaves the notebook.

Also a **Break Through Tech AI Studio Fellow** (selected from 4,000+ applicants nationwide) and a **Teaching Assistant** for 200+ students in Data Structures and Algorithms.

---

<!-- =========================================================
     🔭  CURRENTLY
     ========================================================= -->
## 🔭 What I'm Working On

> [!NOTE]
> 🤖 **Language-conditioned robot manipulation** for my senior capstone, built on Hugging Face's [LeRobot](https://github.com/huggingface/lerobot). Aiming at a workshop submission.
>
> 🔗 **Graph-based threat intelligence @ PotatoNet**, scaling attacker-family clustering across a live Neo4j store.
>
> 📚 **Learning**: Cypher and graph algorithms, vision-language-action models, and Rust for the parts of the stack Python shouldn't own.

---

<!-- =========================================================
     💼  FEATURED WORK
     ========================================================= -->
## 💼 Featured Work

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
| **[Census Income Classification](https://github.com/BatOrgil7/census-income-ml-pipeline)** 📌 | End-to-end ML pipeline on 32K+ census records. Tuned on F1 rather than accuracy to handle class imbalance, found a 3-layer Keras net barely beat logistic regression (0.70 vs 0.68), and shipped the simpler model. **Audited coefficients for fairness, surfaced a discrimination risk, and recommended against lending deployment.** | `Python` `Scikit-learn` `Keras` `Pandas` |
| **[Streaming Evaluation Protocol for CSLR](https://github.com/BatOrgil7/signstream-eval)** 🔬 | A standardized evaluation protocol for streaming sign language recognition, adapting latency and stability metrics from streaming ASR and simultaneous MT to fill a gap left by offline-only benchmarks. Includes a fault-tolerant landmark extraction pipeline over PHOENIX-2014T. | `Python` `MediaPipe` `Multiprocessing` |
| **[Real-Time ASL Translation](https://github.com/BatOrgil7/ASL-Translation-Capstone)** 🤟 | Live ASL recognition from webcam input, built for interactive frame rates on consumer hardware rather than batch inference. | `Python` `TensorFlow` `OpenCV` `MediaPipe` |
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

---

<!-- =========================================================
     🏆  ACHIEVEMENTS
     ========================================================= -->
## 🏆 Achievements & Certifications

🎓 **Break Through Tech AI Studio Fellow** · selected from 4,000+ applicants nationwide for a one-year applied ML fellowship

📜 **Machine Learning Foundations** e-Certificate · Cornell University via Break Through Tech

📜 **Career Essentials in Generative AI** · Microsoft & LinkedIn

💰 **Freeman Grant Recipient** · $9,000

⭐ **Chancellor's Honor Roll** · Fall 2024, Spring 2025 · GPA 3.78

---

<!-- =========================================================
     🎾  BEYOND THE CODE
     ========================================================= -->
## 🎾 Beyond the Code

👨‍🏫 **Teaching Assistant & CS Tutor** for 200+ students across four courses, plus 50+ one-on-one mentees. Teaching is the fastest way I've found to locate the holes in my own understanding.

🎾 Tennis · 🏋️ In the gym most mornings · 📈 Markets and valuation modeling as a hobby · 🇰🇷 Learning Seoul one subway line at a time

---

<!-- =========================================================
     📊  GITHUB STATS
     ========================================================= -->
## 📊 GitHub Stats

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=BatOrgil7&show_icons=true&hide_border=true&count_private=true&include_all_commits=true&theme=tokyonight" alt="GitHub stats"/>
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=BatOrgil7&layout=compact&hide_border=true&theme=tokyonight" alt="Top languages"/>
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=BatOrgil7&hide_border=true&theme=tokyonight" alt="GitHub streak"/>
</p>

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
