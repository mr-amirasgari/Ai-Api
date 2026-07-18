<div align="center">

# AI API Examples

A practical Jupyter Notebook collection for experimenting with text, image, audio, and multimodal AI APIs in Python.

![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Gradio](https://img.shields.io/badge/Gradio-Web%20Demos-FF7C00?style=for-the-badge)
![API Keys](https://img.shields.io/badge/API%20Keys-Environment%20Variables-2EA44F?style=for-the-badge)

</div>

---

## Overview

This repository contains independent educational examples for working with several AI APIs and Python libraries.

The notebook demonstrates:

- Streaming text generation
- Terminal-based chat
- Listing available models
- Text-to-speech
- Speech-to-text
- Image generation
- Multimodal image analysis
- Gradio web interfaces
- LangChain integrations
- Cohere examples
- OpenRouter examples

> The notebook sections are independent examples. They are not intended to be executed from top to bottom as one application.

## Repository Structure

```text
ai-api-examples/
├── .env.example
├── .gitignore
├── ai_api_examples.ipynb
├── README.md
└── requirements.txt
```

## Open in Google Colab

[Open the notebook in Google Colab](https://colab.research.google.com/github/mr-amirasgari/ai-api-examples/blob/main/ai_api_examples.ipynb)

## Installation

Clone the repository:

```bash
git clone https://github.com/mr-amirasgari/ai-api-examples.git
cd ai-api-examples
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.\.venv\Scripts\Activate.ps1
```

Activate it on macOS or Linux:

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
python -m pip install -r requirements.txt
```

Start Jupyter:

```bash
jupyter notebook
```

Then open:

```text
ai_api_examples.ipynb
```

## API Key Configuration

Copy the example environment file:

```powershell
Copy-Item .env.example .env
```

On macOS or Linux:

```bash
cp .env.example .env
```

Add only the keys required for the examples you plan to run:

```env
OPENAI_API_KEY=your_openai_api_key
AVALAI_API_KEY=your_avalai_api_key
OPENROUTER_API_KEY=your_openrouter_api_key
COHERE_API_KEY=your_cohere_api_key
```

The notebook loads these values using `python-dotenv`:

```python
import os
from dotenv import load_dotenv

load_dotenv()

api_key = os.getenv("OPENAI_API_KEY")
```

> Never commit the `.env` file or real API keys to GitHub.

## Examples Included

| Section | Main Library or Provider | Purpose |
|---|---|---|
| Streaming chat | OpenAI Python SDK | Display generated text incrementally |
| Terminal chatbot | OpenAI Python SDK | Maintain a simple conversation history |
| Model listing | Requests | Retrieve models from an API endpoint |
| Text-to-speech | OpenAI-compatible API | Generate an audio file from text |
| Speech-to-text | OpenAI-compatible API | Transcribe an audio file |
| Image generation | OpenAI-compatible API | Generate images from prompts |
| Image analysis | LangChain | Send text and Base64 images to a multimodal model |
| Image-analysis UI | Gradio and LangChain | Build a simple browser interface |
| Cohere chat | Cohere SDK | Generate text using Cohere |
| OpenRouter example | OpenAI Python SDK | Access an OpenAI-compatible third-party endpoint |
| TTS interface | Gradio | Generate and play speech in a browser |
| Chat interface | Gradio and LangChain | Build a simple web chatbot |

## Usage Notes

1. Run only the cells related to the example you want to test.
2. Confirm that the required API key is available in `.env`.
3. Confirm that the selected model is supported by your provider.
4. Some examples create local output files such as MP3 files.
5. API usage may involve provider charges or rate limits.

## Security

This repository follows these basic practices:

- API keys are read from environment variables.
- `.env` is excluded through `.gitignore`.
- Notebook outputs and execution counts are cleared before publication.
- Generated audio and local output folders are ignored.

## Important Limitations

- Model names and provider availability can change.
- OpenAI-compatible providers may not support every OpenAI feature.
- Some notebook examples require local images or audio files.
- Error handling is intentionally minimal because the repository is educational.
- Review provider documentation, pricing, and data policies before production use.

## Possible Improvements

- Split each example into a separate notebook
- Add automated notebook validation
- Add structured error handling
- Add provider-specific configuration helpers
- Add reusable utility functions
- Add examples for asynchronous requests
- Add tests with mocked API responses

## Author

**Amir Mohammad Asgari**

[GitHub Profile](https://github.com/mr-amirasgari)  
[Official Website](https://www.am-asgari.ir/)