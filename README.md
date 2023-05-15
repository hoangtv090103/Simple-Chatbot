# Simple-Chatbot
# Chatbot Project Documentation

## Introduction
This is a simple chatbot project written in Python. The chatbot interacts with users by answering questions based on a knowledge base stored in a JSON file.

## Prerequisites
- Python 3.x
- JSON module
- difflib module

## Project Structure
The project consists of the following files:
- `knowledge_base.json`: JSON file containing the knowledge base of questions and answers.
- `chatbot.py`: Python script implementing the chatbot functionality.

## Functionality
The chatbot performs the following actions:

1. Load Knowledge Base:
   - Reads the knowledge base from the `knowledge_base.json` file using the `load_knowledge_base()` function.
   - Returns the loaded knowledge base as a dictionary.

2. Save Knowledge Base:
   - Saves the modified knowledge base to the `knowledge_base.json` file using the `save_knowledge_base()` function.

3. Find Best Match:
   - Compares the user's question with a list of existing questions using the `get_close_matches()` function from the `difflib` module.
   - Returns the best match if the similarity ratio is above a certain threshold.

4. Get Answer for Question:
   - Searches for the given question in the knowledge base dictionary.
   - Returns the corresponding answer if found.

5. Chat Bot:
   - Loads the knowledge base using `load_knowledge_base()`.
   - Repeatedly prompts the user for input.
   - If the user enters "quit", the chatbot terminates.
   - Uses `find_best_match()` to find the best matching question in the knowledge base.
   - If a match is found, retrieves the answer using `get_answer_for_question()` and displays it.
   - If no match is found, prompts the user to provide an answer and updates the knowledge base accordingly using `save_knowledge_base()`.

## Usage
1. Make sure you have Python installed.
2. Place the `knowledge_base.json` file in the same directory as `chatbot.py`.
3. Run the `chatbot.py` script using the command `python chatbot.py`.
4. Enter your queries or questions when prompted by the chatbot.
5. To quit the chatbot, type "quit".

## Conclusion
This chatbot project demonstrates a basic implementation of a question-answering system using a knowledge base stored in a JSON file. You can extend and modify the project to suit your specific requirements.
