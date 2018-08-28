---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Courses API Select students for moderation
  description: Select students for moderation.
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /audit/grade_change/students/{student_id}:
    get:
      summary: Query by student.
      description: Query by student..
      operationId: query-by-student
      x-api-path-slug: auditgrade-changestudentsstudent-id-get
      parameters:
      - in: query
        name: end_time
        description: The end of the time range from which you want events
      - in: query
        name: start_time
        description: The beginning of the time range from which you want events
      responses:
        200:
          description: OK
      tags:
      - Audit
      - Grade
      - Change
      - Students
      - Student
      - Id
  /courses/{course_id}/assignments/assignment_id/gradeable_students:
    get:
      summary: List gradeable students
      description: List gradeable students.
      operationId: list-gradeable-students
      x-api-path-slug: coursescourse-idassignmentsassignment-idgradeable-students-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Gradeable
      - Students
  /courses/{course_id}/assignments/assignment_id/moderated_students:
    get:
      summary: List students selected for moderation
      description: List students selected for moderation.
      operationId: list-students-selected-for-moderation
      x-api-path-slug: coursescourse-idassignmentsassignment-idmoderated-students-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Moderated
      - Students
    post:
      summary: Select students for moderation
      description: Select students for moderation.
      operationId: select-students-for-moderation
      x-api-path-slug: coursescourse-idassignmentsassignment-idmoderated-students-post
      parameters:
      - in: query
        name: student_ids[]
        description: user ids for students to select for moderation
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Moderated
      - Students
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