# Sample Products API

Sample Products API is a small HTTP API used to list, create, and read products.

Base URL: `https://api.example.com/v1`

## Operations

| Method | Path | Description |
| --- | --- | --- |
| GET | `/products` | List products |
| POST | `/products` | Create a product |
| GET | `/products/{productId}` | Get one product by id |

## Create a product

Send a JSON body with `name` and `price`.

```json
{
  "name": "Sample Widget",
  "price": 19.99
}
```

A successful create returns `201` and the stored product, including its `id`.

## Product

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| id | string | yes | Product identifier, for example `prod-1001` |
| name | string | yes | Product name |
| price | number | yes | Product price |

`GET /products/{productId}` returns `404` when the product does not exist.
