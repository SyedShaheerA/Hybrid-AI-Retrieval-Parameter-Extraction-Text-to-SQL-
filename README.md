# Tax Settlement AI Assistant

An advanced Natural Language Processing (NLP) pipeline designed to bridge the gap between human language and relational databases. This project enables users to query complex **Tax Settlement** and **Financial Reporting** data using natural English, which is then dynamically translated into executable SQL queries.

---

## 🚀 Key Features

* **Multi-Model Similarity Engine**: Combines **TF-IDF**, **Cosine Similarity**, and **Euclidean Distance** to map user intent to the most relevant SQL query templates.
* **Semantic Understanding**: Leverages **HuggingFace Transformers** (`BAAI/bge-m3`) and BERT-based models for high-dimensional sentence embeddings and intent recognition.
* **Dynamic Entity Extraction**: Integrated **Question-Answering (QA) Pipeline** that extracts specific parameters (Dates, Document Numbers like 'TS-00001', and VAT values) directly from prompts to populate SQL queries.
* **Intelligent Refinement Loop**: Built-in feedback mechanism allowing users to iteratively refine AI suggestions before execution.
* **Robust Preprocessing**: Comprehensive text normalization using **NLTK** and **SpaCy**, including POS tagging, stop-word removal, and regex-based tokenization.

---

## 🛠️ Technical Stack

| Category | Tools & Libraries |
| :--- | :--- |
| **NLP Frameworks** | SpaCy, NLTK, HuggingFace Transformers |
| **Machine Learning** | Scikit-learn (TfidfVectorizer, Cosine Similarity) |
| **Deep Learning** | PyTorch (Mean Pooling, Sentence Embeddings) |
| **Data Handling** | Pandas, NumPy, Regex |
| **Backend Integration** | Python Requests (Database API Connectivity) |

---

## 📖 How It Works

1.  **Preprocessing**: The system cleans user input and performs Part-of-Speech (POS) tagging to understand the grammatical structure.
2.  **Candidate Selection**: Using statistical methods (TF-IDF/Cosine Similarity), it identifies the top-ranking SQL templates from the knowledge base.
3.  **Parameter Injection**: A transformer-based QA model extracts values from the prompt and injects them into the SQL template (e.g., replacing `some_start_date` with `2024-01-01`).
4.  **Database Execution**: The finalized query is dispatched to a local API endpoint via `POST` requests to fetch real-time financial data.

---

## 💻 Sample Queries

* *"Show me tax settlement starting from date 2020-01-01 and till 2024-12-12"*
* *"What is the tax for the 3rd quarter?"*
* *"Show me the tax settlement description for TS-00001"*
* *"Show settlement where input vat is 0.01"*

---

## ⚙️ Installation & Usage

1. **Clone the repository**:
   ```bash
   git clone [https://github.com/your-username/tax-ai-assistant.git](https://github.com/your-username/tax-ai-assistant.git)
