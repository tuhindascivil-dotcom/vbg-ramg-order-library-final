# Permanent storage setup
1. Create a Supabase project.
2. Run supabase_schema.sql in SQL Editor.
3. The app will create the private `vbg-ramg-orders` bucket automatically.
4. In Render add SUPABASE_URL and SUPABASE_SERVICE_ROLE_KEY, plus ADMIN_USER, ADMIN_PASSWORD and SESSION_SECRET.
5. Keep the service_role key only in Render environment variables; never put it in GitHub.
PDFs are stored in Supabase Storage and metadata in Supabase Postgres, so Render restarts do not erase uploaded files.
