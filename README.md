# RelayDesk Supabase Setup

1. In Supabase, open **SQL Editor**, paste `supabase-schema.sql`, and click **Run**.
2. Open **Authentication → Providers → Email** and turn off email confirmation.
3. Upload `index.html`, `styles.css`, `app.js`, `config.js`, and `.nojekyll` to the root of the GitHub Pages repository.
4. Open RelayDesk and create the administrator account using the name `Imran Sohail`.
5. Return to SQL Editor and run:

```sql
update public.profiles
set is_admin = true
where lower(display_name) = lower('Imran Sohail');
```

Never place a Supabase secret key or service-role key in these website files.
