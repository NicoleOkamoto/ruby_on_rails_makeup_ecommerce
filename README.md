# 💄 Makeup Product API Integration

This project retrieves and processes data from the [Makeup API](http://makeup-api.herokuapp.com/api/v1/products.json). It extracts product details, including brands, product categories, prices, and descriptions, and stores them in a structured database for future use.

## 📖 Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Setup and Installation](#setup-and-installation)
  - [Prerequisites](#prerequisites)
  - [Installation Steps](#installation-steps)
- [Fetching and Seeding Data](#fetching-and-seeding-data)
- [Database Structure](#database-structure)
- [Running the Project](#running-the-project)
- [Contributing](#contributing)
- [License](#license)

---

## 📝 Project Overview

This application fetches data from an external open API, the **Makeup Product API**, and processes it into a local database. The goal of this project is to provide an organized collection of makeup products with details such as product name, brand, price, and description.

### ✨ Key Features:
- **Data retrieval**: Fetches product data from the Makeup API.
- **Data storage**: Stores product details, categories, and brands in a structured database.
- **Product filtering**: Organize products by brand and category.
- **Admin Panel**: Manage products, categories, and brands via an admin interface.

---

## 🔧 Technologies Used
- **Python**: Core language for data processing.
- **OpenURI**: To fetch data from the API.
- **JSON**: To parse API responses.
- **PostgreSQL**: Database to store products, categories, and brands.
- **Ruby on Rails**: Backend framework for handling CRUD operations.
- **ActiveAdmin**: To manage data with a user-friendly admin interface.

---

## ⚙️ Setup and Installation

### Prerequisites
Make sure the following are installed on your system:
- **Python 3.x**
- **PostgreSQL**
- **Ruby on Rails**
- **Bundler** (for managing Ruby gems)

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/makeup-product-api.git
   cd makeup-product-api
   ```

2. **Install dependencies:**
   ```bash
   bundle install
   ```

3. **Database setup:**
   Ensure PostgreSQL is running and create the database:
   ```bash
   rails db:create
   rails db:migrate
   ```

4. **Environment configuration:**
   Set up environment variables if necessary (e.g., for database connections).

5. **Run the server:**
   ```bash
   rails server
   ```

---

## 🌐 Fetching and Seeding Data

To retrieve and seed data from the Makeup API:

1. **Run the seed file:**
   The seed script fetches makeup product data from the API and stores it in the database.
   ```bash
   rails db:seed
   ```

2. **Output:**
   After seeding, you will see output like:
   ```
   Seed data imported successfully.
   Total Makeup Products: [Number]
   Total Product Categories: [Number]
   Total Brands: [Number]
   Unique Product Types: [List]
   ```

---

## 🗃️ Database Structure

This project uses three primary models: `MakeupProduct`, `ProductCategory`, and `Brand`.

### Models:

- **MakeupProduct**: Stores details about each product, including name, price, description, and associated brand and category.
- **ProductCategory**: Organizes products by type and category.
- **Brand**: Stores unique brands associated with the makeup products.

### Relationships:

- `MakeupProduct` belongs to both `Brand` and `ProductCategory`.
- `Brand` has many `MakeupProducts`.
- `ProductCategory` has many `MakeupProducts`.

---

## 🚀 Running the Project

1. **Start the Rails server:**
   ```bash
   rails server
   ```

2. **Access the app**:
   Open your browser and visit `http://localhost:3000` to interact with the application.

3. **Admin Panel:**
   Access the admin panel (in development mode) at `http://localhost:3000/admin`:
   ```
   Email: admin@example.com
   Password: password
   ```

---

## 🤝 Contributing

If you'd like to contribute to this project:

1. Fork the repository.
2. Create a new branch for your feature/bugfix.
3. Commit and push your changes to the branch.
4. Open a pull request describing your changes.

---
