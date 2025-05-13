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
   - Defines a function `get_gemini_response(question)` to interact with Gemini's `gemini-2.0-flash` model and generate responses.

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

<details >
  <summary> <b> <h3> Q&A Chatbot Application with Streamlit and Google's Gemini (Chat Mode - 'chat.py') </h3> </b> </summary>
   

## Overview
The Python script 'chat.py'  creates a Q&A chatbot with chat history and streaming responses using:
- **Streamlit** for the web-based user interface.
- **Google's Generative AI (Gemini)** for generating responses to user questions.
- **dotenv** for managing environment variables.

## Key Features
1. **Environment Configuration**:
   - Loads the `GOOGLE_API_KEY` from a `.env` file.
   - Configures the `google.generativeai` library with the API key.

2. **Gemini Chat Initialization**:
   - Initializes a `GenerativeModel` object for Gemini (`gemini-2.0-flash`).
   - Starts a chat session with an empty history using `model.start_chat(history=[])`.

3. **Gemini Response Function**:
   - Defines a function `get_gemini_response(question)` to send a message to the chat session.
   - Streams the response back in chunks for real-time updates.

4. **Streamlit UI**:
   - Displays a text input field for user questions.
   - Includes a button to submit the question.
   - Streams the AI-generated response chunk by chunk.
   - Displays the chat history after the response.

## How It Works
1. User enters a question in the input field.
2. The "Ask the question" button triggers the `get_gemini_response` function.
3. The response from Gemini is streamed and displayed in real-time.
4. The chat history is displayed below the response.

## Code Structure
- **Imports**: Handles environment variables, text formatting, and UI rendering.
- **Functions**:
  - `get_gemini_response`: Sends a message to the chat session and streams the response.
- **Streamlit App**:
  - Initializes the app with a title and header.
  - Provides an input field and button for user interaction.
  - Streams the AI-generated response and displays the chat history.

## Example Workflow
1. Open the Streamlit app by running command in terminal.
```
streamlit run qachat.py
```
2. Enter a question in the input field.
3. Click "Ask the question."
4. View the AI-generated response streamed in real-time.
5. Review the chat history displayed below the response.

</details>