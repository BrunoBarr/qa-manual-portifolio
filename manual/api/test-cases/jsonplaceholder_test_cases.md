# API Test Cases – JSONPlaceholder

## TC-API-GET-01 — Get all posts

**Method:** GET  
**Endpoint:** /posts

**Steps:**
1. Send GET request to `/posts`

**Expected Result:**
- Status code 200
- Response body contains a list of posts

---

## TC-API-GET-02 — Get post by valid ID

**Method:** GET  
**Endpoint:** /posts/1

**Expected Result:**
- Status code 200
- Response contains post with ID 1

---

## TC-API-GET-03 — Get post by invalid ID

**Method:** GET  
**Endpoint:** /posts/9999

**Expected Result:**
- Status code 404 or empty response

---

## TC-API-POST-01 — Create new post

**Method:** POST  
**Endpoint:** /posts

**Body (JSON):**
```json
{
  "title": "QA Test",
  "body": "Testing API with Postman",
  "userId": 1
}
```
**Expected Result:**
- Status code 201
- Response returns created object with ID

## TC-API-DELETE-01 — Delete post

**Method:** DELETE
**Endpoint:** /posts/1

**Expected Result:** 
- Status code 200 or 204