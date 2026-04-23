# Montecito Electric

Modern, responsive redesign of **montecitoelectric.com** — a family-run, C-10 licensed electrical contractor serving Santa Barbara and Montecito, CA since 1985.

---

## Overview

This is a static, dependency-free website built with hand-written HTML, CSS, and a small vanilla-JS enhancement layer. It is designed to be:

- **Fast** — no framework, no build step, no tracking
- **Responsive** — fluid layouts from 320px to 1920px+
- **Accessible** — semantic HTML, keyboard-navigable, `prefers-reduced-motion` respected
- **Editorial in tone** — coastal California design language (deep navy + golden-hour amber on warm ivory), suited to Montecito's clientele

## Pages

| File             | Purpose                                                |
| ---------------- | ------------------------------------------------------ |
| `index.html`     | Homepage — hero, services overview, about, testimonial |
| `services.html`  | Detailed service catalogue with deep-link anchors      |
| `about.html`     | Company story, values, service area                    |
| `contact.html`   | Contact info, service-request form, map                |

## File structure

```
.
├── index.html
├── services.html
├── about.html
├── contact.html
├── README.md
└── assets/
    ├── css/
    │   └── styles.css       # complete design system
    ├── js/
    │   └── main.js          # mobile nav, scroll reveals, form handler
    └── images/              # (place logo.png here if using original logo)
```

## Local preview

Any static server will do:

```bash
# Python
python3 -m http.server 8000

# Node
npx serve .
```

Then open http://localhost:8000.

## Deployment

Because the site is 100% static HTML/CSS/JS, it can be deployed anywhere:

- **GitHub Pages** — push to `main`, enable Pages in repo settings
- **Netlify / Vercel / Cloudflare Pages** — connect repo, no build step needed
- **Traditional shared hosting** — drag the folder into your webroot

## Customization

### Using the original logo

The header currently uses a clean SVG wordmark. If you'd prefer to use the original PNG logo from the legacy site:

1. Save the original logo into `assets/images/logo.png`
2. In each HTML file, find the `<span class="brand-mark">` and `<span class="brand-text">` block inside the header, and replace it with:

```html
<img src="assets/images/logo.png" alt="Montecito Electric" style="height:56px; width:auto">
```

### Changing colors / fonts

All design tokens are defined as CSS custom properties at the top of `assets/css/styles.css` under `:root`. Edit those values and every page updates.

### Contact form

The contact form currently uses a `mailto:` fallback (opens the visitor's email client). To send submissions to a real inbox without a backend, replace the form handler in `assets/js/main.js` with a form service like **Formspree**, **Basin**, or **Netlify Forms**.

## Credits

- Type: [Fraunces](https://fonts.google.com/specimen/Fraunces) (display) + [Inter](https://fonts.google.com/specimen/Inter) (body) via Google Fonts
- Icons: custom inline SVG (Lucide-style)
- Map: Google Maps embed

## License

Source code © 2026 Montecito Electric. All rights reserved.
C-10 State License No. 485353.
