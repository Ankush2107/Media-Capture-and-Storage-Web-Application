# Media Storage Application

A full-stack application for secure media storage and management, built with the MERN stack (MongoDB, Express.js, React, Node.js) and AWS S3 for file storage.

## Live Demo

- Frontend: [https://mediacaptureandstorage.netlify.app](https://mediacaptureandstorage.netlify.app)
- Backend API: [https://media-capture-and-storage-backend-1.onrender.com](https://media-capture-and-storage-backend-1.onrender.com)

## Features

- **User Authentication**
  - Secure registration and login
  - JWT-based authentication
  - Protected routes

- **Media Management**
  - Upload images and videos
  - View media in a responsive grid layout
  - Filter between images and videos
  - Full-screen media viewer
  - Delete media files
  - Preview before upload

- **Cloud Storage**
  - AWS S3 integration for reliable file storage
  - Secure file handling
  - Unique file naming

- **Responsive Design**
  - Mobile-friendly interface
  - Grid-based layout
  - Material-UI components

## Technology Stack

### Frontend
- React.js with Vite
- Redux Toolkit for state management
- Material-UI (MUI) for components
- React Router for navigation
- Axios for API calls
- Notistack for notifications
- Deployed on Netlify

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- AWS SDK for S3 integration
- Multer for file handling
- Deployed on Render

## Prerequisites

- Node.js (v14 or higher)
- MongoDB
- AWS Account with S3 bucket
- npm or yarn

## Environment Variables

### Frontend (.env)
```env
VITE_API_URL=https://media-capture-and-storage-backend-1.onrender.com/api
```

### Backend (.env)
```env
PORT=5000
MONGODB_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
AWS_ACCESS_KEY=your_aws_access_key
AWS_SECRET_KEY=your_aws_secret_key
AWS_REGION=your_aws_region
AWS_BUCKET_NAME=your_bucket_name
```

## Installation

1. Clone the repository
```bash
git clone <repository-url>
```

2. Install Backend Dependencies
```bash
cd server
npm install
```

3. Install Frontend Dependencies
```bash
cd client
npm install
```

## Running the Application

1. Start the Backend Server
```bash
cd server
npm start
```

2. Start the Frontend Development Server
```bash
cd client
npm run dev
```

The application will be available at `http://localhost:5173` for local development.

For production, visit:
- Frontend: https://mediacaptureandstorage.netlify.app
- Backend: https://media-capture-and-storage-backend-1.onrender.com

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login

### Media
- `POST /api/media/upload` - Upload media file
- `GET /api/media` - Get user's media files
- `DELETE /api/media/:id` - Delete media file

## Project Structure

```
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── pages/        # Page components
│   │   ├── redux/        # Redux state management
│   │   └── App.jsx       # Main application component
│
├── server/                # Backend Node.js application
│   ├── config/           # Configuration files
│   ├── controllers/      # Route controllers
│   ├── middleware/       # Custom middleware
│   ├── models/          # Mongoose models
│   ├── routes/          # API routes
│   └── app.js           # Express application setup
```

## Security Features

- Password hashing with bcrypt
- JWT token authentication
- Protected API routes
- Secure file upload handling
- AWS S3 secure storage
- Input validation
- Error handling

## Deployment

### Frontend Deployment (Netlify)
- Platform: Netlify
- Build command: `npm run build`
- Publish directory: `dist`
- Environment variables must be set in Netlify dashboard

### Backend Deployment (Render)
- Platform: Render
- Build command: `npm install`
- Start command: `node app.js`
- Environment variables must be set in Render dashboard

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.

## Acknowledgments

- Material-UI for the component library
- AWS S3 for file storage
- MongoDB Atlas for database hosting
- Netlify for frontend hosting
- Render for backend hosting