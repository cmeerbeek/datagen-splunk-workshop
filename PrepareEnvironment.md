# Prepare the workshop environment

Use the following steps to prepare your workshop environment.
If you need screenshots use the powerpoint.

## Getting the files

Make sure you have Docker Desktop or equivalent on your system

1. Clone repository https://github.com/cmeerbeek/datagen-splunk-workshop
2. Go into the directory datagen-splunk-workshop and run ‘docker-compose up’

## Configure Splunk

1. Go to http://localhost:18000 and login with admin and changeme (change the password if you want to do so)
2. Go to Settings -> Data Inputs -> HTTP Event Collector
3. Click Global Settings -> uncheck “Enable SSL” -> click Save

## Configure Cribl

1. Go to http://localhost:19000 and login with admin and admin (change the password if you want to do so)
2. Click on Manage
3. Click on Default
4. Click on QuickConnect
5. Click on "Add data source"
6. Type "datagen" in the searchbox and click on it
7. Type "SourcesApacheCommon" in the first box
8. Select "apache_common.log" from the dropdown
9. Change 10 to 4 for Events per Second
10. Click Save
11. Click "Add Destination"
12. Search for "HEC" and click on "Splunk HEC"
13. Type Outputs ID is "OutputsSplunkHEC"
14. Change the URL to http://splunk_server:8088/services/collector/event
15. Add to "HEC Auth Token": 00000000-0000-0000-0000-0000000000000
16. Click Save
17. Click on the + sign right next to your datagen and dragg it on top of the Splunk HEC outputs
18. On release select Passthru and press Save
19. Click on "Commit"
20. Enter a commit message and click "Commit and deploy"
21. Wait for a few minutes before some data starts flowing into Splunk
22. Click on "Monitoring" to see that
