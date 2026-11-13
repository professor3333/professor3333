<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/banner-light.svg">
  <img src="assets/banner-dark.svg" width="100%" alt="Niroj Danai, Machine Learning Engineer. End-to-end ML systems, measured on data they have never seen.">
</picture>

<p align="center">
  <a href="#featured-work"><b>Featured work</b></a> &nbsp;·&nbsp;
  <a href="#how-i-work"><b>How I work</b></a> &nbsp;·&nbsp;
  <a href="#toolbox"><b>Toolbox</b></a> &nbsp;·&nbsp;
  <a href="#get-in-touch"><b>Get in touch</b></a>
</p>

## About

I'm a software engineering graduate based in Kathmandu, Nepal. I build machine learning systems end to end: the data pipeline, the model, the API, the review interface, the deployment and the monitoring around it.

My projects cover computer vision, NLP and tabular ML, and they share one habit. Models are tested on data they have never seen: a later month, a new camera, a different site. Targets are written down before the test set is opened, and when a model misses one, the README says so and the automation stays switched off.

**Open to Machine Learning Engineer and Applied ML Engineer roles, remote or on-site, and open to relocation.**

## Featured work

### [ProtocolLedger](https://github.com/professor3333/ProtocolLedger)
<sup>NLP &nbsp;·&nbsp; information extraction &nbsp;·&nbsp; <a href="https://44.222.11.189.sslip.io"><b>Live demo</b></a></sup>

Turns free-text lab protocols into an editable preparation sheet of actions, materials, quantities and conditions. Every extracted value links back to the exact characters it came from, and uncertain readings go to a human reviewer.

- A SciBERT span-and-relation model reaches **0.766 entity F1** and **0.580 end-to-end relation F1** on the WNUT-2020 test split, ahead of a CRF baseline at 0.504.
- Isotonic calibration cuts expected calibration error from 0.172 to **0.021**.

<sub><code>PyTorch</code> <code>Transformers</code> <code>ONNX Runtime</code> <code>FastAPI</code> <code>MLflow</code> <code>Docker</code> <code>Prometheus</code> <code>AWS</code></sub>

### [Fraud Risk Scoring](https://github.com/professor3333/fraud-risk-scoring)
<sup>Tabular ML &nbsp;·&nbsp; calibration &nbsp;·&nbsp; <a href="https://fraud-risk-scoring-m1fp.onrender.com"><b>Live dashboard</b></a> &nbsp;·&nbsp; <a href="https://fraud-risk-scoring-m1fp.onrender.com/docs">API docs</a></sup>

Scores card-not-present transactions with a calibrated fraud probability, then picks approve, review or block for each one under a policy sized to an analyst team's daily review budget.

- **0.907 ROC-AUC** and **0.561 PR-AUC** on a held-out later month where about 3.5% of transactions are fraud, at **43% lower cost** than approving everything.
- A random split would have reported 0.810 PR-AUC. The time-respecting split reports 0.616, and that is the number the project is built on.

<sub><code>XGBoost</code> <code>scikit-learn</code> <code>SHAP</code> <code>FastAPI</code> <code>MLflow</code> <code>Docker</code> <code>GitHub Actions</code></sub>

### [WildInbox](https://github.com/professor3333/wildinbox)
<sup>Computer vision &nbsp;·&nbsp; image classification &nbsp;·&nbsp; human-in-the-loop</sup>

A review inbox for trail-camera photos. It groups a memory card's photos into capture events, suggests a species for each, explains why an event needs a person, and exports an observation log with provenance.

- Event grouping alone cuts the review queue by **61.4%** (23,275 photos become 8,982 events).
- A fine-tuned EfficientNet-B0 scores **0.447 macro-F1 on nine unseen cameras**, against 0.285 for the frozen baseline. That fell short of the bar for automatic filtering, so every event still goes to a reviewer.

<sub><code>PyTorch</code> <code>FastAPI</code> <code>Streamlit</code> <code>Redis + RQ</code> <code>PostgreSQL</code> <code>Docker Compose</code> <code>AWS</code></sub>

