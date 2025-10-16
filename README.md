# Manoj Blog - Full-Stack Blogging Platform

A modern, full-featured blogging platform built with Node.js, Express, MongoDB, and EJS. This application provides a complete blogging experience with user authentication, post management, commenting system, and cloud-based image storage.

## 🚀 Features

- **User Authentication & Authorization**
  - Secure registration and login using Passport.js
  - Password encryption with bcryptjs
  - Session management with MongoDB store
  - Protected routes and role-based access

- **Blog Post Management**
  - Create, read, update, and delete blog posts
  - Rich text content support
  - Multiple image uploads per post
  - Author attribution and timestamps

- **User Profiles**
  - Customizable user profiles with bio
  - Profile picture upload
  - View user's published posts
  - Edit profile information

- **Comment System**
  - Add comments to blog posts
  - Edit and delete own comments
  - Comment moderation

- **Cloud Storage Integration**
  - Image uploads to Cloudinary
  - Optimized image storage and delivery
  - Support for profile pictures and post images

## 🛠️ Tech Stack

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling

### Authentication & Security
- **Passport.js** - Authentication middleware
- **bcryptjs** - Password hashing
- **express-session** - Session management
- **connect-mongo** - MongoDB session store

### File Upload & Storage
- **Multer** - File upload middleware
- **Cloudinary** - Cloud-based image storage

### View Engine
- **EJS** - Embedded JavaScript templating
- **Bootstrap** - Responsive UI framework
- **Font Awesome** - Icon library

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Manoj-3428/BlogApplication.git
   cd BlogApplication
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory and add:
   ```env
   PORT=3000
   MONGODB_URL=your_mongodb_connection_string
   CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   ```

4. **Start the application**
   ```bash
   npm start
   ```

5. **Access the application**
   
   Open your browser and navigate to `http://localhost:3000`

## 📁 Project Structure

```
BlogApplication/
│
├── config/              # Configuration files
│   ├── cloudinary.js    # Cloudinary configuration
│   ├── multer.js        # Multer configuration
│   └── passport.js      # Passport authentication strategy
│
├── controllers/         # Route controllers
│   ├── authController.js
│   ├── postControllers.js
│   ├── commentControllers.js
│   └── userController.js
│
├── middlewares/         # Custom middleware
│   ├── auth.js          # Authentication middleware
│   └── errorHandler.js  # Error handling middleware
│
├── models/              # Database models
│   ├── User.js
│   ├── Post.js
│   ├── Comment.js
│   └── File.js
│
├── routes/              # Application routes
│   ├── authRoutes.js
│   ├── postRoutes.js
│   ├── commentRoutes.js
│   └── userRoutes.js
│
├── views/               # EJS templates
│   ├── partials/        # Reusable components
│   ├── home.ejs
│   ├── login.ejs
│   ├── register.ejs
│   ├── profile.ejs
│   ├── posts.ejs
│   ├── postDetails.ejs
│   ├── newPost.ejs
│   ├── editPost.ejs
│   └── editProfile.ejs
│
├── app.js               # Application entry point
├── package.json         # Dependencies and scripts
└── .gitignore          # Git ignore file
```

## 🔑 Key Functionalities

### Authentication Flow
- User registration with email validation
- Secure login with Passport.js local strategy
- Session persistence with MongoDB
- Logout functionality

### Post Management
- Create new posts with title, content, and images
- View all posts with author information
- Edit own posts
- Delete own posts
- View individual post details

### User Interaction
- Comment on posts
- Edit and delete own comments
- View user profiles
- Update profile information

## 🌐 API Routes

### Authentication Routes (`/auth`)
- `GET /auth/login` - Login page
- `POST /auth/login` - Login user
- `GET /auth/register` - Registration page
- `POST /auth/register` - Register new user
- `GET /auth/logout` - Logout user

### Post Routes (`/posts`)
- `GET /posts` - View all posts
- `GET /posts/add` - New post form (protected)
- `POST /posts` - Create post (protected)
- `GET /posts/:id` - View post details
- `GET /posts/:id/edit` - Edit post form (protected)
- `PUT /posts/:id` - Update post (protected)
- `DELETE /posts/:id` - Delete post (protected)

### User Routes (`/user`)
- `GET /user/profile` - User profile (protected)
- `GET /user/profile/edit` - Edit profile form (protected)
- `PUT /user/profile` - Update profile (protected)

### Comment Routes
- `POST /posts/:id/comments` - Add comment (protected)
- `PUT /comments/:id` - Update comment (protected)
- `DELETE /comments/:id` - Delete comment (protected)

## 🔒 Security Features

- Password hashing with bcryptjs
- Protected routes with authentication middleware
- Session-based authentication
- Secure cookie handling
- Environment variable protection for sensitive data

## 🎨 UI Features

- Responsive design with Bootstrap
- Modern, clean interface
- User-friendly navigation
- Dynamic content rendering
- Error handling and validation messages

## 📝 Environment Variables

| Variable | Description |
|----------|-------------|
| `PORT` | Server port (default: 3000) |
| `MONGODB_URL` | MongoDB connection string |
| `CLOUDINARY_CLOUD_NAME` | Cloudinary cloud name |
| `CLOUDINARY_API_KEY` | Cloudinary API key |
| `CLOUDINARY_API_SECRET` | Cloudinary API secret |

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## 👨‍💻 Author

**Manoj**
- GitHub: [@Manoj-3428](https://github.com/Manoj-3428)

## 📄 License

This project is open source and available under the [ISC License](LICENSE).

## 🙏 Acknowledgments

- Built as part of Full-Stack Web Development Bootcamp
- Thanks to all contributors and supporters

---

⭐ If you found this project helpful, please give it a star!

