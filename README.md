# Text Summarizer

A web-based text summarization application built using **FastAPI** and **Hugging Face Transformers**. The application uses a fine-tuned **T5 model** to generate concise summaries from user-provided text through a simple web interface.

## Features

* Text summarization using a fine-tuned T5 model
* FastAPI backend for handling summarization requests
* Hugging Face Transformers integration
* Simple and responsive web interface
* Automatic text preprocessing
* CPU, CUDA, and Apple MPS device support

## Technologies Used

* **Python**
* **FastAPI**
* **Hugging Face Transformers**
* **PyTorch**
* **T5 (Text-to-Text Transfer Transformer)**
* **HTML**
* **CSS**
* **JavaScript**

## Project Structure

```text
text_summarizer/
│
├── app.py
├── index.html
├── README.md
│
└── saved_summary_model/
    ├── config.json
    ├── generation_config.json
    ├── model.safetensors
    ├── tokenizer.json
    └── tokenizer_config.json
```

## Installation

Clone the repository:

```bash
git clone https://github.com/Sourjya-Mitra/text_summarizer.git
cd text_summarizer
```

Install the required dependencies:

```bash
pip install fastapi uvicorn torch transformers sentencepiece
```

## Running the Application

Start the FastAPI server:

```bash
uvicorn app:app --reload
```

The application will be available at:

```text
http://127.0.0.1:8000
```

Open the URL in your browser and enter the text you want to summarize.

## How It Works

```text
User Input
    ↓
Web Interface
    ↓
FastAPI API
    ↓
Text Preprocessing
    ↓
Fine-Tuned T5 Model
    ↓
Generated Summary
    ↓
Web Interface
```

The application cleans the input text, tokenizes it using the T5 tokenizer, passes it to the trained model, and decodes the generated output into a readable summary.

## API Endpoint

### POST `/summarize/`

Request:

```json
{
    "dialogue": "Enter the text you want to summarize here."
}
```

Response:

```json
{
    "summary": "Generated summary of the input text."
}
```

## Model

The application uses a fine-tuned **T5** model for text summarization. The trained model and tokenizer are stored in the `saved_summary_model` directory.

## Future Improvements

* Add support for multiple summarization models
* Improve the user interface
* Add summary length controls
* Add support for document and PDF summarization
* Deploy the application online
* Add authentication and user history

## Author

**Sourjya Mitra**

Production Engineering Student
Jadavpur University

## License

This project is intended for educational and learning purposes.
