# Usury Calculation

## When to Use

Read this file before performing any APR or interest-rate calculation on an
MCA agreement. This covers single agreements and stacked deals (where a second
agreement from the same funder uses part of the proceeds to pay down the first).

## The Formula

New York courts use a simple-interest formula to determine whether a loan
exceeds the 25% criminal usury threshold (Penal Law § 190.40):

    Rate = Interest / (Principal × Time)

Where:

- **Principal** is the amount advanced to the merchant.
- **Interest** is the total amount to be repaid minus the principal.
- **Time** is the repayment period expressed as a fraction of a year.

"Interest" is construed broadly and includes origination fees, closing fees, and
any other amounts deducted from the gross advance before the merchant receives
funds (*Adar Bays*, 37 N.Y.3d at 336–37; GOL § 5-501(2)). It also reaches a
contingent payment whose fate is left to the lender's sole discretion — that
counts as interest, and the rate is computed on the *net* funds the borrower
actually received (*Blue Wolf Capital Fund II, L.P. v. American Stevedoring,
Inc.*, 105 A.D.3d 178, 183–84 (1st Dept. 2013); see [Loan vs. Purchase](<loan-vs-purchase.md>)).

Always compute two rates:

1. **Gross principal** — the stated purchase price before fee deductions.
2. **Net principal** — the amount actually received by the merchant after all
   fees are deducted.

Both rates are relevant. If either exceeds 25%, the loan is criminally usurious.

## Stacked Agreements

A funder often issues a second agreement while the first is still outstanding.
Part of the second advance pays off the remaining balance on the first — the
merchant never sees that money. This is sometimes called "stacking."

### How to identify a stacked deal

The agreement itself may not spell out the stacking. Look for a **Funds
Disbursement and Authorization Letter** (or similar payoff/disbursement
schedule) attached to the agreement. It will list each payee and amount. Common
patterns:

- A payment to the funder itself or a related entity (e.g., a securitization
  vehicle like "Fora Financial AS 2024, LLC") — this is the payoff of the prior
  balance.
- A payment labeled as a processing or origination fee back to the funder.
- The remainder going to the merchant's bank account.

The agreement's face page may show a "Disbursement Amount" that is much smaller
than the "Purchase Price." The difference is fees plus the prior-balance payoff.

### Calculation steps

1. Start with the **Purchase Price** (gross advance) of the new agreement.
2. Subtract the **prior-balance payoff** — the amount routed back to the funder
   or its affiliate to retire the earlier deal. The merchant never received this.
3. Subtract any **origination, processing, or closing fees** deducted from the
   advance.
4. The result is the **net cash received** by the merchant (should match the
   Disbursement Amount on the face page).
5. Compute the interest rate using net cash received as the principal and the
   full Purchased Amount as the total repayment obligation.

The payoff of the first agreement's balance is economically identical to a fee:
it reduces the cash the merchant actually receives while the repayment
obligation stays the same. This typically makes the effective interest rate on
the second agreement dramatically higher than it appears from the face of the
contract alone.

### Repayment period for stacked deals

Use the remittance amount and purchased amount to derive the number of payments:
`weeks = purchased_amount / weekly_remittance`. Then convert to years as usual
(`weeks / 52`).

## How to Calculate

Use `python3 -c` to perform arithmetic. Examples:

### Single agreement

Given: $750,000 gross advance, $36,375 origination fee, $1,049,250 total
repayment, 20 weekly payments.

```bash
# Net proceeds
python3 -c "print(750000 - 36375)"
# 713625

# Interest (using net proceeds)
python3 -c "print(1049250 - 713625)"
# 335625

# Repayment period in years (20 weeks / 52 weeks)
python3 -c "print(round(20/52, 4))"
# 0.3846

# Annual interest rate using net proceeds
python3 -c "
principal = 713625
interest = 1049250 - principal
time = 20 / 52
rate = interest / (principal * time) * 100
print(f'{rate:.1f}%')
"
# 122.4%
```

### Stacked agreement

Given: Purchase Price $500,000, Processing Fee $15,000, prior-balance payoff
$344,080 (to funder's securitization affiliate), Purchased Amount $680,000,
weekly remittance $13,600. The Disbursement Amount to the merchant is $140,920.

```bash
python3 -c "
purchase_price = 500000
processing_fee = 15000
prior_balance_payoff = 344080
purchased_amount = 680000
weekly_remittance = 13600

net_cash = purchase_price - processing_fee - prior_balance_payoff
weeks = purchased_amount / weekly_remittance
interest = purchased_amount - net_cash
time = weeks / 52

rate = interest / (net_cash * time) * 100
print(f'Net cash received: \${net_cash:,.2f}')
print(f'Interest: \${interest:,.2f}')
print(f'Repayment period: {time:.4f} years ({weeks:.0f} weeks)')
print(f'Annual interest rate: {rate:.1f}%')
"
```

## Presentation

When presenting the calculation in a draft or memo:

- Show your work: state the principal, interest, and time values before giving
  the rate.
- Always note whether you used gross or net principal.
- For stacked deals, explain that the payoff amount never reached the merchant
  and should be excluded from principal.
- Compare the computed rate to the 25% criminal usury threshold.
