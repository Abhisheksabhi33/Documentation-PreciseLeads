# Express.js Application Documentation

This is a Node.js application built using Express.js. It serves as an API that interacts with an Airtable database, fetching data from various sources, performing analyses, and updating the database records.

## Dependencies Used

- `dotenv`: For loading environment variables from a `.env` file.
- `express`: For handling HTTP requests.
- `axios`: For making HTTP requests.
- `Airtable`: For interacting with the Airtable database.

## Endpoints

### `GET /crunchbase`

- **Purpose**: Fetches data using `crunchbasefetcher`.
- **Functionality**:
  - Retrieves records from the Airtable database.
  - Invokes `crunchbasefetcher` for each record.
  - If no records are found, it waits for 5 minutes before attempting again.
  - Updates the database with the fetched data or error logs.

### `GET /apollo`

- **Purpose**: Retrieves data using `apollofetcher`.
- **Functionality**:
  - Retrieves records from the Airtable database.
  - Invokes `apollofetcher` for each record.

### `GET /Relevance`

- **Purpose**: Updates data relevance using various scripts.
- **Functionality**:
  - Retrieves records from the Airtable database.
  - Invokes `blogScript` and `checkDEIOnCompanyPage` for each record.

### `GET /GptAnalyser`

- **Purpose**: Analyzes data using `gpt_analyser`.
- **Functionality**:
  - Retrieves records from the Airtable database.
  - Invokes `gpt_analyser` for each record.

### `GET /blogDetailProvider`

- **Purpose**: Fetches blog details using `blogDetailProvider`.
- **Functionality**:
  - Retrieves records from the Airtable database.
  - Invokes `blogDetailProvider` for each record.

### `GET /Pricing`

- **Purpose**: Updates pricing data.
- **Functionality**:
  - Retrieves records from the Airtable database.
  - Invokes `Pricing` for each record.

### `/`

### `gpt_analyser` Function Details

- **Function Purpose**: Analyzes website content and updates the database with relevant information.
- **Input Parameters**:
  - `record`: Represents a record fetched from the Airtable database.
  - `table`: Represents the Airtable instance/table.
- **Steps**:
  1. Checks the presence of a checkbox and the status of the analyser.
  2. Retrieves website URL and existing relevance data from the record.
  3. Constructs a request body for scraping website content.
  4. Utilizes `fetch` to send a POST request to a URL specified in the environment variables.
  5. Divides the scraped text into chunks and sends them to the GPT-3.5 model for analysis.
  6. Interprets model responses to identify the presence of specific content on the website.
  7. Updates the Airtable record with the relevant content found on the website.


# `crunchbasefetcher` Function Documentation

## Description
The `crunchbasefetcher` function interacts with the Crunchbase API to retrieve and update company data based on the provided record and table.

# `apollofetcher` Function Documentation

## Description
The `apollofetcher` function interacts with the Apollo API to retrieve and update company data based on the provided record and table.


# `blogDetailProvider` Function Documentation

The `blogDetailProvider` function interacts with external websites and retrieves blog details for a given record and table, updating the Airtable database with the extracted information.

## Function Overview

### Purpose
The function is designed to fetch blog details from a specified URL and enrich the database record with extracted data.


# `blogScript` Function Documentation

The `blogScript` function performs various checks and fetches relevant URLs based on the company details provided in the record. It updates the Airtable database with the fetched URLs and relevant tags.

## Function Overview

### Purpose
The function checks and collects URLs associated with different aspects of the provided company and updates the database record with the gathered information.


# `checkDEIOnCompanyPage` Function Documentation

The `checkDEIOnCompanyPage` function is designed to verify the presence of Diversity, Equity, and Inclusion (DEI) keywords on a company's careers website and update the Airtable database with the relevant information.

## Function Overview

### Purpose
This function checks if a company's careers website contains DEI-related keywords and updates the database accordingly.





- **Purpose**: Root endpoint.
- **Functionality**: Returns a JSON response indicating that the application is running.

## Operational Notes

- The application listens on port `3000`.
- Various routes retrieve records from the Airtable database's "Grid view".
- Error handling is implemented to catch and log errors during data fetching and processing.
- Asynchronous operations are handled using `async/await` and `Promise.all`.

## Usage

1. Ensure the `.env` file contains the required environment variables.
2. Start the application using `npm start` or another appropriate method.

## Getting Started

To run the application:

1. Clone the repository.
2. Install dependencies using `npm install`.
3. Set up the `.env` file with the required variables.
4. Start the application using `npm start`.

## Conclusion

This Express.js application serves as a data-fetching API interacting with an Airtable database, performing various data-related operations and updates.
