# D7084E XAI Lab 4.2: Robustness, Attacks and Honest Explanations

This repository contains the Lab 4.2 analysis notebook, its saved result tables, and the B1 noise plot. The notebook evaluates binary benign/attack classification, input corruption, constrained evasion, feature importance, ensemble behavior, and explanation fidelity.

## Dataset

The notebook reads all CSV files from 'data/'. The files currently used here are CICIDS2017 flow CSVs, and the notebook's preprocessing and saved results correspond to those files. The assignment handout in this course folder names CICIDS2018; confirm with the instructor or the Lab 1 dataset which version is intended before submission. Do not treat results from one dataset version as results for the other.

Dataset files are not stored in this Git repository. Place the required CSV files in 'data/' before running the notebook. The notebook combines the files, removes capture identifiers and exact duplicates, replaces infinities with missing values, converts feature columns to numeric, drops unlabeled rows, and maps 'BENIGN' to 0 and all attack labels to 1.

## Environment and Run

Use Python with Jupyter and these packages:

'''bash
python -m pip install jupyter numpy pandas matplotlib scipy scikit-learn shap lime
'''

Open 'Lab4_2_Robustness_Attacks.ipynb' in VS Code or Jupyter, select that Python environment, and run all cells from top to bottom from the repository root. 'SEED = 42' is used throughout. 'USE_SAMPLE = False' runs on the full dataset; this is computationally intensive, especially the feature-removal experiments in E2. Set it to 'True' only for a quick smoke test, not for the reported final results.

The notebook writes CSV tables to 'results/' and the B1 noise figure to 'figures/'. The notebook itself also contains the plots and analysis answers. Existing outputs are saved in the notebook and the CSVs; rerunning the notebook reproduces them only with the same dataset and compatible package versions.

## Repository Contents

- 'Lab4_2_Robustness_Attacks.ipynb': analysis and saved cell outputs for Parts A-F.
- 'results/': exported baseline, robustness, attack, feature-removal, and explanation tables.
- 'figures/B1_noise.png': macro-F1 and recall under clipped Gaussian noise.
- 'README.md': setup and reproducibility notes.

## Submission Notes

The assignment also requires a separate 2-3 page report with the specified headings, captioned figures/tables, a screenshot of the code, and a one- or two-line "Who did what" statement. That report and contribution statement are not included in this repository yet. The assignment also asks users of AI assistants to disclose that use in the report. No authorship or contribution details are inferred here.