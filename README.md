# ASCEND Academy Website

A simple, static (with light interactivity) website for ASCEND Academy, a 501(c)(3) nonprofit teaching PSAT 8/9 prep and machine learning to younger and underrepresented students.

## Structure

```
/
├── index.html              Homepage
├── programs.html           PSAT 8/9 + ML program details
├── about.html               Mission, story, team
├── get-involved.html        Apply / Volunteer / Donate
├── contact.html              Contact form + FAQ
└── assets/
    ├── css/style.css         All site styling
    └── js/main.js             Nav toggle, scroll reveals, FAQ accordion, form handling
```

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `ascend-academy-site`).
2. Push these files to the repository root (or to a `docs/` folder — see settings below).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment," set **Source** to "Deploy from a branch."
5. Choose the `main` branch and the `/ (root)` folder, then click **Save**.
6. After a minute or two, your site will be live at:
   `https://<your-username>.github.io/<repo-name>/`

### Using a custom domain (optional)

In **Settings → Pages**, add your custom domain (e.g. `ascendacademy.org`) under "Custom domain." You'll need to add a `CNAME` record (for a subdomain) or `A` records (for an apex domain) at your domain registrar pointing to GitHub's Pages servers. GitHub will show you exact instructions once you enter your domain.

## What's placeholder and needs to be replaced

- **Text content**: mission copy, bios, testimonial, EIN number — all placeholder, written to be easy to swap.
- **Forms**: the student application, volunteer, and contact forms currently just show a success message locally. To receive real submissions, connect them to a form backend like [Formspree](https://formspree.io), [Getform](https://getform.io), or a Google Form embed — GitHub Pages can't run server-side code, so a form needs an external service to actually deliver submissions to your inbox.
- **Donate button**: links to `#` — connect it to your actual donation platform (Givebutter, Stripe Payment Links, PayPal Giving Fund, etc).
- **Team photos**: currently initials placeholders in `.person-photo` — replace with real headshots.
- **Email address**: `hello@ascendacademy.org` is a placeholder used throughout.

## Customizing

- **Colors**: all defined as CSS variables at the top of `assets/css/style.css` (`:root` block) — change `--blue`, `--accent`, etc. in one place to re-theme the whole site.
- **Fonts**: Fraunces (headings) + Inter (body) + IBM Plex Mono (labels/stats), loaded from Google Fonts in each page's `<head>`.
- **Adding a page**: copy any existing page, update the `<title>`, breadcrumb, and nav `active` class, and update the footer/nav links on the *other* pages to include the new one.

## Local preview

No build step required. Open `index.html` directly in a browser, or run a simple local server from the project root:

```
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
