# Bonjour Cafe ☕

Bonjour Cafe landing page migrated to a **Static Site Generator** setup with a **Git-based CMS**.

## Live Demo

- Website: [https://bonjourcafe.me](https://bonjourcafe.me)

## Lab 4 Stack

- **SSG:** [Eleventy (11ty)](https://www.11ty.dev/)
- **Git CMS:** [Decap CMS](https://decapcms.org/)
- **CSS framework:** [Tailwind CSS](https://tailwindcss.com/) (kept from Lab 3)

## What Is Editable via CMS

Almost all homepage content is editable through Decap CMS, including:

- meta title and description
- brand name and navigation links
- hero texts and buttons
- mobile banner text
- about section title, image, paragraphs, and stats
- menu cards (title, description, price, image)
- testimonials (text, author, role, avatar)
- locations (name, address, image)
- promo section text and CTA
- footer links and social links
- mascot bubble message and mobile sticky CTA

CMS content source file: `src/_data/site.json`

## Project Structure

```text
.
├── .eleventy.js
├── package.json
├── src/
│   ├── _data/
│   │   └── site.json
│   ├── _includes/
│   │   └── layouts/
│   │       └── base.njk
│   ├── admin/
│   │   ├── config.yml
│   │   └── index.html
│   ├── img/
│   ├── index.njk
│   └── style.css
└── _site/ (generated)
```

## Development

```bash
npm install
npm run dev
```

Local site: `http://localhost:8080`

Build static output:

```bash
npm run build
```

Generated site is in `_site/`.

## CMS Usage (Decap)

CMS admin route after running locally or deploying:

- `/admin/`

Config file:

- `src/admin/config.yml`

Notes:

- `local_backend: true` is enabled for local CMS workflow.
- Production backend is set to `git-gateway` for Netlify-compatible Git editing.

## Deployment (Recommended: Netlify)

To satisfy live deployment + Git CMS editing:

1. Connect repo to Netlify.
2. Build command: `npm run build`
3. Publish directory: `_site`
4. In Netlify, enable Identity.
5. Enable Git Gateway.
6. Invite users for CMS access (Identity).
7. Open `https://<your-site>.netlify.app/admin/` to edit content.

## Previous Visuals

Screenshots from earlier labs are still available in `screenshots/`.
