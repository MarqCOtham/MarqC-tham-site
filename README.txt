MARQCØTHAM — DEPLOY
Static site, no build step. Upload everything in this folder. Publish directory = this folder.

FILES
index.html            the site (all artwork is inside it)
404.html              "Signal lost" page for bad URLs (Netlify / Cloudflare Pages / GitHub Pages / Vercel use it automatically)
favicon.svg, apple-touch-icon.png   browser tab + phone home-screen icon
og-image.jpg          1200x630 link-preview image

BEFORE YOU GO LIVE (in index.html, search for "SITE.contact" near the top of the <script>)
1. contact.formAction is already set to your Formspree form (https://formspree.io/f/xvkgejpk). After deploying, submit one real test from each form and check your Formspree inbox.
   contact.publicEmail = optional; shows a small Contact line
2. Add news: edit SITE.announcements (one line per announcement). Add a video: SITE.videos. Add a social account: SITE.socials.

AFTER YOU HAVE YOUR DOMAIN (e.g. https://marqcotham.com) paste inside <head> of index.html:
<link rel="canonical" href="https://marqcotham.com/">
<meta property="og:url" content="https://marqcotham.com/">
<meta property="og:image" content="https://marqcotham.com/og-image.jpg">
<meta name="twitter:image" content="https://marqcotham.com/og-image.jpg">
and change <meta name="twitter:card" content="summary"> to content="summary_large_image"

COUNTDOWN (About > Coming soon): SITE.countdown.target in index.html is set to 2026-10-10T00:00:00 (visitor's local time). Change it there if the release date or time changes.
