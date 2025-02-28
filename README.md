# -Link-Shortener
Skills Required – Node, MongoDB,JavaScript

Key Features of the URL Shortener
The URL shortener I've created includes:

URL Shortening: Convert long URLs to short, memorable ones
Redirection: Redirect from short URL to the original long URL
Click Tracking: Count how many times each short URL has been accessed
Statistics API: Get usage stats for each shortened URL
URL Validation: Ensure only valid URLs are shortened
Persistence: Store all URLs in MongoDB database

Project Structure
The project is organized into several files:

index.js: Main server file that sets up Express and MongoDB
models/Url.js: MongoDB schema for URL data
routes/url.js: API endpoints for URL operations
utils/generateShortUrl.js: Helper to generate unique short codes

API Endpoints

POST /api/url/shorten: Create a short URL

Request body: { "longUrl": "https://example.com/very/long/path" }
Response: URL object with both long and short URLs


GET /:code: Redirect to the original long URL

Example: http://localhost:5000/abc123 redirects to the original URL


GET /api/url/stats/:code: Get statistics for a specific URL

Returns details including click count


GET /api/url/list: List all shortened URLs

How to Run the Project

Install Node.js and MongoDB
Create a new directory and save the files as shown in the code above
Run npm install to install dependencies
Create a .env file with your configuration
Start MongoDB
Run the server with npm start or npm run dev

Possible Enhancements
If you'd like to expand this project, consider:

Adding user authentication to track who created which URLs
Creating custom short URLs instead of randomly generated ones
Adding expiration dates for URLs
Implementing rate limiting to prevent abuse
Building a front-end interface
Adding analytics (geolocation, browser info, etc.)

Alternative Technologies
If you prefer to use a different tech stack:

Python: Use Flask/Django with PyMongo or SQLAlchemy
Java: Spring Boot with JPA/Hibernate
PHP: Laravel with Eloquent ORM
Go: Use Gin or Echo frameworks with GORM
