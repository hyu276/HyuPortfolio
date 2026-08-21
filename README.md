# Hyu Portfolio

Static CV / portfolio project backed by Supabase.

## Structure

- `index.html` — public portfolio/CV frontend.
- `portfolio-admin/` — GitHub Pages admin dashboard for editing live portfolio data.
- `vercel.json` — Vercel static-site configuration.
- `.vercelignore` — prevents the admin dashboard and backend notes from being included in Vercel deployments.
- `supabase/schema.sql` — portfolio-specific Supabase schema reference.

## Runtime architecture

Public frontend: Vercel

Admin dashboard: GitHub Pages

Backend and content data: Supabase project `zkrhwqgmynbbmoktokdq`

Portfolio tables used by the current application:

- `portfolio_profile`
- `portfolio_settings`
- `portfolio_highlights`
- `portfolio_projects`
- `portfolio_skills`
- `portfolio_education`
- `portfolio_sections`
- `portfolio_section_items`

The browser uses a Supabase publishable key. Secret/service-role keys must never be committed to this repository.

## Admin features

The dashboard supports profile/settings editing, dynamic timeline sections, add/edit/delete, hide/show, clone, live CV preview, and local draft autosave for accidental modal exits.

## Deployment

Vercel should deploy the repository root. `.vercelignore` excludes `portfolio-admin/` and `supabase/` from the public Vercel deployment.

GitHub Pages can serve the admin dashboard at `/portfolio-admin/` from the `main` branch.
