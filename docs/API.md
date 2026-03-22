# API Documentation

## Base URL
```
http://localhost:5000/api
```

## Authentication
All protected endpoints require a JWT token in the Authorization header:
```
Authorization: Bearer <token>
```

## Endpoints

### Authentication
- `POST /auth/register` - Register a new user
- `POST /auth/login` - Login user
- `POST /auth/logout` - Logout user
- `POST /auth/refresh-token` - Refresh JWT token

### Users
- `GET /users/:id` - Get user profile
- `PUT /users/:id` - Update user profile
- `DELETE /users/:id` - Delete user account

### Customers
- `GET /customers/:id` - Get customer details
- `POST /customers/:id/rides` - Request a ride
- `GET /customers/:id/rides` - Get ride history
- `GET /customers/:id/ratings` - Get customer ratings

### Drivers
- `GET /drivers/:id` - Get driver details
- `PUT /drivers/:id/status` - Update driver availability
- `GET /drivers/:id/rides` - Get driver ride history
- `GET /drivers/:id/earnings` - Get driver earnings
- `GET /drivers/nearby` - Find nearby drivers

### Rides
- `GET /rides/:id` - Get ride details
- `POST /rides/:id/accept` - Driver accepts ride
- `POST /rides/:id/reject` - Driver rejects ride
- `POST /rides/:id/complete` - Complete ride
- `POST /rides/:id/cancel` - Cancel ride

### Ratings
- `POST /ratings` - Submit a rating
- `GET /ratings/:id` - Get ratings for user

### Payments
- `POST /payments` - Process payment
- `GET /payments/:id` - Get payment details
- `GET /payments/history/:user_id` - Get payment history