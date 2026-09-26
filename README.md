# Niroj Danai

**Building ML systems from raw data to deployed services, with evaluation at every step.**

[LinkedIn](https://www.linkedin.com/in/niroj-danai-5b15b4305/) · [Email](mailto:danainiroj09@gmail.com) · [Selected projects](#selected-projects)

<!-- Optional: add [Portfolio](https://YOUR-PORTFOLIO-URL) above when ready. -->

![Python](https://img.shields.io/badge/Python-334155?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-334155?style=flat&logo=pytorch&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-334155?style=flat&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-334155?style=flat&logo=docker&logoColor=white)

## About

I'm a Software Engineering graduate from **Nepal College of Information Technology**, working toward a **Machine Learning Engineer** role through independent, end-to-end projects.

My software engineering foundation shapes how I approach ML: define the data contract, compare against a useful baseline, expose the model through a tested API, and make failures diagnosable. My repositories include evaluation reports, design decisions, and reproducible workflows alongside the code.

<sub>Data collection → Training → Evaluation → Serving → Monitoring → Retraining</sub>

## Currently building & learning

My main focus is **[WildInbox](https://github.com/professor3333/wildinbox)**: helping people review trail-camera photos through event grouping, species suggestions, and human corrections. I'm developing my computer vision and PyTorch skills around a practical question: **what still works when the camera moves somewhere new?**

Across my projects, I'm deepening my understanding of temporal validation, probability calibration, data drift, and reliable model releases, including when to fall back, roll back, or keep a person in the loop.

## Selected projects

### [WildInbox](https://github.com/professor3333/wildinbox)

**Computer vision · Human review · Asynchronous inference**

A trail-camera review system with a fine-tuned EfficientNet-B0, a review interface, and recoverable background workers.

- Grouped **23,275 photos into 8,982 capture events** on the locked test from nine unseen cameras: **61.4% fewer review items**. Every event still receives human review; automated filtering remains disabled because release criteria were not met.
- Built versioned model releases, correction tracking, monitoring, and rollback; validated deployment on an AWS VM.

[Walkthrough](https://github.com/professor3333/wildinbox/blob/main/docs/demo.md) · [Evaluation](https://github.com/professor3333/wildinbox/blob/main/reports/final_evaluation/README.md)

### [NYC Taxi Trip Duration](https://github.com/professor3333/nyc-taxi-trip-duration)

**Reproducible ML · AWS deployment · Model lifecycle**

A trip-duration API connecting DVC pipelines and MLflow model management to a containerized FastAPI service on AWS Lambda.

- Reduced MAE by **8.2% on average across 23 historical monthly backtests**, compared with a zone-pair median baseline.
- Implemented baseline fallback, gated model promotion, deployment rollback, and CloudWatch monitoring; verified pipeline reproduction from a clean clone.

[Backtest results](https://github.com/professor3333/nyc-taxi-trip-duration/blob/main/docs/backtest.md) · [Architecture](https://github.com/professor3333/nyc-taxi-trip-duration/blob/main/docs/architecture.md)

### [Fraud Risk Scoring](https://github.com/professor3333/fraud-risk-scoring)

**Tabular ML · Calibration · Decisions under constraints**

An IEEE-CIS fraud-scoring system that connects calibrated XGBoost probabilities to a simulated analyst workflow.

- Implemented batch approve/review/block decisions constrained by a daily review budget, with an analyst dashboard and prediction audit trail.
- Used temporal evaluation and training-to-serving parity checks; documented performance decay, delayed labels, and the limitations of automated blocking.

[Model card](https://github.com/professor3333/fraud-risk-scoring/blob/main/docs/model_card.md) · [Review policy](https://github.com/professor3333/fraud-risk-scoring/blob/main/docs/review_policy.md)

### [Shelf Life](https://github.com/professor3333/shelf-life)

**Self-collected data · Delayed outcomes · Temporal evaluation**

A system in development to estimate which job postings will disappear from a board within seven days, using my own daily collection pipeline.

- Built ingestion, labeling, leakage checks, temporal evaluation, and an API/UI serving structure.
- Kept the seven-day model unreleased while sufficient labeled history accumulates. The target is posting removal; it does not establish that a role was filled.

[Design](https://github.com/professor3333/shelf-life/blob/main/docs/design.md) · [Data readiness](https://github.com/professor3333/shelf-life/blob/main/reports/readiness.md)

## Tools I use

| Area | Stack |
| --- | --- |
| Languages & data | Python, SQL, pandas, NumPy |
| Modeling | PyTorch, torchvision, scikit-learn, XGBoost |
| APIs & applications | FastAPI, Pydantic, Streamlit |
| Storage & workers | PostgreSQL, SQLite, SQLAlchemy, Redis, RQ |
| ML lifecycle & cloud | MLflow, DVC, Docker, GitHub Actions, AWS Lambda, EC2, S3, ECR, CloudWatch |
| Engineering | Git, pytest, Ruff, mypy, uv |

## Where I'm headed

I'm targeting **junior Machine Learning Engineer roles** where I can contribute to data pipelines, model evaluation, and deployed ML services while learning from an experienced team.

My current interests are computer vision with human review, dependable inference services, and MLOps: connecting model quality to release decisions, observability, and retraining.

---

**Get in touch:** [LinkedIn](https://www.linkedin.com/in/niroj-danai-5b15b4305/) · [danainiroj09@gmail.com](mailto:danainiroj09@gmail.com)
