---
title: "Create a blog for free on github pages - using astro and github codespaces"
pubDate: 2026-03-06
description: "How to create a simple blog for free using github and astro."
---

Step 1 — Create a GitHub Codespace for Your Astro Blog

1. Go to GitHub
Open your GitHub account in the browser.

2. Create a new repository
Name it something like: my-new-awesome-blog

3. Add a file to the repository. An empty .gitignore is fine.

4. Click the + icon Create New and select Create New Codespace.
Select your my-new-awesome-blog as repository and click create codespace.

GitHub will open a full VS Code environment in your browser.

You now have:

- A terminal
- A file explorer
- A code editor
- Node.js preinstalled
- Git preconfigured

All running in the cloud.


🚀 Step 2 — Create Your Astro Project Inside Codespaces

Inside the Codespaces terminal, run:
npm create astro@latest

Astro will ask you a few questions:

✔ Project name
You can press Enter to use the current folder.

✔ Template
Choose: Blog

✔ TypeScript or JavaScript
Either is fine — TypeScript is recommended but optional.

✔ Install dependencies
Choose Yes.

✔ Initialize Git repo
Choose Yes (it’s already a repo, but Astro will detect that).

When it finishes, you’ll see your Astro project files appear in the Codespaces file explorer.

🚀 Step 3 — Run Your Blog in Codespaces
Still in the terminal: npm run dev
if you created a directory, make sure you are running the command inside that directory.

Codespaces will show a popup like:

“Your application is running on port 4321 — open in browser?”

Click Open in Browser.

You now have your Astro blog running live in a new tab.

You can edit files in Codespaces and the site updates instantly.

🚀 Step 4 — Add Your First Blog Post
In the file explorer, go to: src/content/blog/

Create a new file: my-first-post.md
or update the first-post.md that comes with the template.

Add something simple:
---
title: "My First AI Conversation"
pubDate: 2026-01-01
description: "Starting my Awesome blog with a simple conversation."
---

**Me:** Hello Astro  
**Astro:** Hello human, welcome to your new awesome blog.

More experiments coming soon.


Save it — the blog updates automatically.

🚀 Step 5 — Push Everything to GitHub
In the terminal:
git add .
git commit -m "Initial Astro blog"
git push


🚀 Step 6 — Deploy to GitHub Pages
Astro has a built‑in adapter for GitHub Pages.

Install it:
npm install @astrojs/github

Then open astro.config.mjs and update it:
import { defineConfig } from 'astro/config';
import github from '@astrojs/github';

export default defineConfig({
  site: 'https://yourusername.github.io/my-astro-blog',
  adapter: github(),
});


Now go to your GitHub repo:

Settings → Pages → Build and Deployment → GitHub Actions

GitHub will automatically detect Astro and deploy your site.

Your blog will appear at:
https://yourusername.github.io/my-new-awesome-blog

🎉 You now have a live Astro blog running from Codespaces.


🌱 What you can do next 

- Add more posts

- Customize the theme

- Add chat‑style components

- Add analytics

- Add a custom domain

- Add SEO integration

- Add a newsletter