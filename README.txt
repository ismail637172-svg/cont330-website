CONT-330 / CONT-340 WEBSITE BACKUP
==================================

Files:
- index.html        -> CONT-330 (ترميم وتشطيب الرياض) full site code
                       Live: https://brewpage.app/public/ejBrtDfNRA
                       Owner token: B7eJkq3kTzTbgFn9E7AtI59IKBdNl3sy
                       Tracking number: +966 55 533 7459 (0555337459)
                       GSC verification tag: bU_KQvYGBccsIvZMg--IW_4wUJar5h41vHctKu1Z6Os

- cont340_index.html -> CONT-340 (خطوط الإتقان للدهانات) full site code
                       Live: https://brewpage.app/public/gTsZptV9mo
                       Owner token: B7eXBjbLqqDJDpxsyYnYSmkEudhKaocL
                       Phone: +966 53 256 7274

IMPORTANT SETTINGS (index.html):
- All phone links use <bdi dir="ltr"> and tel:+966555337459 / wa.me/966555337459
- Full-page scroll animation uses 3 sprite sheets hosted on catbox.moe:
  https://files.catbox.moe/1eqjds.jpg
  https://files.catbox.moe/zxjbpv.jpg
  https://files.catbox.moe/4owb2m.jpg
  (300 frames, 30fps, mapped to whole-page scroll)
- Bilingual Arabic/English toggle (EN button in nav)
- SEO: meta keywords, canonical, OpenGraph, Twitter card,
  LocalBusiness JSON-LD, FAQPage JSON-LD, google-site-verification meta tag
- Hero + sections transparent so the scroll animation shows through

UPDATE COMMAND (CONT-330):
curl -s -X PUT "https://brewpage.app/api/html/public/ejBrtDfNRA" \
  -H "X-Owner-Token: B7eJkq3kTzTbgFn9E7AtI59IKBdNl3sy" \
  -H "Content-Type: text/html; charset=utf-8" \
  --data-binary @index.html

Saved: 2026-11-21

GITHUB (auto-deploy source)
===========================
Repo: https://github.com/ismail637172-svg/cont330-website
Branch: main
Local folder: /data/user/0/com.termux/files/home/.gemini/antigravity-cli/scratch/riyadh_leads/cont330_site

CLOUDFLARE PAGES AUTO-DEPLOY SETUP (one time)
=============================================
1. Open https://dash.cloudflare.com/?to=/:account/pages
2. Create project -> "Connect to Git" -> choose GitHub -> select repo: cont330-website
3. Build settings:
   - Framework preset: None
   - Build command: (leave empty)
   - Build output directory: /   (root - index.html is at repo root)
4. Deploy. Every git push to main auto-deploys.

TO UPDATE THE SITE LATER
========================
1. Edit index.html in the local folder (or on GitHub)
2. cd cont330_site && git add . && git commit -m "update" && git push
3. Cloudflare auto-deploys within ~30 seconds.

GSC VERIFICATION ON PAGES
=========================
- Use URL-prefix property with the pages.dev URL
- HTML file method: google0fe3b142e5b32fb1.html is at repo root -> served at https://<project>.pages.dev/google0fe3b142e5b32fb1.html
- Or HTML tag method: tag already in index.html <head>
