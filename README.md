# 🧠 Mental Health Among LGBTQ+

Analysis and Results for Poster Presentation for the 2025 annual meeting of the Society for Affective Science in Portland, OR. 

## 📌 Introduction

Suicide rates have risen in recent decades, with LGBTQ+ individuals reporting higher rates of depression, anxiety, and suicidality than peers (Wittgens et al., 2022; Hatzenbuehler et al., 2008; Kapatais et al., 2023).

---

## 🎯 Study Overview

- **Participants**: 625 LGBTQ+ individuals in relationships (mean age: 34.5)  
  - Lesbian (n=109), Gay (n=102), Bisexual (n=395), Other (n=19)
- **Platform**: Data collected online via *Connect* (2024)
- **Target**: Suicidal ideation in past two weeks (BDI-II)
- **Note**: This study was approved by an Institutional Review Board (IRB).
  - Due to the sensitive nature of the data and to protect participant privacy, the dataset cannot be publicly shared.

---

## 📊 Measures

Top 10 predictors (via Random Forest feature selection):

- **Mental Health**: BDI-II, STAI, Perceived Stress Scale  
- **Minority Stress**: Internalized Homonegativity, Concealment, Stigma Consciousness  
- **Emotion Regulation**: PANAS (Negative), NMR Scale, DERS  
- **Attachment**: ECR (Avoidance subscale)

---

## 🤖 Models Tested

| Model               | Balanced Accuracy | ROC AUC |
|---------------------|-------------------|---------|
| Logistic Regression | 0.82              | 0.94    |
| Naïve Bayes         | 0.86              | 0.91    |
| Random Forest       | 0.82              | 0.91    |
| Boosted Tree        | 0.78              | 0.91    |
| Tuned Models        | ~0.80–0.82        | ~0.91–0.92 |

🔍 **Naïve Bayes** and **Logistic Regression** performed best.  
⚠️ Model tuning led to overfitting without significant gains.

---

## 🧮 Confusion Matrices

- ### Logistic Regression
|                            | Actual Non-Suicidal    | Actual Suicidal     |
|----------------------------|------------------------|---------------------|
| **Predicted Non-Suicidal** | 97                     | 13                  |
| **Predicted Suicidal**     | 10                     | 34                  |

### Naïve Bayes
|                            | Actual Non-Suicidal    | Actual Suicidal     |
|----------------------------|------------------------|---------------------|
| **Predicted Non-Suicidal** | 87                     | 4                  |
| **Predicted Suicidal**     | 20                     | 43                  |

---

## 💡 Key Takeaways

- All models predicted suicidal ideation with high accuracy.
- Emotion- and stress-based predictors are strong indicators—valuable even outside clinical settings.
- Focusing on sexual minority data improves model relevance and effectiveness.

---

## 📚 References

See Poster PDF for full references
