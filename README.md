# BusBazaar - Web-Based Bus Ticket Reservation System

## Introduction

Digital transformation of public transport has become a critical step in enhancing passenger convenience and operational efficiency. This report outlines the development of a web-based bus ticket reservation system, **BusBazaar**, designed to streamline the ticket booking process for passengers and simplify bus operators’ tasks. 

The platform bridges the gap between passengers and operators by providing real-time access to bus schedules, seat availability, and a secure ticket purchasing process. By addressing common problems such as long waiting times, lack of preferred seating, and manual verification methods, this system ensures a hassle-free travel experience for passengers and better resource management for bus operators.

## Objectives

### 1. Develop a digital platform for seamless bus ticket reservations and payments.
- Provide a user-friendly web interface for easy booking and payment.

### 2. Offer a user-friendly interface for passengers to:
- Book preferred seats dynamically.
- Receive e-tickets via email.
- Access real-time journey and seat availability information.

### 3. Enable bus operators (admins) to:
- Add and manage buses, view checkers and buses, schedules, and seating arrangements in the system.
- Monitor and update booking statuses in real-time.
- Freeze or release bus schedules as required for maintenance or operational adjustments.

### 4. Allow checkers (assigned by companies) to:
- Verify passenger identities by scanning QR codes from e-tickets.
- Access real-time updates on seat occupancy to manage bus entries effectively.

### 5. Ensure secure and reliable financial transactions.

### 6. Reduce passenger waiting time and improve overall public transport accessibility.

## Features

- **Dynamic Seat Booking**: Passengers can select seats based on availability in real time.
- **E-Tickets**: Secure ticket generation and delivery via email to passengers.
- **Real-Time Seat Availability**: Access up-to-date information on available and booked seats.
- **Admin Controls**: Admins can manage buses, routes, schedules, and bookings.
- **Checker Verification**: QR code scanning feature for checkers to verify e-tickets.
- **Payment Gateway**: Secure and reliable integration for online payments.

## Technologies Used

- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Payment Gateway**: Stripe
# BusBazaar Frontend

A modern, responsive React-based frontend for the BusBazaar bus booking system.

## Features

- **Home Page** - Welcome page with feature overview
- **Bus Search** - Search buses by route and date
- **Booking System** - Select seats and complete bookings
- **User Authentication** - Admin and Checker login
- **Admin Dashboard** - Manage buses (add, edit, delete)
- **Checker Dashboard** - Verify bookings and update status
- **Responsive Design** - Works on desktop, tablet, and mobile
- **Modern UI** - Clean and intuitive interface

## Project Structure

```
src/
├── components/
│   └── Navbar.js
├── pages/
│   ├── Home.js
│   ├── BusSearch.js
│   ├── Booking.js
│   ├── AdminLogin.js
│   ├── AdminDashboard.js
│   ├── CheckerLogin.js
│   └── CheckerDashboard.js
├── services/
│   └── api.js
├── styles/
│   ├── index.css
│   ├── App.css
│   ├── Navbar.css
│   ├── Home.css
│   ├── Auth.css
│   ├── BusSearch.css
│   ├── Booking.css
│   └── Dashboard.css
├── App.js
└── index.js
```

## Installation

1. **Navigate to frontend folder:**
```bash
cd BusBazaar-Frontend
```

2. **Install dependencies:**
```bash
npm install
```

3. **Create .env file:**
```
REACT_APP_API_URL=http://localhost:3200
```

4. **Start the development server:**
```bash
npm start
```

The app will open at `http://localhost:3000`

## API Integration

The frontend connects to the backend API at:
- **Base URL**: `http://localhost:3200` (configurable in `.env`)

### Available Endpoints:

- `POST /auth/admin` - Admin login
- `POST /auth/checker` - Checker login
- `GET /bus` - Get all buses
- `GET /search` - Search buses by route and date
- `POST /booking` - Create booking
- `GET /booking` - Get all bookings
- `PUT /booking/:id` - Update booking status
- `GET /api/getAllCities` - Get all cities
- `GET /api/getAllBusCompanies` - Get all companies

## Components Overview

### Navbar
Navigation bar with links to all pages and login/logout functionality.

### Home Page
Landing page with features overview and CTA button to search buses.

### BusSearch Page
- Search buses by origin, destination, and date
- Display available buses with details
- Direct booking from search results

### Booking Page
- Select seats from available options
- Enter passenger details (email, phone)
- Proceed to payment

### Admin Dashboard
- View all buses
- Add new buses
- Edit bus details
- Delete buses

### Checker Dashboard
- View all bookings
- Filter by status
- Mark bookings as checked
- Print/verify tickets

## Styling

The application uses custom CSS with:
- **Color Scheme**: Purple gradient (#667eea to #764ba2)
- **Responsive Grid Layout** - Mobile first approach
- **Smooth Transitions** - Better UX

## Authentication

- Routes are protected using React Router v6
- Tokens stored in localStorage
- Different dashboards for Admin and Checker roles

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## How to Use

1. **Search Buses**: Go to "Search Buses" and use filters
2. **Book Seat**: Click "Book Now" on any bus
3. **Admin Access**: Log in as Admin to manage buses
4. **Checker Access**: Log in as Checker to verify bookings

## Environment Variables

```
REACT_APP_API_URL=http://localhost:3200    # Backend API URL
```

## Build for Production

```bash
npm run build
```

Creates an optimized production build in the `build/` folder.

## Future Enhancements

- Payment integration (Stripe)
- Email notifications
- SMS alerts
- QR code generation for tickets
- Advanced filtering options
- User profile management
- Booking history
- Rating and reviews
- Multi-language support

## License

This project is part of the BusBazaar system.

## Support

For issues or questions, please contact the development team.

