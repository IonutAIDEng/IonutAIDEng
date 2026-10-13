# Hi, I'm Ionuț-Cristian Vințe 👋
### **Data & AI Engineer | Building Production LLM Systems, Pipelines & Cloud Infrastructure**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ionut-vinte-a07624226)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:vinteionut@gmail.com)

---

# About me

## 🧰 Core Engineering Skills

- **AI & Data Engineering:** RAG Architectures, Agentic Workflows, LLM Evaluation (LLM-as-a-Judge), Golden Datasets, ETL/ELT Pipelines, Data Quality & Governance.
- **Languages & Frameworks:** Python, FastAPI, JavaScript, PostgreSQL, SQLAlchemy, Alembic, REST APIs, C#, Java, React.
- **Automation & Web Data:** Playwright, Patchright, Camoufox (Stealth/Anti-Bot Bypass), Mozenda, XPath, RegEx.
- **Cloud & DevOps:** AWS (S3, ECR, Secrets Manager), Docker, Terraform (IaC), GitLab CI/CD, ArgoCD, GitOps, Kubernetes, Grafana/Prometheus.

---

## 📈 Proven Impact (Production Experience)
- **AI Predictors in Production:** Built and deployed LLM pipelines (Vertex AI + Gemini) with **>96% precision**, saving **tens of hours/day** for analyst teams.
- **Data Quality Automation:** Designed an automated QA evaluation framework using LLM-as-a-Judge & Golden Datasets (**~97% precision**), replacing manual QA blocks (~100 hours saved per 5-week block).
- **Cloud Infrastructure:** Provisioned IaC via Terraform, automated container workflows via Docker/AWS ECR, and managed GitOps pipelines with ArgoCD & GitLab CI/CD.

---

# My Projects

## 🚀 Featured Project: TailorBuy (AI & E-Commerce Search Platform)

> **One-Liner:** A mobile-first discovery platform for Romanian e-commerce (eMAG, Altex) that filters and ranks products against strict user preferences (cash-on-delivery, min rating, price caps) using a multi-tiered API + Gemini AI chain. *(Deployment to Play Store in progress)*.

<!-- 📱 DEMO / SCREENSHOTS PLACEHOLDER 
<p align="center">
  <img src="https://via.placeholder.com/800x400.png?text=TailorBuy+App+Demo+%2F+Screenshots" width="100%" alt="TailorBuy App Demo" />
</p>
-->

### 🛠️ Technical Architecture & Stack
- **Backend & API Layer:** Python 3.12, FastAPI, Router-Service-ORM Layered Architecture, REST APIs.
- **AI & LLM Integration:** Google Gemini (`gemini-3.8-flash`) with Google Search Grounding; optimized with `thinking_budget=0` to eliminate unnecessary reasoning tokens and latency.
- **Database & Data Modeling:** PostgreSQL (Neon.tech), SQLAlchemy 2.x, Alembic (Idempotent raw SQL migrations), Pydantic v2.
- **Data Acquisition Chain:** Multi-tier scraper fallback pipeline (Apify eMAG Scraper Actor → SerpApi → Graceful UI Degradation).
- **Security & Auth:** PyJWT + bcrypt (12 rounds), 15-min access + 7-day rotated refresh tokens with SHA-256 reuse/replay detection.
- **Frontend / Mobile:** React Native + Expo (TypeScript), `expo-router`, `expo-secure-store`.

### ⚙️ Quantifiable Engineering Highlights
- **Cost-Optimized Architecture:** Designed a zero-LLM-cost execution path for 95%+ of searches by routing standard queries to external API tiers, reserving Gemini Grounding strictly for admin-managed exception lists.
- **Dual-Rail Quota & Rate Limiting:** Implemented a multi-level guardrail system combining daily per-user database counters (30 searches/day), IP-based rate limiting (`slowapi`), and strict spend caps on external APIs (`maxTotalChargeUsd=0.1`).
- **Production-Grade Testing Suite:** Built 255 automated tests achieving **94% branch coverage**, utilizing HTTP mocking for external search APIs to execute the full test suite offline in under 30 seconds.
- **Custom Ranking & Scoring:** Developed a deterministic Python scoring algorithm to rank extracted products by `(match_score, rating)` and tag status matches without incurring secondary LLM evaluation calls.

> 🔒 *Note: The source code for TailorBuy is in a private repository due to commercial IP. Code walk-throughs or access to architectural folders can be provided upon request during technical interviews.*

---

📬 **Let's Connect:** If you'd like to discuss Data & AI Engineering, building resilient production LLM applications, or cloud pipelines, feel free to reach out via [LinkedIn](https://linkedin.com/in/vinteionut) or [Email](mailto:vinteionut@gmail.com).
