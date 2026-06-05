# Ben Jeffreys — XR portfolio site

A dark, XR-themed portfolio built as plain HTML/CSS. No build tools, no frameworks — two files you can open in any browser and edit in any text editor.

```
index.html      Homepage: hero, selected work (5 projects), about, contact
project.html    A reusable case-study page (currently the E1 Series Simulator)
assets/         (you create this) — put your images, videos and CV here
```

## 1. See it right now

Double-click `index.html`. It opens in your browser exactly as it will look online. Edit a file, save, refresh the tab — that's the whole loop.

## 2. Add your own media (the important part)

The site is built; the only thing missing is your work. Everywhere you need to add something, there's a `<!-- TODO -->` or `<!-- REPLACE -->` comment in the HTML telling you exactly what goes there.

Make a folder next to the HTML files called `assets`, drop your files in, then:

**A project thumbnail (homepage).** Find the card, e.g.:

```html
<div class="thumb">
  <span class="tag">AR · BROADCAST</span>
  <!-- REPLACE: <img src="assets/e1-cover.jpg" alt="E1 Series Simulator"> -->
  <i class="ph">◎</i>
</div>
```

Delete the `<i class="ph">…</i>` line and uncomment the image line:

```html
<div class="thumb">
  <span class="tag">AR · BROADCAST</span>
  <img src="assets/e1-cover.jpg" alt="E1 Series Simulator">
</div>
```

**A hero video (homepage or project page).** Use a short, muted, looping MP4 — it autoplays as a silent background. The exact snippet is already in the file as a comment; just uncomment it and point it at your file. Keep clips under ~10–15 MB so the page loads fast.

**Your CV.** Put the PDF in `assets/` and update the "Resume" link in the nav of `index.html`:
`<a href="assets/Ben-Jeffreys-CV.pdf">Resume</a>`

**LinkedIn.** Search the files for `LinkedIn` and replace the `#` with your profile URL (appears in the contact band and footer).

Image tips: export thumbnails around 1600px wide, JPG, compressed (TinyPNG or Squoosh). Dark sites are unforgiving of low-res or white-background screenshots, so favour clean, full-bleed captures.

## 3. Add more case-study pages

`project.html` is a template. To add a second project:

1. Copy `project.html` → `shatterfall.html`.
2. Edit the title, role metadata, text, and media.
3. On `index.html`, point that project's card at the new file: `href="shatterfall.html"`.

Repeat per project. The strongest case studies state your **specific role** and **what you designed**, not just the studio name — recruiters for design roles look for that first.

## 4. Put it online (free) — GitHub Pages

This is the recommended host: free, fast, permanent, and a custom domain is optional.

1. Create a free account at github.com.
2. Make a new **public** repository named `your-username.github.io`.
3. Upload `index.html`, `project.html`, and your `assets/` folder (drag-and-drop works in the browser — "Add file → Upload files").
4. Go to the repo's **Settings → Pages**, set Source to "Deploy from a branch", branch `main`, folder `/ (root)`, Save.
5. Wait ~1 minute. Your site is live at `https://your-username.github.io`.

**Custom domain (optional, ~£10/yr):** buy a domain (Namecheap, Cloudflare, etc.), then in Settings → Pages add it under "Custom domain" and follow the DNS instructions. Update the `og:url` line in `index.html` to match.

### Alternative: Framer (no code)
If you'd rather edit visually and never touch HTML again, rebuild this layout in Framer (framer.com) — free tier, great with video, drag-and-drop. Use this site as your reference design. Trade-off vs. GitHub Pages: easier editing, but a Framer badge/paid tier for a custom domain.

## 5. Quick polish checklist before you share it

- [ ] Real thumbnails on all 5 project cards
- [ ] At least one full case study fully written (E1 or Helmsman are your strongest)
- [ ] Hero showreel or a strong hero still
- [ ] CV PDF linked
- [ ] LinkedIn + ArtStation links filled in
- [ ] A 1200×630 `assets/social-preview.jpg` for nice link previews (update `og:image`)
- [ ] Open it on your phone and check it reads well

Everything else — colours, fonts, spacing — lives in the `<style>` block at the top of each file. The two accent colours are `--teal` and `--violet`; change those two values to re-skin the whole site.
