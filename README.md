# Receipt Generator — The Paper Conservation Studio

A single-page web app for generating professional conservation receipts as PDFs.

## Files

- `index.html` — The entire application (HTML, CSS, JS in one file)
- `receipt_template.html` — Styled template used for the on-screen review preview in Step 4

## Features

- 4-step wizard: Receipt Info → Client Details → Items → Review
- Supports multiple items per receipt (auto-labelled A, B, C…)
- Image upload with EXIF orientation correction and manual rotation
- Agreed next steps with optional pricing
- PDF generation via jsPDF (no server required)
- Share via WhatsApp or Email directly from the app

## Usage

Because the app fetches `receipt_template.html` for the review preview, it needs to be served over HTTP rather than opened directly as a local file.

### Option 1 — VS Code Live Server
Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension, right-click `index.html`, and choose **Open with Live Server**.

### Option 2 — Python
```bash
python -m http.server 8080
```
Then open `http://localhost:8080` in your browser.

## Dependencies (CDN)

| Library | Purpose |
|---|---|
| [Tailwind CSS](https://tailwindcss.com/) | UI styling |
| [jsPDF 2.5.1](https://github.com/parallax/jsPDF) | PDF generation |
| [piexif.js](https://github.com/hMatoba/piexifjs) | EXIF orientation fix on image upload |
