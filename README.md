# Inexo Solutions website

Website for Inexo Solutions: IT advice, automation, custom tools, websites and content/video for small businesses. Site language: Dutch.

Static HTML/CSS, no build step. Hosted on Netlify; every push to `main` goes live automatically.

## Pages

| File | Page | Content |
|---|---|---|
| `index.html` | Home | Hero, services overview, automation example, 4-step way of working, call to action |
| `diensten.html` | Diensten | Per service: icon, who it's for, "Waar ik bij help" (examples of tasks, not a fixed package), an example. Anchors (`#automatisering` etc.) are linked from Home |
| `over.html` | Over mij | Short introduction of Timo |
| `contact.html` | Contact | Contact form (Netlify Forms) |
| `bedankt.html` | Bedankt | Shown after sending the form |
| `privacy.html` | Privacyverklaring | Privacy statement (contact form, Netlify, rights) |
| `404.html` | Not found | Shown by Netlify for unknown URLs |

Services, in this order: IT-advies, Automatisering, Tools op maat, Websites, Content en video.

## Design

**Logo:** the `<i>` code tag (`assets/logo.svg`). Blue brackets, dark "i".

**Colours** (defined in `assets/styles.css`):

| Name | Hex | Use |
|---|---|---|
| Paper | `#F5F7FB` | Page background |
| Surface | `#FFFFFF` | Alternate sections, form fields |
| Ink | `#172033` | Text, "i" in logo |
| Muted | `#5B6577` | Secondary text |
| Line | `#D6DDEA` | Dividers, borders |
| Blue | `#2D5BFF` | Brand colour, buttons, brackets |
| Blue tint | `#E8EEFF` | Icon backgrounds, automated steps |

**Type:** Bricolage Grotesque for headings, Instrument Sans for body text. Self-hosted in `assets/fonts` (no Google Fonts, better for privacy).

**Signature element:** the large `<` … `/>` brackets around the homepage hero, echoing the logo. Use this motif only there; keep the rest calm.

**Layout rules**
- Left-aligned content, max width 68rem.
- Services as a list with dividers, not cards. Each service has a line icon (inline SVG, blue).
- Numbers only where there is a real sequence (the 4 steps).
- Short copy: one idea per sentence, no jargon.
- Works on mobile; visible keyboard focus.

## Structure

```
index.html, diensten.html, over.html, contact.html, bedankt.html
assets/styles.css   shared styles and colour tokens
assets/logo.svg     logo and favicon
assets/og-image.png preview image for links shared on social media
assets/fonts/       self-hosted fonts and their licences
netlify.toml        Netlify settings
```

## To do

- Add a photo to "Over mij".
- Review the privacy statement (retention period: 12 months).
- Add a custom domain.
- Before going live: remove the noindex block from `netlify.toml`.

## Future additions and improvements

- Client portal: a separate web app (own repo) where clients log in to stay in touch and discuss projects. Likely Netlify Identity or Supabase for login and data.
