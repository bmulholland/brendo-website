# brendo.ca

The public site for **Brendo** — Brendan Mulholland's DJ project. One static page: who he is, what it sounds like, four recorded sets, where he has played, the rider, and the booking address. It exists so that a promoter handed a link lands somewhere that transmits the sound rather than a list of platform icons.

This file explains why the page looks and reads the way it does. `CLAUDE.md` is the operative contract for anyone — person or agent — about to change it; `AGENTS.md` is a symlink to it, so Codex and Claude read the same file and it cannot drift.

---

## The short version

The page is deliberately small. Brendan's brief was the vibe rather than the content, and the content constraint runs the same way: nearly everything that could be said about this project either already lives somewhere better or is not yet settled enough to publish. So the page carries the few things that are true, settled, and his, and stops.

## Where the facts come from

**This repository holds no facts of its own.** Everything on the page has a home in the Obsidian vault at `~/Documents/Obsidian`, and that vault is the source of truth. The site is a *derived artifact* — re-derived by reading the source, never generated from it by a script. This is the same relationship the vault's own root instruction files have with their rationale documents, and it is deliberate: a generator would freeze one reading of the source and quietly rot.

| On the page | Its home |
|---|---|
| The line under the wordmark | `Canon/Music/Brendo's Sound — Territory and Description.md` §How to actually describe the sound |
| Recorded sets, venues, rider | `Canon/Music/DJ Press Kit.md` |
| Which photographs exist and may be used | `Canon/Music/DJ Press Kit.md`, head section |
| The domain's own state and open work | `Canon/Music/DJ Press Kit.md` §brendo.ca — the one surface he owns |
| Aesthetic constraints | `Canon/Self/Taste and Presentation/Personal Style.md` §Nightlife and DJing |
| Why any of this is the sound | `Canon/Music/DJ Identity.md` |

The route runs both ways. `DJ Press Kit` §brendo.ca records that this site exists and depends on it, so a vault session editing the venue list can see that the change is not finished when the document is saved.

---

## The design, and where each decision came from

### Palette: near-black and hot red

There is **no commissioned brand identity**. The 2026 Weiter Studio engagement delivered brand strategy and copy — a moodboard, a positioning concept, a bio — and no logo, palette or typeface. The yellow-on-black moodboard in the vault is Weiter's own slide styling, and mistaking it for a delivered brand colour is the easiest error available here.

So the palette was derived from the photographs. Sampling the red-lit booth shot returns almost exactly two things: near-black, and a ramp of hot red from `#180000` up to `#a81830`, with a faint blue-violet in the smoke. That became:

```
--ink      #08060b   near-black, biased violet — a club's dark is never neutral grey
--ember    #e8202a   the strip light over the mixer
--ember-hi #ff4a2e   hover, small red labels, and the italic phrase
--bone     #ece5df   warm off-white — film white, not #fff
--dim      #8d8189   warm-violet grey
--rule     #241d29   the hairline between sections
```

Corroborating rather than driving the choice: Brendan's SoundCloud avatar and banner are also black-and-red. He had already converged on this without writing it down.

The one place boldness is spent is the `o` of the wordmark. Everything else stays quiet. That also carries a small piece of continuity — the 2015 site had a coloured `o` too, in `#3399FF`.

### Type: Big Shoulders Display / Newsreader / Space Mono

Three faces, three jobs.

- **Big Shoulders Display** at 800 for the wordmark, 700 for section headings and the booking address, and 500 for set titles. Condensed, industrial, drawn for civic signage. The wordmark uses `-0.035em` tracking so the letters press against each other — the brand concept's word is *cramped*, and the type is where that gets expressed rather than in a caption saying so.
- **Newsreader** at 300, upright and italic, for the single line of prose. A low-contrast serif against condensed industrial sans is the deliberate pairing: it keeps the page from reading as generic techno-brutalism and gives *a bit haunted* somewhere to live.
- **Space Mono** for labels, dates, venues and the rider — the flyer-and-tech-spec register, where the information is genuinely list-shaped.

### Layout: a build, then a release

