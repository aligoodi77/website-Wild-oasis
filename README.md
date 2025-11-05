# README.md — The Wild Oasis

## Project

**The Wild Oasis** — A Next.js website for the Jonas project. This repo contains the frontend built with Next.js (React) and related assets.

---

## Tech stack

- Next.js (React)
- Node.js
- Vercel for deployment (recommended)
- Tailwind CSS (optional)
- Supabase / MongoDB / any API for backend (if used)

---

## Features

- SSR / SSG pages with Next.js
- Responsive layout
- Image optimization using Next/Image
- Environment-driven API endpoints

---

## Quick start (local)

1. Clone the repository:

```bash
git clone <your-repo-url>
cd the-wild-oasis
```

2. Install dependencies:

```bash
npm install
# or
# pnpm install
# or
# yarn install
```

3. Create an `.env.local` file in the project root and add required environment variables (example below).

4. Run the dev server:

```bash
npm run dev
# or
# pnpm dev
# or
# yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## Environment variables (example)

Create `.env.local` and add variables used by your project. **DO NOT** commit `.env.local` to git.

```env
NEXT_PUBLIC_API_URL=https://example.com/api
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
DATABASE_URL=
NEXTAUTH_URL=http://localhost:3000
# any other keys your app needs
```

---

## Scripts

- `dev` — starts Next.js in development mode
- `build` — builds the production app
- `start` — runs the production build
- `lint` — runs linter (if configured)

Example in `package.json`:

```json
"scripts": {
  "dev": "next dev",
  "build": "next build",
  "start": "next start",
  "lint": "next lint"
}
```

---

## Deployment

Recommended: Vercel (automatic with GitHub). Make sure to set the same environment variables in Vercel dashboard.

Steps:

1. Push repo to GitHub.
2. Connect the repository to Vercel.
3. Configure environment variables in the Vercel project settings.
4. Deploy.

If using other providers (Netlify, Render), follow their Next.js guides.

---

## Folder structure (suggested)

```
/
├─ public/            # static assets
├─ src/
│  ├─ app/            # Next.js app router (or pages/ if using pages router)
│  ├─ components/
│  ├─ styles/
│  └─ lib/             # helpers, api clients
├─ .env.local
├─ package.json
└─ README.md
```

---

## Common gotchas & tips

- If you see CORS errors from your backend, configure `Access-Control-Allow-Origin` on the backend or proxy requests during development.
- Keep secrets out of git — always add `.env*` to `.gitignore`.
- If deploying to Vercel and using SSR with external APIs, ensure those APIs are accessible from Vercel.

---

## Contributing

1. Fork the repo
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Commit your changes: `git commit -m "feat: add ..."`
4. Push and open a pull request

---

## License

Add license information here (MIT, Apache-2.0, etc.)

---

---
