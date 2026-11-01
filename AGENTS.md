<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

- Study data lives in browser localStorage via src/lib/store.ts (no backend) — keeps the app fast, free and account-less.
- Text processing (summary, quiz, glossary, SRS) is local in src/lib/nlp.ts and src/lib/srs.ts; AI (Groq) is opt-in only — the product goal is saving tokens.
- The retired /laboratorio URL redirects permanently to /resumenes to preserve existing published links; no legacy laboratory is exposed in the application.
- Enriched summaries use src/lib/enriched-summary.ts to extract concepts and cited passages from selected local documents; never invent facts or silently call AI for enrichment.
