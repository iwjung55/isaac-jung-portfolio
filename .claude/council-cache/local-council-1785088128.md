# Local Council — Portfolio direction (data focus / smoother UI / single page)

**Local council** — these perspectives all come from Claude playing different roles, not from different AI vendors. Treat agreement as a shared starting point to pressure-test, not as independent confirmation.

Question: reposition the portfolio around "data" in general; make the UI feel smoother; combine the multi-page site into one page.

Members: Devil's Advocate · Simplicity Champion · Security/Integrity Auditor

---

## 🗳️ Devil's Advocate

### Position
Two of the three goals solve problems this site doesn't have, and the "data" reframe risks trading a distinctive editorial identity for the most crowded self-label a CMU stats student can pick. Consolidate only if you name the user problem it fixes; resist "data" as a theme — it's anti-positioning.

### Key points
- "Combine into one page" is a feeling, not a diagnosed problem. Collapsing projects.html/experience.html into anchors makes shared/recruiter links fragile and loses four title/h1/meta pairs (worse for search & link previews).
- "Data in general" is the weakest available positioning — every stats/ML student is "about data." The differentiated assets are the specific combos (Rotman 2nd, LLM safety, John Locke essays, policy). Essays/policy are NOT data work; a data spine flattens or demotes them.
- The existing motion system is already competent; "smoother" is where you can only lose (scroll-jacking, parallax, a JS lib betraying the no-build ethos).
- Reduced-motion commitment doubles the cost of any signature motion (build it twice); the honest wins are boring — kill font CLS, unify easing.
- The redesign may be displacing the real lever: monogram placeholders where real work artifacts should be.

### Risks & blind spots
- Deep-link/shareability loss is invisible in a design review; bites weeks later.
- Bigger data-aesthetic risk than "dashboard cliché" = thematic monoculture; the interesting move is to let the identity be the *range*, with "rigor with data" as one thread.
- Combining pages multiplies per-page scripts onto one long DOM → can undermine "smoother."
- Nobody's asking whether the current uncommon identity is worth preserving.

### Confidence
medium — high on concrete costs; lower on positioning without knowing the target audience.

---

## 🗳️ Simplicity Champion

### Position
Collapse to one page — but as a *deletion* exercise, not construction. For a site this small (four thin, ~60% duplicated pages), one page is simpler to build and use. "About data" and "smoother" are traps that invite adding components; the wins are removing pages, removing external deps, and shrinking the motion vocabulary.

### Key points
- Single-page is a net simplification: the four files re-implement the same nav/menu/footer/#toTop/reduced-motion (already drifting). Anchors + existing scroll-smooth/scroll-mt-24 need zero new JS. Section numbers are built for one continuous read.
- "About data" is a copy/IA problem — solve with words, not widgets. Rewrite the hero, reorder Selected Works so quant/LLM-safety/trading lead; let the 00/01/02 numbering + 1px grid BE the data aesthetic. One chart would undercut the thesis.
- "Smoother" = less and consistent. Current durations are a grab-bag (150/200/300/500/1000ms + 1s reveal + 2s SVG draw). Collapse to one easing, two durations. Consistency reads as smooth.
- Delete render-blocking externals: three Google Fonts links incl. Material Symbols (for a couple arrows). Inline SVG/Unicode arrows, self-host the two real fonts. Biggest smoothness lever on a static site.
- One shared chrome defined once.

### Risks & blind spots
- SEO/deep-link regression: old .html URLs need meta-refresh stubs or accept 404s (Pages has no server redirects). Name it.
- IntersectionObserver reveal is a liability on one long page — content at opacity:0 depending on JS; failure = blank below fold. Make content visible by default, reveal as progressive enhancement.
- Consolidation can quietly become a redesign (pinned/parallax/scroll-jack) — hold the line.
- Near-zero payoff polishing motion while images are placeholders; real content moves the needle.

### Confidence
high — small legible codebase; duplication, font weight, inconsistent durations all visible; SEO redirect is the only genuine tradeoff.

---

## 🗳️ Security / Integrity Auditor

### Position
Consolidation + "smoother" are net-positive *only if* smoothness stays native (CSS/IntersectionObserver, no CDN animation library) — the site's real strength is zero third-party runtime JS, and the biggest risk is trading that for motion polish. The one live privacy exposure is Google Fonts + Material Symbols phoning home every load; self-host regardless.

### Key points
- Zero-JS-dependency is the security moat; don't spend it on smoothness (no Lenis/GSAP/Locomotive from CDN — reintroduces supply-chain surface). Keep native scroll + CSS transforms.
- Self-host fonts — the only real privacy leak (Google Fonts GDPR ruling). You already vendored Tailwind to local styles.css; do the same for fonts + inline SVG icons → zero external runtime requests.
- Consolidation concentrates PII (mailto Gmail, LinkedIn, GitHub, resume.pdf on one crawlable URL) — accept/obfuscate the email; check resume.pdf for a home address/phone you didn't mean to publish.
- A meta-CSP becomes reachable: move inline JS to one external main.js + self-host fonts, then ship default-src 'self' with no unsafe-inline — highest-leverage hardening the redesign enables.
- Deploy integrity: hand-committed styles.css → risk is stale CSS, not compromise; a tiny GitHub Action (npm run build, fail on dirty diff) removes human error.

