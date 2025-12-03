# Contact API Spec

## Create Contact

Endpoint : PUT /api/contacts/:

Request Headers :
~ X-API-TOKEN : token (from login)

Request Body :

```json
{
  "first_name": "Tandiri",
  "last_name": "Lambun",
  "email": "tandiri@example.com",
  "phone": "+62"
}
```

Response Body (success) ;

```json
{
  "data": {
    "id": 1,
    "first_name": "Tandiri",
    "last_name": "Lambun",
    "email": "tandiri@example.com",
    "phone": "+62"
  }
}
```

Response Body (failed) ;

```json
{
  "error": "First Name must not blank"
}
```

## Update Contact

Endpoint : PUT /api/contacts/:id

Request Headers :
~ X-API-TOKEN : token (from login)

Request Body :

```json
{
  "first_name": "Tandiri",
  "last_name": "Lambun",
  "email": "tandiri@example.com",
  "phone": "+62"
}
```

Response Body (success) ;

```json
{
  "data": {
    "id": 1,
    "first_name": "Tandiri",
    "last_name": "Lambun",
    "email": "tandiri@example.com",
    "phone": "+62"
  }
}
```

Response Body (failed) ;

```json
{
  "error": "First Name must not blank"
}
```

## Get Contact

Endpoint : GET /api/contacts/:id

Request Headers :
~ X-API-TOKEN : token (from login)

Response Body (success) ;

```json
{
  "data": {
    "id": 1,
    "first_name": "Tandiri",
    "last_name": "Lambun",
    "email": "tandiri@example.com",
    "phone": "+62"
  }
}
```

Response Body (failed) ;

```json
{
  "error": "Contact Not Found"
}
```

## Search Contact

Endpoint : GET /api/contacts

Query Parameter:

- name : string, contact first name or contact last name, optional
- phone : string, contact phone, optional
- email : string, contact email, optional
- page : number, default 1
- size : number, default 10

Request Headers :
~ X-API-TOKEN : token (from login)

Response Body (success) ;

```json
{
  "data": [
    {
      "id": 1,
      "first_name": "Tandiri",
      "last_name": "Lambun",
      "email": "tandiri@example.com",
      "phone": "+62"
    },
    {
      "id": 2,
      "first_name": "Enma",
      "last_name": "Tokio",
      "email": "enma@example.com",
      "phone": "+6282"
    }
  ],
  "paging": {
    "current_page": 1,
    "total_page": 10,
    "size": 10
  }
}
```

Response Body (failed) ;

```json
{
  "error": "Unauthorized"
}
```

## Remove Contact

Endpoint : POST /api/contacts:id

Request Headers :
~ X-API-TOKEN : token (from login)

Response Body (success) ;

```json
{
  "data": "OK"
}
```

Response Body (failed) ;

```json
{
  "error": "Contact Not Found"
}
```
