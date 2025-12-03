# Address API

## Create Address

Endpoint : POST /api/contacts/:idContacts/addresses
Request header :
X-API-TOKEN : token

Request Body :

```json
{
  "street": "Jalan apa",
  "city": "Kota apa",
  "province": "Provinsi apa",
  "country": "Negara apa",
  "postal_code": "12312"
}
```

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "street": "Jalan apa",
    "city": "Kota apa",
    "province": "Provinsi apa",
    "country": "Negara apa",
    "postal_code": "12312"
  }
}
```

Response Body Failed:

```json
{
  "errors": "Postal Code is required"
}
```

## Update Address

Endpoint : PUT /api/contacts/:idContacts/addresses/:idAddress
Request header :
X-API-TOKEN : token

Request Body :

```json
{
  "street": "Jalan apa",
  "city": "Kota apa",
  "province": "Provinsi apa",
  "country": "Negara apa",
  "postal_code": "12312"
}
```

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "street": "Jalan apa",
    "city": "Kota apa",
    "province": "Provinsi apa",
    "country": "Negara apa",
    "postal_code": "12312"
  }
}
```

Response Body Failed:

```json
{
  "errors": "Postal Code is required"
}
```

## Get Address

Endpoint : GET /api/contacts/:idContacts/addresses/:idAddress
Request header :
X-API-TOKEN : token

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "street": "Jalan apa",
    "city": "Kota apa",
    "province": "Provinsi apa",
    "country": "Negara apa",
    "postal_code": "12312"
  }
}
```

Response Body Failed:

```json
{
  "errors": "Address is not Found"
}
```

## List Address

Endpoint : GET /api/contacts/:idContacts/addresses/:idAddress
Request header :
X-API-TOKEN : token

Response Body Success:

```json
{
  "data": [
    {
      "id": 1,
      "street": "Jalan apa",
      "city": "Kota apa",
      "province": "Provinsi apa",
      "country": "Negara apa",
      "postal_code": "12312"
    },
    {
      "id": 2,
      "street": "Jalan apa",
      "city": "Kota apa",
      "province": "Provinsi apa",
      "country": "Negara apa",
      "postal_code": "12312"
    }
  ]
}
```

Response Body Failed:

```json
{
  "errors": "Contact is not found"
}
```

## Remove Address

Response Body Success:

```json
{
  "data": "OK"
}
```

Response Body Failed:

```json
{
  "errors": "Address is not found"
}
```
