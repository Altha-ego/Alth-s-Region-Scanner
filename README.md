#  Alth's Region Scanner

A browser extension that helps users quickly extract **region lock information** for Steam keys from popular game stores.

Built for the [SteamGifts](https://www.steamgifts.com/) community — this tool is especially useful when creating **region-restricted giveaways**.

Built to work, for convenience, directly with TamperMonkey and the script previously provided by Lex

Installation information provided below.

---

##  Currently Supported Stores

- ✅ Fanatical
- ✅ Humble Bundle
- ✅ Green Man Gaming
- ✅ GamersGate

---

##  Features

- 🧩 Scans region restriction data
- 🌍 Outputs **allowed**, **blocked** and **Filtered** region codes
- 📋 Optimized for SteamGifts + Tampermonkey integration
- 💻 Dark-themed popup for easy copy/paste
- ⌨️ Shortcut-based (Ctrl + Shift + F) or via addon toolbar
- 🔍 Works per-site — does not run on unsupported stores

---

##  How to Install (Firefox and Chrome)

1. The extension is available for:
	Firefox Add-ons:  WillUpdateWhenAvailable
	Chrome Web Store: WillUpdateWhenAvailable
	
2. Click **Add to Firefox** or **Add to Chrome**

---

##  How to Use It

Visit one of the currently supported stores and follow these instructions:

**Note - You may need to allow pop-ups on the store site for this to work**
This only effected me a couple of times but still.

---

### 🟠 Fanatical

1. Open any **store game page**
2. Click **"View All"** under the "Activates In" section
3. Click on the **first Country** in the list (i.e Afghanistan)
4. Press **Ctrl + Shift + F** or open the extension and click **Scan Now**
5. The Add-on will automatically go through the countries, then,
6. A new tab will open displaying the ✅ allowed and ❌ blocked regions

---

### 🟡 Humble Bundle

1. In you store **Keys and Entitlements** select **Gift to a friend**
2. If any **Region Restrictions** are shown on the **Gifting this Item** pop-up box,
3. Press **Ctrl + Shift + F** or open the extension and click **Scan Now**
4. A new tab will open displaying the ✅ allowed and ❌ blocked regions

---

### 🟢 Green Man Gaming

1. On a **store game page**, click **"View Regions"**. After the list loads,
2. If any regions are shown press **Ctrl + Shift + F** or open the extension and click **Scan Now**
3. The extension uses its helper to convert country names to ISO codes
4. A new tab will open displaying the ✅ allowed and ❌ blocked regions

> ⚠️ If you see: _"Please expand the 'View Regions' section first."_, and the region info displays "This title will redeem in your region of purchase"
the addon will stop as I don't know what this means HAHAHA I only saw it on a couple of games but I have no clue and I'm not messaging GMG to find out ^^

---

### 🔵 GamersGate

1. Open any game page and click **"Show Regions"**
2. Once visible, press **Ctrl + Shift + F** or open the extension and click **Scan Now**
3. The extension uses its helper to convert country names to ISO codes
4. A new tab will open displaying the ✅ allowed and ❌ blocked regions

---

**Users are responsible for ensuring restrictions are correct when creating giveaways on SteamGifts.**
##     How to Use with SteamGifts + Tampermonkey

1. **Install [Tampermonkey](https://www.tampermonkey.net/)**
2. **Install the [SteamGifts Region Lock Helper Script](https://greasyfork.org/en/scripts/520676-steamgifts-region-helper)**
3. When creating a region restricted giveaway:
   - Check ✅ **"Region Restricted"**
   - Use one of the two methods below:

**Users are responsible for ensuring restrictions are correct when creating giveaways on SteamGifts.**

---

### ✅ Method 1: Allowed List
- Paste the ✅ allowed region codes into the helper box on the Create a Giveaway page (TamperMonkey script by Lex)
- Click **"Add Regions"**

### ❌ Method 2: Blocked List
- Click **"Select All"** on SteamGifts
- Paste the ❌ blocked regions into the helper box on the Create a Giveaway page (TamperMonkey script by Lex)
- Click **"Remove Regions"**

---

## 🔧 Developer Notes

- **Manifest v3** (for Chrome)
- **Manifest v2** (for Firefox)
- Uses **DOM scraping** and **content scripts**
- Handles **variant country names** converting them to their ISO codes
- Fully modular and ready for additional stores in future updates
- Filters output results to only display input option available on SteamGifts GA creation


---

##  Disclaimer

This tool **does not modify store content**, **it does not collect, store or send any data** and **does not automate purchases**.

It reads visible region data only. 

**Users are responsible for ensuring restrictions are correct when creating giveaways on SteamGifts.**

---

##  Credits

Created by **Althalus** for the **SteamGifts community.**
*Inspired by hundreds of region-locked giveaways*

TamperMonkey Script **SteamGifts Region Helper** created for the **SteamGifts** community by **Lex**
**[SteamGifts Region Helper](https://www.steamgifts.com/discussion/0cMuP/steamgifts-region-helper)**
