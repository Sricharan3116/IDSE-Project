# 🤖 Sortbot Factory

**Learn data science by playing.**

You run a fruit-sorting factory and teach a robot to tell oranges from lemons. Each of the 5 shifts is a different real data science job, and a live **Data Science Notebook** next to the game shows the actual Python (pandas / scikit-learn), DataFrame rows and the confusion matrix updating as you play.

![Screenshot](assets/screenshot.png)

---

## 🎮 Play

**Live Game:** [🚀 Play Sortbot Factory](https://sricharan3116.github.io/IDSE-Project/)

**GitHub Repository:** [View Source Code](https://github.com/Sricharan3116/IDSE-Project)

**Run Locally:** Download the repository and double-click `index.html`. No build step, no dependencies.

---

## The 5 Shifts

| # | Shift | Data science skill | What you do | What you learn |
|---|---|---|---|---|
| 1 | Draw the Line | Classification | Drag two handles to place a line on the colour/size map | A classifier is a **decision boundary** |
| 2 | Clean the Belt | Data cleaning | Pick the right pandas tool (`fillna`, `dropna`, `clip`, `drop_duplicates`) for dirty fruit before it reaches the robot | Missing values, outliers and duplicates corrupt a model |
| 3 | Pick the Sensors | Feature selection and leakage | Choose 2 of 5 sensors; one is noise, one (`price_tag`) disappears at an audit | Good features are informative **and** available in production |
| 4 | Tune the Brain | Overfitting (k-NN) | Set `k` and memory size while 20% of labels are wrong; compare practice vs real accuracy | Tiny `k` memorises noise; always test on unseen data |
| 5 | Drift Watch | Monitoring and retraining | Watch the quality monitor and press **Retrain** at the right time ($25 each) | Deployed models decay when data **drifts** |

Stars are earned from profit. There is no game over: replay any shift from the numbered buttons.

---

## 📊 The Live Notebook

For every fruit the robot sorts, the notebook updates:

- `df.tail()`: the latest rows (green = correct, pink = mistake).
- The Python for the current step (`LogisticRegression`, `SGDClassifier`, `KNeighborsClassifier`, cleaning calls).
- `confusion_matrix` plus precision, recall and F1.

---

## 🛠️ Tech Stack

Single-file vanilla HTML, CSS and JavaScript with:

- Canvas API
- Web Audio API (sound effects and mute button)
- Online logistic regression
- Batch retraining
- k-NN classifiers

The classifiers are implemented in plain JavaScript. The only external resource is an optional Google Font (Fredoka) with a system fallback.

---

## 🚀 Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/Sricharan3116/IDSE-Project.git
