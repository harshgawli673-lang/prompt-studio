# Hawk AI

Hawk AI is a mobile-friendly prompt generator with email/password accounts.

## Use the live app

Open [Hawk AI](https://harshgawli673-lang.github.io/prompt-studio/) on desktop or mobile. Create an account with your name, email, and password. Email confirmation is required before the first login.

The optional marketing checkbox is unchecked by default. A person's name, email, and consent choice are saved in the private `public.leads` table. Account passwords are managed by Supabase Auth and are never stored in this website's files.

## One-time Supabase setup

For email confirmation links to return to the live GitHub Pages site, set these values in the Supabase project dashboard:

1. Open **Authentication → URL Configuration**.
2. Set **Site URL** to `https://harshgawli673-lang.github.io/prompt-studio/`.
3. Add that same address to **Redirect URLs**, including the trailing slash.

Then check the signup email confirmation template and send a test signup. Leads can be viewed in **Table Editor → public → leads**. The `marketing_opt_in` column records the checkbox choice.

## Security

The page uses a Supabase publishable key, which is intended for browser use. The leads table has Row Level Security enabled. Signed-in users can read only their own record; only the signup trigger creates records. Do not place a Supabase secret or service-role key in this site.

## Prompt generator

Describe an idea, choose a task and tone (or let Hawk AI choose), and optionally add an audience, format, or constraints. Generate and copy the result into the AI service you want to use. The generator itself does not send prompt text to Supabase.