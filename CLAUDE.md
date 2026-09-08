# brendo.ca — Claude Code Instructions

The public site for **Brendo**, Brendan Mulholland's DJ project. One static page, no build step, no dependencies: `index.html` carries its own CSS, `images/` carries the photographs, `CNAME` binds the apex domain, and GitHub Pages serves the repository root from the `gh-pages` branch.

**Read `README.md` before changing anything.** It carries the design rationale, the photographs and what is known about each, deployment and the live DNS defect, and the open questions. This file carries only what must not be got wrong.

## This repository holds no facts of its own

Everything on the page has a home in the Obsidian vault at `~/Documents/Obsidian`, and **the vault is the source of truth**. The site is derived from it semantically — by reading the source — and never by a generator. Do not invent copy here, and do not correct a fact here: correct it at its home and bring the change down.

| On the page | Its home |
|---|---|
| The line under the wordmark | `Canon/Music/Brendo's Sound — Territory and Description.md` §How to actually describe the sound |
| Recorded sets, venues played, tech rider | `Canon/Music/DJ Press Kit.md` |
| The photographs, and which may be used how | `Canon/Music/DJ Press Kit.md`, head section |
| This site's own state and open work | `Canon/Music/DJ Press Kit.md` §brendo.ca — the one surface he owns |
| Aesthetic constraints | `Canon/Self/Taste and Presentation/Personal Style.md` §Nightlife and DJing |
| Why this is the sound | `Canon/Music/DJ Identity.md` |

A change here that is really a change to one of those is not finished until the vault edit lands too. Say so when you make one.

## Constraints

**No bio, and do not write one.** Both bios in the vault are blocked — the June 2026 press copy uses words Brendan rules out, the draft replacement is unverified in his voice. A bio is vault work, not site work.

**Three words are ruled out anywhere on the page:** _driving_, _hypnotic_, and _psychedelic_ hitched to the psy- prefix. Genre names generally do not describe this music; `Canon/Music/DJ Identity.md` §Genre Language Does Not Describe the Sound carries the reasoning.

**There is no commissioned visual identity.** The 2026 Weiter Studio engagement delivered strategy and copy only. The yellow-on-black moodboard in the vault is that studio's slide styling, not Brendo's colour. The palette here was derived from the photographs and is this site's own choice — revise it on its merits, but do not "restore" a brand standard that does not exist.

**Never caption a photograph with a venue or date the vault does not confirm.** `README.md` states exactly what is and is not known about each image.

**No Facebook link.** The account is not maintained. Its absence is deliberate.

Canadian English, matching the vault.

## House style

Single file, no libraries, no build, no analytics, no JavaScript. Fonts by `<link>` from Google Fonts; everything else local. It is a deliberately dark, single-theme page — do not add a light theme or a theme toggle, and paint every colour explicitly so it holds on any host background. Keep it working with images that fail to load and with `prefers-reduced-motion` set.

## Deploying

Commit to `gh-pages` and push. Verify at `https://brendo.ca`, not the `github.io` URL. **That verification currently fails**: the apex `A` records still point at a retired GitHub address block, so the domain is HTTP-only. `README.md` §The DNS defect has the four current addresses and the fix.
