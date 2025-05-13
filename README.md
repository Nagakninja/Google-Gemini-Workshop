# Google-Gemini-Project

<details open>
  <summary> <b> <h3>Q&A Chatbot Application with Streamlit and Google's Gemini (app.py) </b></h3></summary>
  

## Overview
The Python app.py script creates a simple Q&A chatbot using:
- **Streamlit** for the web-based user interface.
- **Google's Generative AI (Gemini)** for generating responses to user questions.
- **dotenv** for managing environment variables.

## Key Features
1. **Environment Configuration**:
   - Loads the `GOOGLE_API_KEY` from a `.env` file.
   - Configures the `google.generativeai` library with the API key.

2. **Gemini Response Function**:
   - Defines a function `get_gemini_response(question)` to interact with Gemini's `gemini-pro` model and generate responses.

3. **Streamlit UI**:
   - Displays a text input field for user questions.
   - Includes a button to submit the question.
   - Displays the AI-generated response when the button is clicked.

## How It Works

1. Run the pip install with requirements.txt in terminal using command 
```
pip install -r requirements.txt
```
2. Run the app with streamlit in terminal using command 
```
streamlit run app.py
```
3. User enters a question in the input field.
4. The "Ask the question" button triggers the `get_gemini_response` function.
5. The response from Gemini is displayed on the Streamlit app.

</details>