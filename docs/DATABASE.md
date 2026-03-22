# Database Schema Documentation for Taxi Cab Application

## Tables

### Users
- **user_id** (Primary Key): Unique identifier for each user.
- **username**: The username chosen by the user.
- **password_hash**: The hashed password for user authentication.
- **email**: User's email address.
- **created_at**: Timestamp of when the user account was created.
- **updated_at**: Timestamp of the last update on user account.

### Customers
- **customer_id** (Primary Key): Unique identifier for each customer.
- **user_id** (Foreign Key): References the user who is the customer.
- **phone_number**: Contact number of the customer.
- **address**: Address of the customer.
- **created_at**: Timestamp of when the customer was added.
- **updated_at**: Timestamp of the last update on customer details.

### Drivers
- **driver_id** (Primary Key): Unique identifier for each driver.
- **user_id** (Foreign Key): References the user who is the driver.
- **license_number**: The driver's license number.
- **vehicle_details**: Details of the vehicle associated with the driver.
- **rating**: Current rating of the driver.
- **created_at**: Timestamp of when the driver was added.
- **updated_at**: Timestamp of the last update on driver details.

### Rides
- **ride_id** (Primary Key): Unique identifier for each ride.
- **customer_id** (Foreign Key): References the customer who requested the ride.
- **driver_id** (Foreign Key): References the driver assigned to the ride.
- **pickup_location**: Location where the customer will be picked up.
- **dropoff_location**: Location where the customer will be dropped off.
- **ride_status**: Status of the ride (e.g., completed, ongoing, canceled).
- **created_at**: Timestamp of when the ride was requested.
- **updated_at**: Timestamp of the last update on ride details.

### Ratings
- **rating_id** (Primary Key): Unique identifier for each rating.
- **ride_id** (Foreign Key): References the ride that is being rated.
- **customer_id** (Foreign Key): References the customer who provided the rating.
- **driver_id** (Foreign Key): References the driver who is being rated.
- **score**: Rating score given by the customer (e.g., 1 to 5).
- **comments**: Feedback comments provided by the customer.
- **created_at**: Timestamp of when the rating was given.

### Payments
- **payment_id** (Primary Key): Unique identifier for each payment.
- **ride_id** (Foreign Key): References the ride associated with this payment.
- **amount**: The amount paid for the ride.
- **payment_method**: Method used for the payment (e.g., credit card, cash).
- **payment_status**: Status of the payment (e.g., completed, pending).
- **created_at**: Timestamp of when the payment was made.