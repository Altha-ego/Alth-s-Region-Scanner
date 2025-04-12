# ✅ TODO – Alth’s Region Scanner

This file tracks upcoming features, bugs, enhancements, and developer tasks planned for future updates of the extension.

---

## 🐞 Bugs / Known Issues

### 1. Humble Bundle – Inconsistent Phrasing
- Gift links show either:
  - "This key is **only available** in..."
  - "This key is **not available** in..."
- 🔧 Logic must parse these and reverse accordingly
- Status: ✅ Fixed (verified via `interpretRegionList()` logic updates)

### 2. GamesPlanet – Modal Region Info Box
- Some games use a lightbox with text “See full list of country restrictions”
- Previously ignored in scans — now supported via fallback
- Status: ✅ Implemented (scans fallback modal `#modal_regionlocks_details`)

### 🧠 Country Override Mapping (Store-specific normalization)

- Create an `overrideMap` system for converting store-specific country aliases 
  to standardized `country-helper.js` entries  
  _(e.g., `Czechia` → `Czech Republic`)_
- Reduces redundancy in `countryToISO` mapping table
- Improves accuracy when multiple phrasing variants exist for the same country across stores
- Status: 


---

## ✨ Features & Enhancements

### 1. 🆕 Output UI Enhancements
- 📋 Add "Copy" buttons next to Allowed and Blocked sections (✅ Done)
- Move output into `output.html` to separate concerns (✅ Done)
- Removed scan button from output page for clarity (✅ Done)
- Removed duplicated output of ISOs caused by repeated entries in `country-helper.js` using `dedupe(array)` (✅ Done)
- Toolbar scan button and supported stores (hyperlinked) configured in `popup.html` (✅ Done)

### 2. Additional Store Support (TBD)
- IndieGala: unreliable / partial info (Deferred)
- GameBillet / Voidu: based on IP geolocation (Low feasibility - Must infer definition of "Region")
- Add: detection stubs or partial fallback warnings for unsupported formats

### 3. UX & UI Settings (Planned)
- ⏳ Option to toggle auto-scan on page load (When 3rd party input not required)
- ⏳ Highlight region sections on store pages
- ⏳ "Manual Mode" toggle to adjust region output before copy (Creation of pre-defined region copying)

---

## 🧪 Dev / Engineering Tasks

- [ ] Test harness for new region parsing modes
- [ ] Unified error handler for all store scanners
- [ ] Create store-specific override map if country names mismatch
- [ ] CI-ready config for linting / syntax checking before PRs
- [ ] Chrome Manifest V3 compatibility: inline script blocker workaround (✅ mitigated by moving to external script tags)

---

## 📚 Documentation

- [x] CHANGELOG.md (Complete history with 1.0.0 detail)
- [x] FAQ.md (Expanded with clearer phrasing + examples)
- [x] README.md (Rewritten with full usage details)
- [x] STOREAUDIT.md (Audited all supported stores + status)
- [x] Short "How to Contribute" guide for GitHub
- [ ] Add screenshots / walkthroughs to README


---

## ✅ Recently Completed

- [x] Country name normalization via `country-helper.js`
- [x] ISO code filtering for SteamGifts compatibility `steamgifts-region.filter.js`
- [x] Scan via toolbar popup, and shortcut (Ctrl+Shift+F)
- [x] Firefox + Chrome support with manifest handling
- [x] Full visual overhaul with dark theme and usability focus
- [x] GitHub repository structure, documentation, and issue tracking

