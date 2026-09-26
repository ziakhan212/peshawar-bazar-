# Change the app yourself

You can update the most common business details in:

`config/app.ts`

Edit these values:

- `appName` — the app name
- `region` — the marketplace area, currently `KP Province`
- `country` — the country shown beside the area
- `defaultSellerName` — the name used for new listings and the profile
- `memberSince` — the profile membership year

To change the starter products shown on the home screen, edit:

`data/products.ts`

Each product includes its title, price, category, seller, location, distance, condition, description, and image.

After changing code, save the file and refresh the mobile preview. If you change dependencies or the app configuration, restart the mobile preview.