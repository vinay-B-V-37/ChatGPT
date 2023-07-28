# Chatbot Application using OpenAI LLM (Language Model)

This is a simple chatbot application that uses the OpenAI GPT-3.5 Turbo language model to provide responses to user input. The application is built using HTML, CSS, and Python (Flask framework) to create a user-friendly chat interface.

## Prerequisites

To run this chatbot application locally, you need to have the following installed on your system:

- Python (3.6 or later)
- Flask (Web framework)
- OpenAI Python library
- An API key from OpenAI

## Getting Started

1. Clone the repository to your local machine.

2. Install the required Python packages. You can use pip to install them:

   ```
   pip install Flask openai
   ```

3. Set up your OpenAI API key:

   - In the `app.py` file, replace `'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'` with your own API key from OpenAI. You can sign up for an API key on the OpenAI website.

4. Start the Flask server:

   ```
   python app.py
   ```

5. Open your web browser and navigate to `http://localhost:5000` to access the chatbot.

## How It Works

The chatbot application uses a web interface (HTML and CSS) to display the conversation between the user and the chatbot. The chat history is presented in a chat box, and the user can type messages in the input area.

When the user sends a message (by clicking the "Send" button or pressing Enter), the application makes a POST request to the `/api` endpoint of the Flask server. The user's message is sent as a JSON payload to the server.

In the `api()` function (defined in `app.py`), the server processes the user's message and sends it to the OpenAI GPT-3.5 Turbo model using the `openai.ChatCompletion.create()` method. The model generates a response, which is then returned to the server.

The server sends the response back to the web interface, and the chat history is updated with the chatbot's reply. If the model fails to generate a response, the chatbot displays "Failed to Generate Response!"



## Note

- Remember to use the OpenAI API responsibly and be aware of any usage limitations imposed by OpenAI.
- The provided API key is a placeholder and will not work. Make sure to replace it with your own valid API key.
