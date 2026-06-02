# CoffeeGo

CoffeeGo is a React Native app built with Expo and React Navigation. This homework 08 version adds Fetch API integration with an external coffee API so the menu is loaded from remote data instead of hardcoded items.

## API Integration

- API URL: https://api.sampleapis.com/coffee/hot
- Fetch API is used for network requests.
- API logic is isolated in `src/services/coffeeApi.js`.
- Data is normalized before rendering so screens receive consistent coffee items.
- Loading and error states are handled on the Home screen.

## Features

- Coffee list loaded from API
- Search by coffee name
- Category filtering (All, Latte, Cappuccino, Espresso)
- Product Details screen
- Drawer navigation
- Bottom tab navigation
- Size selector (S / M / L)
- Add to Cart button UI

## Data Flow

- Coffee data is fetched from the API when the Home screen loads.
- Results are stored in component state using React hooks.
- Coffee items are rendered using FlatList.
- Selecting a coffee opens Product Details and passes route parameters:
  - id
  - title
  - price
  - imageUrl
  - description

## Navigation Structure

```text
Drawer Navigator
└── Stack Navigator
    ├── Home
    ├── Product Details
    ├── Orders
    ├── Cart
    └── Profile
```

Additional Drawer Screens:
- Settings
- Help
- Contact

## Run Instructions

```bash
npm install
npm run web
```

## Screenshots

### Home Screen
![Home Screen](assets/homescreen.png)

### Product Details Screen
![Product Details](assets/product-details.png)

### Drawer Navigation
![Drawer Navigation](assets/drawer.png)
