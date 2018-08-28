---
swagger: "2.0"
x-collection-name: Google Classroom
x-complete: 0
info:
  title: Google Classroom API Get Student
  description: |-
    Returns a student of a course.

    This method returns the following error codes:

    * `PERMISSION_DENIED` if the requesting user is not permitted to view
    students of this course or for access errors.
    * `NOT_FOUND` if no student of this course has the requested ID or if the
    course does not exist.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: classroom.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/courses/{courseId}/students/{userId}:
    get:
      summary: Get Student
      description: |-
        Returns a student of a course.

        This method returns the following error codes:

        * `PERMISSION_DENIED` if the requesting user is not permitted to view
        students of this course or for access errors.
        * `NOT_FOUND` if no student of this course has the requested ID or if the
        course does not exist.
      operationId: classroom.courses.students.get
      x-api-path-slug: v1coursescourseidstudentsuserid-get
      parameters:
      - in: path
        name: courseId
        description: Identifier of the course
      - in: path
        name: userId
        description: Identifier of the student to return
      responses:
        200:
          description: OK
      tags:
      - Student
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