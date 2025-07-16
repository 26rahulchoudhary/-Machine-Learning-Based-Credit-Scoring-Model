
# Credit Score Analysis

## Score Distribution Overview

The credit scores assigned to wallets span from **0 to 1000**, grouped into 10 ranges. Below is the count of wallets in each score bracket:

| Score Range | Number of Wallets |
|-------------|-------------------|
| 0-99 | 0 |
| 100-199 | 0 |
| 200-299 | 8 |
| 300-399 | 14 |
| 400-499 | 2011 |
| 500-599 | 1430 |
| 600-699 | 23 |
| 700-799 | 8 |
| 800-899 | 3 |
| 900-999 | 0 |

![Credit Score Distribution](/mnt/data/score_distribution.png)

## Key Observations

- The majority of wallets (3441 out of 3497) fall into the **400-599** range.
- Very few wallets score above **600**, and none fall below **200** or above **900**, indicating a **mid-heavy distribution**.

## Behavior Analysis

### Wallets in Lower Range (200–399)
- These wallets typically show **low average or total transaction volume**.
- They interact less frequently with key actions like `deposit` or `repay`.
- Behavior may suggest **infrequent participation**, **high-risk activity**, or **limited asset diversity**.

### Wallets in Higher Range (700+)
- These wallets generally display **consistent and high transaction activity**.
- Likely to have **higher total volume**, **low liquidation frequency**, and **broad asset diversity**.
- Exhibit characteristics aligned with **stable and responsible usage** of the protocol.

## Conclusion

The current scoring system effectively differentiates wallets based on transactional behavior, but shows a strong central bias. Further model refinement or calibration may enhance score range utilization and interpretability.
