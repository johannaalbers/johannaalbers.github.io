---
layout: page
title: Projects
subtitle: Selected work, with the code behind it
---

All code is on [GitHub](https://github.com/johannaalbers). These three are the ones worth your time.

---

### ICU lactate and mortality, interpreted by a language model

An end to end pipeline: SQL cohort extraction from MIMIC-III, a multivariable logistic regression on 22,302 ICU stays, and a language model that turns the model output into a publication style results paragraph.

Higher lactate was strongly associated with ICU death (OR 2.82, 95% CI 2.66 to 2.99). The pipeline is built to stay inside the PhysioNet Data Use Agreement: only aggregate statistics ever leave the machine.

*Python, SQL, statsmodels.* [Repository](https://github.com/johannaalbers/icu-lactate-llm-interpreter)

---

### Extracting heart failure signals from clinical notes

Ejection fraction, the single most important number in heart failure, usually lives in free text rather than in a structured database field. This project pulls it out of discharge summaries and echocardiogram reports in MIMIC-III using regular expressions.

The extracted data reproduces the known bimodal distribution of reduced and preserved ejection fraction, which is the best available evidence that the extraction works. It also surfaced a physiologically impossible value above 150 percent, a reminder that data quality checks are not optional.

*R, SQL, regex.* [Repository](https://github.com/johannaalbers/EHR-NLP-Heart-Failure-Analysis)

---

### Heart disease markers, from analysis to dashboard

Exploratory analysis in Python to identify which diagnostic markers separate patients with and without heart disease, then an explanatory Power BI dashboard built for a clinical audience.

The point of the project is the second half: translating a statistical result into something a decision maker understands in thirty seconds.

*Python, Power BI.* [Repository](https://github.com/johannaalbers/heart-disease-explanatory-visualization)

---

### Also on GitHub

Survival analysis (Kaplan Meier, Nelson Aalen, Cox proportional hazards), applied regression and missing data imputation in R, and supervised classification in scikit-learn.
