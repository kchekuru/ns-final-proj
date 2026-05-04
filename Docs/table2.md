+----+-----------+----------+-----------+--------------------+------------------+------------------+---------------------------+------------------------------+
| ID | Model     | Dataset  | Case Type | Sample/Window Ref  | Raw Score        | Decision         | Dominant Factors          | Interpretation               |
+----+-----------+----------+-----------+--------------------+------------------+------------------+---------------------------+------------------------------+
|  1 | Kitsune   | OS-Scan  | TP        | [fill]             | [fill]           | Attack           | [fill: MAC-IP/IP/... ]    | Correct attack detection     |
|  2 | Kitsune   | OS-Scan  | FN        | [fill]             | [fill]           | Benign           | [fill: MAC-IP/IP/... ]    | Missed attack                |
|  3 | Kitsune   | OS-Scan  | FP        | [fill]             | [fill]           | Attack           | [fill: MAC-IP/IP/... ]    | False alarm on benign flow   |
|  4 | RNN-IDS   | NSL-KDD  | TP        | [fill]             | [fill]           | Attack           | [fill: feature groups]    | Correct sequence detection   |
|  5 | RNN-IDS   | NSL-KDD  | FN        | [fill]             | [fill]           | Benign           | [fill: feature groups]    | Under-sensitive prediction   |
|  6 | RNN-IDS   | NSL-KDD  | FP        | [fill]             | [fill]           | Attack           | [fill: feature groups]    | Over-sensitive prediction    |
+----+-----------+----------+-----------+--------------------+------------------+------------------+---------------------------+------------------------------+