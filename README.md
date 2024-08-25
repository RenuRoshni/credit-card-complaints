# Credit Card Complaints Analysis Dashboard

## Overview
The Credit Card Complaints Analysis Dashboard provides a comprehensive overview of customer complaints related to credit card services using Tableau. This dashboard focuses on understanding the nature, volume, and resolution of complaints to help financial institutions improve customer service and identify trends that may require attention.

## Key Performance Indicators (KPIs)
- **Total Complaints**: Total number of credit card complaints received.
- **Complaints in the Last 12 Months**: Number of complaints received over the last year.
- **Timely Response Rate**: Percentage of complaints resolved within the targeted timeframe.
- **In-Progress Complaints**: Number and percentage of complaints that are currently unresolved.
- **Top Complaint Issues**: Most frequent types of complaints received.
- **Company Response Breakdown**: How companies have responded to complaints (e.g., monetary relief, explanation, non-monetary relief).

## How the Project Was Done in Tableau

### Steps to Create the Dashboard

1. **Data Collection**:
   - The first step was to gather credit card complaint data from a reliable source.

2. **Data Preparation**:
   - The raw data was imported into Excel to perform initial cleaning. This involved removing duplicates, filling in missing values, standardizing formats, and filtering out irrelevant data.
   - The cleaned dataset was saved in a format compatible with Tableau, such as CSV or Excel.

3. **Data Import into Tableau**:
   - The prepared data file was then imported into Tableau Desktop. In Tableau, we established a connection to the data source by selecting "Connect to Data" and choosing the CSV or Excel file.
   - Reviewed the data types for each field (e.g., dates, numbers, text) to ensure they were correctly interpreted by Tableau.

4. **Data Modeling in Tableau**:
   - **Calculated Fields**: Created calculated fields to derive key metrics, such as the "Timely Response Rate" and "Complaints in the Last 12 Months". For example:
     - **Timely Response Rate**: A calculated field using the formula `IF [Days to Respond] <= 30 THEN 'Timely' ELSE 'Not Timely' END`.
     - **Rolling 12 Months Complaints**: A calculated field using Tableau’s date functions to filter data to the last 12 months dynamically.
   - **Data Blending**: Where necessary, we blended data from multiple sources to enrich the analysis, such as combining complaint data with demographic information.

5. **Dashboard Development**:
   - **Create Visuals**:
     - Created various visualizations (worksheets) for each KPI. For example:
       - **Total Complaints**: A simple KPI card showing the total number of complaints.
       - **Weekly Trends**: A line chart to show trends over time.
       - **Top Issues Bar Chart**: A horizontal bar chart to display the top 10 complaint categories by count.
       - **State-wise Complaints Map**: A filled map (choropleth) to visualize complaint density across different states using Mapbox integration within Tableau.
       - **Company Response Breakdown**: A stacked bar chart showing the breakdown of company responses.
       - **Daily Complaints Heatmap**: A heatmap created using a calendar view to display daily complaints.
   - **Combine Worksheets**:
     - These individual visualizations were then combined into a single dashboard. Used Tableau's drag-and-drop interface to arrange the worksheets on the dashboard canvas.
     - **Layout and Formatting**: Adjusted the size, position, and format of each visual element to create a cohesive and user-friendly layout.

6. **Adding Interactivity**:
   - **Filters and Parameters**: Added filters (e.g., date range, state, company) to allow users to customize their view. For example, a drop-down filter for "State" allowed users to focus on specific geographical areas.
   - **Actions**: Configured actions to allow interaction between different sheets. For instance, clicking on a state in the map would filter the data in other charts to show only the complaints from that state.
   - **Tooltips**: Enhanced the tooltips to provide more context when users hover over data points, such as displaying detailed complaint information or additional metrics.

7. **Dashboard Publishing**:
   - Once the dashboard was complete, it was published to Tableau Server or Tableau Public. This involved selecting "File" > "Publish to Tableau Server" or "Tableau Public" and following the prompts to upload the dashboard online.
   - **Sharing**: The published dashboard was shared with stakeholders by providing the link, allowing them to access the dashboard from any device.

## Key Visuals
- **Total Complaints and Trends**: A line chart displaying the number of complaints over time, helping to identify patterns or spikes in complaint volume.
- **Top Issues Bar Chart**: Visual representation of the most common complaint types, providing insight into recurring issues faced by customers.
- **State-wise Complaints Map**: A density map showing the geographic distribution of complaints, highlighting regions with higher concentrations of customer issues.
- **Company Response Breakdown**: A stacked bar chart showing how companies have responded to complaints, categorized by response type (monetary relief, non-monetary relief, explanation, etc.).
- **Daily Complaints Heatmap**: A calendar-style heatmap illustrating the volume of complaints received on each day, highlighting daily or seasonal trends.

## Insights
- **Complaint Volume and Patterns**: There is a noticeable peak in complaints around 2019, suggesting a period of increased customer dissatisfaction or a specific issue affecting many users.
- **Top Complaint Issues**: Billing disputes are the most frequent type of complaint, suggesting a need for better billing clarity or processes.
- **Geographical Concentrations**: Certain states exhibit higher complaint densities, indicating potential regional issues or higher concentrations of credit card users.
- **Response Effectiveness**: A high percentage of complaints are resolved with explanations, but there is a notable portion requiring monetary or non-monetary relief, indicating financial impact and potential areas for process improvement.
- **Preferred Complaint Submission Channels**: Most complaints are submitted online, reflecting the digital engagement of customers and the importance of maintaining effective online complaint handling mechanisms.

## Usage
1. **Access the Dashboard**: Visit the Tableau Public link or Tableau Server where the dashboard is hosted.
2. **Interact with the Dashboard**: Utilize filters and interactive elements to explore the data and customize the view based on specific criteria or time periods.
3. **Export Data**: Use the export options to download reports for offline analysis or presentations.

## Conclusion
The Credit Card Complaints Analysis Dashboard is a valuable tool for financial institutions to monitor, analyze, and respond to customer complaints effectively. By understanding the trends and root causes of complaints, companies can enhance customer service, improve satisfaction, and proactively address issues to prevent future complaints.

