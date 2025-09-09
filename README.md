## Project Overview
This project is an AI-powered email writer application, consisting of a React frontend and a Spring Boot backend. It leverages the Gemini API for generating email content based on user input.

## Table of Contents
- [Features](#features)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [API Reference](#api-reference)
- [Gemini API Key](#gemini-api-key)
- [Contributing](#contributing)
- [License](#license)

## Features
- Generate professional emails using AI (Gemini API)
- User-friendly React frontend
- RESTful Spring Boot backend
- Customizable email templates

## Project Structure
```
AI-email-writer/
├── email-writer-react/        # React frontend
├── email-writer-sb/           # Spring Boot backend
└── hello/                     # Sample browser extension (optional)
```

### Frontend (`email-writer-react`)
- Built with React and Vite
- Handles user input and displays generated emails

### Backend (`email-writer-sb`)
- Built with Spring Boot
- Exposes REST API endpoints for email generation
- Integrates with Gemini API

## Getting Started

### Prerequisites
- Node.js (v18+ recommended)
- npm or yarn
- Java 17+
- Maven

### Installation

#### 1. Clone the repository
```powershell
git clone https://github.com/shubhamkumarsharma03/AI-email-writer.git
cd AI-email-writer
```

#### 2. Install frontend dependencies
```powershell
cd email-writer-react
npm install
```

#### 3. Build and run backend
```powershell
cd ../email-writer-sb
mvn spring-boot:run
```

#### 4. Start frontend
```powershell
cd ../email-writer-react
npm run dev
```

## Configuration

### Gemini API Key
This project uses the Gemini API to generate email content. You must provide your own Gemini API key.

#### How to Get a Gemini API Key
1. Visit [Google AI Studio](https://aistudio.google.com/app/apikey) and sign in with your Google account.
2. Click on "Get API Key" and follow the instructions.
3. Copy your personal API key.

#### Where to Add the API Key
- **Frontend:** Add your Gemini API key to the environment file (`.env`) in `email-writer-react`:
	```env
	VITE_GEMINI_API_KEY=your_api_key_here
	```
- **Backend:** If required, add the API key to `application.properties` in `email-writer-sb`:
	```properties
	gemini.api.key=your_api_key_here
	```

## Usage
1. Open the frontend in your browser (usually at `http://localhost:5173`).
2. Enter your email requirements and submit.
3. The AI will generate a professional email using the Gemini API.

## API Reference
- **POST /api/generate-email**
	- Request: `{ "subject": "...", "body": "..." }`
	- Response: `{ "generatedEmail": "..." }`

## Contributing
Contributions are welcome! Please open issues or submit pull requests for improvements.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

**Note:** Never share your Gemini API key publicly. Keep it secure and use environment variables for configuration.
# AI-email-writer
