# Vehicle Approval Checklist (staff only)

Single `index.html` plus an `images/` folder (example collision and optimization screenshots). No build step.
Run locally with VS Code Live Server, `npm start`, or `python3 -m http.server 5600`.

## What's inside
- 70 checks across: submission pack, lore, optimization, collision, functionality, meta files, hierarchy, appearance, final approval.
- **handling.meta checker** — paste a submitted file; fixed / max / min fields are compared to the reference for the class (Off Road 4x4 and Commercial 6x6 for now) and the matching checklist items are filled in automatically.
- **Brand feature lookup** — tick each signature feature that has been altered.
- **Example screenshots** on the collision and optimization checks.
- Copy report / Print to PDF. Progress saves in the reviewer's own browser.

## Publish
Push this whole folder (keep `images/` next to `index.html`) to its **own** GitHub repo or a Netlify / Vercel / Cloudflare Pages project. Redeploying keeps the same URL.

## Keeping it staff-only
- The page is `noindex`, but anyone with the link can open it. Share the link only in a staff channel.
- Optional passcode: set `STAFF_PASSCODE` at the top of the script. It only stops casual visitors; the code is readable in page source.
- Real access control: Cloudflare Pages + Cloudflare Access, or Netlify password protection.

## Updating
- Rules: edit the `SECTIONS` list. Each item is `['text', 'hint', 'exampleKey', 'id']` (last two optional).
- When you add handling.meta for more classes to the guide, add the same rules to `HMETA` (field → [value, "fixed" | "max" | "min"]).
- The data blocks (`CLASSES`, `HMETA`, `LORE`, `REFS`) were generated from the final guide.