### [PassageWatch](https://github.com/professor3333/passagewatch)
<sup>Computer vision &nbsp;·&nbsp; detection and tracking &nbsp;·&nbsp; sonar video</sup>

Counts fish moving upstream and downstream in sonar recordings, and keeps the evidence so a technician can check and correct every count before exporting a report.

- **0.213 directional count error (nMAE)** across four unseen locations, against 0.388 for a tuned classical baseline.
- Runs at about 10 frames per second on a laptop CPU through ONNX Runtime.

<sub><code>PyTorch</code> <code>YOLOX</code> <code>OpenCV</code> <code>ONNX Runtime</code> <code>FastAPI</code> <code>TypeScript</code> <code>Docker Compose</code></sub>

### [Shelf Life](https://github.com/professor3333/shelf-life)
<sup>Tabular ML &nbsp;·&nbsp; self-collected data &nbsp;·&nbsp; <a href="https://shelf-life-2l8tanmdatboms9mhxh3rj.streamlit.app/"><b>Live app</b></a> &nbsp;·&nbsp; <a href="https://shelf-life-5hin.onrender.com">API</a></sup>

Predicts which job postings will be taken down within seven days, trained on a panel I scraped from seven job boards, and ranks them into a shortlist a person can review each day.

- On a held-out block of days, **75% of the daily shortlist were real removals**, a hit rate **6.8 times** that of reading the board unaided.
- The label was audited against the live boards: 57 of 60 sampled removals were confirmed gone.

<sub><code>scikit-learn</code> <code>XGBoost</code> <code>pandas</code> <code>FastAPI</code> <code>Streamlit</code> <code>MLflow</code> <code>Docker</code></sub>

### [BeltWatch](https://github.com/professor3333/beltwatch)
<sup>Computer vision &nbsp;·&nbsp; semantic segmentation &nbsp;·&nbsp; in development</sup>

Audits paper-recycling conveyor lines for cardboard, plastic and metal contamination. It segments the suspect material, estimates visible coverage, and queues images for review based on coverage, model uncertainty and image quality.

- SegFormer-B0 reaches **0.336 foreground macro IoU** against 0.152 for a tuned random forest, with coverage error down from 16.8 to **5.0 percentage points**.

<sub><code>PyTorch</code> <code>SegFormer</code> <code>U-Net</code> <code>DVC</code> <code>MLflow</code> <code>FastAPI</code> <code>Prometheus</code></sub>

## How I work

<table>
  <tr>
    <td width="32%"><b>Evaluation that matches deployment</b></td>
    <td>Wherever the data allows, test sets are held out by time, camera, location or recording instead of a random shuffle, so the reported number is the one a new site or a new month would see.</td>
  </tr>
  <tr>
    <td width="32%"><b>Targets set before the test set is opened</b></td>
    <td>Projects state their bar up front. Results that miss it are published next to the ones that clear it.</td>
  </tr>
  <tr>
    <td width="32%"><b>A person in the loop, with evidence</b></td>
    <td>Uncertain predictions go to a reviewer. Corrections are kept with their provenance and can be exported.</td>
  </tr>
  <tr>
    <td width="32%"><b>Shipped as a service</b></td>
    <td>Models run behind an API in a container, with CI and experiment tracking, and the heavier ones are benchmarked for latency and memory on CPU.</td>
  </tr>
</table>

## Toolbox

