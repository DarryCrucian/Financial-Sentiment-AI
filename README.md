# Financial Sentiment AI


Financial Analyst AI is a project that applies artificial intelligence to analyze earnings calls and other financial documents. It leverages various NLP (Natural Language Processing) models to perform tasks such as speech recognition, text summarization, sentiment analysis, company and location extraction, and identifying forward-looking statements.

# Features
The key features of Financial Analyst AI are:

Speech Recognition: Users can record speech using a microphone and the system will transcribe it into text for further analysis.

Text Summarization: Users can input a text document and the system will generate a summary of the text using a summarization model.

Sentiment Analysis: Users can analyze the sentiment of the summarized text using a pre-trained sentiment analysis model that is specifically designed for financial texts.

Company and Location Extraction: Users can identify companies and locations mentioned in the text using a pre-trained named entity recognition (NER) model.

Financial Tone and Forward Looking Statement Analysis: Users can analyze the financial tone of sentences in the text using a pre-trained sentiment analysis model, and also identify forward-looking statements.

# Installation

Note: Please make sure to set the auth_token variable with your Hugging Face API token in order to use the models from Hugging Face Hub.
To use Financial Analyst AI, follow these steps:

1. Install the required Python libraries using the following commands:
```
!pip install transformers
!pip install gradio
!pip install spacy 
```

2. Load the necessary models and dependencies using the provided code:
```
import os
os.system("pip install gradio==3.0.18")
from transformers import pipeline, AutoTokenizer, AutoModelForSequenceClassification, AutoModelForTokenClassification
import gradio as gr
import spacy
nlp = spacy.load('en_core_web_sm')
nlp.add_pipe('sentencizer')
```
3. Define the functions for various tasks, such as speech recognition, text summarization, sentiment analysis, company and location extraction, and forward-looking statement analysis using the provided code.

4. Create a Gradio interface to interact with the functions using the provided code:
```
demo = gr.Blocks()

with demo:
    # Define the UI components such as buttons, textboxes, and highlighted text for displaying results
    # Associate the functions with the buttons using the `click` method
    ...
    
demo.launch()
```

5. Launch the Gradio interface using the launch method to start using Financial Analyst AI.

# Usage
Once the Gradio interface is launched, users can perform the following actions:

*Click the "Recognize Speech" button to record speech using a microphone and transcribe it into text.

*Click the "Summarize Text" button to generate a summary of the input text.

*Click the "Classify Financial Tone" button to analyze the sentiment of the summarized text.

*Click the "Financial Tone and Forward Looking Statement Analysis" button to analyze the financial tone and identify forward-looking statements in the input text.

*Click the "Identify Companies & Locations" button to extract companies and locations mentioned in the input text.

The results of these tasks will be displayed in the respective UI components, such as textboxes and highlighted text.

# Credits
The Financial Analyst AI project uses several pre-trained models from the Hugging Face Transformers library and other open-source libraries. The project was developed by Aryaman and Tejeshwar.

# License

The Financial Analyst AI project is licensed under MIT.
