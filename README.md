# 🧹 CleanLx — Data Cleaning Workbench

A powerful, fully browser-based data cleaning tool. No installation, no server, no backend — everything runs locally in your browser.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-cyan?style=flat-square)](https://dannylexi.github.io/Cleanlx/)

---

## ✨ Features

### Supported Formats
| Format | Extension |
|--------|-----------|
| CSV / TSV | `.csv` `.tsv` |
| Excel | `.xlsx` `.xls` |
| JSON | `.json` |
| Plain text | `.txt` |
| SQLite database | `.db` `.sqlite` `.sqlite3` |
| SQL dump | `.sql` |

### Cleaning Rules
- **Remove duplicates** — drop exact duplicate rows
- **Trim whitespace** — strip leading/trailing spaces from all cells
- **Title case text** — capitalise text-heavy columns
- **Fill missing values** — blanks → `N/A` (text) or `0` (numeric)
- **Remove empty rows** — drop rows where every cell is blank
- **Standardise numbers** — strip `$`, `,`, `%` from numeric fields
- **Normalise booleans** — `yes/no/1/0/true/false` → `true/false`
- **Detect date columns** — flag columns with inconsistent date formats

### Large File Chunker
Process files of any size by splitting into configurable batches (default: 50,000 rows/chunk). Clean each chunk independently, then merge and export.

### Paginated Preview
Browse raw and cleaned data with full pagination — 50 / 100 / 200 / 500 rows per page, numbered page buttons, and a jump-to-page input.

### AI Report (Gemini)
Paste a free Google Gemini API key to generate an AI-powered data quality report after each clean. Get a quality score, issue breakdown, and actionable recommendations.

> Get a free key at [aistudio.google.com](https://aistudio.google.com) → **Get API key**

### SQLite / Database Support
Drop a `.db` or `.sqlite` file — CleanLx detects all tables, shows a table selector, and lets you switch between tables without re-uploading.

### Export
Download cleaned data as **CSV**, **JSON**, or **XLSX**.

---

## 🚀 Usage

### Option 1 — GitHub Pages (recommended)
Visit the live demo link above. Nothing to install.

### Option 2 — Run locally
```bash
git clone https://github.com/DannyLexi/cleanlx.git
cd cleanlx
# Just open index.html in your browser
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

No build step, no `npm install`, no dependencies to manage.

---

## 🔒 Privacy

- **All processing happens in your browser** — your data never leaves your machine
- The only outbound request is to Google's Gemini API (only when you provide a key and run a clean)
- No cookies, no tracking, no analytics

---

## 🛠 Tech Stack

| Library | Purpose |
|---------|---------|
| [PapaParse](https://www.papaparse.com/) | CSV / TSV parsing |
| [SheetJS](https://sheetjs.com/) | Excel read/write |
| [sql.js](https://sql.js.org/) | SQLite (WebAssembly) |
| [Google Gemini API](https://aistudio.google.com/) | AI quality report (optional) |

All loaded from CDN — no bundler or build tool needed.

---

## 📁 Project Structure

```
cleanlx/
├── index.html      # The entire app — one self-contained file
└── README.md
```

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you'd like to change.

---

## 📄 License

MIT — free to use, modify, and distribute.

---

*Built by [Danny](https://github.com/DannyLexi)*
