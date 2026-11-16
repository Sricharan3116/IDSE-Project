# 🤖 Sortbot Factory

**Learn data science by playing.** You run a fruit-sorting factory and teach a robot to tell oranges from lemons. Each of the 5 shifts is a *different* real data science job, and a live **Data Science Notebook** next to the game shows the actual Python (pandas / scikit-learn), the DataFrame rows and the confusion matrix updating as you play.

## Play

- **Online:** enable GitHub Pages (Settings, Pages, Deploy from branch, `main` / root) and open `https://<your-username>.github.io/<repo-name>/`
- **Locally:** download the repo and double-click `index.html`. No build step, no dependencies.

## The 5 shifts

| # | Shift | Data science skill | What you do | What you learn |
|---|-------|--------------------|-------------|----------------|
| 1 | Draw the Line | Classification | Drag two handles to place a line on the colour/size map | A classifier is a **decision boundary** |
| 2 | Clean the Belt | Data cleaning | Pick the right pandas tool (`fillna`, `dropna`, `clip`, `drop_duplicates`) for dirty fruit before it reaches the robot | Missing values, outliers and duplicates corrupt a model |
| 3 | Pick the Sensors | Feature selection and leakage | Choose 2 of 5 sensors; one is noise, one (`price_tag`) disappears at an audit | Good features are informative **and** available in production |
| 4 | Tune the Brain | Overfitting (k-NN) | Set `k` and memory size while 20% of labels are wrong; compare practice vs real accuracy | Tiny `k` memorises noise; always test on unseen data |
| 5 | Drift Watch | Monitoring and retraining | Watch the quality monitor and press **Retrain** at the right time ($25 each) | Deployed models decay when data **drifts** |

Stars are earned from profit. There is no game over: replay any shift from the numbered buttons.

## The live notebook

For every fruit the robot sorts, the notebook updates:

- `df.tail()`: the latest rows (green = correct, pink = mistake)
- the Python for the current step (`LogisticRegression`, `SGDClassifier`, `KNeighborsClassifier`, cleaning calls)
- `confusion_matrix` plus precision, recall and F1

## Tech

Single-file vanilla HTML, CSS and JavaScript with the Canvas API and Web Audio (sound effects, mute button). The classifiers (online logistic regression, batch retraining, k-NN) are implemented in plain JS. The only external resource is an optional Google Font (Fredoka) with a system fallback.

## Project structure

```
index.html        the whole game
assets/           screenshot for this README
LICENSE           MIT
```

## Ideas to extend

- Add a shift on train/test splits or cross-validation
- Let players edit the Python code and run it
- Save best stars with `localStorage`

## License

MIT
