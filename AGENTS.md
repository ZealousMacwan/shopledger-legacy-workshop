# Repository Guidelines

## Stack and Module Map

ShopLedger uses Node.js, CommonJS JavaScript, Express 4, and `body-parser`. The app entry point is `server.js`; runtime settings are in `config.js`. API endpoints are grouped in `routes/` (products, orders, customers, reports). Business logic is in `lib/` (orders, inventory, pricing, tax, coupons, ledger, invoices, reports, dates, and JSON storage). The browser app is under `public/`, and its local JSON store is `data/db.json`.

## Commands

- `npm install` installs the dependencies declared in `package.json`.
- `npm start` runs `node server.js`.
- `npm test` currently prints “Error: no test specified” and exits unsuccessfully; no test runner is configured.

## Change Rules

- Write characterization tests before changing behavior.
- Change only the module the ticket is about.
- Tests must never read or write `data/db.json`.
- Add no dependencies.
