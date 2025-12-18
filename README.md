# Predicting Cascading Failure Onset in Power Systems — Multi-Model ML

**Goal**  
Predict onset urgency (Urgent / Relatively Urgent / Non-Urgent) so operators can prioritize interventions and reduce outage risk.

**Data & Features**  
Graph/adjacency matrices → engineered node/graph features (degree, centrality, clustering, deltas).  
Raw data may be restricted; see `data/README.md` for access or samples.

**Models & Results (test)**  
- SVM ≈ 84.9%  
- Decision Tree ≈ 82.7%  
- KNN ≈ 77.8%  
(plus precision/recall/F1 and confusion matrices in `figures/`)

**Repo map**  
- `notebooks/cascading_failure_models.ipynb` — end-to-end workflow  
- `src/main.py`, `src/utils.py` — training/eval + loaders  
- `figures/` — confusion matrices & ROC/PR curves  
- `docs/` — paper, slides, method notes  
- `data/` — sample or instructions (raw not committed)

**How to run**  
```bash
pip install -r requirements.txt
# Option A: open the notebook and Run All
# Option B (scripts, if provided):
# python -m src.main --model svm
