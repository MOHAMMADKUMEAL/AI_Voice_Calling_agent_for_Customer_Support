# AI Voice Calling Agent for Customer Support

An intelligent voice calling system that handles customer support calls using AI. The system can understand customer queries, provide relevant responses, and manage customer interactions effectively using state-of-the-art AI technologies.

## Features
- Automated voice call handling using Twilio
- Real-time speech-to-text conversion using Google Speech Recognition
- Advanced Natural Language Processing for intent recognition using OpenAI GPT
- Natural-sounding text-to-speech conversion using Google Cloud TTS
- Intelligent call flow management and routing
- Comprehensive customer query handling
- Call recording and monitoring capabilities
- Real-time call status tracking
- Call transfer functionality
- Configurable response templates
- Error handling and fallback mechanisms

## Technical Architecture
- **Flask Backend**: Handles HTTP requests and webhooks
- **Twilio Integration**: Manages voice calls and telephony features
- **Speech Processing**: Converts between speech and text
- **AI Engine**: Processes intents and generates responses
- **Call Management**: Handles call flow and status
- **Configuration System**: Manages settings and environment variables

## Requirements
- Python 3.8+
- Twilio account for voice calling capabilities
- Google Cloud account for speech services
- OpenAI API key for natural language processing
- Stable internet connection
- SSL certificate for production deployment

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/ai-voice-calling-agent.git
cd ai-voice-calling-agent
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
   - Copy `.env.template` to `.env`
   - Fill in your API keys and configuration:
```
TWILIO_ACCOUNT_SID=your_account_sid
TWILIO_AUTH_TOKEN=your_auth_token
TWILIO_PHONE_NUMBER=your_phone_number
OPENAI_API_KEY=your_openai_key
GOOGLE_APPLICATION_CREDENTIALS=path_to_credentials.json
```

## Configuration
- Adjust settings in `config.py` for:
  - Call duration limits
  - Speech timeout
  - Retry attempts
  - AI confidence thresholds
  - Language settings
  - Logging preferences

## Usage

1. Start the Flask server:
```bash
python app.py
```

2. Configure Twilio:
   - Set up a Twilio phone number
   - Configure the webhook URL to point to your server:
     - Voice URL: `http://your-domain/incoming_call`
     - HTTP Method: POST

3. Testing:
   - Make a test call to your Twilio number
   - Monitor the logs for any issues
   - Check call recordings in Twilio console

## Project Structure
```
ai-voice-calling-agent/
├── app.py                 # Main Flask application
├── speech_processor.py    # Speech processing logic
├── ai_agent.py           # AI conversation handling
├── call_handler.py       # Call management
├── config.py             # Configuration settings
├── requirements.txt      # Project dependencies
├── .env                  # Environment variables
└── README.md            # Documentation
```
 