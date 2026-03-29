# LocalBasket — Backend

This is the backend for LocalBasket, a grocery/local store ordering platform. Built with Node.js and Express, connected to MongoDB, with Cloudinary for image storage, Razorpay for payments, and an OpenAI-powered chatbot baked in.

---

## What's inside

```
localbasket-backend/
├── chatbot/          # AI chatbot logic (OpenAI)
├── config/           # DB connection and other config
├── controllers/      # Route handlers / business logic
├── models/           # Mongoose schemas
├── routes/           # Express route definitions
├── uploads/          # Temp file storage before Cloudinary upload
├── utils/            # Helper functions
├── server.js         # Entry point
└── package.json
```

---

## Tech Stack

- **Node.js + Express** — REST API
- **MongoDB + Mongoose** — database
- **JWT + bcrypt** — auth and password hashing
- **Cloudinary + Multer** — image uploads
- **Razorpay** — payment integration
- **OpenAI** — chatbot
- **node-cron** — scheduled tasks
- **dotenv** — environment config

---

## Getting Started

**1. Clone the repo**

```bash
git clone https://github.com/harshasidhu/localbasket-backend.git
cd localbasket-backend
```

**2. Install dependencies**

```bash
npm install
```

**3. Set up your `.env` file**

Create a `.env` in the root with something like:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_KEY_SECRET=your_razorpay_secret

OPENAI_API_KEY=your_openai_key
```

**4. Run the server**

```bash
npm run dev    # development (nodemon)
npm start      # production
```

Server starts on `http://localhost:5000` by default.

---

## Features

- User registration and login with JWT auth
- Product listing and management with image uploads via Cloudinary
- Cart and order management
- Razorpay payment flow
- Built-in AI chatbot for customer queries
- Scheduled jobs via node-cron (probably for stuff like order status updates or cleanup)

---

## Notes

- Make sure MongoDB is running before starting the server
- Cloudinary and Razorpay keys are required for image upload and payment features to work
- The chatbot won't work without a valid OpenAI API key

---

## Author

[harshasidhu](https://github.com/harshasidhu)
