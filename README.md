# Hospital-API


 API using Node.js and MongoDB for the doctors of a Hospital which has been allocated by the govt for testing and quarantine + well being of COVID-19 patients.

## Features

There can be 2 types of Users
- *Doctors* & *Patients*
- Doctors can log in
- Each time a patient visits, the doctor will follow 2 steps:
    - Register the patient in the app (using phone number, if the patient already exists, just return the patient info in the API)
    - After the checkup, create a Report.
- Patient Report will have the following fields
    - Created by doctor
    - Status: Can be either of: *[0 :Negative, 1:Travelled-Quarantine, 2:Symptoms-Quarantine, 3:Positive-Admit]*
    - Date

## How to INSTALL and RUN?

1. Clone the project.
2. Navigate to the folder `cd Hospital-API ` where the project has been Stored.
3. Open Terminal and type `npm install` to install required files.
4. Run following command: `Nodemon .\index.js `

## How to USE?

URL: ` http://localhost:8000/api/v1`

#### Steps(Postman):
1. `/doctors/register`(POST): Register the new doctor using name,email and password(all requireds).




2. `/doctor/login`(POST): Doctor can Login using email and password.

- Generate JWT Token




3. `/patients/register`(POST): Doctor can Register the patient using name and Phone Number.




4. `/patients/:id/create_report`(POST): Doctor can create report of the Patients.

5. `/patients/:id/all_reports`(GET):Retrive all reports of a patient by ID.




6. `/reports/:status`(GET):Retrieve all reports from DB filter on the basis of Status sent in params.







## Folder Structure
- **Entry point** : index.js.
- **config** : Contains configuration files of Mongoose,Passport JWT Strategies and Status.
- **controllers** : The controllers for various urls like Doctor API or Patient API or Report API.
- **models** : Mongoose Schemas for the Doctors, Patients and reports.
- **routes** : Different routes for different request urls.





