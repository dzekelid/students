---
name: Google Classroom
x-slug: google-classroom
description: Google Classroom is mission control for your classes. As a free service
  for teachers and students, you can create classes, distribute assignments, send
  feedback, and see everything in one place. Instant. Paperless. Easy.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-classroom.png
x-kinRank: "9"
x-alexaRank: "0"
tags: Student
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/student/master/_listings/google-classroom/apis.md
specificationVersion: "0.14"
apis:
- name: Google Classroom - Get Student
  x-api-slug: v1coursescourseidstudentsuserid-get
  description: |-
    Returns a student of a course.

    This method returns the following error codes:

    * `PERMISSION_DENIED` if the requesting user is not permitted to view
    students of this course or for access errors.
    * `NOT_FOUND` if no student of this course has the requested ID or if the
    course does not exist.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-classroom.png
  humanURL: https://classroom.google.com/
  baseURL: ://classroom.googleapis.com//
  tags: Education, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/student/master/_listings/google-classroom/v1coursescourseidstudentsuserid-get-openapi.md
- name: Google Classroom - Delete Student
  x-api-slug: v1coursescourseidstudentsuserid-delete
  description: |-
    Deletes a student of a course.

    This method returns the following error codes:

    * `PERMISSION_DENIED` if the requesting user is not permitted to delete
    students of this course or for access errors.
    * `NOT_FOUND` if no student of this course has the requested ID or if the
    course does not exist.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-classroom.png
  humanURL: https://classroom.google.com/
  baseURL: ://classroom.googleapis.com//
  tags: Education, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/student/master/_listings/google-classroom/v1coursescourseidstudentsuserid-delete-openapi.md
- name: Google Classroom - Add Student
  x-api-slug: v1coursescourseidstudents-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-classroom.png
  humanURL: https://classroom.google.com/
  baseURL: ://classroom.googleapis.com//
  tags: Education, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/student/master/_listings/google-classroom/v1coursescourseidstudents-post-openapi.md
- name: Google Classroom - Get Students
  x-api-slug: v1coursescourseidstudents-get
  description: |-
    Returns a list of students of this course that the requester
    is permitted to view.

    This method returns the following error codes:

    * `NOT_FOUND` if the course does not exist.
    * `PERMISSION_DENIED` for access errors.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-classroom.png
  humanURL: https://classroom.google.com/
  baseURL: ://classroom.googleapis.com//
  tags: Education, Google APIs, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/student/master/_listings/google-classroom/v1coursescourseidstudents-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://google.civic.information.api.gallery.streamdata.io
- type: x-api-stack
  url: http://google.classroom.stack.network
- type: x-button
  url: https://developers.google.com/classroom/guides/sharebutton
- type: x-developer
  url: https://developers.google.com/classroom/
- type: x-getting-started
  url: ""
- type: x-issues
  url: https://code.google.com/a/google.com/p/apps-api-issues/issues/list?can=2&q=label%3AAPI-Classroom
- type: x-website
  url: https://classroom.google.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---