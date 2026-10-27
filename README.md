# AI-Based Career Guide

A Computer Science capstone project exploring how one platform can help job seekers plan their next career step—from comparing skills with job requirements to preparing for interviews.

**Project URL:** [career-guide-ai-nine.vercel.app](https://career-guide-ai-nine.vercel.app) · **Source:** this repository

## Features
- Browse job listings and analyse skill gaps against selected roles.
- Maintain a career profile and resume data; generate resume improvements.
- Create learning paths and discover learning resources.
- Practise text-based or voice-assisted mock interviews and review feedback.

## Stack
Next.js App Router, React, TypeScript, PostgreSQL, Prisma, Better Auth, Google Gemini API and optional ElevenLabs text-to-speech.

## Local setup
Requirements: a compatible Node.js release, npm and a PostgreSQL database.

1. Clone the repository and install dependencies:
   ```bash
   git clone https://github.com/Ezra2121-et/career-guide-ai.git
   cd career-guide-ai
   npm install
   ```
2. Create `.env` in the repository root (see `.env.example`). Set `DIRECT_URL`, `BETTER_AUTH_SECRET` and `BETTER_AUTH_URL`. Add `GEMINI_API_KEY` for Gemini features; `ELEVEN_LABS_API_KEY` enables voice synthesis.
3. Generate the Prisma client, apply the existing migrations and start the development server:
   ```bash
   npx prisma generate
   npx prisma migrate deploy
   npm run dev
   ```
4. Open `http://localhost:3000`.

## Notes
AI and voice features require their respective API keys. Keep secrets server-side, never commit `.env`, and do not treat generated career guidance as a guarantee of employment outcomes. The deployment URL is provided for demonstration; availability depends on its configured services.

## License
Released under the MIT License. See [LICENSE](LICENSE). Third-party packages and services remain subject to their own terms.
