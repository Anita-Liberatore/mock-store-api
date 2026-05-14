# Kreas Products API — Mock Data

Questo repository contiene il file JSON da usare come sorgente dati per il progetto e-commerce Vue.js.

## Come usare il JSON

Nella tua applicazione Vue.js, usa il percorso raw di GitHub per recuperare i dati:

```js
const res = await fetch(
  'https://raw.githubusercontent.com/Anita-Liberatore/kreas-products-api/main/products.json'
)
const products = await res.json()
```

## Struttura di un prodotto

```json
{
  "id": 1,
  "name": "Sneakers Urban Pro",
  "category": "Footwear",
  "price": 89.99,
  "description": "...",
  "image": "https://...",
  "stock": 12,
  "rating": 4.5
}
```

| Campo | Tipo | Descrizione |
|-------|------|-------------|
| `id` | number | Identificativo univoco |
| `name` | string | Nome del prodotto |
| `category` | string | Categoria (`Footwear`, `Clothing`, `Accessories`, `Electronics`) |
| `price` | number | Prezzo in euro |
| `description` | string | Descrizione breve del prodotto |
| `image` | string | URL immagine (Unsplash, 600px) |
| `stock` | number | Quantità disponibile |
| `rating` | number | Valutazione media (1–5) |

## Prodotti inclusi (12 totali)

| # | Nome | Categoria | Prezzo |
|---|------|-----------|--------|
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

## Regola sconto

> Se il cliente acquista **più di 3 prodotti**, applica uno sconto del **10%** sul totale del carrello.

```js
const discount = cartItems.length > 3 ? total * 0.10 : 0
const finalTotal = total - discount
```
