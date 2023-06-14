# Discharge-Without-Delay
A Power App designed to improve collaboration between acute and community teams as they negotiate the discharge of a patient. This app allows acute teams to enter the intial data about a patient, after which an automated notification is posted to a Teams channel for the community "district" to which the patient belongs. The community team adds data, and the teams go back and forth entering data, receiving notifications, and coordinating using the appropriate Teams channels. A link from the patient list takes the user directly to a chat thread in Teams created for each patient.

Each time the record is saved, all data is written to an audit table. When the patient is released, the patient record can be exported to PDF for upload to the EPR, and the record then archived from the app.

![DWD app list view](https://user-images.githubusercontent.com/56914706/235075752-7950ee06-3702-4910-9d73-7a42254ef121.jpg)
The list view of all patients, including filters for District, hospital, and ward

![DWD app acute form](https://user-images.githubusercontent.com/56914706/235075801-0ff27af9-6079-44c1-aa78-2ba553b035ad.jpg)
The patient detail form: acute team info

![DWD app community form](https://user-images.githubusercontent.com/56914706/235075836-0b99e0fa-9f35-4354-865c-938153b586cf.jpg)
The patient detail form: community team info

![DWD PDF export](https://user-images.githubusercontent.com/56914706/235075894-1b972956-bae2-48eb-ad7c-afb4d3fc2307.jpg)
Export the data as a PDF for upload to an EPR

![DWD app notifications](https://user-images.githubusercontent.com/56914706/235075870-fa9fd579-a4e9-4992-ac68-2bde42630d0d.jpg)
Various notifications sent to the Teams channel for the district

See [Installation Instructions](/Install.md)
and [detailed tech documentation](/documentation.md)
