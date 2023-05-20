# PDF AI Assistant
This codebase is built for the purpose of interacting with PDF documents through a chat interface and get instant answers for your queries.<br>
This project is built using Langchain for question answer retrieval, Qdrant Vector DB to store embeddings and Gradio for frontend demo.<br>

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
