# AudiSense
Code and dataset for the paper: "AudiSense: Dynamic Fusion of Behavioral and Textual Signals  for Suicidal Ideation Detection on TikTok"
## Abstract
AudiSense is a multimodal late-fusion framework for detecting suicidal ideation on TikTok. It fuses XLM-RoBERTa text encoding with XGBoost behavioral engagement classification through a Dynamic Gating Network (DGN) that learns per-video modality weights. The system addresses the algospeak problem — where creators replace sensitive words with coded expressions to evade moderation — by leveraging engagement signals that are harder to manipulate than text.
## Files
- `AudiSense1.ipynb`: full experiment code
- `DataCollection1.ipynb`: data collection and Whisper transcription
- `audisense_dataset_prepared.csv`: full dataset (136 videos)
- `split_train.csv`: training split (95 videos)
- `split_val.csv`: validation split (20 videos)  
- `split_test.csv`: test split (21 videos)
## Results

| System | AUPRC | ROC-AUC | F1 |
|--------|-------|---------|-----|
| **AudiSense (Ours)** | **0.86** | **0.92** | **0.75** |
| LR Stacking | 0.76 | 0.88 | 0.36 |
| XGBoost (engagement only) | 0.76 | 0.88 | 0.36 |
| XLM-RoBERTa (text only) | 0.48 | 0.68 | 0.59 |
| TF-IDF + SVM | 0.50 | 0.58 | 0.45 |
| Early Fusion MLP | 0.29 | 0.36 | 0.43 |
