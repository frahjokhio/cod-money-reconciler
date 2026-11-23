# COD Money Reconciler (COD Ledger)

A polished, lightweight **Cash on Delivery (COD) reconciliation tool** designed for online sellers and e-commerce merchants in Pakistan.

Online merchants receive payments through multiple courier companies (TCS, Leopards, PostEx, etc.). This dashboard gives sellers a clear, single view to compare internal order invoices with courier statement payouts, automatically flag payment shortages, and track pending settlements.

---

## ⚡ Quick Start

No build step, Node, or server required! 

1. **Clone the repository:**
   ```bash
   git clone https://github.com/frahjokhio/cod-money-reconciler.git
   cd cod-money-reconciler
   ```

2. **Run the app:**
   * **Option 1:** Simply double-click **`index.html`** to open it directly in any modern web browser (Chrome, Edge, Firefox, Safari).
   * **Option 2:** Run a local lightweight HTTP server:
     ```bash
     # Python 3
     python -m http.server 3000

     # Node (npx)
     npx serve .
     ```
     Then open `http://localhost:3000` in your browser.

---

## 🎯 Key Features

* **Automated Reconciliation Math:** Compares order invoice amounts against courier settlement deposits. If a courier underpays, the app automatically flags it as **Mismatch** (with the exact deficit highlighted in red).
* **Dynamic Client-Side CSV Import:** Upload any courier statement (`.csv`). The app instantly parses all records, incorporates new customers, and recalculates totals on the fly.
* **100% Private & Offline:** All parsing, matching, and metric calculations run entirely client-side inside your browser. No data or contact details are sent to external servers.
* **Executive Summary Cards:**
  * **Total COD Expected:** Total gross revenue expected from shipments.
  * **Received:** Total confirmed payouts deposited into the bank account (with settlement percentage).
  * **Pending Settlement:** Shipments currently inside courier payout cycles.
  * **Discrepancies:** Count of mismatched orders requiring seller dispute, along with total rupee shortfall.
* **Live Status Filters & Search:** Instantly filter orders by status (*All*, *Settled*, *Pending*, *Mismatch*) or search in real time by Order ID, Customer Name, or Courier.

---

## 📁 Sample CSV Format

The reconciler accepts standard courier settlement CSV exports. A sample file is included in the root directory: [`cod-courier-statement-sample.csv`](cod-courier-statement-sample.csv).

| AWB_Number | Order_ID | Customer_Name | Courier | Order_Amount | Courier_Settled | Difference | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `TCS-89214701` | `#COD-1048` | Ayesha Khan | TCS | 4500 | 1500 | 3000 | Mismatch |
| `LBN-33918202` | `#COD-1047` | Ahmed Ali | Leopards | 3200 | 0 | 3200 | Pending |
| `TCS-89214703` | `#COD-1046` | Sara Malik | TCS | 5000 | 4500 | 500 | Mismatch |
| `LBN-33918204` | `#COD-1045` | Bilal Shah | Leopards | 2800 | 2800 | 0 | Settled |

---

## 🎙️ 60–90 Second Screen Recording Script

Use this structured walkthrough for quick product demos or video pitches:

1. **The Problem (0:00–0:15):**  
   *"Online merchants in Pakistan receive bulk COD disbursements through multiple courier companies. Without automated reconciliation, it is difficult to spot unpaid parcels or courier deductions."*
2. **Dashboard Overview (0:15–0:30):**  
   *"The COD Ledger dashboard instantly highlights critical numbers: Total Expected COD, money cleared to bank, amounts pending in courier payout cycles, and payment discrepancies."*
3. **Filtering Discrepancies (0:30–0:50):**  
   * Click **Pending** to view shipments awaiting payout.
   * Click **Mismatch** to spotlight shortfalls (e.g. order `#COD-1048` where TCS deposited Rs 1,500 instead of Rs 4,500, creating a Rs 3,000 deficit).
4. **CSV Statement Import (0:50–1:15):**  
   * Click **Import Courier CSV** and upload a settlement file.
   * Point out the real-time recalculation of summary cards and new customer entries appearing in the ledger.
5. **Closing (1:15–1:25):**  
   *"COD Ledger provides merchants with a single, clear source of truth to protect cash flow and verify every rupee owed."*

---

## 🛠️ Built With

* HTML5 & Modern Vanilla JavaScript (ES6+)
* [Tailwind CSS CDN](https://tailwindcss.com/)
* [Lucide Icons](https://lucide.dev/)
* Inter Font by Google Fonts

---

## 📄 License

MIT License — Feel free to use and adapt this project for your own store or portfolio.
