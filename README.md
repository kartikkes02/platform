

# 🚀 CareerAI — Integrated AI Resume Analyzer & AI Mock Interview Platform

<div align="center">
  <img src="ai-interview-platform/public/readme/hero.webp" alt="CareerAI Banner" width="100%" onerror="this.style.display='none'" />
  <br /><br />

  <div>
    <img src="https://img.shields.io/badge/Next.js_16-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js 16" />
    <img src="https://img.shields.io/badge/React_19-4c84f3?style=for-the-badge&logo=react&logoColor=white" alt="React 19" />
    <img src="https://img.shields.io/badge/React_Router_v7-CA4245?style=for-the-badge&logo=react-router&logoColor=white" alt="React Router v7" />
    <img src="https://img.shields.io/badge/Tailwind_CSS_v4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
    <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
    <img src="https://img.shields.io/badge/Google_Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" alt="Google Gemini" />
    <img src="https://img.shields.io/badge/Puter.js-181758?style=for-the-badge&logoColor=white" alt="Puter.js" />
    <img src="https://img.shields.io/badge/Stream_Video_%26_Chat-005FFF?style=for-the-badge&logo=stream&logoColor=white" alt="Stream SDK" />
    <img src="https://img.shields.io/badge/Clerk_Auth-6C47FF?style=for-the-badge&logo=clerk&logoColor=white" alt="Clerk Auth" />
    <img src="https://img.shields.io/badge/Prisma_Postgres-2D3748?style=for-the-badge&logo=prisma&logoColor=white" alt="Prisma" />
  </div>

  <br />
  <p align="center">
    <strong>An End-to-End AI-Powered Career Readiness, ATS Resume Evaluation & Live Interview Platform</strong><br />
    A comprehensive college minor project combining intelligent client-side ATS resume scoring, multi-model AI feedback, real-time video/audio mock interviews, dynamic AI question generation, and mentor booking.
  </p>
</div>

---

## 📌 Abstract of Project

> **Problem Being Addressed**: Modern job applicants face significant barriers in today's automated recruitment landscape, primarily due to opaque Applicant Tracking Systems (ATS) and a lack of accessible, personalized interview preparation. Traditional resume reviews are often costly or non-standardized, while high-stakes interview anxiety remains unaddressed due to limited access to real-time feedback and practice environments.
> 
> **Proposed Solution**: To resolve these challenges, this project presents an integrated, end-to-end **AI Resume Analyzer & AI Mock Interview Platform**. The proposed solution combines two synergistic modules into a unified career readiness ecosystem: an intelligent client-side ATS Resume Scorer and a real-time AI-Powered Mock Interview Marketplace. The platform leverages Mozilla PDF.js for in-browser text extraction, Puter.js serverless architecture for cloud storage and multi-model AI routing (GPT-4o, Gemini 2.0, Claude 3.5), Next.js 16 with Stream SDKs for real-time video/audio streaming, and Clerk with Arcjet for secure authentication and bot protection.
> 
> **Key Objectives**: The primary objectives of this project are:
> 1. **Automated ATS Evaluation**: Deliver multi-dimensional ATS resume scoring ($0-100$) across tone, structural formatting, impact metrics, and job-description keyword matching.
> 2. **Dynamic AI Question Generation**: Utilize Google Generative AI (Gemini) to craft role-specific, adaptive technical and behavioral interview questions based on candidate resumes.
> 3. **Real-Time Video/Audio Streaming**: Enable interactive AI mock interviews and peer coaching sessions with video/audio streaming and live chat via Stream SDKs.
> 4. **Zero-Trust Serverless Execution**: Maintain complete user data privacy, low-latency execution, and cost-effective cloud persistence without heavy backend overhead.
> 
> **Expected Outcome**: The expected outcome is a fully functional, production-ready web application that empowers job seekers to optimize their resumes for automated ATS filters, practice realistic technical and behavioral interviews, receive actionable performance feedback, and schedule peer mentorship sessions. By bridging candidate preparation gaps through multi-modal artificial intelligence, this platform significantly improves applicant employability and confidence in modern recruitment workflows.

