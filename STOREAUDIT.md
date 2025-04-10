# 🧾 Store Audit – Steam Key Retailers Compatibility

This audit helps evaluate which authorized Steam key retailers may be compatible with the Alth’s Region Scanner browser extension. The goal is to determine whether the store displays accurate region restrictions and whether that data can be reliably parsed.

---

| Store             | Supported Store |Region Info Visible Before Purchase | Structured/Parsable Data | Extraction Feasibility | Notes |
|-------------------|-----------------|------------------------------------|--------------------------|----------------------|-------|
| **Fanatical**              | ✅ Yes | ✅ Yes                               | ✅ Yes                | ✅ Easy               | Already integrated. Region info presented in structured DOM — parsed from expandable field. |
| **Green Man Gaming (GMG)** | ✅ Yes | ✅ Yes                               | ✅ Yes                | ✅ Easy               | Already integrated. Region info presented in structured DOM — parsed from expandable field. |
| **GamersGate**             | ✅ Yes | ✅ Yes                               | ✅ Yes                | ✅ Easy               | Already integrated. Region info presented in structured DOM — parsed from expandable field. |
| **Humble Bundle**          | ✅ Yes | ❌ No (only after purchase)          | ✅ Yes                | ✅ Easy               | Already integrated. Region data is not visible pre-purchase. Parsed post-transaction from gift link lightbox. |
| **WinGameStore**           | ⚠️ Review | ⚠️ Review Required                | ⚠️ Review Required    | ⚠️ Review Required    | Store Review Pending. Quick check appears info available before purchase. Region info presented in structure DOM - parsable from expandable field. |
| **MacGameStore**           | ⚠️ Review | ⚠️ Review Required                | ⚠️ Review Required    | ⚠️ Review Required    | Store Review Pending. Quick check appears info available before purchase. Region info presented in structure DOM - parsable from expandable field. |
| **GamesPlanet**            | ⚠️ Review | ⚠️ Review Required                | ⚠️ Review Required    | ⚠️ Review Required    | Store Review Pending. Quick check info available before purchase in Orange Box if restrictions apply. Multiple ways info relayed, plain DOM and lightbox dependant. More review needed. |
| **DLGamer**                | ⚠️ Review | ⚠️ Review Required                | ⚠️ Review Required    | ⚠️ Review Required    | Store Review Pending. Quick check info available before purchase. DOM - parsed on hover. |
| **Nuuvem**                 | ⚠️ Review | ⚠️ Review Required                | ⚠️ Review Required    | ⚠️ Review Required    | Store Review Pending. Quick check appears info available before purchase. Parsed through toggled lightbox in (i) panel. |
| **Gamesload**              | ❌ No | ❌ No (all region ifo withheld)       | ❌ No                 | ❌ Deferred           | Store Review Pending. Withholds any regional information besides a simulated pupop by IP advising if the game is unavailable in your region.|
| **GameBillet**             | ❌ No | ✅ Yes (e.g. “ACTIVATES IN AU”)       | ❌ No (based on IP)   | ❌ Approximation Only | Shows “Activates in XX” by IP. Region must be inferred. Can't guarantee correct results. |
| **Voidu**                  | ❌ No | ✅ Yes (e.g. “ACTIVATES IN AU”)       | ❌ No (based on IP)   | ❌ Approximation Only | Hidden modal in activation area checked. Does not contain region data despite region location. Shows “Activates in XX” by IP. Region must be inferred. Can't guarantee correct results. |
| **IndieGala Store**        | ❌ No | 🟡 Sometimes                          | ❌ No                 | ❌ Deferred           | Inconsistent and unreliable region data display. Displays by IP in Regions. Region must be inferred. Inconsistent with popup warning. |

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
