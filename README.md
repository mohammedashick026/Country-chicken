## Country Chicken – POS & Billing Web App

Simple single–page web app for a **chicken center shop** with menu, cart, billing, Excel export, and monthly sales reports, built using **HTML, CSS, and JavaScript only** (no backend).

### Features

- **Clean UI**
  - Orange themed background and responsive layout
  - Sections: `Menu`, `Cart`, `Manage`, `Reports`

- **Menu**
  - Default items: 250g, 500g, 750g, 1kg chicken
  - Each item shows image, weight, price
  - Click an item to add it directly to the cart

- **Cart & Billing**
  - Increase / decrease quantity, remove when quantity reaches 0
  - Cart total updates automatically
  - **Pay Now** opens a modal with total amount
  - **Generate Bill** downloads an **Excel (.xlsx)** bill file

- **Sales & Reports**
  - Each bill is saved as a “sale” in browser `localStorage`
  - Monthly report view with:
    - List of bills, items, totals
    - Summary: total bills, total items sold, total revenue
  - Export monthly report to **Excel (.xlsx)**
  - **Clear Reports** button to delete all saved sales data

- **Menu Management (CRUD)**
  - Add new menu items (name, weight, price, image URL)
  - Edit existing items
  - Delete items
  - All changes are stored in `localStorage`

### Tech Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript (no frameworks)
- **Storage**: Browser `localStorage`
- **Libraries (CDN)**:
  - `xlsx` (SheetJS) – Excel export for bills and reports

### Project Structure

```text
chicken center/
├─ index.html        # Main single-page app
├─ styles.css        # Styling and layout
├─ script.js         # App logic (menu, cart, billing, reports)
├─ BISMILLAH COUNTRY CHICKEN.jpg  # Favicon / logo (used in <head>)
└─ README.md         # Project documentation
```

### How to Run

1. **Download or copy** the project folder to your computer.
2. Make sure the files listed above are in the same folder.
3. Open `index.html` in a modern browser (Chrome / Edge / Firefox).
   - You can simply double–click `index.html`, or
   - Right–click → “Open with” → select your browser.

No server or installation is required; everything runs in the browser.

### Usage Guide

- **Menu tab**
  - Click any chicken item card to add it to the cart.

- **Cart tab**
  - Use `+` and `–` to change quantity.
  - Click **Clear Cart** to empty the cart.
  - Click **Pay Now** to open the payment modal.
  - Click **Generate Bill** to download an Excel bill and record the sale.

- **Manage tab**
  - Click **Add New Item** to create a new menu entry.
  - Use **Edit** to change item details.
  - Use **Delete** to remove an item.

- **Reports tab**
  - Select a month using the month picker.
  - View monthly summary and bill list.
  - Click **Export to Excel** to download the report.
  - Click **Clear Reports** to erase all stored sales data.

### Data Persistence

The app uses browser `localStorage` keys:

- `chickenCenterMenu` – menu items (CRUD managed)
- `chickenCenterCart` – current cart contents
- `chickenCenterSales` – all completed sales (used for reports)

Clearing your browser storage or using a different browser / device will reset the data.

### Notes / Customization

- **Prices & Weights**: You can change default items in `script.js` (`initializeMenu()`).
- **Branding**: 
  - Title and header text are set in `index.html`.
  - Favicon/logo image is set via:
    - `<link rel="icon" href="BISMILLAH COUNTRY CHICKEN.jpg?v=1">`
- **Currency**: Currently formatted for Indian Rupees (₹) and `en-IN` locale; you can change currency symbols and locales in `script.js` if needed.

### Limitations

- No real payment integration (the **Pay Now** button only shows total and leads to bill generation).
- All data is **local to the browser**; clearing cache or using a different device will lose data.


