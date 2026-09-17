# What a concept. — portfolio site

A static, dependency-free rebuild of the Base44 portfolio site (Games / Artworks / CV / Contact), ready to host on GitHub Pages.

## Structure

```
index.html      Games page (homepage)
artworks.html   Artworks gallery
cv.html         CV / experience
contact.html    Contact page + form
css/style.css   All styling
js/nav.js       Mobile menu toggle
images/         Put your artwork here
```

## Add your images

This clone ships with placeholder frames where your artwork goes, since I couldn't pull the original images from the Base44 app. For each placeholder:

1. Drop your image file into `images/` (e.g. `images/horned-monster.jpg`).
2. In the relevant `.html` file, find the commented-out `<img>` tag inside the `.frame` or `.frame-empty` div and uncomment it, or replace the placeholder `<p class="placeholder-label">` with an `<img src="images/your-file.jpg" alt="...">`.

## Contact form

The form currently doesn't submit anywhere (`action="#"`). To make it work without a backend, the easiest options are:
- [Formspree](https://formspree.io) — free tier, just change `action` to your Formspree endpoint and keep `method="post"`.
- A `mailto:` link (already included as a fallback under "Direct").

## Deploy to GitHub Pages

1. Create a new repo (or use an existing one) and push these files to it.
2. In the repo, go to **Settings → Pages**.
3. Under "Build and deployment", set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Save — your site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

If you want it at the root of `https://<your-username>.github.io/`, name the repo `<your-username>.github.io`.

## Admin page

The original site had an "Admin" nav link, which was almost certainly Base44's built-in backend/CMS. A static HTML site has no backend, so that link and its functionality are left out here — if you need to edit content, just edit the HTML files directly (or wire up a headless CMS like Netlify CMS / Decap CMS later).
