# Taxi Cab App - Ride Sharing Platform

A full-stack taxi cab/ride-sharing application connecting passengers with drivers in real-time.

## 🚀 Features

### Customer App
- Browse available drivers
- Request rides in real-time
- Track driver location in real-time
- Make payments
- Rate drivers and leave feedback
- View ride history

### Driver App
- Accept/reject ride requests
- Navigate to pickup location
- Complete rides
- Earn ratings and reviews
- View earnings dashboard
- Manage availability status

### Backend/API
- User management (customers & drivers)
- Ride matching algorithm
- Real-time location tracking via WebSockets
- Payment processing
- Rating and review system
- Admin controls

### Admin Dashboard
- Analytics and insights
- User management
- Support and dispute resolution
- Revenue tracking
- Driver and customer statistics

## 🛠️ Tech Stack

- **Frontend**: React.js
- **Backend**: Node.js + Express
- **Database**: PostgreSQL
- **Real-time Communication**: WebSockets
- **Authentication**: JWT
- **Payment Gateway**: (To be integrated)
- **Maps**: Google Maps API or similar

## 📁 Project Structure

```
maak/
├── backend/              # Node.js backend
│   ├── src/
│   │   ├── config/       # Database and app config
│   │   ├── controllers/  # Route controllers
│   │   ├── models/       # Database models
│   │   ├── routes/       # API routes
│   │   ├── middleware/   # Custom middleware
│   │   ├── services/     # Business logic
│   │   └── app.js        # Express app
│   ├── .env.example      # Environment variables template
│   ├── package.json      # Dependencies
│   └── server.js         # Server entry point
│
├── frontend/             # React frontend
│   ├── public/           # Static files
│   ├── src/
│   │   ├── components/   # React components
│   │   ├── pages/        # Page components
│   │   ├── services/     # API and WebSocket services
│   │   ├── hooks/        # Custom React hooks
│   │   ├── context/      # React Context
│   │   ├── styles/       # CSS/styling
│   │   └── App.js        # Main App component
│   ├── .env.example      # Environment variables
│   ├── package.json      # Dependencies
│   └── index.js          # React entry point
│
├── docs/                 # Documentation
├── .gitignore
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v14+)
- npm or yarn
- PostgreSQL (v12+)

### Backend Setup

1. Navigate to backend directory:
```bash
cd backend
```

2. Install dependencies:
```bash
npm install
```

3. Create `.env` file from `.env.example`:
```bash
cp .env.example .env
```

4. Configure your database and other variables in `.env`

5. Run database migrations:
```bash
npm run migrate
```

6. Start the backend server:
```bash
npm run dev
```

### Frontend Setup

1. Navigate to frontend directory:
```bash
cd frontend
```

2. Install dependencies:
```bash
npm install
```

3. Create `.env` file from `.env.example`:
```bash
cp .env.example .env
```

4. Configure API endpoint in `.env`:
```
REACT_APP_API_URL=http://localhost:5000
```

5. Start the development server:
```bash
npm start
```

## 📚 API Documentation

See [API.md](./docs/API.md) for detailed API endpoints documentation.

## 🗄️ Database Schema

See [DATABASE.md](./docs/DATABASE.md) for database structure and relationships.

## 🤝 Contributing

1. Create a feature branch: `git checkout -b feature/your-feature`
2. Commit changes: `git commit -am 'Add your feature'`
3. Push to branch: `git push origin feature/your-feature`
4. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see LICENSE file for details.

## 📧 Contact

For questions or support, please reach out to the development team.