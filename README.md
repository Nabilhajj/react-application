# Crypto Explorer

A React + Vite app that consumes the [CoinGecko](https://www.coingecko.com/en/api) public API and presents a browsable catalogue of cryptocurrencies, with a list page and a detail page per coin.

## Features

- Browsable list of coins with live price, 24h change, and market cap rank
- Debounced search (300ms) by coin name or symbol
- Sort by rank, price (low/high), or name
- Filter by 24h gainers/losers
- Coin detail page with a controlled, validated price alert form
- Favourites: add/remove any coin from its card, view them on a dedicated Favourites page (shared via Context API)
- Loading, error, and empty states for every fetch
- 404 page for unknown routes
- Shared header/footer layout via a nested route
- Responsive layout from 375px upward

## API used

[CoinGecko API v3](https://www.coingecko.com/en/api) — `/coins/markets` for the list, `/coins/{id}` for coin detail. No API key required.

## Tech stack

- React 19 + Vite
- React Router (list page, detail page, 404, nested layout route)
- Custom hooks: `useFetch` (data fetching), `useDebounce` (search)
- Context API for favourites

## Running locally

```
npm install
npm run dev
```

Then open the local URL Vite prints (e.g. `http://localhost:5173/`).

## Screenshots

![List page](./screenshots/list.png)
![Detail page](./screenshots/detail.png)
![Graph page](./screenshots/graph.png)
![Favourites page](./screenshots/favourites.png)
