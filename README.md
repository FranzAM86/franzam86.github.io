# Francisco Miguel Alatriste Montiel — personal website

A minimal static one-page website built with plain HTML and CSS for GitHub Pages. It has no framework, build step or external dependency other than Google Fonts.

## File structure

```text
index.html          Page content, metadata and mobile menu script
css/styles.css      Design tokens, layout, responsive styles and accessibility states
assets/             SVG monogram, favicon, hero illustration and icon sprite
cv/                 Placeholder PDF for the curriculum vitae
```

## Placeholders to replace

The visible brackets are intentional. Replace the following before considering the site complete:

1. `index.html`, Research & Projects: `[Short description of the project, data sources and method used.]` on desktop and `[Short description]` on mobile.
2. `index.html`, Research & Projects: `[Article title], [Journal], [Year].`
3. `index.html`, Research & Projects: the desktop `Read article` link currently points to `#research`; replace it with the publication URL.
4. `index.html`, CV & Contact: `[professional email]` and its `mailto:%5Bprofessional-email%5D` link; replace both with the professional email address.
5. `cv/francisco-miguel-alatriste-montiel-cv.pdf`: this is a placeholder PDF. Replace it with the real CV, either keeping the same filename or updating the PDF link in `index.html`.

No publication, project description, email address or CV content has been invented.

## Editing content

- Edit text directly in `index.html`. The sections are ordered as About, Research & Projects, Data & Methods, and CV & Contact.
- Text marked with `desktop-copy` and `mobile-copy` is viewport-specific, following the two mockups; update both variants when editing those passages.
- Keep anchor IDs (`about`, `research`, `methods` and `contact`) unchanged unless the navigation links are updated too.
- Method icons use the sprite in `assets/icons.svg`; for example, `<use href="assets/icons.svg#code"></use>`.
- Colours, typography and reusable values are defined as CSS custom properties in `:root` at the top of `css/styles.css`.
- The mobile breakpoint is `767px`, so the desktop rules apply from approximately `768px` upwards.
- The only JavaScript is the small inline mobile-menu toggle at the end of `index.html`.

## Publishing on GitHub Pages

1. Ensure the repository is named `franzam86.github.io` and is public.
2. Commit these files to the `main` branch at the repository root.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and the `/ (root)` folder, then save.
6. GitHub will publish the site at `https://franzam86.github.io/`. The first deployment can take a few minutes.

Because this is a user/organization Pages site in a repository named `<username>.github.io`, pushing to `main` is normally enough after Pages is enabled; there is no build command or output directory to configure.
