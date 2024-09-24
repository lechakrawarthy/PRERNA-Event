---

# PRERANA Event Website

## Overview
The **PRERANA Event Website** is developed for GITAM University to streamline the registration and ticketing process for the PRERANA event. This web application includes features for user authentication (via Google SSO for GITAM users and manual registration for external users), a payment gateway (Razorpay), personalized ticket generation with QR codes, and an admin dashboard for ticket verification.

## Table of Contents
1. [Features](#features)
2. [Tech Stack](#tech-stack)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Contributing](#contributing)
6. [License](#license)

## Features
- **User Authentication**:
  - Google SSO for GITAM students using `@gitam.in` email.
  - Manual registration for external users.
  - Role-based access (Admin, User).
  
- **Homepage**:
  - Event details including schedule, speakers, and registration options.
  - Countdown timer to the event.

- **Ticket Generation**:
  - Personalized tickets with user details (name, photo).
  - QR code on the ticket for event entry and verification.
  - PDF format download option for tickets.

- **Payment Integration**:
  - Razorpay payment gateway.
  - Secure payment methods: UPI, net banking, cards.
  - Automated ticket generation upon payment confirmation.

- **QR Code Verification**:
  - Admins can scan QR codes to verify attendees.
  - Display of user’s name, email, and payment status.

- **User Profile Management**:
  - Ability for users to update personal information.
  - Access to purchased tickets and transaction history.

- **Admin Dashboard**:
  - Manage event attendees, view ticket sales, and analytics.
  - QR code scanning for verification at the event.

## Tech Stack
- **Frontend**: 
  - HTML5, CSS3, Tailwind CSS
  - JavaScript (React.js)
  
- **Backend**:
  - Flask (Python)
  - Flask-Login for authentication
  - Google OAuth 2.0 for SSO
  - Razorpay API for payments
  
- **Database**:
  - MongoDB/MySQL/PostgreSQL (choose based on your preference)

## Installation

### Prerequisites:
- Python 3.x
- Node.js and npm
- MongoDB/MySQL/PostgreSQL
- Razorpay account for payment integration
- Google Cloud Project with OAuth 2.0 credentials

### Setup:

1. **Clone the Repository**:
   ```bash
   git clone git@github.com:yourusername/prerana-event-website.git
   cd prerana-event-website
   ```

2. **Backend Setup**:
   - Create a virtual environment:
     ```bash
     python3 -m venv venv
     source venv/bin/activate  # Linux/Mac
     venv\Scripts\activate  # Windows
     ```
   - Install the required Python packages:
     ```bash
     pip install -r requirements.txt
     ```

3. **Frontend Setup**:
   - Navigate to the frontend directory:
     ```bash
     cd frontend
     ```
   - Install dependencies:
     ```bash
     npm install
     ```

4. **Database Configuration**:
   - Update the `config.py` file with your database connection settings.

5. **Set Up Google OAuth and Razorpay**:
   - Add your Google OAuth credentials in the `config.py` file.
   - Add Razorpay API keys for payment processing in `config.py`.

6. **Run the Application**:
   - Run the backend:
     ```bash
     python app.py
     ```
   - Run the frontend:
     ```bash
     npm start
     ```

7. **Access the website** at `http://localhost:3000`.

## Usage
1. Users can register using their GITAM Google account or manually.
2. After registration, users can purchase tickets through the Razorpay gateway.
3. Once payment is confirmed, users will receive a downloadable ticket with a QR code.
4. Admins will have access to the dashboard to scan and verify tickets.

## Contributing
To contribute:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-branch
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add some feature"
   ```
4. Push to the branch:
   ```bash
   git push origin feature-branch
   ```
5. Open a Pull Request.

## License
Distributed under the MIT License. See `LICENSE` for more information.

---
