# 🌟 Meditrain AI

Meditrain AI is a chatbot system designed to simulate patient interactions, allowing newly graduated doctors to practice and improve their communication skills with patients. By acting as a virtual patient, Meditrain AI provides a realistic and diverse range of scenarios to help doctors build confidence and empathy in a controlled environment.

## 🤖 Working Link
You can check out the live version of the project here: [Visit the live demo](https://meditrain-ai-1-zl6y.onrender.com)

## 🌟Features

- Simulates a realistic patient experience by dynamically varying medical complaints.
- Responds in conversational language suitable for basic medical knowledge.
- Encourages engagement and provides feedback based on the doctor's behavior.
- Offers subtle cues to guide doctors in patient interactions.
- API endpoints to fetch responses and test functionality.

## 📂Project Files

- **`app.py`**: Main Flask application that sets up routes and handles chatbot interactions.
- **`api.py`**: Provides API endpoints for generating chatbot responses and fetching test user data.
- **`memory.py`**: Manages conversation memory using LangChain's ConversationBufferWindowMemory.
- **`requirements.txt`**: Lists the dependencies required for the project.
  
## 🌟UI Overview

![Screenshot (1)](https://github.com/user-attachments/assets/9affb71e-db82-48d0-b28e-41178ca5b0e1)

## Prerequisites

1. Python 3.8+
2. A Groq API key (add it to a `.env` file).
3. Flask, Flask-CORS, and other dependencies listed in `requirements.txt`.

## 📌Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/meditrain-ai.git
   cd meditrain-ai
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up the `.env` file:
   ```plaintext
   <your_groq_api_key>
   ```

4. Run the Flask application:
   ```bash
   python app.py
   ```

5. Access the API at `http://127.0.0.1:5000`.

## API Endpoints

- **`POST /response`**:
  - Description: Get a chatbot response based on user input.
  - Request Body: `{ "query": "Your question here" }`
  - Response: `{ "response": "Chatbot's response" }`

- **`GET /test_users`**:
  - Description: Fetch random test users.
  - Response: List of random user data from the RandomUser.me API.

## Usage

1. Interact with the chatbot by sending POST requests to the `/response` endpoint.
2. Fetch sample test users using the `/test_users` endpoint.
3. Use the chatbot to simulate conversations as a patient for medical training purposes.

## Example Interaction

### Request
```json
{
  "query": "I have been feeling short of breath when climbing stairs. What could it be?"
}
```

### Response
```json
{
  "response": "Can you tell me how long you have been experiencing this and if anything seems to make it better or worse?"
}
```

## Technology Stack

- **Backend**: Flask, LangChain, Groq
- **APIs**: Groq, RandomUser.me

## Future Enhancements

- Expand the range of medical scenarios.
- Add multi-language support for broader accessibility.
- Integrate a dashboard to analyze doctor-patient interaction patterns.

## 😊Acknowledgments

- **Infosys Springboard**: For the opportunity to develop this project as part of the internship.
- **LangChain** and **Groq**: For their APIs and libraries enabling dynamic conversational AI.
