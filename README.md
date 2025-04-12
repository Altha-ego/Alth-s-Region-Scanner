# 🎮 Alth's Region Scanner

A browser extension that extracts **region restriction data** from supported Steam key stores to help create accurate giveaways on [SteamGifts](https://www.steamgifts.com/).

Built for convenience and made to work directly with **Tampermonkey** + **Lex’s SteamGifts Region Helper** script.

---

## 🛒 Supported Stores

- ✅ Fanatical  
- ✅ Humble Bundle  
- ✅ Green Man Gaming  
- ✅ GamersGate  
- ✅ GamesPlanet (.com, .uk, .fr)  
- ✅ Nuuvem  
- ✅ DLGamer  
- ✅ WinGameStore  
- ✅ MacGameStore  

---

## ✨ Features

- 🔍 Scans visible region restriction info from store pages
- 📦 Outputs ISO 3166-1 alpha-2 codes: ✅ **Allowed**, ❌ **Blocked**, ⚠️ **Filtered**
- 💾 Uses logic to interpret phrases like "will activate in" / "won't activate in"
- 📋 Copy-to-clipboard buttons for region code output
- 🧠 Country name resolver for inconsistently named countries ("Côte d’Ivoire", "Ivory Coast")
- 🖱️ Runs via toolbar popup, keyboard shortcut (`Ctrl+Shift+F`), or scan button
- 🌙 Clean, dark-themed UI
- ⚙️ Manifest V2 (Firefox) + Manifest V3 (Chrome-ready)
- 🔒 Does **not** access backend APIs, personal data, or perform automatic actions

---

## 🚀 Installation

This extension will be available on:

- [Firefox Add-ons](https://addons.mozilla.org/) *(Coming Soon)*
- [Chrome Web Store](https://chrome.google.com/webstore) *(Coming Soon)*

---

## 🧪 How to Use

> ⚠️ You may need to **enable popups** for the scan results to open.

1. Open a supported store page
2. On pages with modals (e.g. Fanatical, GamesPlanet), open the **region restriction box**
3. Use either:
   - Toolbar ➜ Click **Scan Now**
   - Or press **Ctrl + Shift + F** (keyboard shortcut)
4. A new tab will open showing:
   - ✅ Allowed ISO regions
   - ❌ Blocked ISO regions
   - ⚠️ Filtered countries not supported on SteamGifts

---

## 🎁 SteamGifts + Tampermonkey Integration

1. Install [Tampermonkey](https://www.tampermonkey.net/)
2. Install [SteamGifts Region Helper](https://greasyfork.org/en/scripts/520676-steamgifts-region-helper) by Lex
3. When creating a giveaway:
   - Tick ✅ “Region Restricted”
   - Choose a method:

### ✅ Method 1 – Allow List

- Paste the **Allowed Regions**
- Click **Add Regions** in Lex's helper

### ❌ Method 2 – Block List

- Click **Select All** on SteamGifts
- Paste the **Blocked Regions**
- Click **Remove Regions** in Lex's helper

---

## 🔧 Developer Notes

- Written in vanilla JavaScript with full DOM traversal support
- Uses `parseCountriesPreservingCommas()` to handle inconsistent country formatting
- Includes `country-helper.js` for mapping real-world names to ISO codes
- Uses `steamgifts-region-filter.js` to exclude unsupported countries automatically
- Fully modular content scripts (per store) for easy updates

---

## 📄 Project Documentation

- [📘 FAQ](./FAQ.md)  
- [📦 Changelog](./CHANGELOG.md)  
- [📌 Supported Store Audit](./STOREAUDIT.md)  
- [📝 TODO](./TODO.md)  
- [🤝 Contributing](./CONTRIBUTING.md)  
- [📄 License](./LICENSE.md)  

---

## 🛑 Disclaimer

This extension:
- Does **not** track your data or activity
- Does **not** access private store APIs
- Only processes data that's visible in the DOM
- Only activates on whitelisted storefronts

Users are **responsible** for verifying region data before submitting a SteamGifts giveaway.

---

## 🙌 Credits

- 🛠️ Developed by **Althalus** for the SteamGifts community  
- 🧠 Uses [Lex’s SteamGifts Region Helper Script](https://www.steamgifts.com/discussion/0cMuP/steamgifts-region-helper)

---

_“If it saves me typing a country name, it’s already a win.”_

