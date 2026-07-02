# Automated Resume Screening & Skill-Gap Analyzer

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-blueviolet?style=flat-square&logo=scikit-learn&logoColor=white)
![spaCy](https://img.shields.io/badge/spaCy-Linguistic_Pipeline-red?style=flat-square&logo=spacy&logoColor=white)
![NLP](https://img.shields.io/badge/NLP-TF--IDF%20%26%20Cosine_Similarity-success?style=flat-square)
![HR-Tech](https://img.shields.io/badge/HR--Tech-ATS_Screening-orange?style=flat-square)

## Executive Summary
This project implements an intelligent, automated **Applicant Tracking System (ATS)** screening engine. Designed for fast-paced HR teams, startup founders, and recruitment managers, the system processes unstructured candidate resumes, calculates their exact mathematical alignment against a target Job Description (JD), ranks them by match score, and outputs a clear skill-gap audit. 

To demonstrate technical calibration on real-world chaotic data, this pipeline includes a gold-standard benchmark profile injection to validate the mathematical precision of the text matching algorithms.

---

## What the Scoring System Means
Evaluating hundreds of applications manually introduces human fatigue and operational bottlenecks. This pipeline replaces manual reviews with an objective, dual-layer Natural Language Processing (NLP) framework:

1. **TF-IDF Vectorization (Context Weights):** The pipeline strips away text formatting, contact noise, and common grammar words. It converts the text into numerical vectors, applying heavier weights to essential, rare domain skills (e.g., *TensorFlow*, *OpenCV*, *YOLOv8*) while ignoring generic corporate phrasing.
2. **Cosine Similarity (The Alignment Metric):** The system calculates the geometric angle between the Job Description vector and each candidate resume vector. The resulting `Match_Score` represents how closely the overall vocabulary of the candidate maps to the role profile. 
3. **Linguistic Skill Audit:** Beyond a raw percentage score, the engine uses a `spaCy` NLP model to check for the presence of precise required keywords, listing exactly what core competencies are met versus missing.

---

## How a Business Can Use This for Strategic Planning
A data-driven candidate screening system transforms how a talent acquisition team operates, allowing startup founders and business managers to execute smarter workforce planning:

* **Massive Reduction in Time-to-Hire:** Instead of recruiters spending days sorting through non-viable resumes, the system instantly identifies the top tier of candidates. Recruiters can skip manual parsing entirely and focus on interviews.
* **Objective Target Validation (The Talent Radar):** If the baseline applicant pool contains an absence of skilled talent, the system safely triggers a low maximum match score across standard applicants (e.g., arbitrary overlap with generic baseline roles). This immediately signals to management that their sourcing channels need optimization.
* **Instant Interview Playbooks via Skill-Gap Audits:** The built-in gap analyzer explicitly separates a candidate's found competencies from missing technical pre-requisites. This outputs an instant, transparent brief for hiring managers, pinpointing the precise technical questions to ask during live evaluations.

---

## Pipeline Calibration & Testing
To ensure the mathematical models function correctly, a highly qualified **Machine Learning Engineer Benchmark** profile was intentionally introduced to test the data array. 

Upon execution, the scoring engine verified system calibration flawlessly: the targeted candidate instantly bypassed irrelevant baseline profiles to secure the top rank with a highly distinct similarity threshold, while the integrated linguistic auditor cleanly mapped the matching and missing technical milestones.
