---
swagger: "2.0"
x-collection-name: SAP
x-complete: 0
info:
  title: SAP Manufacturing Network Customer APIs Reopens a collaboration
  description: "Reopens a completed collaboration.  \nThe collaboration is set back
    to the status 'In Process'.\nThe login user must be a collaboration lead for the
    customer."
  version: 1.0.0
host: hostname
basePath: /dim/api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /collaborationRooms:
    post:
      summary: Creates a collaboration room
      description: "Creates a collaboration room.  \nThe login user must be from a
        customer."
      operationId: creates-a-collaboration-room--the-login-user-must-be-from-a-customer
      x-api-path-slug: collaborationrooms-post
      parameters:
      - in: body
        name: CollaborationRoomCreateRequest
        description: A request about creating a collaboration room
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - Creates
      - Collaboration
      - Room
  /collaborationRooms/{collaborationRoomId}:
    get:
      summary: Retrieves a collaboration room
      description: Retrieves the information of a collaboration room by its ID.
      operationId: retrieves-the-information-of-a-collaboration-room-by-its-id
      x-api-path-slug: collaborationroomscollaborationroomid-get
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      responses:
        200:
          description: Successful response
      tags:
      - Retrieves
      - Collaboration
      - Room
    patch:
      summary: Updates a collaboration room
      description: Updates a collaboration room.
      operationId: updates-a-collaboration-room
      x-api-path-slug: collaborationroomscollaborationroomid-patch
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      - in: body
        name: CollaborationRoomUpdateRequest
        description: A request about updating a collaboration room
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - S
      - Collaboration
      - Room
    delete:
      summary: Deletes a collaboration room
      description: |-
        Deletes a collaboration room
        The login user must be a collaboration lead for the customer and it must be a new or discarded collaboration.
      operationId: deletes-a-collaboration-roomthe-login-user-must-be-a-collaboration-lead-for-the-customer-and-it-must
      x-api-path-slug: collaborationroomscollaborationroomid-delete
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      responses:
        200:
          description: Successful response
      tags:
      - S
      - Collaboration
      - Room
  /collaborationRooms/{collaborationRoomId}/basic:
    get:
      summary: Retrieves basic info of a collaboration room
      description: Retrieves the information of a collaboration room in a simplified
        form.
      operationId: retrieves-the-information-of-a-collaboration-room-in-a-simplified-form
      x-api-path-slug: collaborationroomscollaborationroomidbasic-get
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      responses:
        200:
          description: Successful response
      tags:
      - Retrieves
      - Basic
      - Info
      - Of
      - Collaboration
      - Room
  /collaborationRooms/{collaborationRoomId}/start:
    post:
      summary: Starts a collaboration
      description: "Sets a collaboration in process.  \nThe collaboration must be
        a new collaboration."
      operationId: sets-a-collaboration-in-process--the-collaboration-must-be-a-new-collaboration
      x-api-path-slug: collaborationroomscollaborationroomidstart-post
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      responses:
        200:
          description: Successful response
      tags:
      - Starts
      - Collaboration
  /collaborationRooms/{collaborationRoomId}/complete:
    post:
      summary: Completes a collaboration
      description: |-
        Sets a collaboration as completed
        - The login user must be a collaboration lead for the customer.
        - If there's already a supplier in the collaboration room, the collaboration must already or still be in process.
        - If there's already a completed collaboration with the same additive manufacturing supplier, part ID, and customer, this operation fails.
      operationId: sets-a-collaboration-as-completed-the-login-user-must-be-a-collaboration-lead-for-the-customer-if-th
      x-api-path-slug: collaborationroomscollaborationroomidcomplete-post
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      responses:
        200:
          description: Successful response
      tags:
      - Completes
      - Collaboration
  /collaborationRooms/{collaborationRoomId}/discard:
    post:
      summary: Discards a collaboration
      description: "Sets a collaboration as discarded.  \nThe login user must be a
        collaboration lead for the customer and the collaboration must be in process
        or completed."
      operationId: sets-a-collaboration-as-discarded--the-login-user-must-be-a-collaboration-lead-for-the-customer-and-
      x-api-path-slug: collaborationroomscollaborationroomiddiscard-post
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      responses:
        200:
          description: Successful response
      tags:
      - Discards
      - Collaboration
  /collaborationRooms/{collaborationRoomId}/reopen:
    post:
      summary: Reopens a collaboration
      description: "Reopens a completed collaboration.  \nThe collaboration is set
        back to the status 'In Process'.\nThe login user must be a collaboration lead
        for the customer."
      operationId: reopens-a-completed-collaboration--the-collaboration-is-set-back-to-the-status-in-processthe-login-u
      x-api-path-slug: collaborationroomscollaborationroomidreopen-post
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      responses:
        200:
          description: Successful response
      tags:
      - Reopens
      - Collaboration
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