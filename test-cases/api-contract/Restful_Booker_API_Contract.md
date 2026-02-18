## Restful Booker API Contract

### Base URL
https://restful-booker.herokuapp.com

### Authentication
- Token-based authentication
- Token generated using /auth endpoint

### Endpoints

#### POST /booking
- Creates a new booking

#### GET /booking/{id}
- Retrieves booking details

#### PUT /booking/{id}
- Updates booking (Auth required)

#### DELETE /booking/{id}
- Deletes booking (Auth required)

### Common Status Codes
- 200 OK
- 201 Created
- 403 Forbidden
- 404 Not Found
