# Number Classification API

## Overview
This project is a **Spring Boot API** that classifies a given number based on its mathematical properties and provides a fun fact from the **Numbers API**.

## Features
- Identifies if a number is **prime**
- Determines if a number is **perfect**
- Checks if a number is an **Armstrong number**
- Classifies a number as **odd/even**
- Computes the **sum of digits**
- Fetches a **fun fact** from Numbers API
- Provides **CORS support**

## API Specification
### Endpoint:
`GET /api/classify-number?number={number}`

### Example Request:
```
GET https://topg.up.railway.app/api/classify-number?number=371
```

### Success Response (200 OK):
```json
{
    "number": 371,
    "is_prime": false,
    "is_perfect": false,
    "properties": ["armstrong", "odd"],
    "digit_sum": 11,
    "fun_fact": "371 is an Armstrong number because 3^3 + 7^3 + 1^3 = 371"
}
```

### Error Response (400 Bad Request):
```json
{
    "number": "abc",
    "error": true
}
```

## Installation & Setup
### Prerequisites
- Java 17+
- Maven
- Git

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/dmadindividual/Backend--Number-Classification-API.git
   cd Backend--Number-Classification-API
   ```
2. Build and run the application:
   ```sh
   mvn spring-boot:run
   ```
3. Access the API at:
   ```
   http://localhost:8080/api/classify-number?number=371
   ```

## Deployment
This API can be deployed using **Render, Railway, or Vercel**. Ensure the following:
- CORS is enabled
- The API is publicly accessible

## Contribution
Feel free to open issues and submit pull requests!

## License
MIT License

