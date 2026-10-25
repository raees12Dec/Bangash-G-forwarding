# Bangash Transport ERP

Goods-forwarding / transport ERP and accounting app: trips, invoices, customers, suppliers,
vehicles, drivers, expenses, cash/bank, ledgers, P&L and reports. Built with React, Vite,
Tailwind and Firebase (Auth + Firestore).

## Run locally
```bash
npm install
npm run dev      # http://localhost:3000
npm run build    # production build in dist/
```

## Firebase setup
- Config lives in `firebase-applet-config.json` (web config; safe to be public, security is enforced by rules).
- Deploy rules: `firebase deploy --only firestore:rules`
- Access is limited to the owner email in `firestore.rules` plus any UID added to the
  Firestore `admins` collection (create a doc with the staff member's UID as its ID).

## Notes
- The in-app PIN lock is a convenience only; change the default PIN (1234) in Settings.
