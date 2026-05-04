# Proposal Coauthor Tool

A browser-based tool that automatically generates proposal-ready coauthor and collaborator lists from ORCID, Google Scholar, DOIs, or BibTeX — with affiliation enrichment and CSV export.

**Live tool:** [https://uw-gcrl.github.io/coauthor_tool/](https://uw-gcrl.github.io/coauthor_tool/)

---

## Features

- **Multiple input sources** — ORCID iD, Google Scholar profile URL, pasted DOIs, or BibTeX
- **Automatic deduplication** — merges coauthors across sources using name normalization
- **Affiliation enrichment** — looks up institutional affiliations via CrossRef and OpenAlex
- **Year filtering** — restrict to papers from the last 1–5 years or a custom range
- **CSV download** — coauthor list and fetched publications as spreadsheets
- **Uncertainty flagging** — highlights entries with missing affiliations or abbreviated names that need manual review

---

## Usage

1. Open the tool at [https://uw-gcrl.github.io/coauthor_tool/](https://uw-gcrl.github.io/coauthor_tool/)
2. Enter your name (used to exclude yourself from the list)
3. Select one or more data sources and provide the required input
4. Choose a year range
5. Click **Fetch Coauthors**
6. Review the results and download as CSV

---

## Data Sources & APIs

| Source | API Used |
|---|---|
| ORCID | [ORCID Public API v3](https://pub.orcid.org/) |
| Google Scholar | Proxied via allorigins.win / codetabs.com |
| DOIs | [CrossRef REST API](https://api.crossref.org/) |
| BibTeX | Parsed locally in-browser |
| Affiliation backfill | [OpenAlex API](https://openalex.org/) |

---

## Information Security

Your inputs (ORCID iD, DOIs, author names) are sent to public academic APIs — ORCID, CrossRef, and OpenAlex — to retrieve publication and affiliation data. If you use the Google Scholar option, your profile URL and paper list also pass through third-party CORS proxy services (allorigins.win, codetabs.com). This tool itself does not store or log anything, but those external API calls do leave your device.

---

## Disclaimer

This tool is provided "as is," without warranty of any kind, express or implied. Output is retrieved from third-party public APIs and may contain inaccuracies, omissions, or errors. Mistakes can occur due to inconsistent formatting in the retrieved data — including non-standard name representations, missing or ambiguous institutional affiliations, duplicate entries, or incorrect publication attributions. The developer accepts no responsibility or liability for the accuracy, completeness, or fitness for purpose of the output, nor for any consequences arising from its use. Users are solely responsible for verifying all results before inclusion in any grant proposal or official document.

---

## Development

The entire tool is a single self-contained HTML file (`index.html`) with no build step, no dependencies, and no backend.

To run locally, simply open `index.html` in any modern browser.

To deploy, push `index.html` to a GitHub repository and enable GitHub Pages (Settings → Pages → branch: `main`, folder: `/ (root)`).

---

## Credit

Developed by [Min Chen](https://globalchange.cals.wisc.edu/) · University of Wisconsin–Madison  
Global Change Research Lab · [globalchange.cals.wisc.edu](https://globalchange.cals.wisc.edu/)
