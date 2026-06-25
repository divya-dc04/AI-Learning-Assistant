# Authentication APIs:

1. Register:

POST /api/v1/auth/register

Request
{
  "fullName": "",
  "email": "",
  "password": ""
}

Response
{
  "message": "Registration Successful"
}


2. Login:

POST /api/v1/auth/login

Request
{
  "email": "",
  "password": ""
}

Response
{
  "token": "...",
  "refreshToken": "...",
  "user": {}
}


# User APIs: 

GET /api/v1/users/profile

PUT /api/v1/users/profile

DELETE /api/v1/users/profile


# Document APIs:

POST /api/v1/documents/upload

GET /api/v1/documents

GET /api/v1/documents/{id}

DELETE /api/v1/documents/{id}



# AI APIs (Spring Boot → FastAPI):

These are the APIs Spring Boot will call internally.

POST /summary

POST /quiz

POST /flashcards

POST /chat

Later we'll add:

POST /embeddings

POST /rag/query



# Analytics APIs:

GET /api/v1/analytics/dashboard

GET /api/v1/analytics/progress

GET /api/v1/analytics/quiz


# Decide Response Format:

Instead of every API returning different structures, we'll standardize responses.

Example:

{
  "success": true,
  "message": "Document uploaded successfully",
  "data": {
  }
}

For errors:

{
  "success": false,
  "message": "Invalid credentials",
  "errors": []
}

This makes the frontend much easier to develop.



# HTTP Status Codes:

200 OK → Successful request
201 Created → Resource created
400 Bad Request → Invalid input
401 Unauthorized → Invalid or missing JWT
403 Forbidden → User lacks permission
404 Not Found → Resource doesn't exist
500 Internal Server Error → Unexpected server issue