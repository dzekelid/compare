---
swagger: "2.0"
x-collection-name: GitLab
x-complete: 0
info:
  title: GitLab Get Projects Repository Compare
  version: 1.0.0
  description: Compare two branches, tags, or commits
host: localhost:3000
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/projects/{id}/repository/compare:
    get:
      summary: Get Projects Repository Compare
      description: Compare two branches, tags, or commits
      operationId: getV3ProjectsIdRepositoryCompare
      x-api-path-slug: v3projectsidrepositorycompare-get
      parameters:
      - in: query
        name: from
        description: The commit, branch name, or tag name to start comparison
      - in: path
        name: id
        description: The ID of a project
      - in: query
        name: to
        description: The commit, branch name, or tag name to stop comparison
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Compare
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---