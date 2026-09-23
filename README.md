# getcalcbase-tools
50+ free online calculators for developers,  marketers, finance professionals, and students. All completely  free with no login required.     https://getcalcbase.com
# GetCalcBase Finance Toolkit

Open-source Python implementations of the core financial calculation logic used in [GetCalcBase](https://getcalcbase.com/) — a free web platform with 50+ calculators for finance, health, education, developer, and digital marketing use cases.

This repo exists so the math is transparent and verifiable — instead of asking you to trust a black-box result, you can read exactly how each number is calculated, or run it yourself.

## What's Included

- **Mortgage Amortization** — full monthly payment breakdown (principal vs. interest) over the loan term
- **Mortgage Recast** — recalculates the monthly payment after a lump-sum payment, keeping the same rate and term
- **SIP with Inflation Adjustment** — calculates both nominal and real (purchasing-power-adjusted) investment corpus

## Live Versions (no code required)

If you'd rather use these calculators directly in a browser instead of running Python, the same logic (plus visual results, charts, and amortization schedules) is available for free at:

- [Mortgage Recast Calculator](https://getcalcbase.com/finance-tools/mortgage-recast-calculator/)
- [SIP Calculator with Inflation](https://getcalcbase.com/finance-tools/sip-calculator-with-inflation/)
- [Full tool list — 50+ calculators](https://getcalcbase.com/)

All web versions run entirely client-side in the browser — no financial data is ever sent to a server.

## Usage

```bash
git clone https://github.com/YOUR_USERNAME/getcalcbase-finance-toolkit.git
cd getcalcbase-finance-toolkit
python calculators.py
```

## Example

```python
from calculators import mortgage_amortization, recast_payment, sip_with_inflation

# Mortgage amortization
payment, schedule = mortgage_amortization(320000, 6.5, 30)
print(f"Monthly Payment: ${payment:,.2f}")

# Recast after a lump sum
new_balance, new_payment = recast_payment(280000, 30000, 6.5, 240)
print(f"New Payment After Recast: ${new_payment:,.2f}")

# SIP with inflation
nominal, real = sip_with_inflation(10000, 12, 20, 6)
print(f"Nominal Corpus: ${nominal:,.2f} | Real Corpus: ${real:,.2f}")
```

## Why This Exists

Most online calculators give you a final number with no visibility into how it was reached. This repo is the actual math behind three of GetCalcBase's most-used tools, published openly so anyone can verify it, learn from it, or build on it.

## Contributing

Found a bug in the math, or want to add another calculator (loan comparison, rent-vs-buy, income tax)? PRs are welcome. Open an issue first if it's a larger change.

## Related

- Website: [https://getcalcbase.com/](https://getcalcbase.com/)
- Finance tools category: [https://getcalcbase.com/finance-tools/](https://getcalcbase.com/finance-tools/)

## License

MIT — use freely, attribution appreciated but not required.
