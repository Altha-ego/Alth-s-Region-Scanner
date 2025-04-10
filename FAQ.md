# ❓ FAQ – Alth’s Region Scanner

Frequently Asked Questions about the usage, behavior, and goals of the Alth’s Region Scanner browser extension.

---

## 🔍 What does this extension do?
This tool scans supported Steam key storefronts (Fanatical, Humble Bundle, Green Man Gaming, GamersGate) to extract visible region restriction information. It formats the results as ISO 3166-1 alpha-2 country codes to assist in creating accurate SteamGifts giveaways.

---

## 🌍 What are "allowed" and "blocked" regions?
- **Allowed regions**: Countries where a key can be activated.
- **Blocked regions**: Countries where a key cannot be activated.
- **Filtered regions**: Countries removed from the final output because SteamGifts does not currently support them.

---

## 📦 Why are some countries filtered out?
This extension filters unsupported codes from the output to prevent copy/paste errors when setting giveaway region restrictions using the TamperMonkey script provided by Lex. Filtered countries are still displayed for transparency.

---

## 🛒 How do I use the output?
- Use the popup or hotkey (Ctrl+Shift+F) to scan a supported store page.
- Copy the "Allowed" or "Blocked" region codes.
- Paste the results into the SteamGifts Region Helper Tampermonkey script when creating a giveaway.

---

## 🔄 Why are the results wrong on some Humble Bundle games?
Humble displays region data using different phrasings like:
- "This key is **only available** in..."
- "This key is **not available** in..."

The extension determines logic based on these phrases, but inconsistencies or new formats may occasionally require updates. Report any issues found and I'll attempt to rectify them.

---

## 🧪 Can I use this with other stores like IndieGala?
Currently, IndieGala and similar stores are not supported because they do not expose reliable or structured region restriction data that can be consistently parsed. 
This doesn't exclude all stores however, I just need to find which stores can be added, and if IngieGala updates their format in the future, support for it could be added as well.

---

## 🕵️ Does this extension collect any data?

No. This extension does not collect, transmit, or store any personal or usage data.

It does not activate or interact with any websites beyond the specifically supported storefronts (Fanatical, Humble Bundle, Green Man Gaming, GamersGate). On unsupported sites or unscannable pages, it remains inactive.

### 🛡️ Store-Specific Behavior

For example, the extension is fully compatible with Fanatical and has received direct permission from the Fanatical team after internal testing or veiwing.

To function correctly, the user must open the region info lightbox on a Fanatical product page — the extension only processes data that is already presented by the store in the DOM. It does not access anything hidden or backend-related.

In this sense, the extension is only functional when access to region restriction data is already publicly visible and user-triggered.


---

## 💬 Where can I ask questions or suggest features?
Open an issue on the GitHub documentation repository or visit the SteamGifts discussion thread where the tool was originally introduced.

---

## 🧠 Why did I create this tool?
I created this as normally I have an Excel spreadsheet with information about my product keys that I haven't activated yet. This includes what store it's from, any regional restrictions, and more.
I don't overly use steamDB to advise me of regional information details as it has proven wrong to me in the past. However this information is given to me by the stores, and so far, the store information hasn't cause issues or been incorrect.

So I manually would write or type the restrictions onto either a notepad or the excel spreadsheet. This got annoying, so I found the script Lex created for the box to be added for Giveaways using country ISO codes.
I then created a lookup table in my excel spreadsheet and a new column using a formula to change my countries listed in column A to output in column B converting things like Afghanistan, Australia to AF, AU.

Then I got sick of manually typing every country name. So, this tool was born. I'm lazy so I like to make things I do easier. Might take longer to begin with, but will save so much time in the end.

---

## 🙌 Credits
- Created by **Althalus** for the SteamGifts community
- For use with the **SteamGifts Region Helper** Tampermonkey script by Lex

