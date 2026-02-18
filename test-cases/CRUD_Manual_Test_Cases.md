## Manual API Test Cases – CRUD Operations

### Application
Restful Booker API

### Tool Used
Postman

---

### TC_API_01 – Create Booking (POST)

- **Endpoint:** /booking
- **Method:** POST
- **Request Body:** Valid booking JSON
- **Expected Status Code:** 200
- **Expected Result:** Booking ID should be generated

---

### TC_API_02 – Get Booking by Valid ID (GET)

- **Endpoint:** /booking/{id}
- **Method:** GET
- **Precondition:** Booking exists
- **Expected Status Code:** 200
- **Expected Result:** Booking details should be returned

---

### TC_API_03 – Update Booking with Valid Token (PUT)

- **Endpoint:** /booking/{id}
- **Method:** PUT
- **Headers:** Cookie: token={valid_token}
- **Expected Status Code:** 200
- **Expected Result:** Booking details should be updated

---

### TC_API_04 – Delete Booking with Valid Token (DELETE)

- **Endpoint:** /booking/{id}
- **Method:** DELETE
- **Headers:** Cookie: token={valid_token}
- **Expected Status Code:** 201
- **Expected Result:** Booking should be deleted

---

### TC_API_05 – Verify Deleted Booking (GET)

- **Endpoint:** /booking/{id}
- **Method:** GET
- **Expected Status Code:** 404
- **Expected Result:** Booking should not be found

---

## Negative Test Cases

### TC_API_06 – Update Booking Without Token
- **Method:** PUT
- **Expected Result:** 403 Forbidden

### TC_API_07 – Delete Booking Without Token
- **Method:** DELETE
- **Expected Result:** 403 Forbidden
