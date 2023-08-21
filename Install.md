# Installation Instructions

1. Download the two .zip files
2. In Teams, create channels for each community team district and for each acute team (hospital).
3. In the PowerApps app for Teams, find the list of all components in your Dataverse for Teams environment. If you haven't yet created an app in this team, you may need to generate a new Dataverse for Teams environment first. https://learn.microsoft.com/en-us/power-apps/teams/create-first-app
4. From the Build tab, use the Import menu or the "Import your solution" link to import the "DWDCoordination..." solution zip file. You may need to create new connections, switching back to Teams for each connection. When all connections are made, the import process will take 5-10 minutes. There may be a list of warnings in a yellow banner. These are OK.
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/d16e021d-3f61-413a-bb4d-48ba94825b2c) 
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/a808c452-fa0f-4f5b-add3-aee4f8e05078)
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/ee027898-ec4d-4031-b1c1-9461e92a2eec)

5. Upload a small logo file (100x100 pixels) to the Team hosting the app. From the details pane for the uploaded image file, copy the path to the file. DO NOT use the "get a link / share" commands! Save this to a notepad.
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/1c8ef629-6080-4868-87c4-4fe1864d868b)

6. Open (edit) the app in the PowerApps Teams app, allow permissions for the connections you created, and then use the publish button to add the app to the Teams channels you created. 
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/f219d527-8a3a-4ff6-87ae-5ac2af72d2f9)
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/136d8510-ce02-423d-8e5b-f4017e91a530)

7. Go into the Team and copy the channel IDs from the "get link to channel" option for the district and hospital channels. You only need the part of the URL that starts with "19%" and ends with "thread.tacv2". Also copy the links to the tabs where the app is published (from the drop down on the tab, click "copy link to tab"). Save all of these to a notepad so that you know which IDs & links go to which channel.

8. Go back into the PowerApps app for Teams, and navigate to the Districts table. Complete the Districts table with the names of the districts that map to the channels, as well as the channel IDs and links to the tabs. It should look like this. Do the same for the Hospitals table. (The "Hospital Type" field in the Hospital table is not currently used in this version of the app.)
![image](https://user-images.githubusercontent.com/56914706/224298151-73bbfd37-9171-47fc-9876-c7ac5964c519.png)

9. Edit Ward table to include all the hospitals and wards that you want to include. Your Ward table should be filled out like this:
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/f5eb44fd-9c41-456b-ac90-1fb3e487dc73)

10. Open the PowerAutomate portal https://make.powerautomate.com/ and switch to the environment for your Team
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/d63b3c79-a5c2-48da-8110-2d3778945179)

11. Import the "Newpatient..." zip file as a Package, selecting your existing connections for each of the three "related resources" at the bottom of the import screen. You should now have eight flows.
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/af763f3e-4545-49fc-9472-ce67aa3a1d31)
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/d515e4f6-4d22-474a-b0cd-284b8d45b2c8)

12. In the ExportPDF... flow, in the Create file action, change the Site Address parameter to the location where the exported PDFs will be saved. Save the flow.

13. The New patient, Viable Date Changed, PDD Changed, and DMT Changed flows need the following edits to the purple Teams actions (last step):
- Configure the Team parameter to the Team you created in step 2. 
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/f0577976-debf-40bd-98bc-1004793c0d71)
- The Viable Date Changed and DMT Changed flows also need a channel specified (assumed General, but whatever channel is being used by the acute team).
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/4bdeb817-0dbb-46e2-a296-dce16ec0bb6e)
- Replace the URL in the Adaptive Card code with the path to the logo file you uploaded in step 6.
![image](https://github.com/chslemp/Discharge-Without-Delay/assets/56914706/131293e0-5c67-44c2-93c9-fd70bf1ea576)

14. Ensure all flows are turned on (not greyed out).