Full-bleed photograph, wordmark and sound line over its darkened lower left, then everything after it quiet: three plain sections, rules rather than cards, no boxes. The page is mostly black space.

That is not minimalism for its own sake. Brendan's set-construction philosophy is patience — long tension, careful transitions, the setup mattering more than the peak — and a page that shouts on every section is the opposite claim about the same person.

### Motion: two beats at 127 BPM

The glow on the wordmark's `o` breathes on a `945ms` cycle. That is two beats at 127 BPM, the median tempo of his record collection as measured in the vault's library analysis. It is slow enough to read as atmosphere rather than a blinking element, and it is the one detail on the page that could only belong to this subject.

The production review corrected the implementation to complete the dim–bright–dim cycle within 945ms. The original `alternate` animation took 945ms in each direction, doubling the documented period.

Everything else moves once: a staggered rise on load, and hover states on the set list. All of it is disabled under `prefers-reduced-motion`.

### Grain

A fixed SVG `feTurbulence` layer at 30% opacity in `overlay` blend mode. This is a requirement rather than a flourish: `Personal Style` §Nightlife and DJing states that a black surface has to carry visible texture rather than read as a flat field, and the page is almost entirely black surface.

---

## What is deliberately not here

**A short bio, and no more than that.** Both fuller bios in the vault are blocked. The June 2026 press copy leans on *hypnotic* and *driving* — two words Brendan explicitly rules out as descriptions of his sound, and a reader who has heard him play independently flagged the same sentence.

What the page carries is the vault's draft bio, trimmed. Its first sentence restated the standfirst almost word for word and its last duplicated the Played list, so both were cut; what is left is the two clauses that say something neither of those does — the range he moves across, and the shape of a set. Brendan approved adding it on 8 September 2026. Anything longer is still vault work: the full replacement bio has never been checked in his voice.

**No genre names.** `DJ Identity` §Genre Language Does Not Describe the Sound rules that in this corner of dance music genre labels are retail categories, contested and misleading. The page describes the music instead. Three words are ruled out outright: *driving* (reads as slamming), *hypnotic* (reads as a different lane), and *psychedelic* hitched to the psy- prefix.

**No Facebook.** The account exists and is not maintained. Removed deliberately, not overlooked.

**No AI-generated artwork.** The current SoundCloud avatar and banner are AI composites — blood moon, mountains, brutalist slabs. The palette is right, but the image is the visual form of a failure mode the vault already names in the music itself: the correct territory rendered without character. It also spends the one real advantage here, which is genuine photographs of genuine nights.

**No analytics, no fonts beyond Google Fonts, no cookies, no JavaScript.** There is nothing on this page that needs any of them.

---

## The photographs

Two, both real, both his.

**`images/room.jpg` — the hero.** A wide magenta-lit interior: tall windows onto a floodlit forest, a big matte paper lampshade overhead, Brendan blurred mid-motion behind CDJs. It is the strongest image of the set because it has a *place* in it, and because it reads as dark disco rather than techno — which is where the vault puts his centre of gravity, while techno is the base texture underneath.

It is also the image Weiter Studio picked out, which is worth something given that music branding is their trade.

**Asset, date and location identified.** Apple Photos asset `449163A8-908D-47B1-B321-6D6215B4FFB6` (`IMG_2906.HEIC`), in his `DJ` album. Taken **28 July 2024** at **Schmöckwitzer Werder, Berlin**, on an iPhone 14 Pro. The exact coordinates and capture time are in the vault, not here — see below. Per Brendan's account the event is Futuristische Feen Festival, held at a hotel there, and by his description it was unadvertised and friends-of-friends. The motion blur is a **1/24-second** handheld exposure at ISO 1600 and f/1.78, not a filter.

The file used here is downscaled from the 4032 × 3024 original. **Whether this particular night is Futuristische Feen is his recollection, not established.** His own recording of an FFF set is filed as `Brendo - Hummerhalle - FFF 28.08.2024` — a month later than this photograph and at a differently-named room. Same day of the month, different month and venue, so the two live readings are that these are two separate nights, or that one of the two labels is wrong; nothing to hand decides between them. Do not caption this image with a festival name until it is settled. The date and the place are solid on their own. A near-identical frame five seconds earlier, `9B8ADAA4-CE5F-42F7-88C3-9C9281D26DBB`, has him more central with his arms out and shows more of the window wall. It is a reasonable alternate and is not currently downloaded from iCloud.

