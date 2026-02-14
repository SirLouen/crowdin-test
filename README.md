# Crowdin Translation Test

A minimal web app to test Crowdin integration with two-letter locale codes (`en`, `es`), matching the studiocms translation JSON structure.

## Quick Start

Serve the folder with any static file server:

```bash
# Python
python3 -m http.server 8080

# Node.js (npx)
npx serve .
```

Open `http://localhost:8080` and click **EN** / **ES** to switch languages.

## Structure

```
crowdin-test/
├── crowdin.yml              # Crowdin config (uses %two_letters_code%)
├── index.html               # Single-page app with language switcher
└── translations/
    ├── en.json              # English (source)
    └── es.json              # Spanish (translation)
```

## Translation Format

Matches the studiocms pattern — each JSON file has `displayName` + flat `translations` object:

```json
{
  "displayName": "English (en)",
  "translations": {
    "page-title": "Welcome to StudioCMS",
    "greeting": "Hello! This is a translation test.",
    ...
  }
}
```

## Next Step

Migrate from `%two_letters_code%` (`en`, `es`) to four-letter language-region codes (`en-us`, `es-es`).
