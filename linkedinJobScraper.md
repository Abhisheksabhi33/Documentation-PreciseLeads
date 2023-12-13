# LinkedIn Job Scraper HTML Documentation

This HTML file represents a form-based interface for scraping job data from LinkedIn. Below is an overview of the structure and elements used in the HTML:

### Structure:

- **Head Section:**
  - Contains meta tags and the title of the page.
  - Imports the Tailwind CSS stylesheet from a CDN for styling.

- **Body Section:**
  - Sets a gradient background color using Tailwind CSS classes.
  - Contains a header with the title "LinkedIn Job Scraper" in varying font sizes and styles.
  - Displays a status div (`status`) for showing scraping progress or error messages.

  - **Form Section:**
    - Provides inputs for job-related information such as keywords, company list, location, date posted, job mode, and total jobs required.
    - Uses various input types (text, textarea, select, number) styled with Tailwind CSS classes.
    - Includes a "Scrape Jobs" button (`submit-button`) to trigger the job scraping process.

  - **Footer Section:**
    - Currently commented out but includes a container with information about Precise Leads and the last update date.

### Usage:
- Modify the default values and options within the form inputs according to the requirements.
- Ensure the `script` tag at the bottom of the file points to the correct JavaScript file (`index.js`) for form submission functionality.
- Tailor the footer section or uncomment it to display additional information if necessary.


# LinkedIn Job Scraper JavaScript Documentation

This JavaScript file provides functionality to the HTML form for job scraping. Below is an overview of the functionalities and components within the JavaScript:

### Components:

- **Event Listener:**
  - Listens to the form submission event (`submit`) and prevents the default behavior.
  - Constructs a request body with form data and initiates a POST request to the specified API endpoint.

- **Functions:**
  - `convertToList(input)`: Converts multiline input to a comma-separated list of companies.

- **Workflow:**
  1. **Form Submission Handling:**
     - Constructs a request body by parsing form data.
     - Converts company list input to a comma-separated string using `convertToList()`.

  2. **Data Fetching:**
     - Sends a POST request to the designated API endpoint with the constructed request body.
     - Sets appropriate headers for JSON content.

  3. **Response Handling:**
     - Updates status messages based on the scraping process.
     - Displays success message with the number of scraped jobs or error message if encountered.

### Usage:
- Update the `APIurl` constant in the JavaScript file to target the correct API endpoint (local or hosted) before running the code.
- Ensure the server/API specified in `APIurl` is functional and capable of handling the requests/responses as expected.
- Modify or enhance the error handling and success message display according to specific requirements.
