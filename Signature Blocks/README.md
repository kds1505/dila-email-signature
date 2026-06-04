# Email Signatures — A Day in LA Tours

The Gmail email-signature HTML cards. The hosted images they load live in the **root of this
repo** (`../sig-*.png`), served via GitHub Pages.

## The signatures

Each is a self-contained HTML file — open it in a browser, select the white signature card, copy,
and paste into Gmail → Settings → See all settings → General → Signature.

| File | For |
|------|-----|
| [`email-signature-hosted.html`](email-signature-hosted.html) | Generic / customer-service signature (the original) |
| [`Kevin Silberman/`](Kevin%20Silberman/email-signature-kevin-silberman.html) | Kevin Silberman — President & General Counsel |
| [`Raman Rampal/`](Raman%20Rampal/email-signature-raman-rampal.html) | Raman Rampal — CEO |
| [`Alex Cook/`](Alex%20Cook/email-signature-alex-cook.html) | Alex Cook — Operations Manager |

`email-signature-hosted-spread.html` is a wider layout variant. `email-signature.html` is the old
version with images embedded as base64 — **don't use it** (Gmail re-compresses base64 on paste and
it looks pixelated on Retina). Both kept for reference.

To make a new person's signature, copy one of the person folders, then swap the name, title,
mobile (`tel:` link too), and email.

## Where the images are hosted

The signatures load their 7 images at **full resolution** from **GitHub Pages**, which keeps them
sharp (Gmail leaves real URLs alone instead of downsampling them).

- **Live base URL:** https://kds1505.github.io/dila-email-signature/
- **Image files + size table:** see the [repo root README](../README.md). The PNGs are
  `../sig-*.png`; their design sources are in [`source-art/`](source-art/).

### How to update a hosted image

1. Replace the file at the **repo root** (`../sig-<name>.png`), keeping the same filename.
2. From the repo root: `git add . && git commit -m "Update <image>" && git push`
3. It goes live at the same URL in ~1 minute. Signatures already pasted into Gmail update
   automatically — no need to re-paste (unless you change the HTML itself).

## Notes

- `adayinla.com` is only a 301 redirect to the real WordPress site `www.adayinlatours.com`.
  A redirect domain can't host files, which is why the images live on GitHub Pages instead.
- If you edit the HTML (text, links, layout), you must re-copy the card and re-paste it into Gmail.
- The phone number uses `white-space:nowrap` so it never splits across two lines on a narrow screen.
  The email · website line is likewise glued together so it stays on one line.
