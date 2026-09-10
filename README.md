# CopilotChronicles

Blog Jekyll (GitHub Pages) con le ultime novità sul mondo Copilot, organizzato per tema e per mese.

## Struttura

- `_github-copilot/` — novità GitHub Copilot
- `_copilot-studio/` — novità Microsoft Copilot Studio
- `_m365-copilot/` — novità Microsoft 365 Copilot
- `_business-central/` — novità Copilot in Business Central
- `_azure/` — novità Azure

Ogni collezione contiene sottocartelle `AAAA-MM` con i post del mese.

## Come aggiungere un nuovo post (manuale)

1. Chiedi a GitHub Copilot un riassunto delle novità sulla fonte di interesse:
   - GitHub Copilot: https://github.blog/changelog/label/copilot/
   - Copilot Studio / M365 Copilot: https://www.microsoft.com/en-us/microsoft-365/blog/
   - Business Central: https://www.microsoft.com/en-us/dynamics-365/blog/ (filtra per "Business Central"/"Copilot")
   - Azure: https://azure.microsoft.com/en-us/blog/
2. Crea un file `_<tema>/AAAA-MM/AAAA-MM-GG-titolo-breve.md` con questo front-matter:
   ```yaml
   ---
   title: "Titolo del post"
   date: AAAA-MM-GG
   tags: [tag1, tag2]
   source_url: "https://..."
   source_name: "Nome fonte"
   ---
   ```
3. Scrivi il contenuto in Markdown sotto il front-matter.
4. Fai commit e push: GitHub Pages ricostruisce il sito automaticamente.

## Pubblicazione

Nessuna automazione: pubblicazione manuale via commit/push su GitHub. Abilita GitHub Pages da Settings > Pages, branch `main`, cartella `/ (root)`.
