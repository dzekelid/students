swagger: "2.0"
x-collection-name: Google Classroom
x-complete: 1
info:
  title: Google Classroom
  description: manages-classes-rosters-and-invitations-in-google-classroom-
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
  /v1/courses/{courseId}/students:
    get:
      summary: Get Students
      description: |-
        Returns a list of students of this course that the requester
        is permitted to view.

        This method returns the following error codes:

        * `NOT_FOUND` if the course does not exist.
        * `PERMISSION_DENIED` for access errors.
      operationId: classroom.courses.students.list
      x-api-path-slug: v1coursescourseidstudents-get
      parameters:
      - in: path
        name: courseId
        description: Identifier of the course
      - in: query
        name: pageSize
        description: Maximum number of items to return
      - in: query
        name: pageToken
        description: nextPageTokenvalue returned from a previouslist call, indicating
          thatthe subsequent page of results should be returned
      responses:
        200:
          description: OK
      tags:
      - Student
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
  /v1/courses/{courseId}/students/{userId}:
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