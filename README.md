A demo API to create Github like issues and manage them

API has three resource

* POST /issues
* GET /issues
* PATCH /issues/{id}


Samples Curl requests

1. Create an issue
```
curl --location --request POST 'https://74828fb8-83ac-4a82-b786-b6aa78b0bd5f-prod.e1-us-east-azure.preview-dv.choreoapis.dev/oubo/issues-api/1.0.0/issues' \
--header 'Authorization: Bearer <TokenWithRequiredScope>' \
--header 'Content-Type: application/json' \
--data-raw '{
    "name": "Universal intangible policy"
}'
```


2. List Issues

Request
```
curl --location --request GET 'https://74828fb8-83ac-4a82-b786-b6aa78b0bd5f-prod.e1-us-east-azure.preview-dv.choreoapis.dev/oubo/issues-api/1.0.0/issues' \
--header 'Authorization: Bearer <TokenWithRequiredScope>'
```

3. Open or Close an Issue (Valid status values are "Open" or Closed)

```
curl --location --request PATCH 'https://74828fb8-83ac-4a82-b786-b6aa78b0bd5f-prod.e1-us-east-azure.preview-dv.choreoapis.dev/oubo/issues-api/1.0.0/issues/775ef701-3a0c-4aa8-a973-838041316511' \
--header 'Authorization: Bearer <TokenWithRequiredScope>' \
--header 'Content-Type: application/json' \
--data-raw '{
    "status": "Closed"
}'
```
