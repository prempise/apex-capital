# APEX CAPITAL — Investment Growth Calculator

A single-file browser app. No install. No login. Open the HTML file and use it.

---

## What It Does

You put in numbers about an investment. It tells you what that investment will be worth over time, broken down year by year, with charts.

---

## Inputs

### Core Investment (Required)

**Initial Capital** — The lump sum you are starting with. Can be $0 if you are only making regular contributions.

**Annual Interest Rate** — Your expected yearly return, in %. Enter 7 for 7%.

**Investment Duration** — How many years you are running this projection. Accepts 1 to 100 years.

**Compounding Frequency** — How often interest gets calculated and added to your balance. Options: Annually, Semi-Annually, Quarterly, Monthly (default), Daily. More frequent compounding means a slightly higher final number.

---

### Contributions (Optional)

**Contribution Amount** — A fixed amount you add on top of your initial capital, on a recurring basis.

**Contribution Frequency** — Whether that contribution happens monthly or yearly.

Leave both at 0 if you just want to see what a one-time lump sum does.

---

### Inflation Adjustment (Optional)

**Inflation Rate** — Annual inflation percentage to apply. Default is 2.5%.

**Toggle: Apply Inflation Adjustment** — When on, results will show both the raw (nominal) value and the inflation-adjusted (real) value. When off, only nominal values are shown.

---

## Output

Hit Calculate Growth. Results appear on the right side.

### Summary Cards

Four numbers shown upfront:

1. **Final Portfolio Value** — Total balance at end of your time horizon, in nominal dollars.
2. **Inflation-Adjusted Value** (if inflation toggle is on) or **Total Interest Earned** (if off) — Either what your money is worth in today's purchasing power, or how much of the final value came from interest alone.
3. **Total Contributions** — Everything you put in (initial + all recurring contributions), as a dollar amount and as a percentage of the final value.
4. **Total Interest Earned** — How much the money made on its own, and what percentage of the final value that is.

---

### Chart 1 — Portfolio Growth Over Time

Line chart showing portfolio value year by year. If inflation is on, two lines appear: nominal value and real (inflation-adjusted) value.

---

### Chart 2 — Contributions vs Interest Breakdown

Bar chart showing, per year, how much of your total portfolio came from money you put in versus money earned from interest. Useful for seeing when compound interest starts doing most of the work.

---

### Year-by-Year Table

Scrollable table with one row per year:

- Starting Balance
- Contributions that year
- Interest earned that year
- Ending Balance
- Real Value (only shown if inflation adjustment is on)

---

## Notes

- Works on desktop, tablet, and mobile.
- No data is sent anywhere. All calculations run locally in your browser.
- Formula used: A = P(1 + r/n)^nt + PMT multiplied by [((1 + r/n)^nt minus 1) divided by (r/n)]
- Input validation runs before every calculation. Fields highlight red if values are out of accepted range.
