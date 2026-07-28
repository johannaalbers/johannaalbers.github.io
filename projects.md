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

### When a classifier learns the speaker, not the disease

The UCI Parkinsons dataset is usually described as 195 observations. It is not:
it is 195 voice recordings from 32 people, six or seven each. A random
train/test split therefore places the same voice on both sides, and the model
can recognise the speaker instead of the disease.

Measured across 100 repeated splits, subject-aware splitting drops AUC from 0.93
to 0.80 and specificity from 0.44 to 0.34. Predicting Parkinson's for everyone
already gives 0.75 accuracy, so the honest model beats guessing by two points.

*Python, scikit-learn.* [Repository](https://github.com/johannaalbers/parkinsons-disease-classification)

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
