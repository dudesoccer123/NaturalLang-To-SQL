# Natural Language to SQL Converter using LangChain

## Overview
This project is a **LangChain-powered framework** that translates **natural language queries** into **SQL statements** using **Meta-Llama-3-8B-Instruct** from Hugging Face. It enables users to interact with databases in plain English, eliminating the need to write complex SQL queries manually.

## Features
- **Natural Language to SQL Translation** – Convert user queries into executable SQL statements.
- **Hugging Face LLM Integration** – Uses `Meta-Llama-3-8B-Instruct` for text-to-SQL generation.
- **Custom Prompt Engineering** – Dynamically structured prompts for better SQL generation.
- **MySQL Schema Awareness** – Generates SQL based on the provided database schema.
- **Modular Design** – Can be extended with different LLMs or database systems.

## Installation
Ensure you have Python installed, then install dependencies:
```bash
pip install langchain langchain-community transformers
```
## Setup
- Obtain API Key – Get your Hugging Face Hub API key and store it in tok2.txt.
- Define Your Database Schema – Provide a schema representation for accurate query generation.
- Run the Notebook – Execute NLtoSQL.ipynb to test the framework.

## Prompting Techniques Tested

- Zero-shot Prompting – Directly asking the model to generate SQL without examples.

- Few-shot Prompting – Providing multiple examples of natural language queries and their corresponding SQL outputs to guide the model.

- Chain Of Thought – HElps the model provide reasoning based on the responses generated.

- Self Consistency Prompting – A prompt engineering technique where a large language model (LLM) generates multiple outputs for a single query, and the most consistent answer is selected, improving accuracy and reliability. 

## Usage
The framework takes three inputs:

- Natural Language Query: e.g., "Get all employees who joined after 2020."

- Database Schema: A representation of your MySQL database.

- Prompting Technique: Different methods to refine SQL generation.
