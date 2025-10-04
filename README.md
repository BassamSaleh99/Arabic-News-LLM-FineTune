# Arabic-News-LLM-FineTune

This project focuses on **fine-tuning large language models (LLMs)** on Arabic news data to perform structured information extraction and text understanding tasks. The implementation leverages **parameter-efficient fine-tuning (LoRA adapters)** and integrates with **vLLM** for optimized inference.

---

## 🎯 Project Objective

Develop a domain-adapted LLM capable of processing Arabic news articles with the following capabilities:
- **Entity extraction** (persons, locations, organizations, events, etc.)
- **News classification** (politics, sports, economy, technology, etc.)
- **Keyword and summary generation** for SEO optimization
- **Title generation** for readability and engagement
- **Optimized inference** for deployment in real-world applications

---

## 🛠️ Technical Overview

The project integrates several modern NLP tools and frameworks:

- **[LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory)**  
  Used for fine-tuning with LoRA adapters, enabling efficient training with limited resources.

- **[Hugging Face Transformers](https://huggingface.co/transformers)**  
  Provides the pre-trained models, tokenizer management, and model APIs.

- **[vLLM](https://vllm.ai/)**  
  Powers optimized inference through PagedAttention and efficient GPU utilization.

- **[Weights & Biases](https://wandb.ai/)**  
  Used for experiment tracking and visualization of training metrics.

---

  ## ⚡ Workflow

1. **Environment Setup**  
   Installation of dependencies including `transformers`, `datasets`, `optimum`, `vllm`, and `wandb`.

2. **Dataset Preparation**  
   - Arabic news stories are processed into structured JSON format using **Pydantic schemas**.  
   - Each entry contains the article, extracted entities, category, and summaries.

3. **Fine-Tuning**  
   - LoRA adapters are trained using **LLaMA-Factory**.  
   - Training progress and metrics are logged with **W&B**.

4. **Evaluation**  
   - The model is tested on held-out news articles for extraction accuracy and classification performance.  

5. **Inference & Deployment**  
   - The fine-tuned model is loaded with adapters.  
   - **vLLM** is used for high-throughput and low-latency inference.

---

## 📚 Resources
- 📂 Data: [Google Drive Link](https://drive.google.com/drive/folders/1WJDf4obEqvqI0skV2Jz9_Q6S2MZ2zQkY?usp=drive_link)
- 📂 Model: [Google Drive Link](https://drive.google.com/drive/folders/1tZkibWza655tlTqWSj5I9RgWYrrN0z77?usp=drive_link)

---

## 📊 Results

- Successfully fine-tuned a pre-trained model on Arabic news.  
- Demonstrated capability to extract structured entities and generate concise summaries.  
- Verified cost efficiency through token consumption analysis.  
- Achieved optimized inference performance with **vLLM**.
