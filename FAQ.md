# ❓ FAQ – Alth’s Region Scanner

Frequently Asked Questions about the usage, behavior, and goals of the Alth’s Region Scanner browser extension.

---

## 🔍 What does this extension do?
This tool scans supported Steam key storefronts (Fanatical, Humble Bundle, Green Man Gaming, GamersGate, GamesPlanet, DLGamer, Nuuvem, WinGameStore, and MacGameStore) to extract visible region restriction information. It formats the results as ISO 3166-1 alpha-2 country codes to assist in creating accurate SteamGifts giveaways.

---

## 🌍 What are "allowed," "blocked," and "filtered" regions?
- **Allowed regions**: Countries where a key can be activated.
- **Blocked regions**: Countries where a key cannot be activated.
- **Filtered regions**: Countries removed from the final output because SteamGifts does not currently support them.

---

## 📦 Why are some countries filtered out?
This extension filters unsupported ISO codes from the output to prevent copy/paste errors when setting giveaway region restrictions using the TamperMonkey script provided by Lex. Filtered countries are still displayed at the bottom of the output page with explanations.

---

## 🛒 How do I use the output?
- Use the popup, toolbar button, or hotkey (Ctrl+Shift+F) to scan a supported store page.
- Open the region restriction lightbox if required (e.g., Fanatical, GamesPlanet).
- Copy the "Allowed" or "Blocked" region ISO codes.
- Paste the results into the SteamGifts Region Helper Tampermonkey script when creating a giveaway.

---

## 🔄 Why are the results wrong on some games?
Some stores use inconsistent or ambiguous phrasing, such as:
- "This key is **only available** in..."
- "This key **will not activate** in..."

The extension uses logic to interpret phrasing and infer whether a region list is a whitelist or blacklist. Unexpected formats may still appear and may require a patch. Please report them for review.

---

## 🧪 Can I use this with other stores like IndieGala?
Currently, IndieGala and similar stores are not supported due to the lack of reliably structured, visible region data.

This does not rule out future support — if IndieGala updates its interface to clearly present this information in a consistent, parseable way, it can be added.

---

## 🕵️ Does this extension collect any data?
**No.** This extension:
- Does not collect, transmit, or store any personal data.
- Does not track your browsing activity.
- Only activates on specifically supported storefront domains.

### 🛡️ Store-Specific Behavior
For example, Fanatical's region data must be manually opened by the user — the extension only reads data that is already in the DOM (on the page). It does not scrape or probe any private APIs or backend data. 

---

## 💬 Where can I ask questions or suggest features?
- Open an issue on the [GitHub repository](https://github.com/Altha-ego/Alth-s-Region-Scanner)
- Or post in the [SteamGifts discussion thread]() **Will add link to discussion thread when created**

---

## 🧠 Why did I create this tool?
I originally tracked key data manually using Excel — noting region restrictions, supported stores, and matching ISO codes for SteamGifts giveaways. I later found Lex’s Tampermonkey script that automated region box entries on SteamGifts, so I built a converter formula in Excel to map country names to ISO codes.

Eventually, I got sick of typing country names altogether — and this tool was born.

It might take longer to develop, but in the long run, it saves *a lot* of time.

---

## 🙌 Credits
- Created by **Althalus** for the SteamGifts community
- For use with the **SteamGifts Region Helper** Tampermonkey script by **Lex**
