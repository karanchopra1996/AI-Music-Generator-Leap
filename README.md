# AI Music Generator using Leap AI and Next.js

Music has the power to evoke emotions, create moods, and tell stories. With advancements in artificial intelligence, we can now generate music compositions based on text prompts. In this project, we demonstrate how to build an AI music generator using **Leap AI**, a platform that provides access to powerful AI models, and **Next.js**, a popular React framework for server-side rendering.

## Features
- **Generate AI Music**: Users can provide text prompts to generate custom music compositions.
- **Server-Side Rendering**: Built with **Next.js** for fast and optimized performance.
- **AI-Powered Music Generation**: Uses **Leap AI** to create high-quality, unique music compositions from textual descriptions.

## Prerequisites
Before you begin, make sure you have the following installed:

1. **Node.js** and **npm** (Node Package Manager).
2. Basic knowledge of **JavaScript** and **React**.
3. An active **Leap AI** account and API key. You can sign up for an account at [Leap AI](https://leap-ai.com) to get your API key.

## Getting Started

### 1. Clone this Repository
  Clone the repository to your local machine:
  git clone https://github.com/your-username/ai-music-generator-leap.git
    - cd ai-music-generator-leap
### 2. Install Dependencies
  Run the following command to install the necessary dependencies:
    - npm install
### 3. Set Up Environment Variables
  Create a .env file in the root directory of the project and add the following environment variable:
    - LEAP_API_KEY=<paste-your-token-here>
  Retrieve your API key from your Leap AI account settings.
### 4. Running the Application
  Run the application in development mode:
    - npm run dev

Visit http://localhost:3000 in your browser to start generating music!

## How It Works
### Backend
The backend is built with Next.js API routes. Here's an overview of how the backend works:
  Authentication: The app integrates with Leap AI using the API key stored in the environment variable.
  Music Generation: The system accepts text prompts from the frontend, sends the prompt to Leap AI, and retrieves the generated music.
  Polling: The backend checks the status of the music generation and waits until the music is ready to be served.
### Frontend
  The frontend is built using React and Tailwind CSS:
  Users input a prompt (e.g., "lofi chill beats, bollywood style") into a text field.
  When the "Generate Music" button is clicked, the frontend sends the prompt to the backend API route.
  The generated music URL is returned and displayed as an audio player for playback.

### Code Explanation
  Backend (api/music-generate.js): Handles requests for music generation, communicates with Leap AI, and manages job polling until the music is ready.
  Frontend (pages/index.js): A simple UI for users to input prompts and listen to the generated music. It shows a loading spinner while the music is being generated.

### Sample Prompts
  "Lofi chill beats, bollywood style, rains"
  "Techno style, high bpm, sound drop"
