# User API Spec

## Register User
Endpoint : POST /api/users
Request Body :

```json
{
  "username": "tenten",
  "password": "rahasia",
  "name": "Tandirilambun"
}
```

Response Body (success) ;

```json
{
  "data": {
    "username": "tenten",
    "name": "Tandirilambun"
  }
}
```

Response Body (failed) ;

```json
{
  "error": "Username must not blank, ..."
}
```

## Login User

Endpoint : POST /api/users/login
Request Body :

```json
{
  "username": "tenten",
  "password": "rahasia"
}
```

Response Body (success) ;

```json
{
  "data": {
    "username": "tenten",
    "name": "Tandirilambun",
    "token": "uuid"
  }
}
```

Response Body (failed) ;

```json
{
  "error": "Username or password wrong"
}
```

## Get User
Endpoint : GET /api/users/current

Request Headers :
~ X-API-TOKEN : token (from login)

Response Body (success) ;

```json
{
  "data": {
    "username": "tenten",
    "name": "Tandirilambun"
  }
}
```

Response Body (failed) ;

```json
{
  "error": "Unauthorized"
}
```

## Update User
Endpoint : PATCH /api/users/current

Request Headers :
~ X-API-TOKEN : token (from login)

Request Body :

```json
{
  "password": "rahasia", // tidak wajib
  "name": "Tandirilambun" // tidak wajib
}
```

Response Body (success) ;

```json
{
  "data": {
    "username": "tenten",
    "name": "Tandirilambun"
  }
}
```

Response Body (failed) ;

```json
{
  "error": "Unauthorized"
}
```

## Logout User
Endpoint : DELETE /api/users/current

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
  "error": "Unauthorized"
}
```