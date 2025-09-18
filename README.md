RLS Guard Dog – Mini Project Solution


 Goal
 A secure system with Supabase RLS, Next.js, and MongoDB where:
 • Students → see only their own records.
 • Teachers → manage records for their classes.
 • Head Teachers → see all records in the school.
 • An Edge Function calculates class averages → saved in MongoDB.


 
 Tech Stack
 • Supabase → Auth, DB, RLS policies
 • Next.js → Frontend & API routes
 • MongoDB Atlas → Stores class averages
 • Supabase Edge Function → Calculates averages

 
 Structure
 docs/solution.docx – Solution write-up
 sql/ – Schema, policies, seed data
 nextjs/ – Next.js app
 edge-functions/ – Class average function

 
 Setup
 1 Supabase → Run sql/policies.sql + sql/seed.sql (replace UUIDs).
 2 MongoDB → Add connection string in .env.local.
 3 Next.js → cd nextjs → npm install → npm run dev (Deploy on Vercel).
 4 Edge Function → Deploy class-average.js to Supabase.

 
 Environment
 NEXT_PUBLIC_SUPABASE_URL=...
 NEXT_PUBLIC_SUPABASE_ANON_KEY=...
 SUPABASE_SERVICE_ROLE_KEY=...
 MONGODB_URI=...
 MONGODB_DB=rls_guard
 EDGE_FUNCTION_URL=...

 
 Testing
 • Student → sees own progress.
 • Teacher → sees class progress.
• Head Teacher → sees all progress.
