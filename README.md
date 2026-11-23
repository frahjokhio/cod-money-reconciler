# COD Money Reconciler

An automated **Cash on Delivery (COD) reconciliation dashboard** built for e-commerce sellers and direct-to-consumer (D2C) brands.

Online merchants operating in emerging markets rely heavily on cash-on-delivery payments collected through third-party logistics (3PL) partners (such as TCS, Leopards, and PostEx). Managing payouts across disparate courier statements often leads to unnoticed deductions, delayed settlements, and unaccounted revenue leakage. 

**COD Money Reconciler** solves this problem by providing merchants with a unified ledger to verify courier deposits against merchant invoices, spotlight payment shortfalls, and monitor cash flow in real time.

---

## 🚀 Features

* **Automated Reconciliation Engine:** Real-time mathematical comparison between invoice amounts and courier-reported payouts. Any variance or short-settlement is instantly flagged with status indicators and calculated shortfalls.
* **Dynamic CSV Statement Import:** Seamlessly parses courier settlement statement exports (`.csv`). Automatically extracts orders, updates settlement statuses, maps new customer records, and dynamically updates dashboard analytics.
* **Executive Financial Metrics:**
  * **Total COD Expected:** Gross outstanding revenue expected across logistics partners.
  * **Realized Settlements:** Total cleared funds received in merchant accounts, with settlement percentage.
  * **In-Transit / Pending:** Capital currently locked inside courier disbursement cycles.
  * **Discrepancy Audit:** Immediate visibility into mismatched transactions requiring courier dispute, including total financial shortfall.
* **Instant Filtering & Search:** Search by Order ID, Customer Name, or Courier Partner with real-time status segmentation (*All*, *Settled*, *Pending*, *Mismatch*).
* **Privacy-First Architecture:** 100% client-side computation. All file parsing, matching, and metric calculations run entirely within the browser, ensuring customer and transaction data never leaves the client machine.

---

## 🛠️ Tech Stack

* **Frontend:** Modern Vanilla JavaScript (ES6+), HTML5
* **Styling:** [Tailwind CSS](https://tailwindcss.com/)
* **Icons:** [Lucide Icons](https://lucide.dev/)
* **Typography:** Inter by Google Fonts

---

## 💻 Getting Started

This application requires zero build steps or external dependencies.

1. **Clone the repository:**
   ```bash
   git clone https://github.com/frahjokhio/cod-money-reconciler.git
   cd cod-money-reconciler
   ```

2. **Launch:**
   * Open `index.html` directly in any modern web browser, or
   * Serve locally using your preferred HTTP server:
     ```bash
     python -m http.server 3000
     ```
     Navigate to `http://localhost:3000`.

---

## 📋 Statement Format

The reconciler accepts standard courier settlement CSV exports. A sample template is provided in [`cod-courier-statement-sample.csv`](cod-courier-statement-sample.csv):

| Column | Description |
| :--- | :--- |
| `Order_ID` | Merchant invoice or internal order identifier |
| `Customer_Name` | Consignee / customer name |
| `Courier` | Logistics partner (e.g., TCS, Leopards) |
| `Order_Amount` | Invoiced COD amount to be collected |
| `Courier_Settled` | Actual payout amount reported by the courier |
| `Delivery_City` | Destination hub or delivery city |

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
