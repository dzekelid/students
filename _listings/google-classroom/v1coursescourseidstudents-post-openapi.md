---
swagger: "2.0"
x-collection-name: Google Classroom
x-complete: 0
info:
  title: Google Classroom API Add Student
  description: |-
    Adds a user as a student of a course.

    This method returns the following error codes:

    * `PERMISSION_DENIED` if the requesting user is not permitted to create
    students in this course or for access errors.
    * `NOT_FOUND` if the requested course ID does not exist.
    * `FAILED_PRECONDITION` if the requested user's account is disabled,
    for the following request errors:
        * CourseMemberLimitReached
        * CourseNotModifiable
        * UserGroupsMembershipLimitReached
    * `ALREADY_EXISTS` if the user is already a student or teacher in the
    course.
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
    delete:
      summary: Delete Student
      description: |-
        Deletes a student of a course.

        This method returns the following error codes:

        * `PERMISSION_DENIED` if the requesting user is not permitted to delete
        students of this course or for access errors.
        * `NOT_FOUND` if no student of this course has the requested ID or if the
        course does not exist.
      operationId: classroom.courses.students.delete
      x-api-path-slug: v1coursescourseidstudentsuserid-delete
      parameters:
      - in: path
        name: courseId
        description: Identifier of the course
      - in: path
        name: userId
        description: Identifier of the student to delete
      responses:
        200:
          description: OK
      tags:
      - Student
  /v1/courses/{courseId}/students:
    post:
      summary: Add Student
      description: |-
        Adds a user as a student of a course.

        This method returns the following error codes:

        * `PERMISSION_DENIED` if the requesting user is not permitted to create
        students in this course or for access errors.
        * `NOT_FOUND` if the requested course ID does not exist.
        * `FAILED_PRECONDITION` if the requested user's account is disabled,
        for the following request errors:
            * CourseMemberLimitReached
            * CourseNotModifiable
            * UserGroupsMembershipLimitReached
        * `ALREADY_EXISTS` if the user is already a student or teacher in the
        course.
      operationId: classroom.courses.students.create
      x-api-path-slug: v1coursescourseidstudents-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: courseId
        description: Identifier of the course to create the student in
      - in: query
        name: enrollmentCode
        description: Enrollment code of the course to create the student in
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