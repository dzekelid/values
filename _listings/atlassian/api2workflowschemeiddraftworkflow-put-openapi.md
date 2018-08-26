---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Update draft workflow mapping
  description: |-
    Update the draft scheme to include the passed mapping.

    The body is a representation of the workflow mapping. Values not passed are assumed to indicate no change for that field.
  termsOfService: http://atlassian.com/terms/
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/2/workflowscheme:
    post:
      summary: Create workflow scheme
      description: |-
        Create a new workflow scheme.

        The body contains a representation of the new scheme. Values not passed are assumed to be set to their defaults.
      operationId: com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.createWorkflowScheme_post
      x-api-path-slug: api2workflowscheme-post
      responses:
        200:
          description: OK
      tags:
      - Workflow
      - Scheme
  /api/2/workflowscheme/{id}:
    put:
      summary: Update workflow scheme
      description: |-
        Update the passed workflow scheme.

        The body of the request is a representation of the workflow scheme. Values not passed are assumed to indicate no change for that field.

        The passed representation can have its updateDraftIfNeeded flag set to true to indicate that the draft should be created and/or updated when the actual scheme cannot be edited (e.g. when the scheme is being used by a project). Values not appearing the body will not be touched.
      operationId: com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.updateWorkflowScheme_put
      x-api-path-slug: api2workflowschemeid-put
      parameters:
      - in: path
        name: id
        description: the id of the scheme
      responses:
        200:
          description: OK
      tags:
      - Workflow
      - Scheme
  /api/2/workflowscheme/{id}/draft:
    put:
      summary: Update workflow scheme draft
      description: |-
        Update a draft workflow scheme. The draft will created if necessary.

        The body is a representation of the workflow scheme. Values not passed are assumed to indicate no change for that field.
      operationId: com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.updateWorkflowSchemeDraft_put
      x-api-path-slug: api2workflowschemeiddraft-put
      parameters:
      - in: path
        name: id
        description: the id of the parent scheme
      responses:
        200:
          description: OK
      tags:
      - Workflow
      - Scheme
      - Draft
  /api/2/workflowscheme/{id}/draft/workflow:
    put:
      summary: Update draft workflow mapping
      description: |-
        Update the draft scheme to include the passed mapping.

        The body is a representation of the workflow mapping. Values not passed are assumed to indicate no change for that field.
      operationId: com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.updateDraftWorkflowMapping_pu
      x-api-path-slug: api2workflowschemeiddraftworkflow-put
      parameters:
      - in: path
        name: id
        description: the id of the parent scheme
      - in: query
        name: workflowName
        description: the name of the workflow mapping to update
      responses:
        200:
          description: OK
      tags:
      - Draft
      - Workflow
      - Mapping
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