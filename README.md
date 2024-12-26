# Chatbot-Restaurant-Domain

## Introduction
This project focuses on the development of a restaurant-themed chatbot designed to revolutionize the dining experience. Using **Natural Language Processing (NLP)** and **machine learning**, the chatbot automates essential customer interactions such as table reservations, menu recommendations, issue reporting, and order placement. 
This project demonstrates the integration of **AI and machine learning** into the hospitality industry, offering significant improvements in customer satisfaction and operational efficiency.

---

## Features
The chatbot includes the following functionalities:
- **Table Reservations**: Allows users to book tables by specifying date, time, and party size.
- **Food Recommendations**: Offers personalized suggestions based on dietary preferences (e.g., vegan, vegetarian, non-vegetarian).
- **Order Placement**: Enables seamless order processing, including dine-in and takeout options.
- **Feedback System**: Captures customer feedback to improve restaurant operations.
- **Error Handling**: Corrects minor user-input errors and handles invalid queries gracefully.

---

## Project Structure
```plaintext
Chatbot-Restaurant-Domain
├── README.md                 # Project documentation
├── data/
│   ├── intents.json          # Intents dataset for chatbot
│   ├── food_recc_intents.json # Dataset for food recommendations
├── models/
│   ├── intents_model.pkl     # Trained chatbot model
│   ├── classes.pkl           # Pickle file containing intent classes
│   ├── words.pkl             # Pickle file containing tokenized words
├── notebooks/
│   ├── CA1_Chatbot_Development.ipynb  # Jupyter Notebook for chatbot development
├── src/
│   ├── chatbot.py            # Main chatbot implementation
│   ├── training_script.py    # Script for training the chatbot
├── docs/
│   ├── flowchart.png         # Flowchart of chatbot logic
│   ├── methodology.pdf       # PDF detailing methodology and approach
├── .gitignore                # Files to be ignored by Git
└── LICENSE                   # License information
```

---

## Technologies Used
- **Programming Language**: Python
- **Libraries**:
  - **spaCy**: For Natural Language Processing tasks, including tokenization, lemmatization, and intent recognition.
  - **Keras**: For building and training the chatbot’s machine learning model.
  - **NumPy**: For data manipulation and preparation.
  - **Pickle**: For model serialization and storage.
- **Development Environment**:
  - **Jupyter Notebook**: For model experimentation and development.
  - **Visual Studio Code**: For code implementation and debugging.
- **Version Control**: Git and GitHub for repository management and collaboration.

---

## Implementation Overview

### 1. Dataset Preparation
The chatbot uses an `intents.json` dataset structured into "intents" and "patterns," allowing the model to associate user queries with the appropriate responses. Synonyms and paraphrased queries were included to improve the bot’s ability to process unstructured inputs.

### 2. Model Training
A **Sequential Neural Network** was implemented using Keras to classify intents based on user inputs. The following steps were performed:
- Tokenization and lemmatization using spaCy.
- Bag-of-Words vectorization for feature extraction.
- Training and evaluation with test accuracy exceeding **94%**.

### 3. Natural Language Processing (NLP)
The bot utilizes the following NLP techniques:
- **Intent Recognition**: Classifies user intent based on cosine similarity of tokenized phrases.
- **POS Tagging**: Extracts numerical values and dependencies for contextual understanding.
- **Error Handling**: Recognizes and corrects minor user-input mistakes.

### 4. Logic Flow
The chatbot logic is implemented as a decision tree, guiding users through actions such as:
- **Greeting**
- **Table reservation**
- **Menu recommendations**
- **Ordering food**
- **Providing feedback**

### 5. User Interaction
The chatbot delivers a smooth user experience by:
- Supporting free-form input for better interaction.
- Allowing navigation with commands like **"back"** or **"reset"**.
- Handling invalid inputs with error messages.

## Chatbot Logic Flowchart

Below is the logic flowchart for the restaurant-themed chatbot:

![Chatbot Logic Flowchart](Docs/chatbot_flowchart.png)






