# Imaginate website (static)

Static copy of the Imaginate creative agency site, mirrored from the WordPress
original and pruned of theme demo content. Plain HTML/CSS/JS - no build step,
no server code. Host it anywhere that serves static files.

## What's in here
- ~75 real pages: home, services, portfolio projects, showcases, cookie policy.
- Images and short background videos in `assets/`; theme files in `wp-content/`.
- Videos stay embedded from Vimeo/YouTube (nothing to host).
- Removed: theme demo pages and posts, duplicate "-2/-3" pages, the WooCommerce
  demo shop, blog demo posts, the search box, comment forms, and the dummy-copy
  pages that were never finished.

## Known open items (before go-live)
- Contact form: replaced with a mailto block (info@imaginate.uk / Raj 07999 888 557).
  A static host can't run the old WordPress form - pick a form service
  (e.g. Formspree/Web3Forms) or keep the email/phone block.
- Portfolio grids that spanned multiple pages show page 1 only.
- Social icons in the footer pointed at the (dead) imaginate.uk domain on the
  old site; they need real profile URLs.
- "Our Work" page intro still has placeholder text from the original site.

## Handover: move this repo to the Imaginate owner's GitHub
1. Repo owner: Settings -> General -> Danger Zone -> Transfer ownership,
   enter the new owner's GitHub username. They accept the email invite.
2. After transfer, GitHub Pages keeps working; the preview URL becomes
   <their-username>.github.io/imaginate/.

## Put it on imaginate.uk (or any domain) - DNS cutover
1. In this repo: Settings -> Pages -> Custom domain, enter `imaginate.uk`, save.
   (This adds a CNAME file - keep it.)
2. At the DNS provider (currently Cloudflare): point `imaginate.uk` with a
   CNAME record to `<username>.github.io` (or A records to GitHub's IPs
   185.199.108.153 / .109.153 / .110.153 / .111.153 for the apex).
3. Back in Settings -> Pages, tick "Enforce HTTPS" once the certificate issues.
Nothing is deleted by this; reverting DNS restores the old hosting.

## Preview
Served by GitHub Pages from the `main` branch root.
