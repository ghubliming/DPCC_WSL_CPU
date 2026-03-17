## What's Done vs Remaining (CPU - Seed 5)

| Seed | Status | Epochs |
| --- | --- | --- |
| **Seed 5** | 🔄 **Crashed** | 0–65 complete, stopped at epoch 66 step 417 |
| Seed 6 | ⏳ Not started | — |
| Seed 7 | ⏳ Not started | — |
| Seed 8 | ⏳ Not started | — |
| Seed 9 | ⏳ Not started | — |

---

## Time Per Epoch (from logs)

From your CPU logs, picking sample epochs:

| Epoch | Time |
| --- | --- |
| 0 | 1:35 |
| 1 | 1:48 |
| 2 | 1:39 |
| 17 | 1:44 |
| 35 | 1:52 ← slowest |
| 49 | 1:33 ← fastest |
| **Average** | **~1:40 (100 sec)** |

---

## Total Time Estimate

|  | Calculation | Time |
| --- | --- | --- |
| Seed 5 remaining | ~34 epochs × 1:40 | **~57 min** |
| Seed 6 | 100 epochs × 1:40 | **~2h 47min** |
| Seed 7 | 100 epochs × 1:40 | **~2h 47min** |
| Seed 8 | 100 epochs × 1:40 | **~2h 47min** |
| Seed 9 | 100 epochs × 1:40 | **~2h 47min** |
| **Total remaining** |  | **~12h 5min** |

---

## CPU vs Colab Comparison

|  | CPU (WSL) | Colab T4 |
| --- | --- | --- |
| Speed | ~10 it/s | ~12 it/s |
| Time per epoch | **~1:40** | **~1:22** |
| Time per seed | **~2h 47min** | **~2h 17min** |
| 5 seeds total | **~14h** | **~11.5h** |
| Speedup | 1× | **~1.2×** |

**Both CPU and Colab are essentially the same speed** — confirming the model is **not using GPU** in either case. The T4 GPU is available but untouched. Fixing the device patches would bring this down to **~50 min total** for all 5 seeds. ✓