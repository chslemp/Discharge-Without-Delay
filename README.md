# Discharge-Without-Delay
A Power App designed to improve collaboration between acute and community teams as they negotiate the discharge of a patient. This app allows acute teams to enter the intial data about a patient, after which an automated notification is posted to a Teams channel for the community "district" to which the patient belongs. The community team adds data, and the teams go back and forth entering data, receiving notifications, and coordinating using the appropriate Teams channels. A link from the patient list takes the user directly to a chat thread in Teams created for each patient.

Each time the record is saved, all data is written to an audit table. When the patient is released, the patient record can be exported to PDF for upload to the EPR, and the record then archived from the app.

![DWD app list view](https://user-images.githubusercontent.com/56914706/224285982-6a4bb1c2-7689-4f27-af2c-817d3152ff2c.jpg)
The list view of all patients, including filters for District, hospital, and ward

![DWD app acute form](https://user-images.githubusercontent.com/56914706/224286097-f31d53ec-e18c-4d66-8613-462a79deaf57.jpg)
The patient detail form: acute team info

![DWD app community form](https://user-images.githubusercontent.com/56914706/224286152-83039354-aef2-4fed-9cad-2647585fbf68.jpg)
The patient detail form: community team info

![DWD app notifications](https://user-images.githubusercontent.com/56914706/224286233-97fafd20-2387-44d7-ad9f-decf34eb5daa.jpg)

Various notifications sent to the Teams channel for the district

See [Installation Instructions](/install.md)
