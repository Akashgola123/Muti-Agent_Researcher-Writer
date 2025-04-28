# Muti-Agent_Researcher-Writer
# Multi-Agent Researcher-Writer

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

A project leveraging a multi-agent framework (likely CrewAI) to perform research and writing tasks using local Large Language Models (LLMs) via Ollama.

*(Note: Repository name might be intended as "Multi-Agent...")*

## Overview

This project likely sets up a team of autonomous AI agents using the CrewAI framework. Typical agent roles in such a system might include:

1.  **Researcher Agent:** Gathers information from specified sources (web search, documents, etc.).
2.  **Writer Agent:** Compiles the researched information into a structured output (report, article, summary, etc.).
3.  **(Optional) Manager Agent:** Oversees the process, validates information, or directs the workflow.

The system uses locally run LLMs provided through Ollama, allowing for privacy and offline capabilities.

## Features (Inferred)

*   Orchestrates multiple AI agents for complex tasks.
*   Uses the CrewAI framework for agent and task definition.
*   Integrates with local Large Language Models via Ollama.
*   Automates aspects of research and content generation.

## Prerequisites

Before you begin, ensure you have the following installed:

1.  **Python:** Version 3.10 or higher is recommended.
2.  **Pip:** Python package installer.
3.  **Git:** For cloning the repository.
4.  **Ollama:** For running the required local Large Language Models.

### Ollama Setup

Ollama allows you to easily run powerful LLMs locally on your machine (CPU or GPU).

1.  **Download and Install Ollama:** Visit the [Ollama website](https://ollama.ai/) and download the appropriate version for your operating system (macOS, Linux, Windows). Follow their installation instructions.
2.  **Verify Installation:** Open your terminal or command prompt and run:
    ```bash
    ollama --version
    ```
3.  **Pull a Model:** You need to download an LLM for CrewAI agents to use. CrewAI often works well with models like Mistral, Llama 3, or Mixtral. Pull a model using the command line:
    ```bash
    # Example: Pulling the Mistral 7B instruct model
    ollama pull mistral

    # Example: Pulling a Llama 3.2 Instruct model (smaller, good for testing)
    ollama pull llama3.2:instruct

    # Example: Pulling Llama 3 8B Instruct model (more capable)
    # ollama pull llama3:instruct
    ```
    Make sure the Ollama application/service is running in the background when you execute the Python script.

## Installation & Setup

Follow these steps to set up the project environment:

1.  **Clone the Repository:**
    ```bash
    git clone <your-repo-url> # Replace <your-repo-url> with the actual URL
    cd Muti-Agent_Researcher-Writer
    ```

2.  **Create a Virtual Environment (Recommended):**
    ```bash
    python -m venv venv
    # Activate the environment
    # On macOS/Linux:
    source venv/bin/activate
    # On Windows:
    # .\venv\Scripts\activate
    ```

3.  **Install Requirements:** Install the necessary Python packages listed in `requirement.txt` (note: the filename in the repo image seems corrupted/truncated, assuming it's `requirements.txt`).
    ```bash
    pip install -r requirements.txt
    ```
    *(If the file is indeed named `=0.3.52,`, you'll need to rename it to `requirements.txt` first or install dependencies manually by looking inside it).*

## Configuration

1.  **Ollama Model:** Ensure the LLM you pulled via Ollama (e.g., `mistral`, `llama3:instruct`, `llama3.2:instruct`) is specified correctly within the `main.py` script where the CrewAI agents' LLM is configured. Open `main.py` and look for the section initializing the Ollama LLM for CrewAI agents.
2.  **Environment Variables (Optional):** Check `main.py` to see if any specific environment variables are required (e.g., for API keys if using external tools, specific Ollama URLs if not default, etc.). Create a `.env` file if needed and add them there.

## Running the Application

1.  **Ensure Ollama is Running:** Make sure the Ollama service/application is running in the background.
2.  **Activate Virtual Environment:** If you created one, activate it (`source venv/bin/activate` or `venv\Scripts\activate`).
3.  **Execute the Script:** Run the main Python script from the project's root directory:
    ```bash
    python main.py
    ```
4.  **Check Output:** Observe the terminal output for logs from CrewAI agents about their tasks and progress. The final output will depend on the specific tasks defined in `main.py`.

## About the Key Technologies

### CrewAI
CrewAI is a cutting-edge framework for orchestrating role-playing, autonomous AI agents. It helps developers create sophisticated multi-agent interactions to tackle complex tasks collaboratively. Visit the [CrewAI GitHub](https://github.com/joaomdmoura/crewAI) for more information.

### Ollama
Ollama is a powerful tool that makes it easy to download and run large language models locally. It provides a simple interface and API for interacting with various open-source models, enabling AI development with enhanced privacy and offline capabilities. Visit the [Ollama Website](https://ollama.ai/) to learn more.

## License

This project is licensed under the Apache-2.0 License. See the [LICENSE](LICENSE) file for details.
