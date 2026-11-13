<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/banner-light.svg">
  <img src="assets/banner-dark.svg" width="100%" alt="Niroj Danai, Machine Learning Engineer. End-to-end ML systems, measured on data they have never seen.">
</picture>

Software engineering graduate (B.E., Nepal College of Information Technology, 2026) based in Kathmandu, Nepal. I build machine learning systems end to end, from data pipeline to deployed API, and test them on data they have never seen: a later month, a new camera, a different site. When a model misses its target, the README says so.

**Open to Machine Learning Engineer and Applied ML Engineer roles, remote or on-site.**

<!--
  Add your contact links, then delete the comment markers around this block.

<p>
  <a href="https://www.linkedin.com/in/YOUR-HANDLE"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0a66c2?style=for-the-badge"></a>
  <a href="mailto:YOUR-EMAIL"><img alt="Email" src="https://img.shields.io/badge/Email-0f766e?style=for-the-badge&logo=gmail&logoColor=white"></a>
</p>
-->

## Featured work

### [ProtocolLedger](https://github.com/professor3333/ProtocolLedger)
<sup>NLP &nbsp;·&nbsp; information extraction &nbsp;·&nbsp; <a href="https://44.222.11.189.sslip.io"><b>Live demo</b></a></sup>

Turns free-text lab protocols into an editable preparation sheet, with every extracted value linked back to its source text. A SciBERT span-and-relation model reaches **0.766 entity F1** and **0.580 end-to-end relation F1** on WNUT-2020, ahead of a CRF baseline at 0.504.

<sub><code>PyTorch</code> <code>Transformers</code> <code>ONNX Runtime</code> <code>FastAPI</code> <code>Docker</code></sub>

### [Fraud Risk Scoring](https://github.com/professor3333/fraud-risk-scoring)
<sup>Tabular ML &nbsp;·&nbsp; calibration &nbsp;·&nbsp; <a href="https://fraud-risk-scoring-m1fp.onrender.com"><b>Live dashboard</b></a></sup>

Scores card-not-present transactions with a calibrated fraud probability and picks approve, review or block within an analyst team's daily review budget. It reaches **0.907 ROC-AUC** on a held-out later month, at **43% lower cost** than approving everything.

<sub><code>XGBoost</code> <code>scikit-learn</code> <code>SHAP</code> <code>FastAPI</code> <code>MLflow</code></sub>

### [WildInbox](https://github.com/professor3333/wildinbox)
<sup>Computer vision &nbsp;·&nbsp; image classification &nbsp;·&nbsp; human-in-the-loop</sup>

A review inbox for trail-camera photos that groups shots into capture events and suggests a species for each. Grouping alone cuts the review queue by **61.4%**, and a fine-tuned EfficientNet-B0 scores **0.447 macro-F1 on nine unseen cameras**, against 0.285 for the frozen baseline.

<sub><code>PyTorch</code> <code>FastAPI</code> <code>Streamlit</code> <code>PostgreSQL</code> <code>Redis</code> <code>AWS</code></sub>

### [PassageWatch](https://github.com/professor3333/passagewatch)
<sup>Computer vision &nbsp;·&nbsp; detection and tracking &nbsp;·&nbsp; sonar video</sup>

Counts fish moving upstream and downstream in sonar video and keeps the evidence so a technician can check every count. It reaches **0.213 count error (nMAE)** across four unseen locations, against 0.388 for a tuned classical baseline.

<sub><code>PyTorch</code> <code>YOLOX</code> <code>OpenCV</code> <code>ONNX Runtime</code> <code>FastAPI</code></sub>

### [Shelf Life](https://github.com/professor3333/shelf-life)
<sup>Tabular ML &nbsp;·&nbsp; self-collected data &nbsp;·&nbsp; <a href="https://shelf-life-2l8tanmdatboms9mhxh3rj.streamlit.app/"><b>Live app</b></a></sup>

Predicts which job postings will be taken down within seven days, trained on a panel I scraped from seven job boards. On held-out days, **75% of its daily shortlist were real removals**, 6.8 times the hit rate of reading the board unaided.

<sub><code>scikit-learn</code> <code>XGBoost</code> <code>FastAPI</code> <code>Streamlit</code> <code>MLflow</code></sub>

### [BeltWatch](https://github.com/professor3333/beltwatch)
<sup>Computer vision &nbsp;·&nbsp; semantic segmentation &nbsp;·&nbsp; in development</sup>

Segments cardboard, plastic and metal contamination on paper-recycling conveyor lines and queues uncertain images for review. SegFormer-B0 reaches **0.336 foreground macro IoU**, against 0.152 for a tuned random forest.

<sub><code>PyTorch</code> <code>SegFormer</code> <code>DVC</code> <code>MLflow</code> <code>FastAPI</code></sub>

## Toolbox

<p>
  <img alt="Python" src="https://img.shields.io/badge/Python-334155?style=flat-square&logo=python&logoColor=white">
  <img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-334155?style=flat-square&logo=pytorch&logoColor=white">
  <img alt="scikit-learn" src="https://img.shields.io/badge/scikit--learn-334155?style=flat-square&logo=scikitlearn&logoColor=white">
  <img alt="XGBoost" src="https://img.shields.io/badge/XGBoost-334155?style=flat-square">
  <img alt="Transformers" src="https://img.shields.io/badge/Transformers-334155?style=flat-square&logo=huggingface&logoColor=white">
  <img alt="OpenCV" src="https://img.shields.io/badge/OpenCV-334155?style=flat-square&logo=opencv&logoColor=white">
  <img alt="ONNX Runtime" src="https://img.shields.io/badge/ONNX_Runtime-334155?style=flat-square&logo=onnx&logoColor=white">
  <img alt="MLflow" src="https://img.shields.io/badge/MLflow-334155?style=flat-square&logo=mlflow&logoColor=white">
  <img alt="DVC" src="https://img.shields.io/badge/DVC-334155?style=flat-square&logo=dvc&logoColor=white">
  <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-334155?style=flat-square&logo=fastapi&logoColor=white">
  <img alt="Streamlit" src="https://img.shields.io/badge/Streamlit-334155?style=flat-square&logo=streamlit&logoColor=white">
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-334155?style=flat-square&logo=postgresql&logoColor=white">
  <img alt="Redis" src="https://img.shields.io/badge/Redis-334155?style=flat-square&logo=redis&logoColor=white">
  <img alt="Docker" src="https://img.shields.io/badge/Docker-334155?style=flat-square&logo=docker&logoColor=white">
  <img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub_Actions-334155?style=flat-square&logo=githubactions&logoColor=white">
  <img alt="AWS" src="https://img.shields.io/badge/AWS-334155?style=flat-square">
</p>
