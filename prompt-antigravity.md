Project: "Light Green Bar & Grill" — digital QR menu
Stack: Single index.html file, vanilla HTML/CSS/JS, no build step, no frameworks.
Deployed on Vercel.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
FIX REQUIRED — image asset paths
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

The current index.html references image assets using paths with spaces in the
folder name. This is fragile in git and will break on Vercel.

Current paths used in index.html:
  res/Download%202026-04-05T20-24-10-102Z/logo.png
  res/Download%202026-04-05T20-24-10-102Z/ejemplo-plato.png

Required actions:
  1. Copy (or move) the two files to clean paths:
       res/logo.png
       res/placeholder.png

  2. Update ALL src attributes in index.html:
       res/Download%202026-04-05T20-24-10-102Z/logo.png  →  res/logo.png
       res/Download%202026-04-05T20-24-10-102Z/ejemplo-plato.png  →  res/placeholder.png

  3. Do not change anything else in index.html.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
CURRENT STATE (for reference)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
- Fixed header (196px): logo image + EN|ES language toggle (placeholder)
- Fixed tab bar (58px): GRILL | TAPAS | DRINKS
- Live Music floating balloon (top-left, gold, 68px): opens hidden music panel
- Disclaimer banner: "Grill menu available from 6PM..."
- Scrollable main: section headers (Georgia serif + ✦ ornament) + menu cards
- FAB buttons (left side): WhatsApp + Google Maps
- Back-to-top button (↑), bottom-right

Brand palette (CSS variables — never use hardcoded colors):
  --green-dark: #141f14
  --green-mid:  #2b5226
  --gold:       #c9a84c
  --gold-light: #e8c97a
  --cream:      #f4efe5
