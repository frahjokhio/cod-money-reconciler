# COD Ledger — Demo Quickstart & Walkthrough

A visual frontend prototype for Cash on Delivery (COD) reconciliation for Pakistani e-commerce merchants.

## How to View the Demo

Simply double-click or open **`index.html`** in any web browser (Google Chrome, Microsoft Edge, etc.):
- Direct file path: `file:///C:/Users/HP/.gemini/antigravity/scratch/cod-ledger-demo/index.html`

Alternatively, you can run a local server:
```bash
python -m http.server 3000
```
Then visit `http://localhost:3000`.

---

## 60–90 Second Demo Screen Recording Script

1. **Introduction:**
   > *"Pakistani online merchants receive bulk COD payments through multiple courier companies like TCS and Leopards. It's often painful to track which shipments have been settled, which payouts are pending, and where courier deductions create mismatches."*

2. **Summary Metrics (Point to Top 4 Cards):**
   - **Total COD Expected:** Rs 245,000 across active partner accounts.
   - **Received:** Rs 182,500 (74.5% cleared to bank).
   - **Pending Settlement:** Rs 42,500 currently in courier payout transit.
   - **Discrepancies:** 3 flagged orders requiring merchant audit.

3. **Status Filter Demonstration:**
   - Click the **Pending** pill to isolate the Rs 42,500 waiting on TCS and Leopards.
   - Click the **Mismatch** pill to spotlight orders with shortfalls (e.g. `#COD-1046` with Rs 500 variance, `#COD-1043` with Rs 200 variance).
   - Click **All** to return to the full ledger.

4. **Live Search Filter:**
   - In the search bar, type `Khan` or `#COD-1044` to demonstrate instant customer and order lookup.

5. **Courier Statement Import:**
   - Click **Import Courier CSV**.
   - Either select `sample-tcs-courier-statement.csv` or click **"Load Statement & Reconcile"**.
   - Note the confirmation toast: *"Courier statement imported successfully. 6 records ready to reconcile."*

6. **Closing:**
   > *"COD Ledger gives Pakistani merchants a unified, reliable ledger to verify every rupee owed by couriers and resolve discrepancies before they hurt cash flow."*
