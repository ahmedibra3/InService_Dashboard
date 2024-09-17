# Home Services Management Dashboard

This is a web-based application designed for managing home services. The admin dashboard enables administrators to efficiently add, edit, and delete services or service providers. The platform is secured by providing admins with a unique private link and credentials to access the dashboard. Additionally, the platform allows service providers to register and join the team.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation and Setup](#installation-and-setup)
  - [Install Dependencies](#1-install-dependencies)
  - [Set Environment Variables](#2-set-environment-variables)
  - [Generate Application Key](#3-generate-application-key)
  - [Run Database Migrations](#4-run-database-migrations)
  - [Build Frontend Assets](#5-build-frontend-assets)
  - [Serve the Application](#6-serve-the-application)
- [Usage](#usage)
- [Security](#security)
- [Contributing](#contributing)
- [License](#license)

---

## Features

1. **Admin Dashboard**: A secured platform that allows system admins to manage:
   - **Home Services**: Add, edit, and delete services.
   - **Service Providers**: Manage service providers including adding, updating, and removing them.
  
2. **Admin Access**:
   - Access is restricted through a private link provided by the organization.
   - Admins receive a username and password for logging into the dashboard.

3. **Home Page**: 
   - Displays information about the services provided by the platform.
   - Includes a public-facing introduction to the platform’s benefits and features.

4. **Service Provider Registration**: 
   - A form where service providers can apply to join the platform.
   - Prospective service providers can submit their details to become part of the team.

---

## Technologies Used

- **Frontend**:
  - HTML
  - CSS
  - JavaScript
  - Tailwind CSS

- **Backend**:
  - Laravel (PHP Framework)

---

## Installation and Setup

Follow the steps below to set up the project on your local machine.

**1. Install Dependencies**

Ensure you have [Composer](https://getcomposer.org/) and [Node.js](https://nodejs.org/) installed on your machine.

- Clone the repository:

  ```bash
  git clone https://github.com/yourusername/homeservices-dashboard.git
  cd homeservices-dashboard
- Install PHP dependencies using Composer:
  composer install

**2. Set Environment Variables**
  - Copy the .env.example file to .env:
    cp .env.example .env
  - Edit the .env file and configure your database credentials and other environment-specific settings.
  
**3. Generate Application Key**
    - Generate the application encryption key:
      php artisan key:generate

**4. Run Database Migrations**
    - Run the migrations to create the necessary database tables:
      php artisan migrate
      
**5. Build Frontend Assets**
    - Compile the frontend assets using Laravel Mix:
      npm run dev
      
**6. Serve the Application**
    - Serve the Laravel application:
      php artisan serve
    - Your application will now be available at http://localhost:8000.

---

## Usage
- **Admin Dashboard**:
    - The admin dashboard is only accessible through a unique URL shared with the admin by the organization.
    - Admins can use their provided username and password to log in and manage home services and service providers.
- **Service Provider Registration**:
    - Service providers who wish to join the platform can fill out the registration form available on the public website.
    - Once approved, they will be added to the list of providers on the platform.

  ---

## Security
- Admin access is restricted to those with the private URL and credentials provided by the organization. Ensure that these details are kept confidential to prevent unauthorized access.
- Regularly rotate admin credentials and update the private URL if necessary for enhanced security.
- For additional security, ensure that sensitive data is stored and transmitted securely (e.g., using HTTPS).

---

## Contributing
We welcome contributions from the community to improve the platform! To contribute:

**1. Fork the repository.**
**2. Create a new branch:**
  git checkout -b feature/your-feature-name
**3. Commit your changes:**
    git commit -m "Describe your changes"
**4. Push to the branch:**
    git push origin feature/your-feature-name
**5. Create a pull request on GitHub and describe the proposed changes.**

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.
