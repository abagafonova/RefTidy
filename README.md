# RefTidy

**Browser-based tool for building Zotero-ready bibliographic records from Russian academic sources.**

Builds a clean bibliographic record from what you already have — an Obsidian note clipped from CyberLeninka or eLibrary, a GOST citation string, a URL, or a DOI. The output is a `.ris` file that Zotero imports complete with correct authors and year.

Everything runs in the browser. No file ever leaves your device.

---

## What it does

RefTidy takes one of several inputs and constructs a structured bibliographic record, optionally enriching it with metadata from Crossref or OpenAlex. The record can be downloaded as a `.ris` file for direct Zotero import, or copied as a Markdown reference.

**Single-record mode** — one source at a time, with a live preview and per-field editing before export.

**Batch mode** — paste a reference list and export all records as a single `.ris` file in one click.

---

## Input formats

| Input | How to get it |
|---|---|
| Obsidian `.md` note | Clip with the Obsidian Web Clipper from a CyberLeninka or eLibrary article page |
| GOST citation string | Copy from the "Цитировать" / Cite button on CyberLeninka (GOST tab) or eLibrary |
| Article URL | Paste a direct link to a CyberLeninka or eLibrary article page |
| DOI | Paste a bare DOI (`10.xxxx/…`) or a `https://doi.org/…` link |
| Reference list | Paste a numbered or plain-text bibliography for batch processing |

---

## Output formats

- **`.ris`** — standard RIS file, importable directly into Zotero, Mendeley, or any reference manager
- **`.ris` (English record)** — transliterated version for English-language article metadata
- **Markdown** — formatted reference string for pasting into notes or documents

---

## Romanisation

For generating English-language metadata from Cyrillic sources, RefTidy supports three schemes:

- **ALA-LC** — Library of Congress romanisation, standard for humanities journals
- **GOST 7.79-2000 B** — required by Russian journals indexed in Scopus and Web of Science
- **BGN/PCGN** — used by many British publishers

The Cyrillic original is preserved in the record's note field.

---

## Metadata enrichment

Two optional buttons make external API requests — only when clicked:

- **Crossref** — looks up the DOI in the Crossref database and fills in missing fields
- **OpenAlex** — queries OpenAlex by DOI or title for additional metadata

Without clicking these buttons, no data is sent anywhere.

---

## Supported source parsers

| Parser | What it handles |
|---|---|
| `parseCyberleninka` | Obsidian notes and URLs from cyberleninka.ru |
| `parseElibrary` | Obsidian notes and URLs from elibrary.ru |
| `parseGost` | GOST 7.0.5-2008 citation strings |
| `parseBibliography` | Plain-text reference lists for batch import |
| `parseCitationString` | Generic citation strings (APA, Vancouver, etc.) |
| `parseFrontmatter` | YAML frontmatter from Obsidian `.md` files |
| `parseArchival` | Archival source descriptions |

---

## Using it

Open `RefTidy.html` in any modern browser — no installation, no server, no account required.

1. **Provide the source** — drop an `.md` file, paste a citation string, URL, or DOI into the text area
2. **Review the record** — check the parsed fields in the preview panel
3. **Enrich if needed** — click Crossref or OpenAlex to fill in missing metadata
4. **Export** — download the `.ris` file and drag it into Zotero, or copy the Markdown reference

The UI is available in Russian and English (language switcher in the top-right corner of the hero band).

---

## Privacy

No data is sent to any server by default. The only network requests are the optional Crossref and OpenAlex lookups, made when you explicitly click those buttons. See [privacy.html](privacy.html) for the full policy.

---

## Licence

**Code** — [MIT](LICENSE)  
**Written content and documentation** — [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)  
**Graphic materials** (illustrations, images) — © Anna B. Agafonova, all rights reserved

---

## Author

Anna B. Agafonova, PhD  
Independent researcher · [urbantransmission.org](https://urbantransmission.org)  
ORCID: [0000-0003-3021-4002](https://orcid.org/0000-0003-3021-4002)  
Contact: a.b.agafonova@gmail.com
