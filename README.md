# smileagain_meenarashi
# Smile Again 🌟

## About The Project

Smile Again is an innovative mental health support platform that provides anonymous peer support, professional counseling connections, and AI-powered emotional assistance. The platform is designed to create a safe space where users can share their struggles, connect with others facing similar challenges, and track their journey toward better mental well-being.

### Key Features 🎯

- **Anonymous Registration & Authentication**: Secure, privacy-focused user accounts
- **Community Building**: Auto-generated support groups based on shared experiences
- **AI Chatbot Support**: Empathetic conversation partner available 24/7
- **Professional Counselor Connection**: Direct access to mental health professionals
- **Milestone System**: Community-wide progress tracking with visual transformations
- **Real-time Interactions**: Live chat and community discussions
- **Stress Level Monitoring**: Personalized support recommendations based on user state

## Technology Stack 💻

### Backend Infrastructure
- **Framework**: Flask (Python)
- **Database**: SQLite (Development) / PostgreSQL (Production)
- **Authentication**: Flask-Login with session management
- **Real-time Communication**: Flask-SocketIO
- **API Documentation**: OpenAPI/Swagger

### AI and Machine Learning
- **Core Chat Model**: ModelLake API integration for multilingual empathetic responses
- **Language Support**: Real-time conversation in multiple languages including:
  - English
  - Hindi
  - Telugu
  - Tamil
  - Kannada
  - Marathi
  - Bengali
  - Gujarati
  - Malyalam
- **NLP Processing**: 
  - NLTK for text analysis
  - Language detection and automatic translation
  - Cultural context awareness
  - Sentiment analysis across languages
- **Emotion Detection**: 
  - Cross-cultural emotion classification system
  - Context-aware emotional response generation
  - Cultural sensitivity filters
- **Crisis Detection**: 
  - Multi-language pattern-based crisis identification
  - Culture-specific crisis intervention protocols
  - Region-specific emergency resource recommendations

### Multilingual Empathy Bot Features 🤖
- **Adaptive Language Processing**:
  - Automatic language detection and switching
  - Preservation of emotional context across translations
  - Culture-specific empathy expressions
  - Dialect and regional variation awareness

- **Cultural Competency**:
  - Region-specific mental health approaches
  - Culturally appropriate metaphors and expressions
  - Local support resource recommendations
  - Cultural sensitivity in crisis situations

- **Technical Implementation**:
  - ModelLake API integration for natural language understanding
  - Custom emotion-aware translation pipeline
  - Real-time language switching without context loss
  - Multilingual conversation history management

- **Response Generation**:
  - Culture-aware empathetic responses
  - Language-specific comfort phrases
  - Localized coping strategies
  - Regional support resource integration



## Environment Variables Configuration 🔧

```bash
# ModelLake API Configuration
MODELLAKE_API_KEY=your_api_key
MODELLAKE_MODEL=llama3
MODELLAKE_MAX_TOKENS=300

# Language Support Configuration
DEFAULT_LANGUAGE=en
SUPPORTED_LANGUAGES=en,Te-In,Tl-In,Ml-In,Gj-In,Mr-In,Be-In,Ka-In
TRANSLATION_FALLBACK=en

# Bot Personality Settings
BOT_NAME=Joy
EMPATHY_LEVEL=high
CRISIS_THRESHOLD=0.7

### Security Features
- **Data Encryption**: AES for sensitive data
- **Password Hashing**: Bcrypt
- **Session Management**: Secure cookie handling
- **CORS Protection**: Configured for secure cross-origin requests

## Getting Started 🚀

### Prerequisites

```bash
# Python 3.8+ required
python --version

# Create virtual environment
python -m venv venv

# Activate virtual environment
# For Windows:
venv\Scripts\activate
# For Unix/MacOS:
source venv/bin/activate

##Installation
---bash
# git clone https://github.com/your-username/smile-again.git
cd smile-again

# pip install -r requirements.txt

# cp .env.example .env
# Edit .env with your configuration

# flask db upgrade
python init_db.py  # Loads initial data

# flask run

##Project Structure

