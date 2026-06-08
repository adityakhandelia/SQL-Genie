
 Features<img width="1917" height="899" alt="image" src="https://github.com/user-attachments/assets/51b55312-c9d3-4977-bb0c-242e79a7c38c" />

# SQL Genie 🚀

## Text-to-SQL Generation using Qwen2.5, Mistral-7B and LoRA

SQL Genie is a Generative AI project that converts natural language questions into SQL queries. The project explores parameter-efficient fine-tuning of Large Language Models (Mistral-7B and Qwen2.5) for Text-to-SQL generation using schema-aware prompting.

---

## Overview

The goal of SQL Genie is to enable users to interact with relational databases using plain English instead of manually writing SQL queries. Given a database schema and a user question, the model generates the corresponding SQL statement.

### Example

**Input Question**

```text
List names of students who scored more than 90 in Math
```

**Generated SQL**

```sql
SELECT s.name
FROM students s
JOIN marks m ON s.id = m.student_id
WHERE m.score > 90
AND m.subject = 'Math';
```

---

## Dataset

The model was trained using the **Spider Text-to-SQL Dataset**, a widely used benchmark for evaluating Text-to-SQL systems.

Each training sample contains:

* Database schema information
* Natural language question
* Ground truth SQL query

Schema information is incorporated into the prompt to enable schema-aware SQL generation.

---

## Models Explored

### Mistral-7B

* Initial Text-to-SQL fine-tuning experiments
* LoRA-based parameter-efficient training
* 4-bit quantization for efficient resource utilization

### Qwen2.5-1.5B-Instruct

* Instruction-tuned Large Language Model
* Chat-template based fine-tuning
* Faster training and inference compared to larger models
* Optimized for deployment and experimentation

---

## Fine-Tuning Approach

The project uses:

* LoRA (Low-Rank Adaptation)
* PEFT (Parameter-Efficient Fine-Tuning)
* 4-bit Quantization (BitsAndBytes)
* Hugging Face Transformers

This approach significantly reduces memory requirements while maintaining strong Text-to-SQL generation performance.

---

## User Interface

A lightweight Gradio interface allows users to:

* Enter database schema information
* Ask natural language questions
* Generate SQL queries in real time

### Demo


---

## Tech Stack

* Python
* PyTorch
* Hugging Face Transformers
* PEFT (LoRA)
* Qwen2.5
* Mistral-7B
* BitsAndBytes
* Gradio
* SQL

---

## Key Learnings

* Large Language Model Fine-Tuning
* Prompt Engineering
* LoRA and PEFT
* Quantization Techniques
* Natural Language Processing
* Text-to-SQL Systems
* LLM Inference and Deployment Workflows