**`images/booth.jpg` — the second beat.** Apple Photos asset `083F732D-77F6-4FA1-B966-50D5500930A1`. Brendan at the decks lit red from the mixer, absorbed, in a cramped booth. It sits beside the venue list, where a legible face and visibly working hands do credibility work that the hero cannot. The library dates it near the December 7 2024 Süß war Gestern set, but the image carries no location metadata, so it must not be captioned with that venue.

A third image exists and is not used: a sharp horizontal shot of Brendan smiling behind the decks (`C40F4E2F-9580-415B-AAE9-9221AC185791`). It is warm and very usable, and it reads as a friendly guy rather than as this music. Good for a booking email; wrong for the top of this page.

A fourth image, `images/promo.png`, was left over from 2017 and referenced by no version of this page; it was removed on 8 September 2026 and is recoverable from git history.

### Metadata is stripped

Every JPEG here has had its `APP1` and `APP13` segments removed — EXIF, XMP and the Photoshop/IPTC block — so none of it ships with the site. The pixels are untouched — the segments are dropped rather than the image re-encoded — so it costs no quality and saves about 3 KB a file.

Do the same to any image added later. `sips` preserves EXIF through a resize, so metadata survives an export unless something removes it; verify by parsing the exported file for surviving `APP1`, `APP13` or `COM` segments rather than assuming. A GPS-only check is not enough: XMP rides in `APP1` under a different identifier, and PNG and HEIC keep metadata in chunks and boxes a JPEG-segment check never reaches. The capture provenance belongs in the vault's `DJ Press Kit`, where it is useful; the web copies need none of it.

Earlier commits contain both the unstripped images and three README revisions that printed the coordinates in plain text. Brendan reviewed that on 8 September 2026 and chose to leave it — the location is a hotel and not sensitive — so the history is deliberately not rewritten.

### The set list mirrors the SoundCloud spotlight

The five rows under Recorded Sets are Brendo's SoundCloud **spotlight**, in the order he has pinned them there — not a hand-picked selection and not everything he has uploaded. Brendan asked for that on 8 September 2026, and it makes the profile the single place he curates: reorder the spotlight and this list should be brought into line, rather than the two drifting apart.

The right column is one shape throughout, `when · length`, read from the SoundCloud API rather than typed from the titles. His own titles carry dates in three different formats and one carries a genre phrase the page rules out, so the titles here are normalised and the dates moved into that column, which is also what separates the two Futuristische Feen entries. The fifth row is the *Live Sets* playlist, which is the fifth spotlight item.

### Image exports

Both photographs ship as a `srcset` ladder, generated from the Apple Photos originals rather than from anything previously in this repo. Quality falls as width rises, because the larger the file the less each JPEG artefact costs on screen and the more each byte costs on the wire.

| File | Pixels | Bytes | Quality |
|---|---|---|---|
| `room-1200.jpg` | 1200 × 900 | 259 KB | 74 |
| `room-2000.jpg` | 2000 × 1500 | 541 KB | 70 |
| `room-3200.jpg` | 3200 × 2400 | 951 KB | 62 |
| `booth-700.jpg` | 394 × 700 | 55 KB | 76 |
| `booth-1400.jpg` | 788 × 1400 | 140 KB | 68 |

The hero is full-bleed, so its `sizes` is simply `100vw`. The booth image sits in a grid column that is about 40% of a container capped at 1180px and goes full width below 820px, so its `sizes` is `(max-width: 820px) 100vw, (min-width: 1240px) 458px, 38vw` — 458px is the column's computed width at that breakpoint, and 38vw tracks it below, allowing for the container's 40px inset. The `src` fallbacks are the middle rungs, `room-2000.jpg` and `booth-1400.jpg`, so a browser ignoring `srcset` gets a usable image rather than the largest one.

