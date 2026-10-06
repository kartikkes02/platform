# Prept — AI-Powered Mock Interview Platform

![Next.js 16](https://img.shields.io/badge/Next.js-16.2-black?style=flat&logo=nextdotjs)
![React 19](https://img.shields.io/badge/React-19.2-61DAFB?style=flat&logo=react)
![Tailwind CSS v4](https://img.shields.io/badge/Tailwind-v4-38B2AC?style=flat&logo=tailwind-css)
![Clerk Auth](https://img.shields.io/badge/Auth-Clerk-6C47FF?style=flat&logo=clerk)
![Stream Video & Chat](https://img.shields.io/badge/RTC-Stream.io-005FFF?style=flat&logo=stream)

**Prept** is an end-to-end, AI-powered mock interview platform connecting tech candidates with senior industry interviewers from top companies (FAANG/Tier-1). Features include 1:1 HD video calling, live chat, real-time AI question co-piloting, slot-based availability scheduling, and a credit-based monetization model.

---

## ✨ Features

- **🎓 Candidate Interview Booking**:
  - Filter interviewers by tech domain (*Frontend, Backend, System Design, DSA, AI/ML*).
  - Search by interviewer name, title, or company.
  - Slot-based 1-click booking using session credits.

- **⚡ Live 1:1 Video Calls & Chat**:
  - HD video streaming powered by **Stream Video SDK**.
  - Persistent real-time messaging powered by **Stream Chat SDK**.

- **🤖 AI Questions Co-Pilot**:
  - Live AI co-pilot for interviewers to generate topic-specific technical questions, answers, and evaluation rubrics on demand during calls.

- **💼 Interviewer Monetization & Dashboard**:
  - Set custom slot-based availability.
  - Track earned session credits and completed interviews.
  - Request payouts & monitor withdrawal history.

- **🔐 Seamless Role-Based Auth**:
  - Clerk Authentication integration with role-switching capability between Interviewee and Interviewer modes.

---

## 🛠️ Tech Stack

| Domain | Technology |
| :--- | :--- |
| **Framework** | [Next.js 16 (App Router)](https://nextjs.org/) & [React 19](https://react.dev/) |
| **Styling & UI** | [Tailwind CSS v4](https://tailwindcss.com/), [Radix UI](https://www.radix-ui.com/), [Lucide React](https://lucide.dev/) |
| **Authentication** | [Clerk (`@clerk/nextjs`)](https://clerk.com/) |
| **Video Calling** | [Stream Video SDK (`@stream-io/video-react-sdk`)](https://getstream.io/video/) |
| **Real-time Chat** | [Stream Chat SDK (`stream-chat-react`)](https://getstream.io/chat/) |
| **AI Co-Pilot** | Generative AI integration for dynamic question generation |
| **Notifications** | [Sonner](https://sonner.emilkowal.ski/) |

---

## 📁 Project Structure

```text
my-app/
├── actions/                  # Server Actions
│   ├── aiQuestions.js        # AI interview question generation logic
│   ├── appointments.js       # Interviewee session retrieval
│   ├── call.js               # Stream call data & token generator
│   ├── dashboard.js          # Availability, stats, and withdrawal logic
│   ├── explore.js            # Interviewer directory search
│   └── user.js               # Current authenticated user details
├── app/                      # Next.js App Router pages
│   ├── (auth)/               # Clerk sign-in and sign-up pages
│   ├── (main)/
│   │   ├── appointments/     # Scheduled & past mock sessions
│   │   ├── call/[callId]/    # Live video call & AI panel room
│   │   ├── dashboard/        # Interviewer earnings, slots & stats
│   │   ├── explore/          # Search & filter expert interviewers
│   │   └── interviewer/[id]/ # Individual booking page
│   ├── onboarding/           # Initial role selection page
│   ├── globals.css           # Tailwind v4 styles & theme configuration
│   └── layout.js             # Root layout with ClerkProvider & ThemeProvider
├── components/               # UI & Reusable Components
│   ├── ui/                   # Button, Badge, Card, Dialog, Tabs primitives
│   ├── AppointmentCard.jsx   # Session card component
│   ├── CreditButton.jsx      # Header credit balance indicator
│   ├── Header.jsx            # Top navigation bar wrapper
│   ├── HeaderNav.jsx         # Client navigation controls with Clerk UI
│   ├── PricingSection.jsx    # Subscription & credit plans
│   ├── RoleRedirect.jsx      # Role switcher badge
│   └── reusables.jsx         # Page headers & gold/gray typography titles
├── hooks/                    # Custom React Hooks
│   └── use-fetch.js          # Async server action execution state manager
├── lib/                      # Data & helper utilities
│   ├── checkUser.js          # Server user validation
│   ├── data.js               # Mock data, categories & constants
│   ├── helpers.js            # Date formatting utilities
│   └── userStore.js          # Local state storage for user roles & credits
└── public/                   # Public SVG & graphic assets
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js `18.x` or higher
- npm, pnpm, or yarn

### 1. Clone the repository & Install dependencies

```bash
cd my-app
npm install
```

### 2. Configure Environment Variables

Create a `.env` file in the `my-app` root directory:

```env
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key
NEXT_PUBLIC_STREAM_API_KEY=your_stream_api_key
```

### 3. Run the Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### 4. Build for Production

```bash
npm run build
npm run start
```

---

## 📄 License

Made with ❤️ by Kartikeya Kesarwani.
