# Proposal Coauthor Tool

A browser-based tool that automatically generates proposal-ready coauthor and collaborator lists from ORCID, Google Scholar, DOIs, or BibTeX — with affiliation lookup and NSF/DOE export, entirely client-side.

**Live tool:** [https://uw-gcrl.github.io/coauthor-tool/](https://uw-gcrl.github.io/coauthor-tool/)

---

## Features

- **Multiple input sources** — ORCID iD, Google Scholar profile URL, pasted DOIs, or BibTeX
- **Automatic deduplication** — merges coauthors across sources using name normalization
- **Affiliation enrichment** — looks up institutional affiliations via CrossRef and OpenAlex
- **Year filtering** — restrict to papers from the last 1–5 years or a custom range
- **NSF / DOE export** — one-click formatted collaborator list ready to paste into proposals
- **CSV download** — coauthor list and fetched publications as spreadsheets
- **Uncertainty flagging** — highlights entries with missing affiliations or abbreviated names that need manual review
- **Fully client-side** — no data leaves your browser; no account or API key required

---

## Usage

1. Open the tool at [https://uw-gcrl.github.io/coauthor-tool/](https://uw-gcrl.github.io/coauthor-tool/)
2. Enter your name (used to exclude yourself from the list)
3. Select one or more data sources and provide the required input
4. Choose a year range
5. Click **Fetch Coauthors**
6. Review the results, then download as CSV or export in NSF/DOE format

---

## Data Sources & APIs

| Source | API Used |
|---|---|
| ORCID | [ORCID Public API v3](https://pub.orcid.org/) |
| Google Scholar | Proxied via allorigins / codetabs |
| DOIs | [CrossRef REST API](https://api.crossref.org/) |
| BibTeX | Parsed locally in-browser |
| Affiliation backfill | [OpenAlex API](https://openalex.org/) |

---

## Disclaimer

This tool is provided "as is," without warranty of any kind. Output is derived from third-party public APIs and may contain inaccuracies, omissions, or errors. The developer, the University of Wisconsin–Madison, and the Global Change and Agroecosystems Research Lab accept no responsibility or liability for the accuracy or completeness of the output, nor for any consequences arising from its use in grant proposals or official documents. Users are solely responsible for verifying all results before submission.

---

## Development

The entire tool is a single self-contained HTML file (`index.html`) with no build step, no dependencies, and no backend.

To run locally, simply open `index.html` in any modern browser.

To deploy, push `index.html` to a GitHub repository and enable GitHub Pages (Settings → Pages → branch: `main`, folder: `/ (root)`).

---

## Citation / Credit

Developed by [Min Chen](https://globalchange.cals.wisc.edu/) · University of Wisconsin–Madison  
Global Change and Agroecosystems Research Lab · [globalchange.cals.wisc.edu](https://globalchange.cals.wisc.edu/)
