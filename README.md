# NextSkill Institute Platform

A responsive computer institute website starter with public pages, an admin workspace and a student portal.

## Included
- Public home, course catalogue, about, contact and admission enquiry pages
- Responsive layout for desktop, tablet and mobile
- Admin workspace: student records, admission enquiries, course catalogue, fee overview and attendance overview
- Student portal: course progress, timetable preview, fee summary and learning modules
- Supabase Auth client integration and PostgreSQL schema with Row Level Security
- Preview mode with sample records when Supabase is not configured

## Stack
React 18 · TypeScript · Vite · Tailwind CSS · Supabase · React Router · Lucide

## Run locally
```bash
npm install
cp .env.example .env
# Add VITE_SUPABASE_URL and VITE_SUPABASE_ANON_KEY
npm run dev
```

## Supabase setup
1. Create a Supabase project.
2. Run `supabase/schema.sql` in the SQL Editor.
3. Add the project URL and anon key to Vercel environment variables (or local `.env`).
4. Create an admin account through Supabase Auth, then promote it with the SQL statement at the bottom of the schema.
5. Create student accounts using Supabase Auth. Profiles are created automatically by the trigger.

Never expose a service-role key in the browser. The preview mode is only for UI evaluation; it is not persistent and must not be used for real student data.

## Routes
`/`, `/courses`, `/about`, `/admission`, `/contact`, `/login`, `/admin`, `/student`.

## Before production
Replace the demo institute name, contact details, address, images, course fees, affiliation and policies. Implement and test the remaining LMS workflows (exams, certificates, file storage, live classes and payment verification) before selling those as live capabilities.
