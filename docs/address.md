#  Address API Spec

## Create Address
Endpoint : POST /api/contacts/{idContact}/addresses

Request Header :
- X-API-TOKEN : Token (Mandatory)

Request Body :
```json
{
  "street" : "jl. cihaur",
  "city" : "kuningan",
  "province" : "jawabarat",
  "country" : "indonesia",
  "postalCode": "2342"
}
```
Response Body (success) :
```json
{
  "data" : {
    "id" : "sdifuy293h9",
    "street" : "jl. cihaur",
    "city" : "kuningan",
    "province" : "jawabarat",
    "country" : "indonesia",
    "postalCode": "2342"
  }
}
```

Response Body (Failed) :
```json
{
  "errors": "Contact is not found"
}
```

## Update Address
Endpoint : PUT /api/contacts/{idContact}/addresses/{idAddress}

Request Header :
- X-API-TOKEN : Token (Mandatory)

Request Body :
```json
{
  "street" : "jl. cihaur",
  "city" : "kuningan",
  "province" : "jawabarat",
  "country" : "indonesia",
  "postalCode": "2342"
}
```
Response Body (success) :
```json
{
  "data" : {
    "id" : "sdifuy293h9",
    "street" : "jl. cihaur",
    "city" : "kuningan",
    "province" : "jawabarat",
    "country" : "indonesia",
    "postalCode": "2342"
  }
}
```

Response Body (Failed) :
```json
{
  "errors": "Address is not found"
}
```

## Get Address
Endpoint : GET /api/contacts/{idContact}/addresses/{idAddress}

Request Header :
- X-API-TOKEN : Token (Mandatory)

Response Body (success) :
```json
{
  "data" : {
    "id" : "sdifuy293h9",
    "street" : "jl. cihaur",
    "city" : "kuningan",
    "province" : "jawabarat",
    "country" : "indonesia",
    "postalCode": "2342"
  }
}
```

Response Body (Failed) :
```json
{
  "errors": "Address is not found"
}
```

## Remove Address
Endpoint : DELETE /api/contacts/{idContact}/addresses/{idAddress}

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
  "errors" : "Address is not found"
}
```


## List Address
Endpoint : GET /api/contacts/{idContact}/addresses

Request Header :
- X-API-TOKEN : Token (Mandatory)

Response Body (success) :
```json
{
  "data" : [
    {
      "id" : "sdifuy293h9",
      "street" : "jl. cihaur",
      "city" : "kuningan",
      "province" : "jawabarat",
      "country" : "indonesia",
      "postalCode": "2342"
    }
  ]
}
```

Response Body (Failed) :
```json
{
  "errors": "Contact is not found"
}
```