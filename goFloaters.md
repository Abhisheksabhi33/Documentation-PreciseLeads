**Documentation: Data Retrieval Workflow**

This documentation outlines the step-by-step process to retrieve required data using the specified scripts in the given order. The process involves accessing the Automatic-goFloaters Base and executing several scripts to gather job, company, and people data. Follow these instructions carefully to successfully obtain the required data.

### Step 1: Access Automatic-goFloaters Base

Ensure you have the necessary permissions and access to the Automatic-goFloaters Base. If not, contact your system administrator to grant the required access.

### Step 2: Run Get - Jobs Script

1. Locate the "Get - Jobs" script in the Automatic-goFloaters Base.
2. Execute the script and wait for it to finish processing.
3. Verify that the job data has been successfully retrieved before proceeding to the next step.

### Step 3: Run Get - Company Details Script

1. After the "Get - Jobs" script has completed, locate the "Get - Company Details" script.
2. Execute the script to gather detailed information about the companies associated with the retrieved jobs.
3. Confirm that the company details data has been successfully obtained before moving on to the next step.

### Step 4: Run Company Enrichment by Apollo

1. Once the company details are available, run the "Company Enrichment by Apollo" script.
2. This script likely enhances the company data by incorporating additional information from the Apollo platform.
3. Wait for the script to complete, and verify that the company data has been enriched as expected.

### Step 5: Run Get-People Data

1. With the enriched company data, locate the "Get-People Data" script.
2. Execute the script to retrieve information about the individuals associated with the companies and jobs.
3. Confirm that the people data has been successfully gathered.

### Step 6: Utilize the Acquired Data

1. Once all the scripts have been executed successfully, you should now have comprehensive data, including job details, company information, and individual profiles.
2. Utilize the acquired data as needed for your specific use case or analysis.

Absolutely, regular data refreshes can significantly enhance the volume and quality of acquired information. Here's an addition to the documentation:

### Step 7: Scheduled Data Refresh (Optional)

For maximizing data acquisition:

1. Consider repeating **Step 4 (Company Enrichment by Apollo)** and **Step 5 (Get-People Data)** multiple times within a day, ideally 2-3 times.
2. Scheduling these processes at intervals throughout the day can capture updated, real-time information.
   
   - Set up automated schedules or manual checks to run these scripts periodically.
   - This ensures the data remains current and includes the latest updates or new entries within the given timeframe.

**Note:** The frequency of data refreshes should be determined based on the relevance and urgency of acquiring real-time information. Additionally, consider system load and API usage limits to avoid overloading resources or violating usage policies.

Continuously updating the data fetch process allows for a more comprehensive and up-to-date dataset for analysis or application usage.

**Note:** Ensure that you adhere to data protection and privacy regulations when handling and utilizing the obtained information.

**Disclaimer:** The accuracy and completeness of the data depend on the sources and APIs used in the scripts. Periodic checks and updates may be necessary to maintain the quality of the data over time.