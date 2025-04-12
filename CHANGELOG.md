# 📦 Changelog – Alth’s Region Scanner

All notable changes to this project will be documented in this file.  
This project adheres to [Semantic Versioning](https://semver.org/).

---

## [1.0.0] – 2025-04-09
### Implemented
- Clipboard copy buttons added beside **Allowed** and **Blocked** region outputs
- Support for GamesPlanet modal-based region restriction lightboxes (`#modal_regionlocks_details`) when applicable
- Output display migrated to standalone `output.html` to separate UI from scan logic
- Removed scan button from output screen to eliminate UX confusion
- Parsing logic enhanced to correctly distinguish phrases such as:
  - *Will activate in...*
  - *Will NOT activate in...*
  - *Can only be activated in...* (and similar variants)
- Added `country-helper.js`: a modular mapping of country names and variations (e.g., "Curacao" vs. "Curaçao")
- Filtering integrated using `steamgifts-region-filter.js` to exclude unsupported ISO codes on SteamGifts

### Fixed
- Removed dependency on `clipboardWrite` by using the modern `navigator.clipboard` API
- Resolved Firefox CSP violations by removing inline `<script>` logic and isolating behavior to `output-handler.js`
- Enhanced fallback parsing for GamesPlanet's non-standard region strings
- Added `parseCountriesPreservingCommas()` to safely match countries while preserving comma-containing names (e.g., "Congo, Democratic Republic of")

---

### Initial Release Scope
- Scans region restrictions from the following supported stores:
  - Fanatical
  - Humble Bundle
  - Green Man Gaming
  - GamersGate
  - GamesPlanet (.com / .co.uk / .us variants)
  - DLGamer
  - Nuuvem
  - WinGameStore
  - MacGameStore

> 💡 *Note: This tool does not support unauthorized or grey-market resellers.*

### Features
- Region output categorized into **Allowed**, **Blocked**, and **Filtered** lists using ISO country codes
- Designed to support SteamGifts giveaway creation workflows
- Whitelist/blacklist logic driven by readable language in each store’s UI
- Tampermonkey-compatible output with Lex's **SteamGifts Region Helper** script
- Modern popup UI with:
  - Scan trigger
  - Supported store list
  - Dynamic styling and layout for readability
- Public GitHub documentation:
  - `README.md`
  - `CHANGELOG.md`
  - `TODO.md`
- Firefox Manifest V2 compatible (Manifest V3 support planned for Chrome)

---
