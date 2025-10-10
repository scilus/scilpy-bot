# Scilpy-Bot

A chatbot to help you navigate the Scilpy library. This tool is designed to answer your questions about Scilpy, a Python library for diffusion MRI and tractography processing.

## Installation

To install the Scilpy-Bot for development, clone the repository and install the necessary requirements:

```bash
git clone https://github.com/scilus/scilpy-bot.git
cd scilpy-bot
pip install -r requirements.txt
pip install -e .
```

## API Key Setup

This chatbot can be configured to use either Google's Gemini or OpenAI's ChatGPT models. Please select one and follow the instructions below.

1.  **Get an API Key:**
    *   **Google Gemini:** Obtain your API key from [Google AI Studio](https://aistudio.google.com/app/apikey).
    *   **OpenAI ChatGPT:** Get your API key from the [OpenAI Platform](https://platform.openai.com/api-keys).

2.  **Set Environment Variable:**
    You need to add your API key to your shell's configuration file (e.g., `.bashrc` or `.zshrc`).

    *   For **Gemini**, add the following line:
        ```bash
        export GOOGLE_API_KEY="your_google_api_key"
        ```
    *   For **ChatGPT**, add the following line:
        ```bash
        export OPENAI_API_KEY="your_openai_api_key"
        ```

3.  **Apply Changes:**
    To apply the changes, either restart your terminal or run:
    ```bash
    source ~/.bashrc
    ```
    *(Replace `~/.bashrc` with `~/.zshrc` if you are using Zsh.)*

## Dependencies

The chatbot relies on the following libraries:

*   [scilpy](https://github.com/scilus/scilpy)
*   [openai](https://pypi.org/project/openai/)
*   [google-generativeai](https://pypi.org/project/google-generativeai/)

For information on how to generate the Scilpy documentation, please refer to the [official documentation](https://scilpy.readthedocs.io/en/latest/).

## Usage

Once installed, you can start the chatbot by running:

```bash
scil_chatbot
```

**Note:** Before the first run, you may need to generate the Scilpy documentation cache. If you see a `FileNotFoundError`, please run the following command:
```bash
scil_search_keywords --regenerate_help_files placeholder
```

## Tips for Interacting with the Chatbot

To get the most out of the Scilpy-Bot, here are a few tips:

*   **Be specific:** Instead of asking "How do I use scilpy?", ask "How can I use scilpy to perform tractography on a DWI dataset?".
*   **Provide context:** If you are encountering an error, provide the full error message and the code snippet that is causing the error.
*   **Ask for examples:** If you are unsure how to use a specific function, ask for a code example.
*   **Keep it simple:** Ask one question at a time. This will help the chatbot to provide a more focused and accurate response.