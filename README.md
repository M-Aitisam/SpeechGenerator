# Speech Tools Application


![image](https://github.com/user-attachments/assets/a44ffcd8-6bf6-4600-a13a-354866480afa)


A Blazor web application that provides:
- 🎙️ Speech-to-Text transcription
- 🔊 Text-to-Speech synthesis

## Features

### Speech-to-Text
- Upload audio files (WAV, MP3, M4A)
- Max file size: 20MB
- View transcription results
- Copy text to clipboard

### Text-to-Speech
- Enter any text to convert to speech
- Multiple voice options (Lisa, Bob, Charlie, etc.)
- Adjustable speech speed
- Download generated audio

## Prerequisites

- .NET 8 SDK
- Node.js (for optional frontend tooling)
- API endpoints:
  - Transcription: `http://54.158.238.139:5000/transcribe`
  - TTS: `http://34.204.80.229:5050/api/speak`

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/M-Aitisam/SpeechGenerator.git
   cd SpeechGenerator



Configure the application:

Update API endpoints in Program.cs if needed

Set any environment variables
The application will be available at:
https://localhost:5001 (or your configured port)

API Documentation
Speech-to-Text API
Endpoint: POST /transcribe

Content-Type: multipart/form-data

Parameters:

file: Audio file to transcribe

Response:
{
  "transcription": "The transcribed text"
}

Text-to-Speech API
Endpoint: POST /api/speak

Content-Type: application/json

Parameters:
{
  "text": "Text to speak",
  "speaker": "voice_id",
  "speed": 1.0
}

Response: Audio file in WAV format

Troubleshooting
Common Issues
API Connection Errors:

Verify API endpoints are correct

Check network connectivity

Test APIs manually with curl:

# Test transcription API
curl -X POST http://54.158.238.139:5000/transcribe -F "file=@test.mp3"

# Test TTS API
curl -X POST http://34.204.80.229:5050/api/speak \
  -H "Content-Type: application/json" \
  -d '{"text":"Hello","speaker":"lisa","speed":1.0}'

File Upload Issues:

Ensure file is <20MB

Supported formats: WAV, MP3, M4A

CORS Errors:

Configure CORS in Program.cs if needed

Configuration
Environment variables (optional):

export TranscriptionApiBaseUrl="http://your-transcription-api"
export TtsApiBaseUrl="http://your-tts-api"

Deployment
To Azure/AWS App Service:
az webapp up --name your-app-name --resource-group your-resource-group --runtime-dotnet=8.0

Docker:
docker build -t speech-tools .
docker run -p 5000:80 speech-tools

Contributing
Fork the project

Create your feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some amazing feature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request

License
Distributed under the MIT License. See LICENSE for more information.

Contact
Your Name - @aitisam - aitisamahmed@gmail.com

Project Link: https://github.com/M-Aitisam/SpeechGenerator



## Key Sections Included:

1. **Project Overview**: Brief description and features
2. **Installation**: How to set up the project
3. **API Documentation**: Details about both speech services
4. **Troubleshooting**: Common issues and solutions
5. **Deployment**: Instructions for different hosting options
6. **Contributing**: Guidelines for contributors
7. **License and Contact** information

