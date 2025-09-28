# Zero-Shot Defect Classification with CLIP

This project performs **zero-shot defect classification** on the **hazelnut subset** of the [MVTec-AD dataset](https://www.mvtec.com/company/research/datasets/mvtec-ad) using **OpenAI's CLIP model**. 

The main goal is to classify hazelnuts as either **defect-free ("good")** or belonging to specific **defect categories** such as `"print"`, `"hole"`, `"crack"`, and `"cut"` without training on labeled examples. The system leverages:

- **Natural language prompts** to describe each defect type  
- **Optional support images** to enhance few-shot classification  
- **CLIP embeddings** to measure similarity between images and text prototypes  

The workflow includes:

1. Defining textual prompts and support images for each defect class.  
2. Encoding prompts and support images to create class prototypes.  
3. Encoding test images and computing similarity with prototypes.  
4. Predicting defect categories based on the highest similarity.  
5. Evaluating performance using a **confusion matrix** and per-class metrics.  

This approach extends previous **anomaly detection with CLIP (WinCLIP / CLIP-AC)** to a **multi-class defect classification task**, achieving ~89% overall accuracy on the hazelnut dataset. Misclassifications primarily occur for visually similar defect types with limited samples, highlighting the importance of support images and carefully crafted prompts.
