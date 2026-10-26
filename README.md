# QvalFocus

A staffing and consulting services website: dedicated pages for staffing, consulting and managed services, plus a job portal where candidates can search and filter jobs and apply with file uploads, case studies, separate contact flows for clients and candidates, and a newsletter signup.

## What it does

- Multi-service platform: staffing, consulting and managed services pages, with content for six industry verticals
- Job portal: job search with filtering, featured listings and applications with file upload support
- Case studies showcasing success stories
- Separate contact forms for client and candidate inquiries, plus newsletter subscriptions
- Dark/light mode and a glassmorphism design system (Inter for UI, Playfair Display for headlines)

## Tech stack

- Frontend: React 18 + TypeScript + Vite, Wouter routing, Tailwind CSS, shadcn/ui on Radix UI primitives, TanStack Query, React Hook Form + Zod
- Backend: Express.js + TypeScript, REST API, PostgreSQL session storage via connect-pg-simple
- Data: PostgreSQL (Neon serverless) with Drizzle ORM and Drizzle Kit migrations; schema covers users, job postings, job applications, contact forms, newsletter subscriptions and case studies
- Also present: a Supabase edge function under `supabase/functions/delete-job`

## How to run

```bash
npm install
npm run dev       # vite
npm run build     # vite build
npm start         # tsx server/index.ts
npm run db:push   # drizzle-kit push
```

## Project structure

```
client/            # React frontend
server/            # Express backend (server/index.ts entry point)
shared/            # Shared code between client and server
supabase/functions/delete-job/  # Supabase edge function
replit.md          # Project overview and architecture notes
attached_assets/   # Static assets
```
