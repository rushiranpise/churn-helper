# Churning Helper

A clean, Material Design 3 web app to track closed accounts and their cooling periods.  
It calculates the next eligible churn date, sends browser notifications when the cooling period ends, and stores all data locally in your browser.

## ✨ Features

- **Track accounts** – Add account name, closing date, and cooling period (0–365 days).
- **Automatic calculation** – Next churn date = closing date + cooling period.
- **Days‑left indicator** – Shows “X days left”, “Today”, or “X days overdue” with colored badges.
- **Sortable columns** – Click any table header to sort by name, date, cooling period, next churn, or status. Default order is nearest churn first.
- **Responsive design** – Desktop table with sortable columns, mobile view uses vertical cards.
- **Browser notifications** – Get a system alert (like WhatsApp) when an account’s cooling period ends. Notifications are sent once per period and re‑checked hourly.
- **Local persistence** – All entries are saved to `localStorage`. Data remains after closing the browser.
- **Collapsible add form** – The “Add New” section is collapsed by default to save space. Click the header to expand.
- **Edit / Delete** – Each entry has edit and delete buttons.
- **Clear all data** – One‑click button to wipe everything (with confirmation).

## 📱 Mobile view

On screens narrower than 600px, the table transforms into a vertical card layout – each card contains all fields and the edit/delete buttons. The sorting order is preserved.

## 🔔 Notifications

- Notifications require your permission. Click the bell icon and allow.
- Once enabled, the app checks for ended cooling periods:
  - On page load
  - After adding / editing / deleting an entry
  - Every 60 minutes while the page is open
- You will receive only **one notification per ended period** (no spam).
- The notification icon and message include the account name and the date the cooling period ended.

## 🧰 Technical details

- **Pure HTML/CSS/JS** – No external dependencies (except Google Fonts and Material Icons).
- **UTC date handling** – All dates are stored and compared in UTC to avoid timezone errors.
- **LocalStorage keys**:
  - `churning_helper_data` – stores all entries.
  - `churning_last_notified` – tracks which accounts have already triggered a notification.
- **Sorting** – Uses a custom sort function; default is “next churn” ascending (soonest first).

## 📄 License

Feel free to use, modify, and share this project. No attribution required.

---

**Enjoy never missing a churn opportunity again!** 🚀