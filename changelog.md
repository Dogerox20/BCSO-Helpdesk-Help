## 📅 BCSO Helpdesk Bot Changelog – [Today’s Date]

---

### 🔐 Permissions & Role Locks
- ✅ **Added rank lock** to `/clockin` and `/clockout`
  - Only users with role ID `1348493509698781216` or higher can use them.
  - If denied, the bot responds: `❌ You are not a high enough of a rank to use this command!`
  - Denied attempts are logged via the embed logger.

---

### 📤 Command Logging Enhancements
- ✅ All commands now log **every execution attempt** — success, error, or denied — as an embed in the command log channel.

---

### 📊 Status Monitoring Enhancements
- ✅ Bot presence now reflects bot mode pulled from Google Sheets:
  - `"Homepage!P16"` used to determine active deputy count.
  - `"STATUS!A2"` used to determine if bot is Online or in Maintenance.

- ✅ Updated activity messages:
  - **Online** → `Watching over [number] deputies.`
  - **Maintenance** → `Watching over maintenance operations.`

- ✅ Removed double “Watching” bug and all emoji icons from presence text.
- ✅ Fixed incorrect sheet reference (was pulling from `General-Membership`, now correctly using `Homepage`).
- ✅ Logging now posts **status change embeds** to:
  - `Channel ID: 1353567659509157968`
- ✅ Embed messages now have:
  - 🟢 Online: `"✅ The system is now Online and operational. Commands should work as intended."`
  - 🛠️ Maintenance: `"🛠️ The system has entered Maintenance Mode. Please check the status page for more information — you can locate it in the bot's About Me section."`

---

### 🆘 New Help Command
- ✅ `/help` command created.
  - DMs the user:
    ```
    https://github.com/Dogerox20/BCSO-Helpdesk-Help

    The following GitHub has all of the information related to the bot including commands and what they do, any bugs you may have please post them in <#1353567410250321950>, any suggestion you can put them in <#1353567420727693425>.
    ```

---

### 📁 Script Updates
- ✅ Rewrote and cleaned `/checkid` command with logging and better error handling.
- ✅ Updated and sent you the final versions of `clockin.js` and `clockout.js` with:
  - Rank lock
  - Logging for denied users
  - Improved formatting and stability

---
