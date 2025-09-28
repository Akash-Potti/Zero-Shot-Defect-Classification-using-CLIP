# Zero-Shot Defect Classification with CLIP

This repository implements a **zero-shot defect classification** pipeline using **OpenAI’s CLIP model**. The focus is on the `hazelnut` subset of the **MVTec-AD** dataset. The project demonstrates the extension of zero-shot anomaly classification (normal vs defective) to **multi-class defect classification**.

---

## Table of Contents

- [Overview](#overview)  
- [Dataset](#dataset)  
- [Project Structure](#project-structure)  
- [Installation](#installation)  
- [Usage](#usage)  
- [Methodology](#methodology)  
- [Results](#results)  
- [Observations & Future Improvements](#observations--future-improvements)  
- [License](#license)  

---

## Overview

The goal of this project is to classify hazelnuts into **normal** and different **defect categories** using **zero-shot CLIP embeddings**, with optional support images for few-shot enhancement. The classification pipeline consists of:

1. Generating class prototypes from **text prompts** and optional support images.  
2. Encoding test images using CLIP.  
3. Classifying images based on **cosine similarity** to class prototypes.  

This avoids the need for extensive labeled datasets or model fine-tuning.

---

## Dataset

- **Dataset:** [MVTec-AD](https://www.mvtec.com/company/research/datasets/mvtec-ad) (hazelnut subset)  
- **Data split:** Test set only  
- **Defect types:** `print`, `hole`, `good`, `crack`, `cut`  

Example image filenames: `hazelnut_good_023.png`, `hazelnut_crack_002.png`.

---

## Project Structure

