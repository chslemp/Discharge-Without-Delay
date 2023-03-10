# Installation Instructions

1. Download all three .zip files
2. In Teams, create channels for each district
3. In the PowerApps app for Teams, find the list of all components in your Dataverse for Teams environment
4. Import the "DWDCoordination..." solution zip file. You will need to create new connections.
5. Open the app and publish to the Teams channels you created
6. Go into the Team and copy the channel IDs from the "get link to channel" option. You only need the part of the URL that starts with "19%" and ends with "thread.tacv2". Also copy the links to the tabs where the app is published
7. Go back into the PowerApps app for Teams, and navigate to the Districts table. Complete the Districts table with the names of the districts that map to the channels, as well as the channel IDs and links to the tabs. It should look like this. 
![image](https://user-images.githubusercontent.com/56914706/224298151-73bbfd37-9171-47fc-9876-c7ac5964c519.png)
8. Open the PowerAutomate portal and switch to the environment for your Team
9. Edit the Hospital and Ward tables to include all the hospitals and wards that you want to include, starting with the Hospital table so that you can map the ward names to the hospital in the Ward table.
10. Import the "Dailycheck..." and "Newpatient..." zip files as Packages. You should now have eight flows.
![image](https://user-images.githubusercontent.com/56914706/224299441-3ba7b728-655b-42e7-a028-684b1b51b8c0.png)
11. In the ExportPDF... flow, in the Create file action, configure the location where the exported PDFs will be saved.
12. In the New patient, Ready for PDD, Ready for DMT, and Daily Check flows, look for the "Post adaptive card..." actions, and configure to the Team you created in step 2
