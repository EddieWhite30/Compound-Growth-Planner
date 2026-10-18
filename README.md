# Compound Growth Planner
A single-file web tool for planning how fast an account needs to grow to hit a target balance, using compound growth. Built for trading accounts, but it works for any savings goal, like saving up for a purchase.

## Shared inputs

These sit at the top of the page and feed all three tabs:

- **Starting balance:** your current account balance
- **Target balance:** the balance you want to reach
- **Trading days per week:** how many days you trade
- **Custom weeks (optional):** adds a row for any timeline you want

A summary card shows the total gain needed, the dollar gain, and the growth multiple.

## Tabs
## Options

A table of the daily % and weekly % needed to reach your target in 2 to 52 weeks, plus your custom weeks.

- **Daily** % is color-coded: green under 1%, amber 1–2.5%, red above 2.5%
- **Day 1** and **Last day** show the dollar gain needed on your first and final trading day. With compound growth the dollars grow as the balance grows, so these two numbers show the real range instead of a misleading average

## Futures

The same timeline table, built for futures traders.

- Drop down of about 45 CME contracts across equity index, metals, energy, interest rates, grains, currencies, livestock, and crypto, each with its tick value
- Enter how many contracts you trade
- **Day 1** and **Last day** show the dollars needed, with the ticks per contract needed underneath
- **Add a contract** form for new tickers. Added contracts are saved in your browser only
  
## Withdraw

A "withdraw as you go" calculator for funding a purchase from trading profits without waiting for one big target.

- **Item price:** the price of what you're saving for (subtract anything already saved)
- **Withdraw % of profit:** the share of weekly profit you move out to savings
- **Average daily % gain:** your average gain per trading day, losing days included
- Shows how many weeks it takes to fund the item and where your account ends up
- Compares 25%, 50%, 75%, and 100% withdrawal rates
- Week-by-week table of the balance, amount withdrawn, total saved, and balance after (first 52 weeks)

Your starting balance is treated as the baseline you keep trading with. At each week end, only the balance above that baseline counts as profit.

## Formulas

**Daily % needed (Options and Futures tabs)**

Daily % = (Target ÷ Start)^(1 ÷ Trading days) − 1

Trading days = weeks × trading days per week.

## Day 1 and Last day dollar gains

Day 1 gain    = Start × daily rate
Last day gain = Target × daily rate ÷ (1 + daily rate)

## Ticks per contract

Ticks = Dollar gain ÷ Contracts ÷ Tick value

## Notes
- Assumes every trading day is a winner and ignores fees and taxes. Real results come in streaks with losing days, so treat the numbers as the minimum pace needed
- Tick values are standard CME contract specs entered by hand. Verify them on cmegroup.com before trading, since specs can change
- The page cannot pull new contracts from CME automatically. Add new ones with the form on the Futures tab, or edit the contract list in index.html
- Added contracts are stored in the browser's local storage, so they do not carry over between devices
- Supports light and dark mode and is built for mobile screens
## Disclaimer

For planning purposes only. This is not financial, tax, or investment advice.
