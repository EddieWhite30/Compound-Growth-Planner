# Compound-Growth-Planner
A single-file web tool that shows the daily percentage gain needed to grow an account from a starting balance to a target balance over a set number of weeks, using compound growth.

##Features
- Enter a starting balance, target balance, and trading days per week
- Table of the daily % and weekly % needed for timelines from 2 to 52 weeks, plus a custom weeks option
- Dollar gain needed on the first and last trading day of each timeline
- Color-coded daily % (green under 1%, amber 1–2.5%, red above 2.5%) to show which timelines are realistic
- Futures tab with a drop down of about 45 CME contracts and their tick values, showing the ticks per contract needed each day
- Add your own contracts to the futures list (saved in the browser)
- Light and dark mode, built for mobile

##Formula
- Daily % = (Target ÷ Start)^(1 ÷ Trading days) − 1

##Notes
- Assumes every trading day is a winner and ignores fees and taxes
- Tick values are standard CME specs; verify on cmegroup.com before trading
- For planning purposes only, not financial advice
