# DocCompare Pro — Cross-Format Document & Typographical Diff Engine

DocCompare Pro is a zero-dependency, browser-based document comparison engine designed to detect textual discrepancies, typographical shifts, and layout anomalies between heterogeneous file formats (Word `.docx`, PDF `.pdf`, HTML, and plain text).

🔗 **Live Demo:** [Launch DocCompare Pro](https://pavithran-23-ak.github.io/DocCompare-Pro/)

---

## Key Features

- **Multi-Format Extraction:** Direct client-side parsing of `.docx` (via Mammoth.js) and `.pdf` (via PDF.js) without backend file uploads.
- **Granular Typographical Auditing:**
  - Font styling: Bold, Italic, Underline, and Strikethrough.
  - Positioning: Subscripts ($H_2O$) and Superscripts ($12^{th}$).
  - Font sizing discrepancies normalized to points (pt).
  - Casing mutations, whitespace gaps, line breaks, and tab indentation.
  - Ligature (`fi`, `fl`) and Private Use Area (PUA) bullet-point mapping.
- **PDF Formatting Restoration Engine:** Cross-references plain-text PDF clipboard extracts with raw document streams to re-attribute bold/italic styles and offsets.
- **Dual Visual Modes:** Side-by-side split comparison and unified inline stream diff views.
- **Native Excel Audit Generation:** Generates styled `.xlsx` audit reports with auto-filters and status validation dropdowns via pure client-side XML/ZIP construction.

---

## Technical Architecture

- **Core Algorithm:** Sequence diff combining prefix/suffix trimming, Longest Common Subsequence (LCS), and Patience diff anchors for handling high-volume documents.
- **DOM Sanitization:** Headless iframe isolation to resolve styles, CSS inheritance, and spacing prior to tokenization.
- **Tokenization:** Unicode-aware regular expression engine matching words, punctation, and layout markers.
- **Tech Stack:** Vanilla JavaScript (ES6+), HTML5, Tailwind CSS, PDF.js, Mammoth.js.

---

## Getting Started

1. Clone the repository:
   ```bash
   git clone [https://github.com/pavithran-23-ak/DocCompare-Pro.git](https://github.com/pavithran-23-ak/DocCompare-Pro.git)
