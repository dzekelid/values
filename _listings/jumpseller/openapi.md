---
swagger: "2.0"
x-collection-name: Jumpseller
x-complete: 1
info:
  title: Jumpseller
  description: explore-all-our-endpoints-with-your-own-set-of-of-access-tokens--all-changes-affect-your-production-jumpseller-store-
  version: "1"
host: api.jumpseller.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /products/{id}/options/{option_id}/values.json:
    get:
      summary: Get Products Options Option Values
      description: ""
      operationId: getProductsOptionsOptionValues.json
      x-api-path-slug: productsidoptionsoption-idvalues-json-get
      parameters:
      - in: path
        name: id
        description: ID of the Product
      - in: query
        name: No Name
      - in: path
        name: option_id
        description: ID of the Product Option
      responses:
        200:
          description: OK
      tags:
      - Products
      - Id
      - Options
      - Option
      - Id
      - Values
      - Json
    post:
      summary: Post Products Options Option Values
      description: ""
      operationId: postProductsOptionsOptionValues.json
      x-api-path-slug: productsidoptionsoption-idvalues-json-post
      parameters:
      - in: body
        name: body
        description: Product Option Value parameters
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      - in: path
        name: option_id
        description: Id of the Product Option
      responses:
        200:
          description: OK
      tags:
      - Products
      - Id
      - Options
      - Option
      - Id
      - Values
      - Json
  /products/{id}/options/{option_id}/values/count.json:
    get:
      summary: Get Products Options Option Values Count
      description: ""
      operationId: getProductsOptionsOptionValuesCount.json
      x-api-path-slug: productsidoptionsoption-idvaluescount-json-get
      parameters:
      - in: path
        name: id
        description: ID of the Product
      - in: query
        name: No Name
      - in: path
        name: option_id
        description: ID of the Product Option
      responses:
        200:
          description: OK
      tags:
      - Products
      - Id
      - Options
      - Option
      - Id
      - Values
      - Count
      - Json
  /products/{id}/options/{option_id}/values/{value_id}.json:
    delete:
      summary: Delete Products Options Option Values Value
      description: ""
      operationId: deleteProductsOptionsOptionValuesValue.json
      x-api-path-slug: productsidoptionsoption-idvaluesvalue-id-json-delete
      parameters:
      - in: query
        name: No Name
      - in: path
        name: option_id
        description: Id of the Product Option
      - in: path
        name: value_id
        description: ID of the Product Option Value
      responses:
        200:
          description: OK
      tags:
      - Products
      - Id
      - Options
      - Option
      - Id
      - Values
      - Value
      - Id
      - Json
    get:
      summary: Get Products Options Option Values Value
      description: ""
      operationId: getProductsOptionsOptionValuesValue.json
      x-api-path-slug: productsidoptionsoption-idvaluesvalue-id-json-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: option_id
        description: Id of the Product Option
      - in: path
        name: value_id
        description: ID of the Product Option Value
      responses:
        200:
          description: OK
      tags:
      - Products
      - Id
      - Options
      - Option
      - Id
      - Values
      - Value
      - Id
      - Json
    put:
      summary: Put Products Options Option Values Value
      description: ""
      operationId: putProductsOptionsOptionValuesValue.json
      x-api-path-slug: productsidoptionsoption-idvaluesvalue-id-json-put
      parameters:
      - in: body
        name: body
        description: Product option value parameters to change
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      - in: path
        name: option_id
        description: Id of the Product Option
      - in: path
        name: value_id
        description: Id of the Product Option Value
      responses:
        200:
          description: OK
      tags:
      - Products
      - Id
      - Options
      - Option
      - Id
      - Values
      - Value
      - Id
      - Json
---