### Risks & blind spots
- "About data" invites decorative data-viz that becomes dishonest — placeholder monograms are honest; a fabricated/ornamental chart misrepresents work. Rule: any number/chart is real+attributable or visibly labeled illustrative.
- Verifiability: link concrete claims (Rotman, John Locke, LLM-safety) to sources.
- "Smoother" vs "static/zero-dependency" are in tension — make "no runtime CDN JS" an explicit stated constraint.
- Motion/reduced-motion parity must be re-audited after the merge (new scroll-snap/parallax needs an explicit non-motion path).

### Confidence
high — grounded in the files; softer calls are the trust/PII judgments (advisory).

---

## Synthesis — angles, not consensus

### Shared starting points (a common prior to stress-test, not corroboration)
All three (same-model, so this is a shared instinct, not independent proof) converged on:
1. **Don't literalize "data" into charts/dashboards.** Reposition through copy, ordering, and the existing numeric/grid aesthetic. Any real chart must be real and attributable.
2. **"Smoother" = less, consistent, and native.** Unify motion tokens (one easing, two durations), kill the 1s/2s outliers, and above all do NOT add a scroll/animation JS library.
3. **The biggest quick win isn't motion — it's killing font CLS/latency** by self-hosting the two fonts and dropping the Material Symbols icon font for inline SVG.
4. **The real lever is content**, not the container: monogram placeholders are the credibility gap, not page count.

What they might all be missing *because* they share a model: they all treat this as a craft/hygiene problem and under-weight the **audience question** — who is this for, and does narrowing to "data/quant" help or hurt with safety-lab / policy / econ readers?

### Genuine tensions
- **Consolidate or not (Devil vs. Simplicity).** Simplicity: one page is a net *deletion* (kills 4× duplicated chrome, zero new JS). Devil: one page *loses* deep-linkable URLs a recruiter pastes into an application. Both are right; it hinges on **whether you share specific project links**. Resolution → a hybrid, below.
- **"Data" as spine vs. thread.** Devil: data flattens your range (essays/policy aren't data). Simplicity/Security: fine *if* it's copy-level and honest. The unusual mix (quant + alignment + economics + writing) is the memorable asset — narrowing to "data" risks sanding it off.

### Blind spots one lens caught that the others walked past
- **Security alone** caught the Google-Fonts privacy leak (GDPR-flavored), the PII concentration on one crawlable page (check resume.pdf for a home address/phone), and the meta-CSP opportunity. A pure design/simplicity pass ships right past these.
- **Devil alone** named "redesign as displacement activity" — reorganizing the container because it's more fun than producing case-study content.
- **Not covered by anyone:** the *positive* execution of a tasteful data identity beyond "don't." The only constructive nudge was Simplicity's "let the numbering + 1px grid be the data aesthetic." Worth designing deliberately.

### Suggested direction (my synthesis)
1. **Hybrid, not pure single-page.** Build a single-scroll home that flows About → Work → Experience → Contact (the "feels better to use" narrative), but keep `projects.html`/`experience.html` as canonical deep-link targets — or add `<meta http-equiv="refresh">` stubs at the old URLs so shared links survive. You get the smooth read AND keep shareable/SEO surface. (Supports: Simplicity's consolidation + Devil's deep-link worry.)
2. **"Data" as a thread, not a cage.** Reposition via hero copy + reordering (lead with Rotman / LLM-safety / quant), and let the editorial numbering + grid carry the "data" texture. Keep the essays/policy visible as *range*. If you want one data visual, make it a single **real, attributable** chart (e.g., the actual arbitrage P&L) — never ornamental. (Devil + Security + Simplicity.)
3. **Smoother = tokens + fonts, no library.** One easing, two durations; delete 1s/2s outliers; self-host EB Garamond + Plus Jakarta and replace Material Symbols with inline SVG (fixes CLS *and* the privacy leak); keep native scroll; content visible by default with reveal as progressive enhancement; re-verify reduced-motion after merging. (All three.)
4. **Then spend real effort on content** — swap monogram placeholders for real artifacts / short honest case-study text, and link each credential to a source. (Devil + Simplicity + Security.)

**Where the real uncertainty remains:** the audience. If you're targeting quant desks specifically, the "data/quant" narrowing is probably correct and #2 leans harder into data. If you want to stay legible to safety labs, econ/policy programs, and quant simultaneously, keep the range and treat data as the connective thread.
