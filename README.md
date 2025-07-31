# airline-management-backend
Airline Management System - Backend


-----

# Airline Management API

-----

## Overview

Welcome to the **Airline Management API**\! This project provides a robust and straightforward set of tools to **streamline the process of managing flights and passenger reservations**. 
### Current Capabilities:

The API currently offers core functionalities to get you started:

  * **List Available Flights:** Retrieve a comprehensive list of all flights currently available for booking.
  * **Add New Passenger:** Create new passenger profiles within the system, ready for reservations.
  * **Reserve Flights:** Effortlessly book flights for the registered passengers.
  * **View Reservation Information:** Access detailed information for any existing passenger reservation.
  * **Cancel Reservation:** Easily terminate and remove existing flight reservations.

-----

## Running the API Collection

To help you quickly explore and interact with the Airline Management API, we provide a Postman Collection. You can run this collection directly within the Postman desktop application for an interactive experience, or automate your tests using Newman, Postman's command-line collection runner.

### Option 1: Running via Postman Desktop App

The Postman desktop application offers a user-friendly interface to explore and execute API requests.

#### Prerequisites:

  * **Postman Desktop App:** Make sure you have the Postman desktop application installed. You can download it from [Postman's official website](https://www.postman.com/downloads/).

#### Steps to Run the Collection:

1.  **Import the Collection:**
      * Once you have the `Airline-Management.postman_collection.json` file, open your Postman desktop app.
      * Click the **"Import"** button in the top left corner.
      * Select **"Upload Files"** and choose your collection JSON file.
      * Click **"Import"**. The collection will appear in your "Collections" sidebar.
2.  **Select and Run:**
      * In the "Collections" sidebar, click on the **"Airline Management"** collection to expand it.
      * Click the **"Runner"** button (or hover over the collection in the sidebar and click "Run").
      * Drag the "Airline Management API" collection into the Collection Runner.
      * Select the environment file drom the environment dropdown.
      * Click the **"Run Airline Management"** button.
3.  **Review Results:** The Collection Runner will execute each request and display the results, including status codes, response times, and any Postman test outcomes.

### Option 2: Running via Newman (Command-Line Collection Runner)

Newman is a powerful command-line tool perfect for automating API tests and integrating them into CI/CD pipelines.

#### Prerequisites:

1.  **Node.js:** Newman runs on Node.js. Ensure you have Node.js (v16 or later is recommended) installed from [nodejs.org](https://nodejs.org/).
2.  **Newman:** Install Newman globally using npm:
    ```bash
    npm install -g newman
    ```
3.  **Exported Postman Collection & Environment:**
      * The "Airline Management" collection (`Airline-Management.postman_collection.json`) and the Postman Environment as (`local.postman_environment.json`) saved in the same directory.

#### Steps to Run the Collection with Newman:

1.  **Navigate to Directory:** Open your terminal or command prompt and change to the directory where you saved your collection and environment files:

    ```bash
    cd /path/to/your/api/files
    ```

2.  **Run the Collection:**

      * **Without an Environment:**
        ```bash
        newman run Airline-Management.postman_collection.json
        ```
      * **With an Environment (Recommended):**
        ```bash
        newman run Airline-Management.postman_collection.json -e local.postman_environment.json
        ```
      * **Useful Options:**
          * Generate an HTML report: `--reporters cli,html --reporter-html-export report.html` (you might need to `npm install -g newman-reporter-html` first).
          * Run multiple times: `-n <iterations>`
          * Add a delay: `--delay-request <milliseconds>`
          * Exit on test failure: `--bail`

3.  **Review Output:** Newman will display a summary in your terminal. If you generated an HTML report, open `report.html` in your browser for a detailed breakdown.

-----