---
swagger: "2.0"
x-collection-name: Google Compute Engine
x-complete: 0
info:
  title: Google Compute Engine API Create Autoscaler
  description: Creates an autoscaler in the specified project using the data included
    in the request.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /compute/v1/projects
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{project}/aggregated/autoscalers:
    get:
      summary: Get Autoscalers
      description: Retrieves an aggregated list of autoscalers.
      operationId: compute.autoscalers.aggregatedList
      x-api-path-slug: projectaggregatedautoscalers-get
      parameters:
      - in: query
        name: filter
        description: Sets a filter expression for filtering listed resources, in the
          form filter={expression}
      - in: query
        name: maxResults
        description: The maximum number of results per page that should be returned
      - in: query
        name: orderBy
        description: Sorts list results by a certain order
      - in: query
        name: pageToken
        description: Specifies a page token to use
      - in: path
        name: project
        description: Project ID for this request
      responses:
        200:
          description: OK
      tags:
      - Autoscaler
      - Aggregation
  /{project}/regions/{region}/autoscalers:
    get:
      summary: Get Autoscalers
      description: Retrieves a list of autoscalers contained within the specified
        region.
      operationId: compute.regionAutoscalers.list
      x-api-path-slug: projectregionsregionautoscalers-get
      parameters:
      - in: query
        name: filter
        description: Sets a filter expression for filtering listed resources, in the
          form filter={expression}
      - in: query
        name: maxResults
        description: The maximum number of results per page that should be returned
      - in: query
        name: orderBy
        description: Sorts list results by a certain order
      - in: query
        name: pageToken
        description: Specifies a page token to use
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region scoping this request
      responses:
        200:
          description: OK
      tags:
      - Autoscaler
    patch:
      summary: Update Autoscaler
      description: Updates an autoscaler in the specified project using the data included
        in the request. This method supports patch semantics.
      operationId: compute.regionAutoscalers.patch
      x-api-path-slug: projectregionsregionautoscalers-patch
      parameters:
      - in: query
        name: autoscaler
        description: Name of the autoscaler to update
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region scoping this request
      responses:
        200:
          description: OK
      tags:
      - Autoscaler
    post:
      summary: Create Autoscaler
      description: Creates an autoscaler in the specified project using the data included
        in the request.
      operationId: compute.regionAutoscalers.insert
      x-api-path-slug: projectregionsregionautoscalers-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region scoping this request
      responses:
        200:
          description: OK
      tags:
      - Autoscaler
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