# 🧭 Airline Review Flutter Mobile App Backend [Project ID: P-464]

A comprehensive backend API for managing airline and airport reviews, user profiles, boarding passes, and real-time score calculations. This RESTful API powers a Flutter mobile application that allows users to share and discover flight experiences.

## 📚 Table of Contents

[About](#-about)
[Features](#-features)
[Tech Stack](#-tech-stack)
[Installation](#️-installation)
[Usage](#-usage)
[Configuration](#-configuration)
[Screenshots](#-screenshots)
[API Documentation](#-api-documentation)
[Contact](#-contact)

## 🧩 About

This project provides a robust backend infrastructure for an airline review mobile application. It solves the problem of centralized flight experience management by enabling users to create detailed reviews of airlines and airports, track boarding passes, and access real-time scoring data. The backend handles complex data relationships, automated score calculations, and real-time updates through WebSocket connections. Key goals include providing a scalable API architecture, efficient data storage, and seamless integration with external flight data services like Cirium API.

## ✨ Features

- **User Management** – Create and manage user profiles with badges, points, and profile photos
- **Airline Reviews** – Comprehensive review system with ratings for comfort, cleanliness, service, food, and entertainment
- **Airport Reviews** – Detailed airport experience reviews and ratings
- **Boarding Pass Management** – Store and retrieve boarding pass information with PNR validation
- **Real-time Scoring** – Automated calculation of airline and airport scores based on review data
- **WebSocket Support** – Real-time updates and notifications for live data synchronization
- **Image Upload** – Support for multiple image uploads using AWS S3 integration
- **Cirium API Integration** – Automatic airline and airport data population from external flight data services
- **Score History Tracking** – Historical score tracking for airlines and airports over time
- **Filtered Lists** – Advanced filtering for airlines, airports, and review feeds

## 🧠 Tech Stack

**Languages:** JavaScript (Node.js)

**Frameworks:** Express.js

**Database:** MongoDB (via Mongoose)

**Tools:** 
- WebSocket (ws)
- AWS SDK
- Multer
- Axios
- CORS
- dotenv
- Express Validator

## ⚙️ Installation

### Prerequisites
- Node.js (v16+ recommended)
- MongoDB instance (local or cloud, e.g., MongoDB Atlas)
- AWS S3 bucket (for image storage)
- Cirium API credentials (optional, for airline/airport data)

### Steps

```bash
# Clone the repository
git clone https://github.com/richbeta312/airline-review-backend.git

# Navigate to the project directory
cd airline-review-backend

# Install dependencies
npm install
```

## 🚀 Usage

```bash
# Start the development server
npm start
```

Then open your browser and go to:
👉 [http://localhost:3000](http://localhost:3000)

The server will serve:
- RESTful API endpoints under `/api/v1/` and `/api/v2/`
- WebSocket connections for real-time updates

## 🧾 Configuration

Create a `.env` file in the root directory with the following environment variables:

```
PORT=3000
MONGODB_URI=<your-mongodb-connection-string>
CIRIUM_APP_ID=<your-cirium-app-id>
CIRIUM_APP_KEY=<your-cirium-app-key>
AWS_ACCESS_KEY_ID=<your-aws-access-key>
AWS_SECRET_ACCESS_KEY=<your-aws-secret-key>
AWS_REGION=<your-aws-region>
AWS_S3_BUCKET_NAME=<your-s3-bucket-name>
```

## 🖼 Screenshots




## 📜 API Documentation

All endpoints are prefixed with `/api/v1/` or `/api/v2/` and expect JSON bodies.

### User Management

- `POST /api/v1/user` – Create a new user
- `POST /api/v1/editUser` – Edit user information
- `POST /api/v1/increase-user-points` – Increase user points
- `POST /api/v1/badgeEditUser` – Edit user badges

### Reviews

- `POST /api/v1/airline-review` – Create a new airline review
- `POST /api/v1/airport-review` – Create a new airport review
- `POST /api/v1/airline-review/update` – Update airline review
- `POST /api/v1/airport-review/update` – Update airport review
- `GET /api/v2/airline-reviews` – Get all airline reviews
- `GET /api/v2/airport-reviews` – Get all airport reviews
- `GET /api/v2/top-reviews` – Get top reviews
- `GET /api/v2/user-reviews` – Get user reviews
- `GET /api/v2/entity-reviews` – Get entity reviews
- `GET /api/v2/category-ratings` – Get category ratings

### Boarding Pass Management

- `POST /api/v1/boarding-pass` – Create a new boarding pass
- `POST /api/v1/boarding-pass/update` – Update boarding pass
- `GET /api/v2/boarding-pass` – Retrieve boarding pass information
- `GET /api/v2/boarding-pass/check-pnr` – Check if PNR exists
- `GET /api/v2/boarding-pass/details` – Get detailed boarding pass information

### Airlines & Airports

- `GET /api/v2/airline-airport` – Retrieve airline or airport information
- `GET /api/v2/airline-airport/lists` – Get lists of airlines and airports
- `GET /api/v2/airline-list` – Get filtered airline lists
- `POST /api/v1/airline-airport/create` – Create airline or airport (Admin)
- `POST /api/v1/airline-airport/update` – Update airline or airport (Admin)
- `POST /api/v1/airline-airport/delete` – Delete airline or airport
- `POST /api/v1/airline-cirium/create` – Create airlines from Cirium API (Admin)
- `POST /api/v1/airline-airport/init` – Initialize class counts (Admin)

### Scores & Analytics

- `GET /api/v2/airline-score` – Get airline score data
- `GET /api/v2/airport-score` – Get airport score data
- `POST /api/v1/airline-airport/update-score` – Update score history (Admin)

### Feed & Lists

- `GET /api/v2/feed-list` – Get filtered feed lists




## 📬 Contact

**Author:** Sora Suzuki

**Email:** sorasuzukirich@gmail.com

**GitHub:** @richbeta312

**Website/Portfolio:** sorasuzuki.vercel.app

## 🌟 Acknowledgements

**Libraries & Frameworks:**
- [Express.js](https://expressjs.com/) – Fast, unopinionated web framework for Node.js
- [Mongoose](https://mongoosejs.com/) – Elegant MongoDB object modeling for Node.js
- [WebSocket (ws)](https://github.com/websockets/ws) – Simple to use, blazing fast, and thoroughly tested WebSocket client and server implementation
- [AWS SDK](https://aws.amazon.com/sdk-for-javascript/) – JavaScript SDK for AWS services, used for S3 image storage
- [Multer](https://github.com/expressjs/multer) – Middleware for handling multipart/form-data, primarily used for file uploads
- [Axios](https://axios-http.com/) – Promise-based HTTP client for making API requests to external services
- [Express Validator](https://express-validator.github.io/docs/) – Set of express.js middlewares for input validation
- [CORS](https://github.com/expressjs/cors) – Node.js package for providing a Connect/Express middleware for enabling CORS
- [dotenv](https://github.com/motdotla/dotenv) – Module that loads environment variables from a .env file

**Platforms & Services:**
- [Cirium API](https://www.cirium.com/) – Flight data and airline information service
- [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) – Cloud database hosting
- [AWS S3](https://aws.amazon.com/s3/) – Object storage service for image uploads

**Additional Resources:**
- countries-and-timezones – Library for country and timezone data
- countries-list – Simple list of countries with their ISO codes

**Community & Resources:**
- Node.js community for excellent documentation and support
- Express.js documentation and middleware ecosystem
- MongoDB community for database best practices
