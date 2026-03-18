# CrazyMoe Scanner Ultimate v13

This is the merged final repo-ready build.

What I kept from Claude because it is genuinely stronger:
- isolated event wiring so one missing element does not break scan/navigation
- correct UPC regex
- scan works before any Supabase setup
- Promise.allSettled-style server lookup so one source failing does not kill the rest
- settings accordion
- restored install prompt
- full 5-step flow

What I kept from the better parts of the Grok notes:
- free-first lookup posture
- cleaner no-result messaging
- luxury visual direction

What stayed from our stronger architecture:
- server-side Netlify Function lookup
- storage-backed Supabase save
- image-first result cards
- draft save/restore
- review screen before save

Deploy:
1. Create a GitHub repo
2. Upload ALL contents of this folder (preserve netlify/functions/lookup.js)
3. Netlify -> Import from Git -> pick repo -> Deploy

Optional Netlify environment variable:
- BARCODE_LOOKUP_KEY = your Barcode Lookup API key

Important:
- Scan and lookup should work before Supabase is filled in
- Supabase is only needed at final save
- Do not use Netlify drag-and-drop for this build
