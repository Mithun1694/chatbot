# 🤖 Agriculture Chatbot 🌱

A multilingual Streamlit-based chatbot designed to provide agricultural guidance and support. The chatbot leverages Google's Gemini AI model to deliver intelligent responses and supports multiple Indian languages.

## ✨ Features

- **Multilingual Support**: English, Kannada, Hindi, Telugu, and Tamil
- **Phone-based Authentication**: OTP verification system for user authentication
- **AI-Powered Responses**: Uses Google Gemini 2.0 Flash model for intelligent agriculture-related queries
- **Text-to-Speech**: Automatic voice output in the user's selected language using gTTS
- **Chat History**: Persistent chat storage per user with multilingual content preservation
- **Responsive UI**: Beautiful green-themed agricultural interface with custom CSS styling
- **Language Flexibility**: Switch between languages and view chat history in different languages

## 🛠️ Tech Stack

- **Frontend**: Streamlit
- **AI Model**: Google Gemini 2.0 Flash (via LangChain)
- **Text-to-Speech**: gTTS (Google Text-to-Speech)
- **Language Processing**: LangChain Google GenAI
- **Speech Recognition**: SpeechRecognition library

## 📋 Requirements

Install all dependencies using:

```bash
pip install -r requirements.txt
```

### Dependencies:
- streamlit
- gtts
- langchain-google-genai
- speechrecognition
- pydub
- streamlit-webrtc
- soundfile
- numpy

## 🚀 Setup & Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Mithun1694/chatbot.git
   cd chatbot
   ```

2. **Create a virtual environment** (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up Google API Key**:
   - Go to [Google AI Studio](https://aistudio.google.com/app/apikey)
   - Create an API key
   - Create a `.streamlit/secrets.toml` file in your project root:
   ```toml
   GOOGLE_API_KEY = "your_api_key_here"
   ```

5. **Run the application**:
   ```bash
   streamlit run app.py
   ```

The app will open in your browser at `http://localhost:8501`

## 📱 Usage

### Authentication Flow
1. Enter your 10-digit phone number
2. Click "Send OTP"
3. A demo OTP will be displayed (in real deployment, this would be sent via SMS)
4. Enter the OTP and click "Verify OTP"
5. Once verified, access the chat interface

### Chat Interface
1. **Select Language**: Choose your preferred language from the sidebar (English, ಕನ್ನಡ, हिन्दी, తెలుగు, தமிழ்)
2. **Select History Language**: Choose the language for viewing chat history
3. **Type Your Query**: Ask any agriculture-related questions
4. **Get Response**: AI responds with translations in multiple languages
5. **Listen**: Audio output plays automatically in your selected language

### Chat Management
- **Clear Chat History**: Delete all conversations for your account
- **Change Phone Number**: Log out and switch to a different phone number

## 🌐 Supported Languages

| Language | Code | Native Script |
|----------|------|---------------|
| English | en | English |
| Kannada | kn | ಕನ್ನಡ |
| Hindi | hi | हिन्दी |
| Telugu | te | తెలుగు |
| Tamil | ta | தமிழ் |

## 💾 Data Storage

- Chat histories are saved locally as JSON files: `chat_{phone_number}.json`
- Each message is stored with translations in all supported languages
- Original user input language is preserved

## 🎨 UI Features

- Agricultural green-themed gradient background
- Custom styled chat messages
- Responsive sidebar with language controls
- Phone number status display
- Smooth animations and shadows

## 📝 How It Works

1. **User Input**: User types a message in their preferred language
2. **Translation**: If not in English, the input is translated to English
3. **AI Processing**: Gemini model processes the English prompt
4. **Multi-language Response**: Response is translated to all supported languages
5. **Storage**: All versions stored in chat history

## 🔐 Security Notes

- OTP verification is implemented (demo mode shows OTP on screen)
- In production, integrate with SMS gateway for real OTP delivery
- Store API keys securely using Streamlit secrets management
- User data is stored locally - ensure proper data protection measures

## 🐛 Known Limitations

- Demo OTP is displayed on screen (implement SMS gateway for production)
- Translation quality depends on Gemini model capabilities

## 🚀 Future Enhancements

- Real SMS OTP integration
- Cloud-based chat storage
- Voice input support
- Image recognition for crop diseases
- Location-based recommendations
- Offline language support

 ## Results
![WhatsApp Image 2026-03-04 at 5 59 55 PM](https://github.com/user-attachments/assets/f9145e7f-13d0-4824-abf4-c61bc1cb8e5c)

![WhatsApp Image 2026-03-04 at 6 01 16 PM](https://github.com/user-attachments/assets/a82ca7b4-cacc-4170-a286-485d069f8a5d)

![WhatsApp Image 2026-03-04 at 6 01 17 PM](https://github.com/user-attachments/assets/5f4040fa-3afb-4046-a3db-5eac6ee25b95)



