swagger: "2.0"
x-collection-name: GitLab
x-complete: 1
info:
  title: API title
  version: 1.0.0
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