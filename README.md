# PDF AI Assistant
This codebase is built for the purpose of interacting with PDF documents and get instant answers.
First, upload PDF documents. We are using Langchain library to read PDF document and to extract and split contents from document.
We are using Cohere embeddings to create word embeddings from extract contents and upload those embeddings in Qdrant Vector DB.
We built the frontend chat interface using Gradio app.

This project is hosted on HuggingFace Spaces: [Live Demo of PDF AI Assistant](https://huggingface.co/spaces/heliosbrahma/ai-pdf-assistant).

## Steps:-
- Load PDF document using Langchain's PyMuPDFLoader and then split it into chunks of text using RecursiveCharacterTextSplitter
- Upload chunks of text into Qdrant Vector DB
- Retrieve top 3 similar chunks for each query using RetrievalQA and using custom prompt by PromptTemplate, answer those queries

## How to run it locally:-
If you want to run this app locally, first clone this repo using `git clone`.<br><br>
Now, install all libraries by running the following command in terminal:<br>
```python
pip install -r requirements.txt
```
<br><br>
Now, run the app from terminal:<br>
```python
gradio app.py
```
