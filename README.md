SQL-Genie: Text-to-SQL using Mistral-7B
SQL-Genie is a Large Language Model (LLM)-based system that converts natural language queries into SQL statements over relational database schemas.
The project fine-tunes Mistral-7B using LoRA (PEFT) for efficient training in a resource-constrained environment.

 Features
🔹 Natural Language → SQL query generation
🔹 Fine-tuned Mistral-7B using LoRA (Parameter Efficient Fine-Tuning)
🔹 Schema-aware prompting for accurate query generation
🔹 Optimized for low VRAM (Kaggle GPU) using 4-bit quantization
🔹 Supports filtering, aggregation (COUNT, MAX, SUM), and conditions
Tech Stack
Python
PyTorch
HuggingFace Transformers
LoRA (PEFT)
BitsAndBytes (4-bit quantization)
