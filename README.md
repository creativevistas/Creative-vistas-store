# Creative Vistas Storefront

This repository is dedicated to the Creative Vistas digital storefront. **Theo's fundraiser is completely separate.**

The currently published storefront lives at https://creative-vistas-store.pages.dev/ and has been deployed to Cloudflare Pages using direct uploads. The latest approved source package is `creative-vistas-simplified-storefront.zip` from the ChatGPT conversation. It contains `index.html`, `styles.css`, `script.js`, and an `assets/` folder.

## GitHub → Cloudflare Pages setup

1. Add the **contents** of the latest storefront ZIP to the **root of this repository** so `index.html` is at the top level.
2. In Cloudflare Pages, create a **new Git-connected Pages project** linked to `creativevistas/Creative-vistas-store` (do not replace Theo's Pages project).
3. Use branch `main`, framework **None**, no build command, and output directory `/`.
4. Verify its preview URL; then migrate the desired domain/project name if needed.

Once connected, commits to `main` trigger Cloudflare deployments. Keep Stripe keys, secrets, and private customer data out of the repository.

Current checkout is disabled until Stripe is configured.