The hero original is 4032 × 3024, so even the 3200 rung is a downscale and nothing is enlarged. `room-1200.jpg` doubles as the Open Graph image: link previews want roughly 1200px and should not pull a megabyte.

Regenerate any rung from the originals, not from a smaller export. The hero is Apple Photos `449163A8-908D-47B1-B321-6D6215B4FFB6`; the booth is `083F732D-77F6-4FA1-B966-50D5500930A1`.

---

## Deployment

GitHub Pages, from the **`gh-pages`** branch of `bmulholland/brendo-website`. No build step: commit and push, and Pages serves the repository root. `CNAME` binds it to the apex domain.

Verify at `https://brendo.ca` rather than the `github.io` URL — the custom domain is the part that has historically been broken.

### The DNS defect, resolved 2026-09-08

For about eleven years — the `CNAME` commit dates to June 2015 — the apex `A` records pointed at `192.30.252.153` and `192.30.252.154`, a **retired** GitHub Pages address block. It still answered on plain HTTP, which is why nobody noticed, but the certificate served there covered only `github.com`, so `https://brendo.ca` failed outright and Pages' *Enforce HTTPS* could not be enabled.

The two old records were replaced with the four addresses GitHub documents for an apex domain:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

GitHub then issued a Let's Encrypt certificate covering `brendo.ca` and `www.brendo.ca`, and *Enforce HTTPS* is on. Verified the same day: `https://brendo.ca` returns the page, `http://` answers `301` to the canonical `https://` URL, and the images and favicons load. The `TXT` records were left alone — they carry the Google Workspace SPF and site verification for the `@brendo.ca` mail that `bookings@brendo.ca` runs on, entirely independent of Pages.

`www.brendo.ca` resolves too — a `CNAME` to `bmulholland.github.io.`, covered by the same certificate, `301`-redirecting to the apex. The apex is what the repo's `CNAME` file binds and what the page advertises.

---

## Making changes

**Swap a photograph.** Drop the new file in `images/`, update the `src` and the `alt`, and check the `object-position` — both images are cropped hard and the framing is doing real work. Then record what it is in `DJ Press Kit`, including what is *not* known about it.

**Add a set.** A new row in the `.sets` list. The number in `.set__n` is a position in the list, not an identifier, so renumber the rest. Add it to `DJ Press Kit` §Recorded Sets too, or the next person to derive this page from the vault will delete it.

**Add a venue.** Same: the list here, and `DJ Press Kit` §Venues Played.

**Change the copy.** Almost certainly not a change to this repository. Find the claim's home in the table above and change it there first.

## Known gaps

Everything above is a decision that was made deliberately. These are not — they are things the first build did not get to, listed so nobody has to rediscover them and so nobody mistakes them for choices.

- ~~No favicon.~~ Closed: a local SVG red `o` on the page's near-black, with a 32px ICO fallback. The icon is a simple drawn echo of the wordmark, with no font request.
- ~~No image loading or decoding hints.~~ Closed: eager, high-priority hero; lazy booth; async decoding and intrinsic dimensions on both.
- ~~Hero resolution.~~ Closed: both photographs now ship as `srcset` ladders rather than single files. See §Image exports.
- ~~`og:image` unreachable.~~ Closed by the DNS repair above; it now points at `images/room-1200.jpg`, a 1200 × 900 export sized for link previews rather than the full hero.
- ~~No canonical URL and no `theme-color`.~~ Closed, with `og:type`, image dimensions and image alt text also supplied.
- ~~`README.md` and the agent contracts served as public pages at `https://brendo.ca/README.md`.~~ Closed by `_config.yml`, which excludes them from the Jekyll build.
- ~~Hero contrast unmeasured.~~ Closed for the tested viewports; measurements and their scope are below. The veil and the red letter's dark supporting shadow were strengthened after failures.
- ~~Only headless Chrome at two widths.~~ Closed. Chrome and headless Firefox by machine; Brendan checked desktop Safari and iPhone on 8 September 2026 and reported both good.

## Production review — 2026-09-08