---

## 📋 Table of Contents

- [📌 Abstract of Project](#-abstract-of-project)
- [✨ Key Features & Dual Modules](#-key-features--dual-modules)
  - [Module 1: Resumind — AI Resume Analyzer & ATS Scorer](#module-1-resumind--ai-resume-analyzer--ats-scorer)
  - [Module 2: AI Mock Interview & Mentorship Platform](#module-2-ai-mock-interview--mentorship-platform)
- [⚙️ Tech Stack Matrix](#️-tech-stack-matrix)
- [🧠 System Architecture & Data Flow](#-system-architecture--data-flow)
- [📁 Project Structure](#-project-structure)
- [🚀 Quick Start & Installation](#-quick-start--installation)
- [🤖 AI Evaluation & Scoring Categories](#-ai-evaluation--scoring-categories)
- [🔒 Authentication, Security & Privacy](#-authentication-security--privacy)
- [🛠️ Available Scripts](#️-available-scripts)
- [📄 License & Academic Declaration](#-license--academic-declaration)

---

## ✨ Key Features & Dual Modules

The platform is structured into two core operational modules that work together to guide job seekers from resume submission to mock interview mastery:

### Module 1: Resumind — AI Resume Analyzer & ATS Scorer

- 🔐 **Puter.js Serverless Authentication**:
  - Sign in seamlessly using **Google, Microsoft, Apple, or Email**.
  - Secure session management with zero custom backend infrastructure required.

- 📄 **Client-Side PDF Processing**:
  - In-browser text extraction using **`pdfjs-dist`** for 100% accurate, private resume reading.
  - Automatic PDF page rendering to high-resolution PNG previews using HTML5 Canvas.

- 🎯 **Intelligent ATS & Resume Scoring**:
  - Detailed **ATS Suitability Score (0-100)** with keyword matching and formatting suggestions.
  - Categorized evaluation: **Tone & Style**, **Content Quality**, **Structure**, and **Skills**.
  - Job-specific evaluation when target Job Title and Job Description are provided.

- ☁️ **Private Cloud Storage & KV Database**:
  - Resumes (`.pdf`) and preview images (`.png`) stored in user's private Puter Cloud File System (`puter.fs`).
  - Analysis results and ATS reports persisted in Puter's Key-Value Database (`puter.kv`).

- ⚡ **Multi-Model Fallback Engine**:
  - Resilient AI pipeline supporting **GPT-4o**, **GPT-4o-mini**, **Claude 3.5 Sonnet**, **Gemini 2.0 Flash**, and Puter AI models.

---

### Module 2: AI Mock Interview & Mentorship Platform

- 🎥 **Real-Time Video & Audio Interview Streaming**:
  - HD video calling powered by `@stream-io/video-react-sdk` and interactive text chat via `stream-chat-react`.
  - Realistic candidate interview experience with real-time audio/video toggle, screen sharing, and recording state.

- 🧠 **AI-Powered Adaptive Questioning**:
  - Driven by **Google Generative AI (Gemini 2.0 / 1.5 Pro)** to generate custom role-tailored questions based on target job description and resume content.
  - Evaluates candidate answers dynamically, measuring technical accuracy, tone, and delivery.

- 🔑 **Enterprise Auth & Security Protection**:
  - Multi-tenant authentication provided by `@clerk/nextjs` with custom dark-mode themes.
  - Threat detection, rate-limiting, and bot defense powered by `@arcjet/next`.

- 📅 **Interviewer Marketplace & Appointment Booking**:
  - Browse verified peer interviewers and industry mentors.
  - Schedule interview slots, manage payouts, and receive automated transactional emails via **Resend** and **React Email**.

- 📊 **Comprehensive Analytics & Feedback Dashboard**:
  - View historical interview performance, progress trends, appointment records, and onboarding profiles.

---

## ⚙️ Tech Stack Matrix

| Domain | Technology | Purpose |
|---|---|---|
| **Frontend Frameworks** | [Next.js 16](https://nextjs.org/) & [React 19](https://react.dev/) | Core SSR/App Router architecture for Interview Platform |
| **Routing (Module 1)** | [React Router v7](https://reactrouter.com/) | Client-side routing, loaders, and actions for Resume Scorer |
| **Cloud & Serverless AI** | [Puter.js v2](https://puter.com/) | Serverless Auth, Cloud FS, KV Database, and multi-model AI Gateway |
| **AI LLM Engine** | [Google Generative AI (Gemini)](https://ai.google.dev/) | Real-time question generation & answer feedback evaluation |
| **Real-Time Video & Chat** | [Stream SDKs](https://getstream.io/) | `@stream-io/video-react-sdk` & `stream-chat-react` for interview calls |
| **Authentication** | [Clerk Auth](https://clerk.com/) & [Puter.js Auth](https://puter.com/) | Secure user identity, social logins, and authorization guards |
| **Database & ORM** | [Prisma](https://www.prisma.io/) & PostgreSQL | Relational data persistence for appointments, bookings, & user roles |
| **Styling & UI** | [Tailwind CSS v4](https://tailwindcss.com/) & [Shadcn UI](https://ui.shadcn.com/) | Modern utility styling, Radix primitives, Sonner toasts, and Lucide icons |
| **PDF Extraction** | [PDF.js (`pdfjs-dist`)](https://mozilla.github.io/pdf.js/) | Client-side PDF text extraction and Canvas preview generation |
| **Security & Rate Limiting** | [Arcjet](https://arcjet.com/) | Shield against abuse, bot attacks, and API rate-limit violations |
| **Email Service** | [Resend](https://resend.com/) & [React Email](https://react.email/) | Transactional email delivery for bookings and reminders |
| **Build & Tooling** | [Vite 6](https://vite.dev/) & [TypeScript](https://www.typescriptlang.org/) | Fast bundler, type safety, and static analysis |

---

## 🧠 System Architecture & Data Flow

```mermaid
graph TD
    User([Candidate / Job Seeker]) --> AuthCheck{Authenticated?}
    AuthCheck -- No --> AuthModal[Log In via Clerk / Puter.js]
    AuthModal --> UserDashboard[Career Dashboard]
    AuthCheck -- Yes --> UserDashboard

    %% Resume Flow
    UserDashboard --> UploadResume[Upload PDF Resume + Target JD]
    UploadResume --> PDFJs[Extract Text & Render Canvas PNG via PDF.js]
    PDFJs --> PuterFS[Store PDF & PNG in Puter Cloud FS]
    PuterFS --> AIAnalysis[Multi-Model AI Scoring: GPT-4o / Gemini / Claude]
    AIAnalysis --> PuterKV[Save Scores & Tips in Puter KV DB]
    PuterKV --> ResumeReport[View ATS Scorecard & Category Tips]

    %% Interview Flow
    ResumeReport --> SkillGaps[Extract Weak Skill Categories]
    SkillGaps --> SetupInterview[Configure AI Mock Interview Role]
    UserDashboard --> SetupInterview
    SetupInterview --> GeminiGen[Generate Custom Questions via Gemini AI]
    GeminiGen --> StreamRoom[Join Live Video/Audio Call via Stream SDK]
    StreamRoom --> RealTimeEval[AI Live Answer Feedback & Audio Transcription]
    RealTimeEval --> FinalReport[Generate Comprehensive Interview Scorecard]
    
    %% Peer Marketplace Flow
    UserDashboard --> ExploreMentors[Explore Peer Interviewers]
    ExploreMentors --> BookSlot[Schedule Appointment & Payout]
    BookSlot --> EmailNotify[Send Confirmation via Resend / React Email]
```

---

## 📁 Project Structure

```
AI_Interview_PlatformN/
├── ai-interview-platform/             # Module 2: AI Mock Interview & Mentorship Platform (Next.js)
│   ├── actions/                       # Server Actions (AI Questions, Bookings, Appointments, Payouts)
│   │   ├── aiQuestions.jsx            # Gemini AI question generator & evaluation logic
│   │   ├── appointments.js            # Appointment management actions
│   │   ├── booking.js                 # Peer interviewer booking system
│   │   ├── call.js                    # Stream Video call token generation
│   │   ├── dashboard.js               # Dashboard metrics & analytics fetcher
│   │   └── user.js                    # Onboarding & profile actions
│   ├── app/                           # Next.js App Router Structure
│   │   ├── (auth)/                    # Sign-in & Sign-up routes (Clerk Auth)
│   │   ├── (main)/                    # Main Application Pages
│   │   │   ├── appointments/          # Candidate booking schedule
│   │   │   ├── call/                  # Live Stream Video/Audio interview call room
│   │   │   ├── dashboard/             # Interview performance dashboard
│   │   │   ├── explore/               # Peer interviewer marketplace
│   │   │   ├── interviewers/          # Mentor profile views
│   │   │   ├── onboarding/            # User role & skills configuration
│   │   │   └── payout/                # Mentorship payout management
│   │   ├── api/                       # Webhooks & Stream Token API endpoints
│   │   ├── globals.css                # Tailwind CSS v4 directives & theme variables
│   │   └── page.jsx                   # Modern Landing page
│   ├── components/                    # UI Components (Shadcn UI, Modals, Stream Video UI)
│   ├── emails/                        # React Email templates for booking notifications
│   ├── hooks/                         # Custom React hooks (UseStreamCall, UseUser)
│   ├── lib/                           # Utility singletons (Prisma Client, Arcjet Security, Stream Client)
│   ├── prisma/                        # Database schema & migrations
│   │   └── schema.prisma              # PostgreSQL models (Users, Bookings, Reviews)
│   ├── public/                        # Static assets, badges, and icons
│   └── package.json                   # Dependencies for Next.js app
│
└── ai-resume-analyzer/                # Module 1: Resumind — AI Resume Analyzer & ATS Scorer (React Router / Vite)
    ├── app/                           # React App Structure
    │   ├── components/                # UI components (ScoreGauge, ATS, Accordion, ResumeCard)
    │   ├── lib/                       # PDF text extractor (pdf2img.ts) & Puter store (puter.ts)
    │   └── routes/                    # Client routes (/auth, /upload, /resume/:id, /wipe)
    ├── constants/                     # Sample resumes, evaluation prompts, JSON schemas
    ├── public/                        # PDF.js worker script (pdf.worker.min.mjs) & assets
    └── package.json                   # Dependencies for Resume Scorer
```

---

## 🚀 Quick Start & Installation

### Prerequisites

Ensure your environment meets the following requirements:
- **Node.js**: `v18.0.0` or higher
- **npm**: `v9.0.0` or higher (or `pnpm` / `yarn`)
- **PostgreSQL Database**: Free hosted instance (e.g., Supabase / Neon) or local Postgres.

### 1. Repository Setup

```bash
# Clone the repository
git clone https://github.com/your-username/AI_Interview_Platform.git
cd AI_Interview_Platform
```

---

### 2. Configure & Run Module 2 (AI Interview Platform)

```bash
cd ai-interview-platform

# Install dependencies
npm install

# Set up environment variables (.env)
cp .env.example .env
```

Add your credentials to `.env`:
```env
# Database
DATABASE_URL="postgresql://user:password@localhost:5432/interview_db?schema=public"

# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="pk_test_..."
CLERK_SECRET_KEY="sk_test_..."

# Stream Video & Chat
NEXT_PUBLIC_STREAM_API_KEY="your_stream_api_key"
STREAM_SECRET_KEY="your_stream_secret_key"

# Google Gemini AI
GEMINI_API_KEY="your_gemini_api_key"

# Arcjet Security
ARCJET_KEY="ajkey_..."

# Resend Email
RESEND_API_KEY="re_..."
```

Run database migrations & start dev server:
```bash
# Generate Prisma Client & Push Schema
npx prisma db push

# Start Next.js Development Server
npm run dev
```
Open **[http://localhost:3000](http://localhost:3000)** in your browser.

---

### 3. Configure & Run Module 1 (AI Resume Analyzer)

```bash
cd ../ai-resume-analyzer

# Install dependencies
npm install

# Start Vite Development Server
npm run dev
```
Open **[http://localhost:5173](http://localhost:5173)** in your browser.

---

## 🤖 AI Evaluation & Scoring Categories

### 📄 Resume ATS Scoring Categories (0 – 100)

| Category | Evaluation Focus |
|---|---|
| **Overall Score** | Weighted composite score indicating general resume impact and completeness. |
| **ATS Suitability** | Header formatting, standard section names, line spacing, and non-parseable tables. |
| **Tone & Style** | Usage of strong action verbs, active voice, elimination of passive pronouns. |
| **Content Quality** | Quantifiable metrics ($%, \$, \text{users}$), concrete achievements, and project results. |
| **Structure & Formatting** | Readability index, bullet length consistency, section ordering, visual hierarchy. |
| **Skills & Keyword Match** | Hard/soft skill alignment against specific target job descriptions. |

### 🎙️ AI Mock Interview Evaluation Metrics

| Metric | Evaluation Focus |
|---|---|
| **Technical Accuracy** | Correctness of conceptual definitions, coding principles, and problem-solving logic. |
| **Communication Clarity** | Speech structure, concise phrasing, and articulation during live calls. |
| **Behavioral Alignment** | Application of the STAR method (Situation, Task, Action, Result) in behavioral prompts. |
| **Confidence & Tone** | Fluency, lack of hesitation/fillers, and professional candidate presence. |

---

## 🔒 Authentication, Security & Privacy

1. **Client-Side Storage**: In the Resume Scorer, raw PDF documents and parsed text are stored in the user's private Puter Cloud File System (`puter.fs`), maintaining user ownership.
2. **Enterprise Threat Defense**: The Interview Platform utilizes **Arcjet** middleware to analyze incoming traffic, block bot attacks, prevent SQL injection/XSS attempts, and enforce strict API rate limiting.
3. **Multi-Tenant Auth**: User identity management is segregated via Clerk Auth, ensuring role-based access control (Candidates vs. Mentors/Interviewer profiles).

---

## 🛠️ Available Scripts

### AI Interview Platform (`ai-interview-platform`)

| Command | Description |
|---|---|
| `npm run dev` | Runs the Next.js 16 development server at `http://localhost:3000` |
| `npm run build` | Compiles and optimizes the production build |
| `npm run start` | Runs the compiled Next.js production server |
| `npm run postinstall` | Generates Prisma client bindings automatically |
| `npm run lint` | Runs ESLint rules across Next.js components and actions |

### AI Resume Analyzer (`ai-resume-analyzer`)

| Command | Description |
|---|---|
| `npm run dev` | Runs Vite dev server at `http://localhost:5173` |
| `npm run build` | Builds static bundle for production deployment |
| `npm run typecheck` | Validates TypeScript types across React Router v7 routes |

---

## 📄 License & Academic Declaration

This project is developed as a **College Minor Project** for academic assessment.

- **License**: [MIT License](LICENSE)
- **Academic Year**: 2025–2026
- **Project Domain**: Artificial Intelligence, Multi-Modal LLM Applications, Real-Time Web Communication.

<div align="center">
  <sub>Built with ❤️ using React 19, Next.js 16, Puter.js, Google Gemini & Stream SDKs.</sub>
</div>
