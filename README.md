# Pari-Shodhana-Sahay: Unified Research Literature Search

A unified literature search tool that combines OpenAlex and CORE to help research scholars find peer-reviewed articles efficiently. Search across multiple scholarly sources simultaneously, filter by journal quality metrics, and export results in multiple formats.

## Features

- **Unified Search**: Query both OpenAlex and CORE APIs in parallel, combining results with automatic deduplication
- **Citation Metrics**: View citation counts from OpenAlex for each paper
- **Journal Quality Filtering**: Filter by SJR quartiles (Q1-Q4) and ABDC grades (A*, A, B, C)
- **Advanced Search Syntax**: Use `AND`, `OR`, `NOT` operators and quotes for phrase search
- **Multiple Export Formats**: Download results as CSV, RIS, or BibTeX
- **Browser-based**: No backend required; journal lists and searches run entirely in your browser
- **Source Attribution**: Visual badges show whether each result came from OpenAlex or CORE

## Getting Started

1. Open `index.html` in a modern web browser
2. (Optional) Load SJR and ABDC journal lists under "Settings" for quality filtering:
   - SJR quartiles: Download CSV from https://www.scimagojr.com/journalrank.php
   - ABDC grades: Download Excel from https://abdc.edu.au/abdc-journal-quality-list/
3. Enter a search query and click "Search Both Sources"
4. Use filters to narrow results by year, citation count, or journal quality
5. Export results in your preferred format

## Search Syntax

Use boolean operators (in capitals) and phrases:

```
(leadership OR followership) AND India
"organizational behavior" NOT psychology
```

## How It Works

- **OpenAlex API**: Provides bibliographic metadata and citation counts
- **CORE API**: Accesses full-text open access papers via a Google Apps Script relay
- **Unified Results**: Results are deduplicated by DOI, then by normalized title and publication year
- **Journal Matching**: Journal quality grades are matched by ISSN, then by exact title

## Technical Notes

- Citation counts come from OpenAlex and may differ from Scopus and Google Scholar
- CORE phrase searches are checked client-side; papers marked "phrase not checked" need manual verification
- CORE has a shared daily limit; if reached, try again the next day
- Journal lists are stored in your browser's IndexedDB and never uploaded

## Deployment

Host `index.html` on any static hosting service (GitHub Pages, Netlify, etc.).

## Credits

Developed by L K Prasad Rayaprolu, Department of Management and Commerce, Sri Sathya Sai Institute of Higher Learning.

Based on [Shodh](https://github.com/rlkprasad-design/Shodh) with unified search across OpenAlex and CORE.
