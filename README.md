# Ramisa Rahman Shitu — portfolio and visual editor

A static, responsive portfolio designed for **GitHub Pages**, with Urbanist 600 typography, light/dark mode, a subtle Shape-Shifter mascot and editorial gradients.

## Publish to GitHub Pages

1. Extract this ZIP. Upload `index.html`, `styles.css`, `app.js`, `defaults.js`, `content.js`, `jszip.min.js`, and the `assets/` folder (when present) to the **root** of a GitHub repository.
2. Go to **Settings → Pages → Build and deployment → Deploy from a branch**. Select `main` and `/(root)`, then save.
3. Open the URL shown by GitHub Pages once deployed. On Android, use that same URL in Chrome.
4. Click **Edit site** on the published website. Make edits, then click **Publish ZIP**. Extract the new ZIP and replace your repository files (including `assets/`).

### Editors

- Home: customizable/reorderable sections, featured campaign projects, clean homepage article previews, gradient motion, font and mascot size, header profile image.
- Works: edit each work card's cover image/video, orientation, tile span, maximum width and height; add media to each case study.
- Perspective: choose a featured article; cover images/videos; create original articles; edit article text directly in the page; add 1–3 columns and text, images, videos and PDF elements with per-element style/size/position controls. Section ordering via up/down and dragging on desktop.
- Identity: upload your profile photo for the header and a PNG signature for the footer. In the site style dialog, change text, typography and background motion.

### File and browser behavior

- New media uploads are saved to this browser's **IndexedDB** and rendered in the current preview. **Publish ZIP includes the actual uploaded files**, with paths in `content.js`. No API key or server-side storage is required.
- Edits to text and layout are saved to browser localStorage as a draft. They are **not live on GitHub until the exported ZIP files are uploaded**.
- Publishing from the editor needs the website opened on `http://` or `https://`, because it reads the site source files to assemble the ZIP. GitHub Pages works, or you can run a local server: `python -m http.server 8000`, then open `http://localhost:8000`.
- DOCX import extracts basic paragraphs into editable text. It may not perfectly preserve tables/images. PDF import embeds the PDF as a viewable document, **not** editable extracted text. Legacy `.doc` needs conversion to `.docx`.
- Editing on a different browser or device: the published site's content and uploaded assets will display, but prior unsaved local draft changes are device-specific.
- Media previews require space in browser storage. Huge videos may exceed browser quota; use optimized files.
- Custom gradient pointer is desktop-only. Mobile and reduced-motion users get simpler interactions.
- Google Fonts needs an internet connection to load Urbanist; system sans-serif is the fallback.

## Contents

`index.html` page shell; `styles.css` responsive design; `app.js` visual editor and rendering; `defaults.js` baseline resume content; `content.js` published content; `jszip.min.js` ZIP packaging library; `assets/` media uploaded later.

## Version 8 updates
- Education navigation is now **Background**; old `#education` links redirect internally.
- Homepage Perspective preview is now a quiet three-item editorial strip with no black panel or heavy hover movement. Select its articles in Edit site → Select homepage articles.
- Perspective has a large featured-article presentation above a horizontal magazine-cover shelf. Choose the featured article from Edit site → Choose featured article & covers.
- Enlarged desktop content gutters and responsive Android spacing.
- Previous cute pastel Shape-Shifter restored with gently floating, blinking eyes (respects reduced motion).

**Note:** CSS changes may be cached by the browser; hard-refresh after uploading these files to GitHub.
