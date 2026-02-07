🧭 Airline Review Flutter Mobile App Backend [Project ID: P-464]
A comprehensive backend API for managing airline and airport reviews, user profiles, boarding passes, and real-time score calculations. This RESTful API powers a Flutter mobile application that allows users to share and discover flight experiences.



📚 Table of Contents
[About](#about)
[Features](#features)
[Tech Stack](#tech-stack)
[Installation](#installation)
[Usage](#usage)
[Configuration](#configuration)
[Screenshots](#screenshots)
[API Documentation](#api-documentation)
[Contact](#contact)



🧩 About
This project provides a robust backend infrastructure for an airline review mobile application. It solves the problem of centralized flight experience management by enabling users to create detailed reviews of airlines and airports, track boarding passes, and access real-time scoring data. The backend handles complex data relationships, automated score calculations, and real-time updates through WebSocket connections. Key goals include providing a scalable API architecture, efficient data storage, and seamless integration with external flight data services like Cirium API.



✨ Features
User Management – Create and manage user profiles with badges, points, and profile photos
Airline Reviews – Comprehensive review system with ratings for comfort, cleanliness, service, food, and entertainment
Airport Reviews – Detailed airport experience reviews and ratings
Boarding Pass Management – Store and retrieve boarding pass information with PNR validation
Real-time Scoring – Automated calculation of airline and airport scores based on review data
WebSocket Support – Real-time updates and notifications for live data synchronization
Image Upload – Support for multiple image uploads using AWS S3 integration
Cirium API Integration – Automatic airline and airport data population from external flight data services
Score History Tracking – Historical score tracking for airlines and airports over time
Filtered Lists – Advanced filtering for airlines, airports, and review feeds



🧠 Tech Stack
Languages: JavaScript
Frameworks: Express.js, Node.js
Database: MongoDB (Mongoose ODM)
Tools: WebSocket (ws), AWS SDK, Multer, Axios, CORS, dotenv, Express Validator



⚙️ Installation
# Clone the repository
git clone https://github.com/richbeta312/airline-review-backend.git

# Navigate to the project directory
cd airline-review-backend

# Install dependencies
npm install




🚀 Usage
# Start the development server
npm start


Then open your browser and go to:
👉 [http://localhost:3000](http://localhost:3000)



🧾 Configuration
Create a `.env` file in the root directory with the following environment variables:

PORT=3000
MONGODB_URI=your_mongodb_connection_string
CIRIUM_APP_ID=your_cirium_app_id
CIRIUM_APP_KEY=your_cirium_app_key
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
AWS_REGION=your_aws_region
AWS_S3_BUCKET_NAME=your_s3_bucket_name




🖼 Screenshots
Add demo images, GIFs, or UI preview screenshots.

Example:




📜 API Documentation
The API is organized into GET and POST endpoints:

**GET Endpoints:**
- `GET /api/v2/airline-airport` – Retrieve airline or airport information
- `GET /api/v2/airline-reviews` – Get all airline reviews
- `GET /api/v2/airport-reviews` – Get all airport reviews
- `GET /api/v2/boarding-pass` – Retrieve boarding pass information
- `GET /api/v2/airline-score` – Get airline score data
- `GET /api/v2/airport-score` – Get airport score data
- `GET /api/v2/airline-airport/lists` – Get lists of airlines and airports
- `GET /api/v2/boarding-pass/check-pnr` – Check if PNR exists
- `GET /api/v2/boarding-pass/details` – Get detailed boarding pass information
- `GET /api/v2/airline-list` – Get filtered airline lists
- `GET /api/v2/feed-list` – Get filtered feed lists
- `GET /api/v2/category-ratings` – Get category ratings
- `GET /api/v2/top-reviews` – Get top reviews
- `GET /api/v2/user-reviews` – Get user reviews
- `GET /api/v2/entity-reviews` – Get entity reviews

**POST Endpoints:**
- `POST /api/v1/user` – Create a new user
- `POST /api/v1/editUser` – Edit user information
- `POST /api/v1/increase-user-points` – Increase user points
- `POST /api/v1/badgeEditUser` – Edit user badges
- `POST /api/v1/airport-review` – Create a new airport review
- `POST /api/v1/airline-review` – Create a new airline review
- `POST /api/v1/boarding-pass` – Create a new boarding pass
- `POST /api/v1/boarding-pass/update` – Update boarding pass
- `POST /api/v1/airline-review/update` – Update airline review
- `POST /api/v1/airport-review/update` – Update airport review
- `POST /api/v1/airline-airport/delete` – Delete airline or airport
- `POST /api/v1/airline-airport/create` – Create airline or airport (Admin)
- `POST /api/v1/airline-cirium/create` – Create airlines from Cirium API (Admin)
- `POST /api/v1/airline-airport/update` – Update airline or airport (Admin)
- `POST /api/v1/airline-airport/init` – Initialize class counts (Admin)
- `POST /api/v1/airline-airport/update-score` – Update score history (Admin)




📬 Contact
Author: Sora Suzuki
Email: sorasuzukirich@gmail.com
GitHub: @richbeta312
Website/Portfolio: sorasuzuki.vercel.app



🌟 Acknowledgements
This project was built using the following open-source libraries and resources:

- **Express.js** – Fast, unopinionated web framework for Node.js
- **Mongoose** – Elegant MongoDB object modeling for Node.js
- **WebSocket (ws)** – Simple to use, blazing fast, and thoroughly tested WebSocket client and server implementation
- **AWS SDK** – JavaScript SDK for AWS services, used for S3 image storage
- **Multer** – Middleware for handling multipart/form-data, primarily used for file uploads
- **Axios** – Promise-based HTTP client for making API requests to external services
- **Cirium API** – Flight data and airline information service
- **Express Validator** – Set of express.js middlewares for input validation
- **CORS** – Node.js package for providing a Connect/Express middleware for enabling CORS
- **dotenv** – Module that loads environment variables from a .env file
- **countries-and-timezones** – Library for country and timezone data
- **countries-list** – Simple list of countries with their ISO codes

Special thanks to the Node.js and Express.js communities for their excellent documentation and support.
