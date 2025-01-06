ShoppyGlobe Backend Code
Welcome to the backend of ShoppyGlobe, a modern and seamless e-commerce platform designed to deliver excellent shopping experiences. This backend is built with Node.js, Express, and MongoDB to provide user authentication, product management, and cart functionality.

🚀 Project Link
ShoppyGlobe Backend on GitHub

🛠 Features
User Authentication: Secure user registration and login with password hashing (Bcrypt).
Product Management: CRUD operations to manage products.
Cart Management: Add, update, and delete items from the shopping cart.
Middleware: Centralized error handling, field validation, and JWT authentication for secure routes.
Database: MongoDB used for storing product and cart data.
⚡ Getting Started
Prerequisites
Make sure you have the following installed:

Node.js (v14 or later)
MongoDB (local or hosted instance)
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/Ayushgreat/Shoppyglobe_backend_Code.git
cd Shoppyglobe_backend_Code
Install dependencies:

bash
Copy code
npm install
Set up your environment variables:

Create a .env file in the root directory and add the following variables:

env
Copy code
PORT=3000
DATABASE_NAME=your_database_name
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET_KEY=your_jwt_secret_key
Start the server:

bash
Copy code
npm start
The server will run on http://127.0.0.1:3000.

📝 API Endpoints
Users
Method	Endpoint	Description
POST	/api/auth/register	Register a new user
POST	/api/auth/login	Login a user
Products
Method	Endpoint	Description
GET	/api/products	Get all products
GET	/api/products/:id	Get a product by its ID
POST	/api/products	Add a new product
PUT	/api/products/:id	Update a product by ID
DELETE	/api/products/:id	Delete a product by its ID
Cart
Method	Endpoint	Description
GET	/api/cart/:id	Get all cart items for a user
GET	/api/cart/items/:id	Get cart item by ID for a user
POST	/api/cart	Add an item to the cart
PUT	/api/cart/items/:id	Update an item in the cart
DELETE	/api/cart/:id	Remove an item from the cart
📂 Project Structure
plaintext
Copy code
shoppy-globe-backend/
├── config/            # Configuration files (e.g., database connection)
├── controllers/       # Route handlers for users, products, and cart
├── middlewares/       # Custom middleware (error handling, validation, authentication)
├── models/            # Mongoose models for MongoDB collections
├── routes/            # API routes for handling endpoints
├── server.js          # Entry point to start the server
└── .env               # Environment variables
⚙️ Dependencies
Express: Web framework for building APIs.
Mongoose: MongoDB ODM for database interactions.
Bcrypt: Password hashing for secure authentication.
jsonwebtoken: JWT for token-based user authentication.
dotenv: Manage environment variables securely.
📝 License
This project is licensed under the MIT License. See the LICENSE file for details.

👨‍💻 API Usage with ThunderClient
Use ThunderClient or Postman to test all the APIs. Here are a few tips:

Login and Registration: Start by registering a user and then log in to get the JWT token.
Authentication: All cart routes are protected. Use the JWT token in the Authorization header (Bearer <your_token>).
