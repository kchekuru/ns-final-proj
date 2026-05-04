+----+-----------+----------+----------+-----------+--------+--------+--------+--------+--------+--------+--------+----------+
| ID | Model     | Dataset  | Type     | Threshold | Acc    | Prec   | Recall | F1     | FPR    | FNR    | AUC    | Notes    |
+----+-----------+----------+----------+-----------+--------+--------+--------+--------+--------+--------+--------+----------+
|  1 | Kitsune   | OS-Scan  | AE       | 0.2077606 | N/A    | N/A    | N/A    | N/A    | N/A    | N/A    | N/A    | Uses published `kitsune.h5`; known TP/FN/FP scores tracked in explanation pipeline |
|  2 | AE-IDS    | NSL-KDD  | AE       | dyn (mu+2s)| N/A   | N/A    | N/A    | N/A    | N/A    | N/A    | N/A    | Threshold computed from reconstruction error in training script |
|  3 | RNN-IDS   | NSL-KDD  | RNN      | 0.5       | N/A    | N/A    | N/A    | N/A    | N/A    | N/A    | N/A    | Binary decision from sigmoid probabilities (`>=0.5`) |
|  4 | ODDS/LSTM | NSL-KDD  | LSTM     | 0.5       | N/A    | N/A    | N/A    | N/A    | N/A    | N/A    | N/A    | Stateful LSTM variant; decision threshold `>=0.5` |
+----+-----------+----------+----------+-----------+--------+--------+--------+--------+--------+--------+--------+----------+

Legend:
- `dyn (mu+2s)` = threshold calculated as mean(reconstruction_error) + 2*std(reconstruction_error)
- `N/A` = aggregate metric not precomputed and persisted in repository artifacts; recompute during final evaluation run