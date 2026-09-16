# Helen & Asnat

A standalone art portfolio prepared for GitHub Pages. No Wix services, external fonts, paid plugins, or build step are required.

## Publish

1. Put these files in the root of the chosen GitHub repository.
2. Open Settings → Pages. Select **Deploy from a branch**, the `main` branch and `/(root)`.
3. Check the GitHub Pages preview before connecting the existing domain.

A public repository supports GitHub Pages on GitHub Free. Private repository Pages availability depends on your GitHub plan.

## Connect the Webgate domain

After the preview is approved:

1. Verify ownership of `helen-and-asnat.com` in your GitHub account's Pages settings, using the TXT record GitHub supplies.
2. In the repository's Pages settings, save `www.helen-and-asnat.com` as the custom domain.
3. At the authoritative DNS provider (Webgate if it hosts your DNS), replace the `www` website record with a CNAME pointing to `YOUR-GITHUB-USERNAME.github.io`. Do not include the repository name.
4. Replace the apex website A records with these GitHub Pages addresses:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153
5. Review any existing apex AAAA records so they do not continue sending visitors to Wix. Preserve email-related MX and TXT records and unrelated subdomains.
6. Enable Enforce HTTPS after GitHub issues the certificate. Verify both root and www addresses, page links, image galleries, email and phone links.
7. Once the replacement works on the domain, cancel only the Wix website subscription. Keep the domain registration renewed at Webgate.

Official guidance: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Editing

Each page is an ordinary `index.html` file. Edit text directly in GitHub's file editor. Upload new artwork into `assets/`, then copy an existing `figure` in the relevant gallery page and update the image path, description and number. The image viewer discovers gallery images automatically.

`style.css` controls the shared appearance. `gallery.js` controls the keyboard-accessible image viewer. Images use WebP to reduce transfer size and are stored with the website.

## Content preserved

The published Wix sitemap's 10 routes are included, with folder-based URLs. GitHub Pages redirects ordinary directory requests to a trailing slash. Artist statements and Doron Polak's essay retain the original wording. Exhibition entries span 2005–2013 as on the source website. The statement mentions Jerusalem; the contact page lists Herzliya. Please confirm whether the historical statement should be updated.

The complete Wix galleries are preserved: 52 works on iron, 14 sculptures, and 24 material details, plus the exhibition photographs. Original titles, descriptions, materials and dimensions are displayed on each gallery card and in the enlarged viewer. `artworks.json` records the source metadata and local image mapping. Work Sans ExtraLight is hosted locally and uses the original site’s bold styling. The unused old home page remains at `copy-of-home-check-1/` to preserve incoming links.

## Validation

Local HTTP preview, page and asset existence checks, and JavaScript syntax validation were performed. Automated visual browser testing was unavailable in this environment; review the preview on desktop and mobile before switching the domain.

## Approved design

The homepage combines the introduction beside a large artwork with all 52 works below. All Works on iron links lead to the homepage; the old route redirects there. `preview.css` contains the approved layout refinements and is required in production.
