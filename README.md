# urlcount
# 🔗 URL Shortener with Visit Tracking

A simple URL shortening service built with **Node.js**, **Express**, and **MongoDB**. It allows users to shorten long URLs and track how many times each has been accessed.

---

## 🚀 Features

- 🔗 Shorten any long URL to a short identifier.
- 🔁 Redirect users to the original URL using the short link.
- 📊 Track each visit with a timestamp.
- 🧪 View all shortened URLs and visit counts via a test route.

---

## 🛠️ Technologies Used

- Node.js
- Express.js
- MongoDB with Mongoose
- JavaScript (ES6)

---

## 📁 Project Structure

├── connect.js # MongoDB connection logic
├── index.js # Main server file
├── models
│ └── url.js # Mongoose schema for URL documents
├── routes
│ └── url.js # Routes for creating short URLs
└── package.json
---

## 🔧 Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/url-shortener.git
   cd url-shortener
npm install
mongodb://localhost:27017/short-url
node index.js

## API Endpoints
POST /url
Create a short URL
{
  "url": "www.example.com"
}

Response:
{
  "shortId": "a1B2c3"
}

## GET /url/:shortId
Redirect to original URL

Logs visit time in the database.

Redirects the user to the actual site.

## GET /test
View all URLs and visit counts

Returns a simple HTML page listing all shortened URLs and how many times each has been visited.

## SUMMARY: This is a Node.js + Express web server that:

1.Connects to MongoDB (short-url database).

2.Shortens long URLs by assigning them a unique shortId.

3.Redirects users from shortId to the original URL (with GET /url/:shortId).

4.Tracks visits — each time someone visits a short URL, a timestamp is saved in visitHistory.

5.Displays all shortened URLs and their visit counts in an HTML list at the GET /test route.

## Technologies Used:
-Node.js

-Express

-MongoDB with Mongoose

## Example Flow:
POST /url → Create short link

GET /url/abc123 → Redirect + log the visit

GET /test → See list of all short URLs and their visit stats
Body (JSON):