<table>
  <tr>
    <td width="22%"><b>Modeling</b></td>
    <td>
      <img alt="Python" src="https://img.shields.io/badge/Python-334155?style=flat-square&logo=python&logoColor=white">
      <img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-334155?style=flat-square&logo=pytorch&logoColor=white">
      <img alt="scikit-learn" src="https://img.shields.io/badge/scikit--learn-334155?style=flat-square&logo=scikitlearn&logoColor=white">
      <img alt="XGBoost" src="https://img.shields.io/badge/XGBoost-334155?style=flat-square">
      <img alt="Transformers" src="https://img.shields.io/badge/Transformers-334155?style=flat-square&logo=huggingface&logoColor=white">
      <img alt="OpenCV" src="https://img.shields.io/badge/OpenCV-334155?style=flat-square&logo=opencv&logoColor=white">
      <img alt="ONNX Runtime" src="https://img.shields.io/badge/ONNX_Runtime-334155?style=flat-square&logo=onnx&logoColor=white">
    </td>
  </tr>
  <tr>
    <td width="22%"><b>Data and experiments</b></td>
    <td>
      <img alt="pandas" src="https://img.shields.io/badge/pandas-334155?style=flat-square&logo=pandas&logoColor=white">
      <img alt="NumPy" src="https://img.shields.io/badge/NumPy-334155?style=flat-square&logo=numpy&logoColor=white">
      <img alt="MLflow" src="https://img.shields.io/badge/MLflow-334155?style=flat-square&logo=mlflow&logoColor=white">
      <img alt="DVC" src="https://img.shields.io/badge/DVC-334155?style=flat-square&logo=dvc&logoColor=white">
    </td>
  </tr>
  <tr>
    <td width="22%"><b>Serving</b></td>
    <td>
      <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-334155?style=flat-square&logo=fastapi&logoColor=white">
      <img alt="Pydantic" src="https://img.shields.io/badge/Pydantic-334155?style=flat-square&logo=pydantic&logoColor=white">
      <img alt="Streamlit" src="https://img.shields.io/badge/Streamlit-334155?style=flat-square&logo=streamlit&logoColor=white">
      <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-334155?style=flat-square&logo=postgresql&logoColor=white">
      <img alt="Redis" src="https://img.shields.io/badge/Redis-334155?style=flat-square&logo=redis&logoColor=white">
      <img alt="SQLite" src="https://img.shields.io/badge/SQLite-334155?style=flat-square&logo=sqlite&logoColor=white">
    </td>
  </tr>
  <tr>
    <td width="22%"><b>Operations</b></td>
    <td>
      <img alt="Docker" src="https://img.shields.io/badge/Docker-334155?style=flat-square&logo=docker&logoColor=white">
      <img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub_Actions-334155?style=flat-square&logo=githubactions&logoColor=white">
      <img alt="AWS" src="https://img.shields.io/badge/AWS-334155?style=flat-square">
      <img alt="Prometheus" src="https://img.shields.io/badge/Prometheus-334155?style=flat-square&logo=prometheus&logoColor=white">
    </td>
  </tr>
  <tr>
    <td width="22%"><b>Code quality</b></td>
    <td>
      <img alt="pytest" src="https://img.shields.io/badge/pytest-334155?style=flat-square&logo=pytest&logoColor=white">
      <img alt="ruff" src="https://img.shields.io/badge/ruff-334155?style=flat-square&logo=ruff&logoColor=white">
      <img alt="mypy" src="https://img.shields.io/badge/mypy-334155?style=flat-square">
      <img alt="uv" src="https://img.shields.io/badge/uv-334155?style=flat-square&logo=uv&logoColor=white">
      <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-334155?style=flat-square&logo=typescript&logoColor=white">
    </td>
  </tr>
</table>

## Education

**Bachelor of Engineering, Software Engineering**, Nepal College of Information Technology (2022 to 2026)

## Get in touch

I'm looking for a Machine Learning Engineer or Applied ML Engineer role, remote or on-site with relocation. If you're hiring, or want to talk through how any of these systems were built and evaluated, I'd be glad to hear from you.

<!--
  Add your contact links, then delete the comment markers around this block.

<p>
  <a href="https://www.linkedin.com/in/YOUR-HANDLE"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0a66c2?style=for-the-badge"></a>
  <a href="mailto:YOUR-EMAIL"><img alt="Email" src="https://img.shields.io/badge/Email-0f766e?style=for-the-badge&logo=gmail&logoColor=white"></a>
</p>
-->

<p align="right"><sub>Kathmandu, Nepal &nbsp;·&nbsp; UTC+5:45</sub></p>
