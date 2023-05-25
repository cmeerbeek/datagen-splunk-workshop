# datagen-splunk-workshop
Docker compose setup for generating sample data to Splunk using Cribl

## Assignments

### Data

1. Viwe data in Splunk (index=main sourcetype=access_common)
2. Filter data on host web03.cribl.io

### Dashboards

1. Create a dashboard with the following panels with data from the last 24 hours
* Percentage status = 2xx in total requests
* Avg bytes across all requests
* Timechart with p99 bytes across all requests
* Max bytes table for each request URI
* Piechart for all status codes
2. Bonus: Add input field to select the timerange which updates the dashboard
3. Bonus: Add input field to set the span for a timechart which updates the dashboard

### Alerting

1. Create an alert which triggers if more than X events are found for status = 5xx events in the last 5 minutes
2. Bonus: Change the alert to only trigger on a certain URI like "/best-of-breed/solutions"

### Reporting

1. Create a report which shows the number of requests per URI
2. Bonus: Add a column which shows the number of request per status

### Lookups

1. Add the lookup http_status_codes.csv to the data so you can see the description of each status code
2. Bonus: Add a panel in the dashboard you created earlier which uses the description instead of the http_status to display the number of events with this description
