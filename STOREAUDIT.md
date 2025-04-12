# 🧾 Store Audit – Steam Key Retailers Compatibility

This audit helps evaluate which authorized Steam key retailers may be compatible with the Alth’s Region Scanner browser extension. The goal is to determine whether the store displays accurate region restrictions and whether that data can be reliably parsed.

---

| Store             | Supported Store | Region Info Visible Before Purchase | Structured/Parsable Data | Extraction Feasibility | Notes |
|-------------------|-----------------|------------------------------------|--------------------------|------------------------|-------|
| **Fanatical**              | ✅ Yes | ✅ Yes                               | ✅ Yes                    | ✅ Easy                 | Integrated. Region data parsed directly from dropdown `<select>` inside `.regional-restrictions-modal`. Each country option is tested dynamically to determine activation outcome. Extracted via DOM traversal and classified as allow/block by result. |
| **Green Man Gaming (GMG)** | ✅ Yes | ✅ Yes                               | ✅ Yes                    | ✅ Easy                 | Integrated. Region data extracted from `<li>` items inside `.region-names` (shown after expanding “View Regions” panel). Associated phrasing parsed from adjacent `.region-warning` elements. Logic interpreted using `interpretRegionList()`. |
| **GamersGate**             | ✅ Yes | ✅ Yes                               | ✅ Yes                    | ✅ Easy                 | Integrated. Region restriction data parsed from DOM text nodes adjacent to `.product-activation-info--regions-title`. Country names extracted from text content using `parseCountriesPreservingCommas()`. Interpretation handled via `interpretRegionList()` with local heading context. |
| **Humble Bundle**          | ✅ Yes | ❌ No (only after purchase)          | ✅ Yes (ISO Provided)     | ✅ Easy                 | Integrated. Region data available post-purchase via lightbox modal on gift link page. Country list extracted from `<li>` items under `#country-list`. ISO format already used. |
| **GamesPlanet**            | ✅ Yes | ✅ Yes                               | ✅ Yes                    | ✅ Easy                 | Integrated. Region info available pre-purchase. Extracted from DOM (`.prod-notice-body`). Format varies but parsed using `parseCountriesPreservingCommas()` and `interpretRegionList()`. |
| **DLGamer**                | ✅ Yes | ✅ Yes                               | ✅ Yes                    | ✅ Easy                 | Integrated. Region data in tooltip-style `data-content` HTML inside `.product-geolock`. Parsed with `DOMParser`. Countries extracted via `parseCountriesPreservingCommas()`. |
| **Nuuvem**                 | ✅ Yes | ✅ Yes                               | ✅ Yes                    | ✅ Easy                 | Integrated. Region info available via lightbox (auto-injected in DOM). `<li>` list parsed from modal container. Assumed whitelist. Uses `parseCountriesPreservingCommas()`. |
| **WinGameStore**           | ✅ Yes | ✅ Yes                               | ✅ Yes                    | ✅ Easy                 | Integrated. Region info parsed from `#geo-locks` or `#geo-blocks`. Country names processed via `parseCountriesPreservingCommas()`. Heading used to determine blacklist/whitelist context. |
| **MacGameStore**           | ✅ Yes | ✅ Yes                               | ✅ Yes                    | ✅ Easy                 | Integrated. Similar structure to WinGameStore. Region data parsed from `#geo-locks` or `#geo-blocks` and processed via `parseCountriesPreservingCommas()`. |
| **Gamesload**              | ❌ No  | ❌ No (all region info withheld)     | ❌ No                     | ❌ Deferred             | Withholds any regional information besides a simulated popup by IP advising if the game is unavailable in your region. |
| **GameBillet**             | ❌ No  | ✅ Yes (e.g. “ACTIVATES IN AU”)       | ❌ No (based on IP)       | ❌ Approximation Only   | Shows “Activates in XX” by IP. Region must be inferred. Can't guarantee correct results. |
| **Voidu**                  | ❌ No  | ✅ Yes (e.g. “ACTIVATES IN AU”)       | ❌ No (based on IP)       | ❌ Approximation Only   | Hidden modal in activation area checked. Does not contain region data despite region location. Shows “Activates in XX” by IP. Region must be inferred. Can't guarantee correct results. |
| **IndieGala Store**        | ❌ No  | 🟡 Sometimes                          | ❌ No                     | ❌ Deferred             | Inconsistent and unreliable region data display. Displays by IP in Regions. Region must be inferred. Inconsistent with popup warning. |

---

## 🔍 Legend
- ✅ Yes – Fully supported, easily parsed. **Capable Integration**
- 🟡 Sometimes – Inconsistent regional information **Unable to guarantee accuracy**
- ❌ No – Unsupported, unavailable, unreliable or unparsable regional information.
- ⚠️ – Requires reviewing or testing.

---

## 📌 Notes
- Gray market resellers (e.g., G2A, Kinguin) are **not included** due to lack of publisher authorization and region lock reliability.
- Only authorized stores will be considered for support.
- Parsing feasibility includes the ability to access DOM data consistently - Notes will elaborate if requiring account login or purchase.
