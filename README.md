# Intellihack_TeamSemiColon_3Here’s a concise *README.md* file in markdown format based on your implementation:

markdown
# Qwen 2.5-3B Fine-Tuning for AI Research Q&A

This project fine-tunes the **Qwen 2.5-3B-Instruct** model to enhance its ability to answer AI research-related questions by leveraging recent research papers, technical blogs, and documents. The goal is to create a specialized model capable of retrieving, interpreting, and generating accurate responses based on technical AI literature.

📌 **Pretrained Model & Code References**
- **Fine-Tuned Model**: [Qwen2.5-3B-Instruct (4-bit)](https://huggingface.co/IsaraLi/TeamSemiColon_unsloth.Q4_K_M.gguf/tree/main)
- **Inference Script**: [Download Here](https://drive.google.com/file/d/1H5Y0q9ygZyXxDB76rn2oyDDANJdQuDpm/view?usp=sharing)

## 🔹Base Model Details
- **Base Model**: [Qwen2.5-3B-Instruct](https://huggingface.co/Qwen/Qwen2.5-3B-Instruct)
- **Quantization**: QLoRA (4-bit) for memory efficiency
- **Training Framework**: Unsloth for accelerated fine-tuning
- **Trainer Used**: SFTTrainer (from `trl`)

## 🔹 Dataset Preparation
The dataset was curated from:
- **Research Papers**: Extracted via PyMuPDF with OCR fallback for scanned documents.
- **Technical Blogs & Documentation**: Processed from Markdown files.
- **Synthetic Q&A Pairs**: Generated using **valhalla/t5-base-qg-hl** for question generation.

### 🔸 Preprocessing Steps
- **Text Extraction & Cleaning** (PDF parsing, OCR, Markdown processing, regex cleaning)
- **Tokenization & Formatting** (Sentence segmentation, text normalization, structured Q&A formatting)
- **Augmentation** (Paraphrasing, synthetic Q&A generation, noise injection, entity replacement)

## 🔹 Evaluation & Results
- **Metrics Used**: Training loss, validation loss, and correctness via DeepEval GEval.
- **Key Observations**:
  - Training loss steadily decreased, indicating successful fine-tuning.
  - Validation loss plateaued after 100 steps, suggesting model stabilization.
  - The model demonstrated improved response accuracy on AI-related queries.

## 🔹 Optimization Techniques
- **QLoRA**: Reduced VRAM usage while maintaining fine-tuning effectiveness.
- **Gradient Accumulation**: Balanced batch size limitations.
- **Paraphrased Data Augmentation**: Increased response diversity.
- **Adversarial Prompting**: Improved robustness in handling ambiguous AI research queries.

## 🔹 Inference
The fine-tuned model can be deployed for AI research Q&A with optimized inference speed.


## 🔹 Conclusion
This fine-tuning process successfully optimized **Qwen2.5-3B-Instruct** for AI research Q&A. The model now exhibits enhanced reasoning and accuracy in answering technical questions from research papers and AI literature.

---
🚀 **Developed with Unsloth, QLoRA, and DeepEval**