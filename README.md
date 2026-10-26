# StreetKart

StreetKart is a polished React/Vite proof of concept for a hyperlocal marketplace connecting customers with mobile street vendors. It uses fictional Chandigarh-area locations and dummy data only.

## Run locally

```bash
npm install
npm run dev
```

Open the local Vite URL shown in the terminal.

## Demo accounts

| Role | Email | Password |
| --- | --- | --- |
| Customer | `customer@streetkart.demo` | `customer123` |
| Vendor | `vendor@streetkart.demo` | `vendor123` |
| Admin | `admin@streetkart.demo` | `admin123` |

The login is intentionally client-side for demonstration and is not production authentication.

## Included modules

- Customer discovery dashboard with product search, category filters, vendor details, favorites, notifications and a responsive simulated map.
- Vendor dashboard with inventory CRUD, availability toggles, profile editing and simulated location updates.
- Admin dashboard with derived statistics, vendor search, approval/suspension controls and a reset-demo-data action.
- Shared React Context state persisted to browser `localStorage`. Changes made in the same browser are reflected across the role views; this POC does not provide multi-device synchronization.
- Seed data includes 8 vendors, 30 products, 5 categories, 3 demo customer accounts and sample notifications.

## Demonstration flow

1. Sign in as Customer and search for `tomatoes`.
2. Open a vendor, save it as a favorite and inspect the simulated map.
3. Sign out, sign in as Vendor, edit inventory or simulate a location update.
4. Sign out, sign in as Customer again to see updated availability/notifications.
5. Sign in as Admin to approve/suspend vendors and review current statistics.
6. Use **Reset demo data** to restore the original seed state.

## Future integration

A real deployment could replace the seed/context layer with a REST API, add server-side authentication, connect a Leaflet/OpenStreetMap map, and add secure vendor verification, payments, reviews and real-time events.
