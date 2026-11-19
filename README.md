# ORRERY JAPAN MARKET HUD — prototype v1

## Included
- Black + blue ARC reactor interface
- iPad landscape responsive layout
- Overview / Watch List / Alerts / Settings tabs
- Initial symbols: 1570 and 285A
- Manual ticker entry and CSV import/export
- Local browser storage for watchlist and alert rules

## Important limitations
This prototype is NOT connected to live market data, SBI Securities, or a brokerage account. Prices and indicators are intentionally shown as unavailable rather than fabricated. Alert rules are saved locally but are not monitored until a licensed market-data feed and server-side monitoring service are connected. It does not place orders.

## CSV format
`code,name,category,shares,cost`

Example:
`7203,トヨタ自動車,長期配当,100,2500`

Import your previous 40-stock list using this format. Existing codes are updated; new codes are added.

## Run on iPad
For a quick local preview, open `index.html` in a browser. For Add to Home Screen / PWA installation, host the folder on an HTTPS static host, open the URL in Safari, then Share -> Add to Home Screen.

## Next implementation phase
1. Obtain the exact 40-stock list.
2. Select a Japanese equities market-data provider with permitted display/redistribution terms.
3. Build a backend adapter and WebSocket updates.
4. Calculate VWAP, moving averages, RSI, MACD, volume signals.
5. Add push notification service and portfolio import workflow.
ORRERY JAPAN MARKET HUD - deployment test