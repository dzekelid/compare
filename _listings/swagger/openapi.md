---
swagger: "2.0"
x-collection-name: Swagger
x-complete: 1
info:
  title: Swagger Hub Registry
  description: the-registry-api-for-swaggerhub
  contact:
    name: SwaggerHub
    url: http://swaggerhub.com
    email: info@swaggerhub.com
  version: 1.0.45
host: api.swaggerhub.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /apis/{owner}/{api}/{version}/compare:
    get:
      summary: Compares two APIs
      description: Compares two apis.
      operationId: compareApis
      x-api-path-slug: apisownerapiversioncompare-get
      parameters:
      - in: path
        name: api
        description: API identifier
      - in: query
        name: method
        description: The method to use for comparing two APIs
      - in: query
        name: otherApiPath
        description: URL to external API or path to internal API
      - in: path
        name: owner
        description: API owner identifier
      - in: path
        name: version
        description: version identifier
      responses:
        200:
          description: OK
      tags:
      - APIs
      - Owner
      - Version
      - Compare
    post:
      summary: Compares two APIs
      description: Compares two apis.
      operationId: compareApisFromFile
      x-api-path-slug: apisownerapiversioncompare-post
      parameters:
      - in: path
        name: api
        description: API identifier
      - in: body
        name: definition
        description: the definition parsed from an uploaded file
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: method
        description: The method to use for comparing two APIs
      - in: path
        name: owner
        description: API owner identifier
      - in: path
        name: version
        description: version identifier
      responses:
        200:
          description: OK
      tags:
      - APIs
      - Owner
      - Version
      - Compare
---