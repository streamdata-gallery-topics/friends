---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 0
info:
  title: Facebook Get User Friends Friend
  description: Checks if the given user is a friend of the current user
  version: 1.0.0
host: graph.facebook.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{user}/friends:
    get:
      summary: Get User Friends
      description: The user's friends
      operationId: getUserFriends
      x-api-path-slug: userfriends-get
      parameters:
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Friends
  /{user}/friends/{friend}:
    get:
      summary: Get User Friends Friend
      description: Checks if the given user is a friend of the current user
      operationId: getUserFriendsFriend
      x-api-path-slug: userfriendsfriend-get
      parameters:
      - in: path
        name: friend
        description: Represents the ID of the users friend
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Friends
      - Friend
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