**At the time of this review, deployment still needed the DNS repair and Brendan's push; both landed later the same day — see §The DNS defect, resolved 2026-09-08.** Read-only `dig` returned `192.30.252.153` and `192.30.252.154`; no apex AAAA answer. `curl -I https://brendo.ca` failed with certificate hostname mismatch. The replacement A records above still match [GitHub's apex-domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site). No DNS, Pages setting or remote branch was changed. The canonical and social image URLs intentionally remain HTTPS; local checks cannot establish a working public preview.

### Copy comparison and resolutions

The standfirst matches the sound home's quoted line verbatim, including punctuation. All four set URLs match `DJ Press Kit` §Recorded Sets, including Steamkat's secret-link suffix. Steamkat and Dark Ambivalence retain their exact titles. The Süß date appears in adjacent metadata using the event-night convention below. The Feen title moves the year and “Festival” into its metadata; the venue list shortens “Futuristische Feen Festival” to “Futuristische Feen”. All other venue names and their groups match. Berlin, the booking address and the footer's peak/after-hours slots have support in the named vault homes. Both image alts describe visible content without adding an event caption.

**Display the event night, even when the set starts after midnight.** Brendan selected **December 6, 2024** for the Süß set on 2026-09-08, recalling that he probably played around 2am on December 7. The convention is settled; the approximate start time remains his recollection. The page now says `06.12.2024`, matching the [SoundCloud title](https://soundcloud.com/brendobrendo/live-at-sus-war-gestern-2024-12-07). The working URL retains its December 7 slug. The vault's recorded-set label still needs this convention carried back; it was left untouched under the review's no-vault-edits instruction.

All four set destinations and the artist profile returned HTTP 200 during review. Their remote titles also differ from the vault's display labels: “Steam Kat”, “Dark Ambivalence - 200x200”, and “Live at Futuristische Feen Festival 2024 (Berlin Underground Techno)”. The site keeps the vault's labels and its rule against genre descriptions. Playback was not tested.

**The rider now carries the vault's requirements in full.** Brendan explicitly requested the missing `CDJ-3000X` on 2026-09-08. The preferred player row now includes both models, the Xone:96 is labelled “Preferred mixer”, and the DJM-V10 specifies “advance notice required”. The minimum player model/count, preferred three-player count and Pro DJ Link, and acceptable mixer models match `DJ Press Kit` §Tech Rider.

The source photographs and their README provenance were updated concurrently by another session. This review used the **2000 × 1500** hero. The 1280 × 960 file it replaced was a working-tree state, never committed, so no blob of it exists in this history. `CLAUDE.md` now points here for each image's provenance instead of repeating the stale claim that both are unresolved. Its rule against unverified captions is unchanged. The photo's July date does not establish a correction to the recording date; the site only gives the Feen set's year.

### Rendering and accessibility

Chrome and Firefox 155.0.1 were driven against a local HTTP server. Firefox used its built-in WebDriver BiDi endpoint and an isolated profile. Tested widths were **320, 360, 390, 768, 819, 820, 821, 1024, 1440, 1920 and 2560px** at 900px height in Firefox; Chrome covered **320, 390, 819, 820, 821, 1440 and 2560px**. In both engines, document scroll width equalled viewport width at every sampled size. Firefox also covered 320 × 568, 390 × 844, 820 × 390, 1440 × 1080 and 2560 × 1440. These are desktop viewport tests, not physical-phone coverage.

The Played grid switches from one column at 820px to two at 821px. Its image fills its frame in both engines. An explicit portrait width prevents its `max-height` from shrinking it horizontally on tablets. Short landscape screens now retain space above the hero text. Heading order is h1 → h2, with h3 venue groups; the page now has a main landmark. Both photographs have descriptive alt text. Firefox rendered the gradient mask and aspect ratio; both prefixed and standard mask declarations remain. `text-wrap: balance` is an enhancement: ordinary wrapping remains the fallback.

All eight links were traversed with Tab in both browsers. Every focused link had a **2px `#ece5df` outline with 4px offset**; Firefox's 320px checks also confirmed the outline fits inside the viewport. The set numbers changed from `#2c3654` (**1.693:1** on `#08060b`) to `#8d8189` (**5.411:1**). Small red headings and hovered numbers now use existing `#ff4a2e` (**6.023:1**), since `#e8202a` was only **4.486:1** on that background. Those solid-colour ratios use the CSS colours, before grain.

**Hero contrast uses rendered pixels, including grain and shadows.** In Firefox, after fonts loaded and entrance animations completed, the glow was frozen at its brightest point. An otherwise identical screenshot with transparent text supplied the background. Separate white-on-black glyph masks selected opaque interior pixels (coverage at least 250/255), excluding antialiasing fringes. The table gives the lowest sampled ratio for each text run, with the actual foreground/background pixel pair. Thresholds are 3:1 for the large wordmark and 4.5:1 for the standfirst, including its smaller mobile size; [WCAG's contrast guidance](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) explains those thresholds. This is a contrast check, not a claim of complete WCAG conformance.

| Viewport | Wordmark bone | Red `o` | Standfirst bone | Italic phrase |
|---|---|---|---|---|
| 320 × 900 | 7.435:1 · `#d0a5a3` / `#3c1216` | 4.129:1 · `#e4202a` / `#1f080e` | 15.129:1 · `#e5ded8` / `#09060b` | 5.836:1 · `#fa4a2e` / `#09060b` |
| 1440 × 900 | 7.750:1 · `#d0a3a2` / `#370b11` | 3.994:1 · `#e8212b` / `#2e0b12` | 15.494:1 · `#e8e1dc` / `#09070d` | 5.776:1 · `#fa492e` / `#0a070c` |

The same glyph test passed at 820, 821 and 2560px widths. Across those five 900px-high viewports the lowest ratios were **7.435:1** for the bone wordmark, **3.994:1** for the red letter, **15.129:1** for the bone standfirst and **5.776:1** for its emphasis. The Berlin label was changed to bone for the photographic background. These samples depend on the current photograph, crop, fonts, veil and glow; changing any of them reopens the check.

Reduced motion was tested in a separate Firefox profile with `ui.prefersReducedMotion=1`: the media query matched, there were no active animations, all entrance elements had opacity 1 and no transform, and scroll behaviour was `auto`. A forced Arial fallback with both image URLs broken retained 320px document width. Safari, physical devices and assistive-technology speech output remain outside this review's observed coverage.

The red glyph also passed at the additional short/tall viewport sizes above. The lowest of those samples was **3.943:1** at 820 × 390 (`#e7202a` over `#2c0d16`).

### Correctness, performance and consistency

HTML Tidy found no structural errors after escaping the font URL's ampersands. Its remaining warnings call `fetchpriority` and `decoding` proprietary; this installed validator predates those standard attributes. CSS was read for cascade and no-op rules. Removed unused colour variables and the `background-color` transition that could not animate the set links' gradient image. Removed body overflow clipping so the width checks measure layout instead of hiding defects. The grain remains fixed at 30% opacity with overlay blending, but its layer now covers one viewport instead of four. Focus styles, SoundCloud capitalization, font-weight documentation and the full glow period are consistent.

The hero is eager and high priority; the booth is lazy, and both have async decoding and intrinsic dimensions. The hero's largest rung is a 951 KB JPEG and its default `src` rung 541 KB, so its transfer is still the dominant local asset. The 1200 rung is the social image. Google Fonts still adds a blocking stylesheet followed by font downloads: both preconnects and `display=swap` remain, and the unused Newsreader 400 request was removed. Firefox loaded Big Shoulders Display at 500/700/800, Newsreader 300 upright/italic, and Space Mono 400/700. Cross-origin timing entries hid transfer sizes, so this review does not claim a measured font-byte saving or a production LCP score. No preload was added for third-party font URLs that Google may change.

No JavaScript, analytics, libraries, build step, light theme, Facebook link or bio was added. The review did not edit the vault.

## Open

- The bio, which is what stands between this and a fuller page.
- Whether the SoundCloud artwork gets replaced with these photographs — same job, same images.
- An `/epk` page, so `bookings@brendo.ca` can point promoters at a URL Brendan owns instead of a Notion page in someone else's workspace. The rider is already here; the bio is the blocker again.
