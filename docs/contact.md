#  Contact API Spec

## Create Contact
Endpoint : POST /api/contacts

Request Header :
- X-API-TOKEN : Token (Mandatory)

Request Body :
```json
{
  "firstName" : "apip",
  "lastName" : "kurniawan",
  "email" : "apip@gmail.com",
  "phone" : "081287237833"
}
```
Response Body (success) :
```json
{
  "data" : {
    "id" : "sdifuy293h9",
    "firstName" : "apip",
    "lastName" : "kurniawan",
    "email" : "apip@gmail.com",
    "phone" : "081287237833"
  }
}
```

Response Body (Failed) :
```json
{
  "errors": "Email format invalid, ..."
}
```

## Update Contact
Endpoint : PUT /api/contacts/{idContact}

Request Header :
- X-API-TOKEN : Token (Mandatory)

Request Body :
```json
{
  "firstName" : "apip",
  "lastName" : "kurniawan",
  "email" : "apip@gmail.com",
  "phone" : "081287237833"
}
```
Response Body (success) :
```json
{
  "data" : {
    "id" : "sdifuy293h9",
    "firstName" : "apip",
    "lastName" : "kurniawan",
    "email" : "apip@gmail.com",
    "phone" : "081287237833"
  }
}
```

Response Body (Failed) :
```json
{
  "errors": "Email format invalid, ..."
}
```

## Get Contact
Endpoint : GET /api/contacts/{idContact}

Request Header :
- X-API-TOKEN : Token (Mandatory)

Response Body (success) :
```json
{
  "data" : {
    "id" : "sdifuy293h9",
    "firstName" : "apip",
    "lastName" : "kurniawan",
    "email" : "apip@gmail.com",
    "phone" : "081287237833"
  }
}
```

Response Body (Failed, 404) :
```json
{
  "errors": "Contact is not found"
}
```

## Search Contact
Endpoint : GET /api/contacts

Query Param : 
- name : String, contact first name or last name, using like query, optional
- phone : String, contact phone, using like query, optional
- email : String, contact email, using like query, optional
- page : Integer, start from 0, default 0
- size : Integer, default 10

Request Header :
- X-API-TOKEN : Token (Mandatory)

Response Body (success) :
```json
{
  "data" : [
    {
      "id" : "sdifuy293h9",
      "firstName" : "apip",
      "lastName" : "kurniawan",
      "email" : "apip@gmail.com",
      "phone" : "081287237833"
    }
  ],
  "paging" : {
    "totalPage" : 10,
    "size" : 10,
    "currentPage" : 0
  }
}
```

Response Body (Failed) :
```json
{
  "errors": "Unauthorized"
}
```

## Remove Contact
Endpoint : DELETE /api/contacts/{idContact}

Request Header :
- X-API-TOKEN : Token (Mandatory)

Response Body (success) :
```json
{
  "data" : "OK"
}
```

Response Body (Failed) :
```json
{
  "errors" : "Contact is not found"
}
```