# 🔑 CoreshiftStudiosCodeChecker

CoreshiftStudiosCodeChecker is a secure, lightweight Discord bot designed to bridge Discord slash commands directly with your Roblox experience using the official **Roblox Open Cloud API**. It allows authorized staff to generate promo codes via Discord that instantly update your game's data stores, and allows users to safely check code validity.

---

## ✨ Features
* 🛠️ **`/createcode`**: Staff command to generate custom promo codes linked to specific reward IDs.
* 🔍 **`/checkcode`**: Public or staff command to verify if a code is currently active and see its rewards.
* 📦 **Roblox Open Cloud Integration**: No flaky, unsecure external web servers or proxies required—updates write directly to Roblox `DataStores`.
* 📜 **Automated Logging**: Tracks code validations to keep your moderation team in the loop.

---

## 🚀 Quick Start & Setup

### 1. Prerequisites
Make sure you have [Node.js](https://nodejs.org) (v16.x or higher) installed on your machine or hosting environment.

### 2. Installation
Clone or download this repository, navigate to the folder, and install the required dependencies:
```bash
npm install discord.js
```

### 3. Environment Configuration
Create a configuration block or `.env` file in your project with the following credentials:
```javascript
const DISCORD_TOKEN = 'YOUR_DISCORD_BOT_TOKEN';
const CLIENT_ID = 'YOUR_BOT_CLIENT_ID';
const ROBLOX_API_KEY = 'YOUR_ROBLOX_API_KEY';
const UNIVERSE_ID = 'YOUR_ROBLOX_UNIVERSE_ID'; 
const DATASTORE_NAME = 'GlobalPromoCodes';
```

### 4. Running the Bot
Launch the script to register your slash commands and start listening for interactions:
```bash
node index.js
```

---

## 🛠️ Roblox Game Integration
To sync this bot with your Roblox place, make sure **Enable Studio Access to API Services** is toggled on under your Game Settings ➡️ Security. Use a script inside `ServerScriptService` to read from the `"GlobalPromoCodes"` DataStore using `DataStoreService:GetDataStore()`.

---

## ⚖️ Legal & Compliance
By utilizing this bot, you agree to comply with Discord's Developer Terms of Service and Roblox's Terms of Use.

* 📄 [Terms of Service](terms.html)
* 🔒 [Privacy Policy](privacy.html)

---

## 🤝 Support
Managed and developed by **Coreshift Studios**. For bugs, feedback, or custom integrations, open an issue in this repository or contact us via our Discord community.
