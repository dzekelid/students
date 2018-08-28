swagger: "2.0"
x-collection-name: PayRun
x-complete: 1
info:
  title: Pay Run.IO
  description: open-scableable-transparent-payroll-api-
  version: 17.18.6.206
host: api.test.payrun.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Templates/studentloanytdpayinstruction:
    get:
      summary: Gets the student loan YTD pay instruction template
      description: Return the student loan YTD pay instruction data object template
      operationId: GetStudentLoanYtdPayInstructionTemplate
      x-api-path-slug: templatesstudentloanytdpayinstruction-get
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      responses:
        200:
          description: OK
      tags:
      - Student
      - Loan
      - YTD
      - Pay
      - Instruction
      - Template
  /Templates/studentloanpayinstruction:
    get:
      summary: Gets the student loan pay instruction template
      description: Return the student loan pay instruction data object template
      operationId: GetStudentLoanPayInstructionTemplate
      x-api-path-slug: templatesstudentloanpayinstruction-get
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      responses:
        200:
          description: OK
      tags:
      - Student
      - Loan
      - Pay
      - Instruction
      - Template
  /Templates/paylinestudentloan:
    get:
      summary: Gets the pay line student loan template
      description: Return the pay line student loan data object template
      operationId: GetPayLineStudentLoanTemplate
      x-api-path-slug: templatespaylinestudentloan-get
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      responses:
        200:
          description: OK
      tags:
      - Pay
      - Line
      - Student
      - Loan
      - Template