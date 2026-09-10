# CopilotChronicles (Daniele Incalza)

A Jekyll blog (GitHub Pages) with the latest news from the world of Copilot, organized by theme and by month.

## Structure

- `_github-copilot/` — GitHub Copilot news
- `_copilot-studio/` — Microsoft Copilot Studio news
- `_m365-copilot/` — Microsoft 365 Copilot news
- `_business-central/` — Business Central Copilot news
- `_azure/` — Azure news

Each collection contains `YYYY-MM` subfolders with that month's posts. Each theme also has a landing page (e.g. `/github-copilot/`) that lists its posts grouped by month.

## How to add a new post (manual)

1. Ask GitHub Copilot for a summary of the news from the source of interest:
   - GitHub Copilot: https://github.blog/changelog/label/copilot/
   - Copilot Studio / M365 Copilot: https://www.microsoft.com/en-us/microsoft-365/blog/
   - Business Central: https://www.microsoft.com/en-us/dynamics-365/blog/ (filter for "Business Central"/"Copilot")
   - Azure: https://azure.microsoft.com/en-us/blog/
2. Create a file `_<theme>/<YYYY-MM>/<YYYY-MM-DD>-<slug>.md` with this front matter:
   ```yaml
   ---
   title: "Post title"
   date: YYYY-MM-DD
   tags: [tag1, tag2]
   source_url: "https://..."
   source_name: "Source name"
   ---
   ```
3. Write the content in Markdown below the front matter.
4. **If this is the first post of a new month for that theme**, create a month archive page at the repo root, named `<theme>-<YYYY-MM>.md`, with `permalink: /<theme>/<YYYY-MM>/` (copy an existing one, e.g. `azure-2026-09.md`, and update the collection name/dates). The theme's landing page (e.g. `azure.md`) automatically links its month headings to this page.
5. Commit and push: GitHub Pages rebuilds the site automatically.

## Publishing

No automation: manual publishing via commit/push to GitHub. Enable GitHub Pages from Settings > Pages, branch `main`, folder `/ (root)`.
