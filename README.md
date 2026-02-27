# Kindred: AI-Powered Friendship Social Platform

Kindred is a modern, friendship-first social application designed to foster meaningful connections through AI-powered matching, activity suggestions, and a zero-tolerance moderation system. Built with a focus on safety and gamification, Kindred helps users find their "circle" through shared interests and personality compatibility.

## 🚀 Key Features

### 1. AI-Powered Intelligence
*   **Automated Moderation**: Every post is scanned in real-time by the **Gemini 3 Flash** model. Content violating safety guidelines (hate speech, nudity, etc.) is instantly rejected, ensuring a safe environment.
*   **AI Friendship Assistant**: A dedicated companion that provides icebreakers, social advice, and conflict resolution tips.
*   **Smart Matching**: An algorithm that calculates compatibility scores based on hobbies, personality types (Introvert/Extrovert), and worldviews.

### 2. Gamification & Reputation
*   **Onboarding Challenges**: Users earn badges (Enthusiast, Friendly, Storyteller) for completing profile milestones.
*   **Reputation System**: A dynamic "Zap" score that rewards positive community contributions like posting, receiving likes, and planning hangouts.
*   **Badge Gallery**: A visual showcase of a user's achievements and community standing.

### 3. Social & Interaction
*   **Post of the Day**: Daily prompts to encourage low-pressure sharing and interaction.
*   **Activity Generator**: Suggests curated hangout ideas (Free, Low-Cost, Paid) based on shared interests between matched users.
*   **Spotify Integration**: Connects with the Spotify API to showcase music taste on user profiles.

## 🛠️ Tech Stack

*   **Frontend**: React 19, Vite, Tailwind CSS 4, Framer Motion (for animations), Lucide React (icons).
*   **Backend**: Node.js, Express.
*   **Database**: SQLite (`better-sqlite3`) for robust, local data persistence.
*   **AI**: Google Gemini API (@google/genai).
*   **Authentication**: Custom session management with Spotify OAuth integration.

## 📦 Installation & Setup

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/kindred.git
    cd kindred
    ```

2.  **Install dependencies**:
    ```bash
    npm install
    ```

3.  **Configure Environment Variables**:
    Create a `.env` file based on `.env.example`:
    ```env
    GEMINI_API_KEY=your_gemini_api_key
    APP_URL=http://localhost:3000
    SPOTIFY_CLIENT_ID=your_spotify_id
    SPOTIFY_CLIENT_SECRET=your_spotify_secret
    ```

4.  **Run in Development Mode**:
    ```bash
    npm run dev
    ```

5.  **Build for Production**:
    ```bash
    npm run build
    npm start
    ```

## 🛡️ Safety & Moderation

Kindred implements a "Moderation Gateway" architecture. When a user submits a post:
1.  The content is sent to the Gemini AI.
2.  The AI evaluates the text against a strict safety rubric.
3.  Only approved content is persisted to the database and displayed on the feed.
4.  Violations trigger immediate feedback and can lead to automated account suspension.

## 📄 License

This project is licensed under the Apache-2.0 License.

---
*Built with ❤️ for meaningful human connection.*
