# Roxiler Backend

Welcome to the Roxiler Backend project! This backend system is created to efficiently manage and analyze product transactions. It seamlessly integrates with a third-party API to fetch product transaction data and offers a variety of APIs for handling transactions, generating statistics, and creating insightful charts based on the acquired data

## API Endpoints

### List All Transactions

- **Endpoint:** `/transactions`
- **Method:** `GET`
- **Description:** Retrieves a comprehensive list of transactions based on provided search criteria and pagination.
  - **Query Parameters:**
    - `month` (required): The month for filtering transactions.
    - `search` (optional): Search text to match against product titles, descriptions, or prices.
    - `page` (optional): Page number for pagination (default: 1).
    - `perPage` (optional): Number of records per page (default: 10).

### Statistics

- **Endpoint:** `/statistics`
- **Method:** `GET`
- **Description:** Provides statistical insights for the selected month.
  - **Query Parameters:**
    - `month` (required): The month for which statistics are requested.

### Bar Chart

- **Endpoint:** `/bar-chart`
- **Method:** `GET`
- **Description:** Generates data for a bar chart illustrating price ranges and the corresponding number of items within each range for the chosen month.
  - **Query Parameters:**
    - `month` (required): The month for which the bar chart is generated.

### Pie Chart

- **Endpoint:** `/pie-chart`
- **Method:** `GET`
- **Description:** Creates data for a pie chart showcasing unique categories and the quantity of items from each category for the specified month.
  - **Query Parameters:**
    - `month` (required): The month for which the pie chart is created.

### Combined Data

- **Endpoint:** `/combined-data`
- **Method:** `GET`
- **Description:** Retrieves data from all the above APIs and consolidates the responses into a unified dataset.

## How to Use

To interact with the APIs, simply make HTTP requests to the designated endpoints with the necessary parameters. Ensure that the `month` parameter is included in all relevant requests.




## Deployment
Clone the repository
install node and check version using node -v
Type the following commands in terminal

npm install express cors sqlite3 

node index.js

Now the backsend project is running then go for front end project

## Access Your APIs:

Once the server is running, you can access your APIs using the appropriate endpoints. For example:

Transactions API: http://localhost:3000/transactions
Statistics API: http://localhost:3000/statistics
Bar Chart API: http://localhost:3000/bar-chart
Pie Chart API: http://localhost:3000/pie-chart
