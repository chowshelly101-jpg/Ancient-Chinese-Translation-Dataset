# Ancient-Chinese-Translation-Dataset
### A dataset for translating Ancient Chinese to Modern Chinese and English.

![DH Awards 2025 Nominee](https://img.shields.io/badge/DH%20Awards-2025%20Nominee-blue)
![Data Size](https://img.shields.io/badge/Total%20Corpus-490k%2B%20Pairs-green)
![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey)

## 📖 Project Overview

This project introduces a comprehensive parallel corpus designed for Digital Humanities research, Classical Chinese translation studies, and Large Language Model (LLM) instruction tuning.

The full corpus consists of approximately **490,000 aligned sentence pairs/triplets**, constructed to bridge the semantic gap between Ancient Chinese, Modern Chinese, and English. It covers **8 major literary genres** and dozens of classic texts, making it one of the most diverse datasets in the field.

**Purpose:** 
This repository serves as a **sample showcase** providing 4,000 representative entries to demonstrate the data structure, quality, and annotation standards.

---

## 🗂 Dataset Composition

The dataset spans **8 distinct categories** of classical literature:
1.  **Military** (e.g., *Sun Tzu's Art of War*)
2.  **Science & Technology** (Traditional Chinese Medicine, Astronomy, Agriculture)
3.  **Philosophy** (e.g., *The Analects*, *Mencius*)
4.  **History** (e.g., *Records of the Grand Historian / Shiji*)
5.  **Literary Criticism** (Wenlun)
6.  **Novels** (Ming and Qing dynasty fiction)
7.  **Prose** (Classical essays)
8.  **Poetry** (Tang/Song poetry)

### Data Statistics
*   **Total Corpus Size:** ~490,000 aligned segments.
*   **Sample Size (Open Access):** 4,000 segments (hosted in this repo).

---

## 📂 Repository Contents (Samples)

We provide two JSON files in this repository:

| File Name | Description | Count |
| :--- | :--- | :--- |
| `antoen_2000.json` | **Ancient Chinese → Modern Chinese** alignment. | 2,000 entries |
| `antomotoen_2000.json` | **Ancient → Modern → English** tri-linear alignment. | 2,000 entries |

### Data Format (LLM-Ready)
The data is formatted in JSON, specifically structured for **Instruction Tuning** (compatible with frameworks like LLaMA-Factory).

**Example Entry:**

```json
{
    "instruction": "你是一名古代典籍翻译家，请将以下古代汉语文本翻译为现代汉语，再基于现代汉语翻译为英文。每个步骤需清晰分段，输出格式请标明“【文言→现代】”和“【现代→英文】”标签。",
    "input": "谓太子曰：\"齐奉太子而立之，楚王请割地以留太子，齐少其地。太子何不倍楚之割地而资齐？齐必奉太子。\"太子曰：\"善。\"倍楚之割而延齐。楚王闻之，恐，益割地而献之，尚恐事不成。故曰可以使楚益人地也。\n",
    "output": "【文言→现代】\n 苏秦对楚国太子说：\"齐国支持太子并且要拥立您，楚王请求割让土地给齐国来把太子留在齐国，齐国嫌楚王割让的土地太少。太子何不奉送比楚王所割让的多一倍的土地来资助齐国呢？齐国一定会支持太子的。\"太子说：\"好。\"就奉送比楚王所割让的多一倍的土地来扩大齐国领地。楚王听说了这件事，很恐惧，就割让更多的土地进献给齐国，却还是担心事情不能成功。所以说可以让楚国割让更多的土地。\n【现代→英文】\n Su Qin had a talk with the crown prince of Chu and said, “The people of the state of Qi support you and want to enthrone you to be king of your state. However, the king of Chu has offered to cede some land to Qi and thus asked Qi to detain you here. But we think Chu is not offering enough land. Why not promise to give Qi twice the amount of land to strengthen Qi? As a result, Qi will definitely support you in fighting for the state of Chu.\" The crown prince said, “Excellent.”Then he offered twice the amount of land to enlarge Qi's territory. When the king of Chu heard of this， he was scared. So he ceded more territory to Qi. After that, he still feared that Qi might not support him. So it is said, “The state of Chu can be coerced into presenting more territory to Qi by exhibiting loyalty to the crown prince of Chu.”"
}
