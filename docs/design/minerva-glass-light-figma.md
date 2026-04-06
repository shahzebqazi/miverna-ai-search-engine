# Minerva — Glass light mode (Figma)

**File:** [Minerva — Glass Light System & Mockups](https://www.figma.com/design/9EpJTVV5gBd3zI0w0h72pG)

## Primary deck (single canvas)

**Page:** **Presentation — Minerva (single canvas)** — all story + screen frames live on **one Figma page** in a horizontal row (zen glass, subtle **Greek architectural motif**: column **flutes** + **meander** hairline, variable tokens `motif/greek-flute`, `motif/meander`).

**Frame naming (sort for Present):** `Deck/00 — Cover`, then for each id `01`–`11`: `Deck/NN — Story` (user story + “As a… I want… so that…”) immediately followed by `Deck/NN — View` (Perplexity-style **answer + sources rail**, Cursor-class **glass** chrome; omnibar: **Minerva** + mono query + **Search** label only). End with `Deck/ZZ — Presenter notes`.

**User stories (11):** Stories **1–10** mirror common Google / Perplexity jobs-to-be-done (quick facts, how-to, news/recency, compare, API/code, academic citations, follow-up, org governance, local ops, deep synthesis). Story **11** is **Minerva-specific**: **embedded SearXNG (Docker sidecar, loopback, editable `settings.yml`) + local LLM** — **inspectable metasearch routing** on your machine, not only a cloud black box (see [`embedded-searxng.md`](../embedded-searxng.md)).

**Presenting:** In Figma, open the Presentation page, select **Deck/00 — Cover** as the first slide, then advance **left → right** (or sort layers by name). Optionally add manual prototype links **Story → View** (instant dissolve) in the editor for click-through stepping.

**Older pages** (Design Guide, Wireframes, High Fidelity, Stakeholder) remain as reference; the **Presentation** page is the consolidated story-led mockup.

Related product spec: [`glass-ui.md`](glass-ui.md).

## Svelte app handoff (when implementing)

- **Stepped UI:** mirror the deck order with routes or a single route + `$state` step index; use **`{#key}`** + **`transition:`** (e.g. `fade`) for calm frame changes per [`transition:`](https://svelte.dev/docs/svelte/transition) docs.
- **Optional:** `onNavigate` + `document.startViewTransition` for browser-native cross-fade between “story” and “view” (see [`$app/navigation`](https://svelte.dev/docs/kit/$app-navigation#onNavigate)).
