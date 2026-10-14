# Inexo Solutions website

Website for Inexo Solutions: IT advice, automation, AI tools, apps/websites and content/video for small businesses. Site language: Dutch.

Static HTML/CSS, no build step. Hosted on Netlify; every push to `main` goes live automatically.

## Pages

| File | Page | Content |
|---|---|---|
| `index.html` | Home | Hero, services overview, 4-step way of working |
| `diensten.html` | Diensten | The five services with examples |
| `over.html` | Over mij | Short introduction of Timo |
| `contact.html` | Contact | Contact form (Netlify Forms) |
| `bedankt.html` | Bedankt | Shown after sending the form |

Services, in this order: IT-advies, Automatisering, AI-tools, Apps en websites, Content en video.

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

**Type:** Bricolage Grotesque for headings, Instrument Sans for body text (Google Fonts).

**Signature element:** the large `<` … `/>` brackets around the homepage hero, echoing the logo. Use this motif only there; keep the rest calm.

**Layout rules**
- Left-aligned content, max width 68rem.
- Services as a list with dividers, not cards.
- Numbers only where there is a real sequence (the 4 steps).
- Short copy: one idea per sentence, no jargon.
- Works on mobile; visible keyboard focus.

## Structure

```
index.html, diensten.html, over.html, contact.html, bedankt.html
assets/styles.css   shared styles and colour tokens
assets/logo.svg     logo and favicon
netlify.toml        Netlify settings
```

## To do

- Check and finalise the copy, especially "Over mij".
- Contact: Netlify → Forms → enable form detection and set email notifications.
- Add a custom domain.
- Before going live: remove the noindex block from `netlify.toml`.

## Later

- Client portal: a separate web app (own repo) where clients log in to stay in touch and discuss projects. Likely Netlify Identity or Supabase for login and data.
