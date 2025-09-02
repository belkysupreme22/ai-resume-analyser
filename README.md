# AI-Powered Resume Analyser

A modern, full-stack React application for uploading, tracking, and receiving AI-powered feedback on your resumes.  
This project leverages [Puter](https://puter.com/) for cloud storage, authentication, AI feedback, and key-value data management.

**Live Demo:**  
[ai-resume-analyser.puter.app]() 

## Features

- 📄 Upload and manage multiple resumes in the cloud
- 🤖 Get smart, AI-powered feedback for your resume using Puter AI
- 👤 User authentication and profile management via Puter
- 🗑️ Delete resumes with a single click
- 🎨 Beautiful UI with TailwindCSS
- 🔒 TypeScript by default

## Powered by Puter

This app uses [Puter](https://docs.puter.com/introduction/) for:

- **Authentication:** Sign in/out, get current user, check authentication status
- **Cloud Storage:** Upload, read, write, and delete files (resumes) in the cloud
- **AI Services:** Chat-based feedback and image-to-text extraction for resumes
- **Key-Value Store:** Save and retrieve resume metadata and feedback

All Puter features are accessed via a global `window.puter` object and managed in React using [Zustand](https://zustand-demo.pmnd.rs/).

## Getting Started

### Installation

Install dependencies:

```bash
npm install
```

### Development

Start the development server:

```bash
npm run dev
```

Your application will be available at [http://localhost:5173](http://localhost:5173).

## Usage

- **Upload Resume:** Click the "Upload Resume" button to add your resume and receive instant feedback.
- **Profile & Logout:** Access your profile and logout options via the profile icon next to the upload button.
- **Resume Management:** View, review, and delete your uploaded resumes from the dashboard.

## Project Structure

```
├── app/
│   ├── components/
│   │   └── Navbar.tsx         # Navigation bar with profile and upload button
│   │   └── ResumeCard.tsx     # Resume display card
│   ├── routes/
│   │   └── home.tsx           # Main dashboard page
│   │   └── upload.tsx         # Resume upload page
│   └── lib/
│       └── puter.ts           # Puter integration and Zustand store
├── public/
│   └── images/                # Static images (background, loading GIF, etc.)
├── README.md
├── package.json
├── tailwind.config.js
```

## Puter Integration

See [`app/lib/puter.ts`](app/lib/puter.ts) for full API details.  
The Zustand store wraps Puter’s API for authentication, file storage, AI feedback, and key-value operations.

## Styling

This project uses [Tailwind CSS](https://tailwindcss.com/) for rapid and responsive UI development.  
You can customize styles in `tailwind.config.js`.

## Deployment

### Docker

Build and run with Docker:

```bash
docker build -t resume-analyser .
docker run -p 3000:3000 resume-analyser
```

### Manual Deployment

Deploy the output of `npm run build` to your preferred Node hosting platform.

## Authentication

- Users must be authenticated to access the dashboard and upload resumes.
- Profile icon displays the authenticated user's name and provides a logout option.

## Contributing

Feel free to fork and contribute! Pull requests are welcome.

---

Built with ❤️ using React, React Router, TailwindCSS, and Puter.
