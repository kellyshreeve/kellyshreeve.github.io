## Generative Answer Chat Bot

<p align="center">
  <img src="/images/qa-chatbot/chatbot-image.png?raw=true"
  width="400"
  height="260"
  alt="Image of a cartoon AI chatbot">
</p>

**Background**: An externship project with <a href="https://dataspeak.co/about" target="_blank">DataSpeak</a>, a data science consulting firm, to develop an AI customer service chatbot that could be used across multiple clients. This chatbot learns from a dataset and answer questions on domain-specific knowledge. 

**Purpose**: There were three goals for the chatbot:    
 1. Generate answers to user questions
 2. Pull information from a domain specific dataset  
 3. Produce accurate answers  

**Techniques**: RAG, Llama-2, LangChain, Chainlit

<a href='https://github.com/kellyshreeve/QA-Chatbot/blob/main/final_chainlit_app.py'
target='_blank'>View App Code</a>

### Examples  

#### Open-Ended Question Answering  

The model accurately responds to open-ended questions with information from the dataset in under 5min on GPU.

<p align="center">
  <img src="/images/qa-chatbot/open-ended-question.png?raw=true"
  width="600"
  height="300"
  alt="Chainlit App open ended question example">
</p>

#### Multiple-Choice Question Answering

The model correctly picks from a list of multiple choice questions, displaying accuracy when answering customer questions.

<p align="center">
  <img src="/images/qa-chatbot/multiple-choice-question.png?raw=true"
  width="600"
  height="270"
  alt="Chainlit App multiple choice question example">
</p>

### Data  

#### Data Acquisition  

Data for this project came from a public dataset of python questions and answers from Kaggle.  

Data Link: https://www.kaggle.com/datasets/stackoverflow/pythonquestions  

#### Data Preparation  

1. Datasets were cleaned of html text, special characters, and capital letters.  
2. Question and answer datasets were merged into one questions-answer dataframe on Id column.  
3. Answers from a sample of 100,000 question-answer pairs were used as a context document for model development.  

### Further Research and Development

This model should be tested on each domain-specific dataset to ensure it is able to learn accurate answers to common customer questions. Additionally response times can be sped up by running the app through GPU and vector storage in Pinecone. This app will can be deployed over a web service for use by customers.


<a href='https://github.com/kellyshreeve/QA-Chatbot'
target='_blank'>Full Project on Github</a>
