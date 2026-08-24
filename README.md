# WOF — Multi-Vendor Marketplace

Multi-vendor e-commerce storefront with separate customer, seller and admin
experiences. Stripe and PayPal checkout, order tracking, coupons, events and
multi-currency support.

## Features

**Customer**
- Product browsing with categories, subcategories, featured products and best deals
- Product detail pages with ratings, reviews and suggested products
- Cart, wishlist and multi-step checkout
- Stripe and PayPal payment flows
- Order tracking and profile management
- Time-limited event/deal campaigns with countdowns

**Seller**
- Seller dashboard with product, order and withdrawal management
- Shop profile and settings

**Admin**
- Dashboard covering users, sellers, products, categories, subcategories, events and withdrawals

## Tech stack

| Layer | Choice |
| --- | --- |
| Framework | React |
| State | Redux Toolkit |
| UI | Material UI (`@mui/material`, `@mui/x-data-grid`), Tailwind CSS |
| Payments | Stripe (`@stripe/react-stripe-js`), PayPal (`@paypal/react-paypal-js`) |
| HTTP | Axios |
| Utilities | `country-state-city`, `js-cookie` |
| Testing | React Testing Library, Jest DOM |

## Getting started

```bash
git clone https://github.com/ARBAB1/wof-frontend.git
cd wof-frontend
npm install
npm start
```

The app runs at `http://localhost:3000`.

### Environment

Create a `.env` file with your API and payment keys:

```
REACT_APP_API_URL=http://localhost:8000/api/v2
REACT_APP_STRIPE_PUBLIC_KEY=pk_test_xxx
REACT_APP_PAYPAL_CLIENT_ID=xxx
```

## Scripts

| Command | Description |
| --- | --- |
| `npm start` | Start the development server |
| `npm run build` | Production build |
| `npm test` | Run tests |

## Project structure

```
src/
├── components/
│   ├── Admin/        # Admin dashboard views
│   ├── Checkout/     # Multi-step checkout
│   ├── Payment/      # Stripe & PayPal
│   ├── Products/     # Detail, ratings, suggestions
│   ├── Profile/      # Account, order tracking
│   ├── Events/       # Campaigns with countdowns
│   └── Route/        # Hero, categories, product cards
└── redux/            # Redux Toolkit store and slices
```

## License

MIT
