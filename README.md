# Mock Store API

A simple static JSON dataset simulating a product catalog for a small e-commerce store.
Designed for front-end exercises and prototyping — no backend required.

## Endpoint

```
GET https://raw.githubusercontent.com/Anita-Liberatore/mock-store-api/master/products.json
```

Works from any HTTP client (Postman, browser, `fetch`, `axios`, etc.) with no authentication.

## Usage example

```js
const response = await fetch(
  'https://raw.githubusercontent.com/Anita-Liberatore/mock-store-api/master/products.json'
)
const products = await response.json()
```

## Product schema

```json
{
  "id": 1,
  "name": "Sneakers Urban Pro",
  "category": "Footwear",
  "price": 89.99,
  "description": "Lightweight urban sneakers with rubber sole and breathable mesh upper.",
  "image": "https://images.unsplash.com/photo-1542291026-7eec264c27ff?w=600&q=80",
  "stock": 12,
  "rating": 4.5
}
```

| Field | Type | Description |
|-------|------|-------------|
| `id` | number | Unique identifier |
| `name` | string | Product name |
| `category` | string | One of: `Footwear`, `Clothing`, `Accessories`, `Electronics` |
| `price` | number | Price in EUR |
| `description` | string | Short product description |
| `image` | string | Unsplash image URL (600px wide) |
| `stock` | number | Units available |
| `rating` | number | Average rating (1–5) |

## Dataset

12 products across 4 categories:

| # | Name | Category | Price |
|---|------|----------|-------|
| 1 | Sneakers Urban Pro | Footwear | €89.99 |
| 2 | Zaino Explorer 30L | Accessories | €59.99 |
| 3 | Felpa Oversize Minimal | Clothing | €44.99 |
| 4 | Cuffia Bluetooth Studio | Electronics | €129.00 |
| 5 | Borraccia Termica 500ml | Accessories | €24.99 |
| 6 | T-Shirt Essential Pack | Clothing | €34.99 |
| 7 | Portafoglio Slim Leather | Accessories | €39.99 |
| 8 | Occhiali da Sole Retro | Accessories | €49.99 |
| 9 | Giacca Softshell Trail | Clothing | €119.00 |
| 10 | Smartwatch Fitness X1 | Electronics | €199.00 |
| 11 | Cap Logo Ricamato | Accessories | €19.99 |
| 12 | Calzini Merino Sport | Clothing | €14.99 |
