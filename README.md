# Our Money — Household Finance v2.2

A mobile-friendly, installable web app for tracking personal and shared household finances in GBP. It stores records locally in the browser; it does not sync data between devices.

## Features
- Manual transaction entry with personal/shared classification.
- Household monthly summary: both salaries, net rental income, recurring shared bills, fixed £500 monthly grocery contribution paid by your wife, estimated disposable income for each person, and settlement balance.
- Proportional split of recurring shared bills based on the two salaries after net rental income is applied against the bills.
- Fixed £500 monthly grocery contribution paid by your wife; the amount is included automatically in settlement, with no need to log individual grocery shops.
- Separate personal budgets and personal recurring bills (e.g. car finance, personal insurance, phone contracts), assigned to either household member.
- Monthly, weekly, quarterly and annual recurring-bill frequencies converted to monthly equivalents.
- JSON backup/restore and CSV transaction export.
- Installable PWA shell and basic offline app caching.

## Publish with GitHub Pages
1. Export a JSON backup from the existing app before updating.
2. Extract this ZIP.
3. Upload the *contents* of this folder to the root of the existing GitHub repository, replacing matching files and adding new files.
4. In GitHub, open Settings → Pages and ensure the existing Pages source is still configured.
5. Wait for deployment to complete. Close the installed app fully, then open the published URL in Chrome and refresh it. If it still shows the old version, open Chrome site settings for that URL and clear the site storage/cache (only after exporting a backup), then reopen the URL and reinstall if needed.
6. Check existing records are present before continuing. Do not clear browser site data.

## Notes on calculations
- Net rental income is rent received minus entered property costs, floored at zero. It is applied against shared recurring bills before the remaining bill balance is split between the two salaries.
- Groceries are fixed at £500/month and your wife is treated as paying the full amount. The £500 is allocated across both incomes by the salary-based percentages for calculating the shared cost, then credited in full against her settlement balance.
- Estimated disposable income = monthly take-home salary − allocated remaining shared bills − allocated shared groceries − active personal recurring bills − recorded personal expenses for that month. If the same personal recurring bill is also entered as a personal transaction, it will be deducted twice; enter it in one place only.
- Personal recurring bills do not affect shared bill contributions or settlement.
- If net rent exceeds recurring shared bills, excess rent is not carried forward or applied to groceries in this version.
- Data is stored in the browser's local storage. Use Settings → Export backup regularly. The app does not yet synchronise across devices.
