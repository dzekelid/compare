swagger: "2.0"
x-collection-name: GitHub
x-complete: 1
info:
  title: GitHub
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /repos/{owner}/{repo}/compare/{baseId}...{headId}:
    get:
      summary: Get Repos Owner Repo Compare Base ... Head
      description: Compare two commits
      operationId: compare-two-commits
      x-api-path-slug: reposownerrepocomparebaseid---headid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: baseId
      - in: path
        name: headId
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Compare
      - Base
      - '...'
      - Head