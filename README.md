**Detailed Description**

In this project, I built a web scraper to automate the task of extracting customer information from Spokeo.com based on a list of phone numbers provided in Excel files. The main tools used were Python libraries such as Pandas for data manipulation and Selenium for browser automation.

**Steps Involved:**

**Reading Excel Files:**
- The script started by loading the Excel file containing phone numbers, area codes, and state information using Pandas. This data was converted into a list for easy iteration.

**Preparing Data:**
- A list of dictionaries was created to store each phone number along with its corresponding area code and state, preparing the data for the scraping process.

**Logging into Spokeo:**
- Using Selenium, the script automated the login process to Spokeo.com. It located the login button and input fields for email and password, sending the necessary credentials to log in.

**Scraping Data:**
- For each phone number in the list, the script:
- Navigated to the search bar on Spokeo.com, cleared any previous input, and entered the current phone number.
- Clicked the search button and waited for the search results to load.
- Attempted to extract customer name and address from the search results. If the elements were not found, it handled the exception by assigning empty strings.
- The extracted details were then populated into the corresponding rows in the original DataFrame.

**Saving Results:**
After processing all phone numbers, the updated DataFrame was saved back into the Excel file, ensuring all extracted customer information was accurately recorded.
The script used WebDriverWait to ensure elements were loaded before interacting with them, enhancing reliability. By automating this repetitive and time-consuming task, the web scraper significantly improved efficiency and accuracy in building a database of customer details from phone numbers. This project demonstrated the effective use of Selenium for web scraping and Pandas for data handling in Python.
