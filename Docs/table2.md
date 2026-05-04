+----+-----------+----------+-----------+--------------------+------------------+------------------+---------------------------+------------------------------+
| ID | Model     | Dataset  | Case Type | Sample/Window Ref  | Raw Score        | Decision         | Dominant Factors          | Interpretation               |
+----+-----------+----------+-----------+--------------------+------------------+------------------+---------------------------+------------------------------+
|  1 | Kitsune   | OS-Scan  | TP        | `kitsune_selected_tp_rows.csv` (last sample) | 0.26677650 | Attack (e>T)   | Group-level view: MAC-IP, IP, Jitter, IPtoIP, Socket | Correct attack detection |
|  2 | Kitsune   | OS-Scan  | FN        | `kitsune_selected_fn_rows.csv` (last sample) | 0.14151901 | Benign (e<=T)  | Group-level view: MAC-IP, IP, Jitter, IPtoIP, Socket | Missed attack |
|  3 | Kitsune   | OS-Scan  | FP        | `kitsune_selected_fp_rows.csv` (last sample) | 0.30298338 | Attack (e>T)   | Group-level view: MAC-IP, IP, Jitter, IPtoIP, Socket | False alarm on benign flow |
|  4 | RNN-IDS   | NSL-KDD  | TP        | Not fixed in repo snapshot                     | N/A        | Attack         | Feature groups g1..g22 (explanation.py grouping)      | Add from final run output |
|  5 | RNN-IDS   | NSL-KDD  | FN        | idx=21930 (`kdd_selected_fn_rows_122.csv`)    | 0.44356757 | Benign (<0.5)  | Feature groups g1..g22                                | Under-sensitive prediction |
|  6 | RNN-IDS   | NSL-KDD  | FP        | idx=571 (`kdd_selected_fp_rows_122.csv`)      | 0.71169140 | Attack (>=0.5) | Feature groups g1..g22                                | Over-sensitive prediction |
|  7 | ODDS/LSTM | NSL-KDD  | FP        | idx=19114 (`kdd_history_selected_fp_rows_122.csv`) | 0.92638266 | Attack (>=0.5) | Feature groups g1..g22                           | Strong false alarm |
+----+-----------+----------+-----------+--------------------+------------------+------------------+---------------------------+------------------------------+

Notes:
- For Kitsune, `Raw Score` is reconstruction error `e`; threshold `T = 0.20776056`.
- For RNN/LSTM paths, `Raw Score` is sigmoid probability with decision threshold `0.5`.