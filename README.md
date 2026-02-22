
#  Medical Assistant — Fine-Tuned LLM

A domain-specific medical chatbot built by fine-tuning **TinyLlama-1.1B-Chat** using **LoRA (PEFT)** on medical Q&A data.

**Purpose:** Improve answer quality on medical questions for education and quick reference.  
⚠️ Not intended for clinical or real-world medical decision-making.

---

## Links

- **Run in Colab:** https://colab.research.google.com/github/Jade-Isimbi/med-assistant-llm/blob/main/med_assistant.ipynb  
---

## Dataset

- **Source:** Medical Meadow Medical Flashcards (Hugging Face)  
- **Training samples:** 4,000  
- **Validation samples:** 508  
- Instruction–Question–Answer format  
- Tokenized to maximum length of 512 tokens  

---

##  Model & Training

- **Base model:** TinyLlama-1.1B-Chat  
- **Method:** LoRA fine-tuning (PEFT)  
- **Epochs:** 2  
- **Batch size:** 2  
- **Gradient accumulation:** 4  
- Trained on Google Colab (T4 GPU)

---

## Results (Base vs Fine-Tuned)

| Metric   | Base Model | Fine-Tuned |
|----------|------------|------------|
| BLEU     | 0.049      | 0.078      |
| ROUGE-1  | 0.265      | 0.354      |

Fine-tuning improved performance and answer relevance on medical questions.

---

## How to Run

1. Open the Colab link above.
2. Enable GPU (Runtime → Change runtime type → T4 GPU).
3. Run all cells in order.
4. Launch the Gradio interface to interact with the chatbot.

---

## ⚠ Disclaimer

This project is for educational purposes only.  
The model may generate incorrect medical information and should not be used for diagnosis or treatment decisions.
