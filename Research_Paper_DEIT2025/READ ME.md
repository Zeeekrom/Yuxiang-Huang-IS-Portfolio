# 📄 Research_Paper_DEIT2025 – Predicting Student Performance in Software Engineering Education Using Random Forest

**Type:** Academic Research Paper (Accepted at DEIT 2025, ACM ICPS)  
**Timeline:** Feb 2025  
**Role:** Co-Author (Data Preprocessing · Feature Engineering · Model Training & Evaluation)  
**Collaborators:** Prof. Linling Zhu et al., Sanda University  

---

## 🎯 Overview

This research investigates how **subjective** and **process-based assessments** (e.g., test plan quality, bug detection accuracy, report completeness) can serve as **early indicators** of students’ future performance in software engineering courses.

By transforming **qualitative instructor evaluations** into structured numerical data, we examined whether **machine-learning models** could predict subsequent grades more effectively than traditional exam-based assessments.  
The paper was accepted and presented at **DEIT 2025 (ACM International Conference Proceedings Series)**.

---

## 🧩 Research Objectives

- Quantify the **predictive value** of subjective evaluation metrics compared with objective grades.  
- Build a **clean, standardized dataset** for 88 students across two courses.  
- Compare **Random Forest Regressor** and **AdaBoost Regressor** to evaluate accuracy, stability, and interpretability.  
- Provide an **analytic framework** that can evolve into an educational early-warning system.

---

## 💼 My Contributions

| **Stage**                                    | **Responsibility**     | **Description**                                              |
| :------------------------------------------- | :--------------------- | :----------------------------------------------------------- |
| **Data Preprocessing & Feature Engineering** | Data Structuring       | Transformed raw evaluation records of 88 students into a consistent, model-ready dataset by unifying five subjective dimensions (test requirements, plans, cases, defect discovery, reports). |
|                                              | Feature Engineering    | Conducted correlation & distribution checks; removed redundant fields; created derived metrics such as weighted process scores. |
|                                              | Dataset Partition      | Split data into train/validation/test sets with controlled random seeds for reproducibility. |
| **Model Training & Evaluation**              | Random Forest Pipeline | Built Random Forest regression model; tuned key hyperparameters (tree depth, leaf size, splits). |
|                                              | Baseline Comparison    | Compared with AdaBoost using identical folds; Random Forest achieved superior performance (MAE ≈ 1.15, R² ≈ 0.93). |
|                                              | Visualization          | Generated prediction–actual scatter, residual plots, and feature-importance charts to interpret variable contributions. |
| **Paper Collaboration**                      | Research Support       | Contributed analysis and visuals; did not participate in manuscript writing. |

---

## 🧠 Why Use Subjective & Process Evaluations?

| **Perspective**      | **Explanation**                                              |
| :------------------- | :----------------------------------------------------------- |
| **Hidden Skills**    | Subjective and process indicators (planning, documentation, collaboration) capture capabilities often diluted in exam scores. |
| **Early Signals**    | These metrics appear mid-semester, providing opportunities for early intervention before final exams. |
| **Noise Reduction**  | Combining multiple dimensions (objective + subjective) triangulates evaluation, improving stability and interpretability. |
| **Course Alignment** | Software engineering inherently values process quality—quantifying those dimensions matches the course’s learning outcomes. |

Additional semi-structured data that can enrich predictive modeling include:

- Refined rubrics: requirement completeness, test coverage, documentation clarity.  
- Process metadata: submission timing, iteration count, bug resolution time.  
- Learning trajectories: tool-usage logs, practice coverage, discussion activity.  
- Peer/self-evaluation: calibrated survey items on teamwork consistency.  
- Text feedback signals: keywords from instructor comments (“insufficient testing”, “naming inconsistent”).  
- Participation indicators: punctuality, task completion ratio, group workload balance.

---

## 🧩 If Deployed in a Real Educational System

A real-world predictive information system based on this research would require the following **modules and governance mechanisms**:

- **Unified Data Dictionary & Rubrics** – Consistent field definitions and event vocabularies to ensure cross-class comparability.  
- **Data Quality & Validation** – Automated anomaly detection, missing-value alerts, random sampling review.  
- **Privacy & Compliance** – Informed consent, anonymization, retention policies, and IRB/ethics approval.  
- **Access Control & Audit (RBAC/ABAC)** – Tiered visibility for teachers, administrators, and auditors with activity logs.  
- **Feature & Model Versioning** – Traceable training data, feature sets, and model checkpoints for reproducibility.  
- **Fairness & Bias Evaluation** – Group-level performance tracking (gender, class, major) with deviation thresholds.  
- **Interpretability & Appeals** – SHAP or feature-contribution visualization with explainable thresholds and appeal procedures.  
- **Intervention Workflow** – Closed-loop design: prediction → early warning → personalized support → follow-up.  
- **Pre-Deployment Validation** – Historical replay, cross-semester testing, and controlled A/B rollout.  
- **Monitoring & MLOps** – Data/model drift detection, SLA metrics, rollback triggers, emergency procedures.  
- **Integration with LMS** – SSO, gradebook, and assignment synchronization for seamless operation.  
- **Training & Change Management** – Teacher handbook, FAQ, risk boundaries, and version release notes.  
- **Reporting & Dashboards** – Multi-level dashboards (teacher / department / admin) with confidence intervals and disclaimers.  
- **Governance Committee** – A standing Data & Algorithm Governance Board including academic, legal, and parent representatives.

---

## 💡 Insights

This project transformed how I perceive educational assessment:  
It demonstrated that even **subjective or semi-structured data**, when cleaned and governed, can become a valid predictive signal.

More importantly, it revealed how **information management principles** — data dictionary, lineage, quality, and compliance — form the **backbone of ethical AI deployment** in education.

> “An algorithm may predict performance, but only governance ensures it is trusted and useful.”

---

## 🧩 Skills Demonstrated

Educational Data Mining · Data Cleaning & Feature Engineering · Machine Learning (Random Forest) · Model Evaluation & Visualization · Data Governance · Ethical AI Frameworks  

---

## 💬 Note

This project was conducted under the supervision of **Sanda University’s research ethics committee**.  
All student data were **anonymized** and used solely for **research and educational purposes**.