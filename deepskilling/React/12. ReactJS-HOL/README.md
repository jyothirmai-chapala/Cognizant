# Ticket Booking App - React

## Overview

This project is created as part of a React hands-on lab experiment.  
The main objective of this experiment is to understand **Conditional Rendering in React applications**.

In this application, a user can view flight details as a guest. After logging in, the user can access the ticket booking page. The application dynamically changes the displayed content based on the user's login status.

---

## Objectives

Through this experiment, I learned:

- How conditional rendering works in React
- How to create and use element variables
- How to control component rendering
- How to implement login and logout functionality using React state
- How React updates the UI dynamically based on user actions

---

## Technologies Used

- React JS
- JavaScript (ES6)
- HTML
- CSS
- Node.js
- NPM
- Visual Studio Code

---

## Application Features

### 1. Guest User Page

- Guest users can browse available flight details.
- Flight information such as flight name, source, destination, and price is displayed.
- Guest users cannot book tickets until they login.

### 2. Logged In User Page

- Logged-in users can access the ticket booking page.
- Users can enter passenger details.
- Users can select flights and book tickets.

### 3. Login and Logout Functionality

- The Login button changes the guest page into the user booking page.
- The Logout button returns the user back to the guest page.
- The displayed components change dynamically using conditional rendering.

---

## Concepts Learned

## 1. Conditional Rendering in React

Conditional rendering allows React applications to display different components based on conditions.

In this project, the login status decides which page should be displayed.

Example:

```javascript
if(isLoggedIn)
{
    page = <UserPage />;
}
else
{
    page = <GuestPage />;
}
