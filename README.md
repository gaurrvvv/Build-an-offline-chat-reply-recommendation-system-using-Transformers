# 💬 Offline Chat-Reply Recommendation System using Transformers

This project builds an *offline chat-reply recommendation system* that predicts the next possible reply from *User A* when *User B* sends a message — using past two-person chat data as context.  
It fine-tunes a *Transformer-based model (GPT-2)* to generate coherent, context-aware replies, evaluated using BLEU and ROUGE metrics.

---

## 📁 Project Structure
ChatRec_Model.ipynb # Jupyter Notebook (model training, generation, evaluation)
Model.joblib # Saved fine-tuned GPT-2 model
Report.pdf # Detailed project report
ReadMe.txt # Offline usage instructions
README.md # GitHub documentation
---

## 🧠 Objective

- Build an *offline* conversational reply generation system.
- Use *Transformer models* (GPT-2) for natural language generation.
- Train the model on *two-person chat datasets*.
- Generate *context-aware* responses.
- Evaluate performance using BLEU, ROUGE, and Perplexity.

---

## 📊 Dataset

Two CSV files are required:

| Column Name      | Description |
|------------------|-------------|
| conversation_id | Unique ID for each conversation |
| user            | User identifier (A or B) |
| timestamp       | Message time (for sorting) |
| message         | Chat message text |

Example:
```csv
conversation_id,user,timestamp,message
1,A,2024-10-01 10:00,Hey there!
1,B,2024-10-01 10:01,Hi! How are you?

🧩 Model Details

Model Used: GPT-2 (fine-tuned offline)

Tokenizer: GPT-2 tokenizer

Max Sequence Length: 512 tokens

Training Epochs: 2

Batch Size: 1

| Metric         | Description                                                |
| -------------- | ---------------------------------------------------------- |
| *BLEU*       | Measures word overlap between generated and actual replies |
| *ROUGE*      | Evaluates semantic similarity                              |
| *Perplexity* | Measures model confidence (optional)                       |
