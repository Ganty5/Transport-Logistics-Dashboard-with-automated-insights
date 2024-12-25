**PROJECT OVERVIEW:**
This project showcases an automated transport logistics dashboard to monitor key metrics such as total cost, distance, weight shipped, delivery performance, and pending orders. 
It integrates Google Sheets as the data source, Python for preprocessing, and Power BI for visualization.

Using Google Sheets to serve as a central data repository where users can easily update and manage transport order data. I authenticated using the Google Cloud JSON Key file for API access.
Retrieved and loaded the transport order data using the gspread Python library, after which I Structured the data as a Pandas DataFrame for further processing.

During the preprocessing using python, 
I took the action of converting the date columns (Timestamp, Shipped date, Delivery Date) into a consistent ISO format (YYYY-MM-DD HH:MM:SS) to ensure compatibility with Power BI.
I afterwards saved the processed data as a CSV file for seamless import into Power BI. I ensured the dataset is clean and ready for analysis by handling potential parsing errors or inconsistent data formats.

Next action was creating my Power BI Dashboard
This was basically to create a dynamic, user-friendly dashboard to visualize transport logistics key metrics needed to be known and for enhancing insights and decision-making.


**Some of the key metrics captured in the dashbiard includes;**
Total Distance Traveled
Total Cost
Total Weight Shipped
Average Delivery Duration
Number of Orders
Delivery Performance (Percentage of On-Time Deliveries)
Charts:
Order Count by Month
Delivery Duration by Month
Transport Types (Pie Chart)
Top Routes (Table)
Order Status by Pickup/Drop-Off Locations (Maps)
Interactive Filters:
Month and Transport Type filters for dynamic exploration.

After designing and creating my Power Bi dashboard, I took on the next step for its automation and updating

Due to certain lines of python script put into consideration during the preprocessing phase, The dataset on Google Sheet has been set to updated dynamically for some rows basically changing order statuses and timestamps.
The Power BI dashboard fetches the updated data via a feature --> scheduled refresh on the Power BI Service. Auto-refresh ensures stakeholders see the latest metrics and insights without manual intervention.

The libraries used in the python script include;
**gspread to enahnce interaction between pthon and Google sheets
pandas for data processing and manipulation
oath2client for aunthentication with Google Cloud**
Json key file for Google Authentication was configured,

Recommendations for future advancement:
Incorporating machine learning to predict delievery delays or ptimize transportation routes
Implemented the usage of automated emails
