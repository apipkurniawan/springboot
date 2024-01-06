#  User API Spec

## Register User
Endpoint : POST /api/users

Request Body :
```json
{
  "username" : "apip",
  "password" : "apip",
  "name" : "apip kurniawan"
}
```
Response Body (success) : 
```json
{
  "data" : "OK"
}
```

Response Body (Failed) :
```json
{
  "errors": "username must not blank.???"
}
```

## Login User
Endpoint : POST /api/auth/login

Request Body :
```json
{
  "username" : "apip",
  "password" : "apip"
}
```
Response Body (success) :
```json
{
  "data" : {
    "token" : "TOKEN",
    "expiredAt" : 28752567256 // milisecond
  }
}
```

Response Body (Failed, 401) :
```json
{
  "errors": "username or password wrong"
}
```

## Get User
Endpoint : GET /api/users/current

Request Header : 
- X-API-TOKEN : Token (Mandatory)

Response Body (success) :
```json
{
  "data" : {
    "username": "apip",
    "name" : "apip kurniawan"
  }
}
```

Response Body (Failed, 401) :
```json
{
  "errors": "Unauthorized"
}
```

## Update User
Endpoint : PATCH /api/users/current

Request Header :
- X-API-TOKEN : Token (Mandatory)

Request Body :
```json
{
  "username" : "apip", // put if only want to update name
  "password" : "new password" // put if only want to update password
}
```

Response Body (success) :
```json
{
  "data" : {
    "username": "apip",
    "name" : "new password"
  }
}
```

Response Body (Failed, 401) :
```json
{
  "errors": "Unauthorized"
}
```

## Logout User
Endpoint : DELETE /api/auth/logout

Request Header :
- X-API-TOKEN : Token (Mandatory)

Response Body (success) :
```json
{
  "data" : "OK"
}
```