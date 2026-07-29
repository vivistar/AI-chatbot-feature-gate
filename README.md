# AI Chatbot Feature Gate

A guided, interactive decision tool that walks designers and PMs through a five-stage gate for adding an AI chatbot — from *"does this need chat at all?"* to a copyable launch-gate brief. Grounded in Suh et al. 2026 (arXiv:2607.25057).

**Live site:** https://vivistar.github.io/AI-chatbot-feature-gate/

## Contents

| File | What it is |
|------|------------|
| [`index.html`](index.html) | **How-to guide** — the landing page. What the gate is, when to use it, how to move through the seven stages. |
| [`tool.html`](tool.html) | **The interactive tool** — job decomposition, scope choice, a live harm-applicability board, an editable pass-behavior worksheet, the launch-gate checklist, and an exportable decision brief. |

Both are self-contained static pages (no build step, no dependencies). Your answers in the tool are saved in your browser's local storage. They render in light or dark theme and match the Terry Web Media brand system.

## Deploying

Served as a static site via **GitHub Pages** from the `main` branch, root folder. To (re-)enable: repo **Settings → Pages → Build and deployment → Source: Deploy from a branch → `main` / `/ (root)`**.

## The stance

A conversational surface is a **cost, not a default.** Most of the gate is about refusing or narrowing the request — treat a "no" or a "narrow it" as a successful outcome.

## License

[Apache License 2.0](LICENSE).
