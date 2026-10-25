# Hawk AI

Hawk AI is a mobile-friendly prompt generator with secure email/password accounts.

## Open the app

Visit [Hawk AI](https://harshgawli673-lang.github.io/prompt-studio/) on desktop or mobile. Create an account with your name, email, and password. Confirm the email address before the first login.

The optional marketing checkbox is unchecked by default. A person's name, email, and consent choice are saved in the private `public.leads` table. Account passwords are managed by Supabase Auth and are never stored in this website's files.

## Leads and privacy

View leads in the Supabase dashboard under **Table Editor → public → leads**. The `marketing_opt_in` column records the checkbox choice. Row Level Security is enabled; users can read only their own lead record, and the signup trigger creates each record.

The Supabase Site URL and allowed Redirect URL are already configured for the live GitHub Pages address. Email confirmation and password reset links return to Hawk AI.

## Security

The page uses a Supabase publishable key intended for browser use. Never place a Supabase secret or service-role key in this site. Prompt text stays in the browser and is not sent to Supabase.

## Prompt generator

Describe an idea, choose a task and tone (or let Hawk AI choose), and optionally add an audience, format, or constraints. Generate and copy the result into the AI service you want to use.