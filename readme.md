# Seed Classification using Random Forest

This project trains a Random Forest classifier to predict one of three seed classes from geometric measurements. It includes a small exploratory chart, a train/test split, model fitting, and accuracy evaluation.

## Dataset

The repository includes `seeds_dataset (2).csv`. The script uses these feature columns:

- `Area`
- `Perimeter`
- `Compactness`
- `Length of kernel`
- `Width of kernel`
- `Asymmetry coefficient`
- `Length of kernel groove`

The target is `Class (1, 2, 3)`. The script drops `Unnamed: 8` and `Unnamed: 9` before training.

## Workflow

1. Load the CSV with pandas and inspect its structure.
2. Remove the two unnamed columns.
3. Print the number of unique values in each remaining column.
4. Group by seed class and plot the sum of `Area`.
5. Split features and target with `random_state=42` and scikit-learn's default test fraction.
6. Fit a default `RandomForestClassifier`.
7. Predict the test labels and print accuracy.

## Technology

- Python
- pandas
- NumPy
- Matplotlib
- scikit-learn

## Run locally

```bash
git clone https://github.com/KARTHIKEYAN-GHOST/Seed_Classification_using_RandomForest.git
cd Seed_Classification_using_RandomForest

python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install pandas numpy matplotlib scikit-learn
```

The script currently reads `/content/seeds_dataset (2).csv`, a Google Colab path. Change it to:

```python
df = pd.read_csv("seeds_dataset (2).csv")
```

Then run:

```bash
python randomforestclassifier_implementation.py
```

## Output

The script displays a bar chart of total seed area by class and prints the accuracy score for the test split.
