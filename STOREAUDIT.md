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
| **MacGameStore**           | ⚠️ Review | ⚠️ Review Required                | ⚠️ Review Required    | ⚠️ Review Required    | Store Review Pending. |
| **GamesPlanet**            | ⚠️ Review | ⚠️ Review Required                | ⚠️ Review Required    | ⚠️ Review Required    | Store Review Pending. |
| **DLGamer**                | ⚠️ Review | ⚠️ Review Required                | ⚠️ Review Required    | ⚠️ Review Required    | Store Review Pending. |
| **Direct2Drive**           | ⚠️ Review | ⚠️ Review Required                | ⚠️ Review Required    | ⚠️ Review Required    | Store Review Pending. |
| **Voidu**                  | ⚠️ Review | ⚠️ Review Required                | ⚠️ Review Required    | ⚠️ Review Required    | Store Review Pending. |
| **Nuuvem**                 | ⚠️ Review | ⚠️ Review Required                | ⚠️ Review Required    | ⚠️ Review Required    | Store Review Pending. Quick check appears info available before purchase. Parsed through toggled lightbox in (i) panel. |
| **Gamesload**              | ⚠️ Review | ⚠️ Review Required                | ⚠️ Review Required    | ⚠️ Review Required    | Store Review Pending. |
| **GameBillet**             | ❌ No | ✅ Yes (e.g. “ACTIVATES IN AU”)       | ❌ No (based on IP)   | ❌ Approximation Only | Shows “Activates in XX” by IP. Region must be inferred. Can't guarantee correct results. |
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
