Project Description

This project implements a simple web-based chatbot interface powered by Google's Gemini AI model.  It allows users to send text messages to the AI and receive responses in a chat-like format. The application is built using Flask (a Python web framework) for the backend, and HTML, CSS, and JavaScript for the frontend.  Notably, the application is designed to handle Markdown formatting in the AI's responses.

Key Components and Functionality

app.py (Flask Backend):
Sets up a Flask web application.
Integrates with the Gemini API to communicate with the AI model.
Defines two routes:
/: Serves the main HTML page (index.html) which provides the user interface.
/chat: Handles user messages sent from the frontend. It sends the message to the Gemini model, receives the AI's response, and sends the response back to the frontend as JSON.
Manages chat history to provide context to the AI.
Includes error handling to gracefully manage potential issues with the AI's responses.
index.html (Frontend Structure):
Creates the basic layout of the chatbot interface.
Includes a chat display area (#chat-box), a user input area (#user-input), and a send button.
Links to the CSS (styles.css) for styling and the JavaScript (script.js) for interactivity.
Imports the marked.js library from a CDN to render Markdown.
script.js (Frontend Logic):
Handles sending user messages to the Flask backend using fetch().
Dynamically updates the chat display area (#chat-box) with both user and AI messages.
Formats the messages within the chat interface.
Uses marked.js to convert the Markdown received from the AI into HTML for display.
Provides basic UI enhancements, such as automatically adjusting the textarea's height as the user types.
Includes error handling for network requests.
styles.css (Frontend Styling):
Defines the visual appearance of the chatbot interface.
Uses a dark color scheme, similar to the ChatGPT interface.
Styles the chat messages, input elements, buttons, and other components.
Implements responsive design elements to ensure proper display on different screen sizes.
Overall Functionality Flow

The user opens the web page (index.html).
The user types a message in the input area and clicks the "Send" button.
JavaScript (script.js) captures the message and sends it to the Flask backend (/chat route) as a JSON object.
The Flask backend (app.py) receives the message, sends it to the Gemini AI model, and gets the AI's response.
The Flask backend sends the AI's response back to the frontend as a JSON object.
JavaScript (script.js) receives the response, converts any Markdown formatting to HTML, and displays the complete message in the chat area.
Key Technologies Used

Flask (Python web framework)
Google Gemini API
HTML
CSS
JavaScript
marked.js (for Markdown rendering)
This project provides a functional foundation for building a more sophisticated chatbot application. It demonstrates the integration of a large language model with a web interface, handling user input, displaying AI responses, and basic styling.
