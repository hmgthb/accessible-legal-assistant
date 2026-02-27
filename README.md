# 301-Proj

DS-UA 301 Intro to Deep Learning and LLMs Project

## Setting Up Python Environment

To ensure that all modules and local imports work correctly in VSCode, follow the steps below to create a clean virtual environment and configure VSCode to use it.

### 1. Create Python Virtual Environment

From the project root:

```bash
python3 -m venv .venv
```

Activate the environment:

```bash
source .venv/bin/activate
```

### 2. Set VSCode to Use .venv Interpreter

In VSCode:

1. Look at the bottom-right corner of the window.
2. Click the currently selected Python interpreter (e.g., Python 3.12.7 (homebrew)).
3. Choose the interpreter:

```bash
.venv (3.12.1)
```

This ensures that VSCode’s Pylance engine and your terminal are using the same environment, preventing import resolution errors.

### 3. Install Dependencies Using requirements.txt

Once your virtual environment is activated, install all required dependencies with:

```bash
pip install -r requirements.txt
```

This will ensure the project has all necessary packages for LangChain, embeddings, vector databases, environment management, and utility tools.

## Setting Up .env

To run the legal assistant, you must create a .env file that stores your API keys and environment variables. Before running the project, create your `.env` file.

### 1. Duplicate the provided .env.example file:

```
cp .env.example .env
```

### 2. Open the new .env file and fill in your API key:

```
OPENAI_API_KEY=your_api_key_here
```

### 3. The application will automatically load these variables at runtime.

Never commit your real `.env` file.

## How to Run The Model

Build vector index from CUAD dataset

```bash
python src/main.py build
```

Run interactive agent

```bash
python src/main.py run
```

Run evaluation

```bash
python src/main.py eval
```