---bash
#smile-again/
├── backend/
│   ├── activity/
│   │   ├── __init__.py
│   │   ├── routes.py
│   │   └── utils.py
│   ├── auth/
│   │   ├── __init__.py
│   │   ├── routes.py
│   │   └── utils.py
│   ├── blogs/
│   │   ├── __init__.py
│   │   ├── routes.py
│   │   └── utils.py
│   ├── bot/
│   │   ├── __init__.py
│   │   ├── routes.py
│   │   └── utils.py
│   ├── chats/
│   │   ├── __init__.py
│   │   ├── routes.py
│   │   └── utils.py
│   ├── community/
│   │   ├── __init__.py
│   │   ├── routes.py
│   │   └── utils.py
│   ├── friends/
│   │   ├── __init__.py
│   │   ├── routes.py
│   │   └── utils.py
│   ├── games/
│   │   ├── routes.py
│   │   └── utils.py
│   ├── meditation/
│   │   ├── routes.py
│   │   └── utils.py
│   ├── mood/
│   │   ├── routes.py
│   │   └── utils.py
│   ├── smile_journey/
│   │   ├── __init__.py
│   │   ├── routes.py
│   │   └── utils.py
│   ├── stress_assessment/
│   │   ├── routes.py
│   │   └── utils.py
│   ├── users/
│   │   ├── __init__.py
│   │   ├── routes.py
│   │   └── utils.py
│   ├── workshops/
│   │   ├── __init__.py
│   │   ├── routes.py
│   │   └── utils.py
│   ├── app.py
│   ├── config.py
│   ├── create_admin.py
│   ├── db_inspector.py
│   ├── extensions.py
│   ├── models.py
│   └── users.db
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── NavAfterLogin.jsx
│   │   │   ├── Bot_Speech.jsx
│   │   │   └─ALL COMPONENTS OF JAVASCRIPT AND CSS ARE IN SRC
│   │   ├── pages/
│   │   │   ├── ChatBotPage.jsx
│   │   │   ├── ProfilePage.jsx
│   │   │   ├── FriendsPage.jsx
│   │   │   ├── BlogsPage.jsx
│   │   │   └── SmileJourney.jsx
│   │   ├
│   │   │   
│   │   │   
│   │   │   
│   │   │   
│   │   │   
│   │   ├── contexts/
│   │   │   ├── AuthContext.jsx
│   │   │   └── UserContext.jsx
│   │   ├── utils/
│   │   │   ├── api.js
│   │   │   ├── constants.js
│   │   │   └── helpers.js
│   │   ├── App.jsx
│   │   ├── index.jsx
│   │   └── index.css
│   ├── package.json
│   ├── .env
│   └── .env.example
├── instance/
├── README.md
├── .gitignore
└── requirements.txt
---bash


##API Documentation 📚

###Authentication Endpoints
- POST /auth/register - User registration
- POST /auth/login - User login
- POST /auth/logout - User logout

###Chat Endpoints

- POST /bot/chat - Send message to AI bot
- GET /chat/history - Retrieve chat history

###Community Endpoints

- GET /groups - List available groups
- POST /groups - Create new group
- POST /groups/<id>/join - Join specific group

###User Management Endpoints

- GET /profile - Get user profile
- PUT /profile - Update user profile
- GET /friends - List friends
- POST /friend-request - Send friend request

###Contributing 🤝

- Fork the repository
- Create your feature branch (git checkout -b feature/AmazingFeature)
- Commit your changes (git commit -m 'Add some AmazingFeature')
- Push to the branch (git push origin feature/AmazingFeature)
- Open a Pull Request

##Core Features Implementation Details 🔧

##Multi lingual AI Chatbot Capabilities
###Anonymous User System
###Unique identifier generation
###Privacy-focused data storage
###Secure session management
###Emotional state detection
###Crisis intervention protocols
###Contextual response generation
###Conversation history management
###Community Management
###Stress Tracking System
###User stress level monitoring
###Intervention triggers
###Progress visualization
###Milestone achievement system

##Security Considerations 🔒

-All sensitive data is encrypted at rest
-Regular security audits
-Rate limiting on all endpoints
-Input validation and sanitization
-XSS and CSRF protection
-Regular dependency updates

###License 📄
-Distributed under the MIT License. See LICENSE for more information.
###Support 💡
-For support, email support@smileagain.com or join our Slack channel.
Acknowledgments 🙏
-Open source community
-All contributors and supporters


###Built with ❤️ by the Smile Again Team
