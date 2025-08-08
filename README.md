# 🧠 ARC Challenge Africa: Abstraction & Reasoning with Logic-Based AI

Welcome to my solution for the [Zindi ARC Challenge Africa](https://zindi.africa/competitions/the-arc-challenge-africa) — a competition inspired by the ARC-AGI benchmark that tests **true reasoning** over traditional training. This repo contains the exact pipeline that earned me a **5th place finish** 🏅!

---

## 📦 Repository Structure

```
📁 ARC-Challenge/
├── ARC_Solution.ipynb          ← My final logic-based solution notebook
├── train.json                  ← Training tasks (input/output pairs)
├── test.json                   ← Test tasks to predict
├── SampleSubmission.csv        ← Submission format to resemble
├── requirements.txt            ← Required libraries
├── README.md                   ← This file!
```

---

## 🎯 Problem Overview

The ARC (Abstraction and Reasoning Corpus) challenge presents grid-based puzzles, where each task contains:
- ✅ **Training examples** (input/output grid pairs)
- ❓ **Test input**, where the goal is to produce a matching output grid

Each grid uses integers 0–9 to represent colors. There’s no model training — the system must reason directly from examples.

---

## 🚀 My Approach: Human-Like Reasoning with Visual Feedback

Instead of machine learning, I built a **logic-driven pipeline** that mimics how a human would solve puzzles.

### 🧩 Step-by-Step Logic Chain

1. **Visualize training and test grids** interactively
2. **Infer the expected output shape** from sample submission
3. **Detect 1-to-1 color mappings** and apply to test input
4. **Apply geometric transformations** (flip, rotate, transpose)
5. **Check shape transformations** (dilation, erosion, outline detection)
6. **Fallback heuristics** (tiling, color shifts, border padding)
7. **Resize output** to match target shape
8. **Flatten and save** as CSV

---

## 👁️ Visualization

Two interactive viewers were used:
- 🧠 **Training Viewer**: See how input→output transforms
- 🔍 **Prediction Viewer**: Inspect test input and generated output

This helped quickly debug and iterate logic.

---

## 📈 Performance

| Metric        | Value                  |
|---------------|------------------------|
| 🏆 Rank        | 5th                  |
| 📊 F1 Score    | 0.33      |
| ⏱️ Inference   | ~10 seconds for all tasks |
| 🤖 Model Used  | Rule-based logic only  |

---
## ⚙️ How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/KEYSTATS/ARC-CHALLENGE-AFRICA.git
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Ensure `train.json`, `test.json`, and your submission CSV are in the same folder.

4. Run the notebook:
   - Open `ARC_Solution.ipynb` in Jupyter or Colab
   - Run all cells to generate `arc_agi_final_submission.csv`

---

## 📌 Key Insights

- ✅ **Lack of training data ≠ lack of patterns** — logic is key.
- 🧠 **Simple rules solve surprisingly many puzzles**
- 🛠️ Combining color, geometry, and shape logic = robust baseline

---

## 🔮 Future Improvements

- Combine multiple transformations for multi-step tasks
- Add symbolic reasoning or counting-based modules
- Train a meta-controller to select best logic block per task

---

## 📚 References

- [ARC-AGI Benchmark (Chollet et al.)](https://arxiv.org/abs/2412.04604)
- [Zindi ARC Challenge Africa](https://zindi.africa/competitions/the-arc-challenge-africa)
- [Zindi Documentation Guidelines](https://zindi.africa/learn/documentation-guideline)

---

## 👨‍💻 Author

**Jackson Kahungu Njeri**  
Data Scientist | Top 5 Finalist  
🔗 [Zindi Profile](https://zindi.africa/users/keystats)

---

⭐ If you find this project inspiring, consider giving it a star!
