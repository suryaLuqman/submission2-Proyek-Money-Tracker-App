## This is a submission project learning path Become a Google Cloud Engineer on Modul dicoding platform

TODO completion steps:

(Criterion 1)
-Create new project (format : submission-mgce-participantname.)

(Criterion 2) Grant Access Rights to Reviewers
  Main Menu -> IAM & Admin -> IAM -> +GRANT ACCESS
new principal = reviewer_googlecloud@dicoding.com
select a role = basic -> viewer

(Criterion 3) Deploy Money Tracker App

*service account settings
- create service account
Main Menu -> IAM & Admin -> service account -> create service account
Service account name = name your project
Create and Continue -> Done

click your service account -> action -> manage key -> Add key -> create new key -> json

open file download and copy all

open cloud shell -> open editor -> open terminal
type git clone https://github.com/suryaLuqman/submission2-Proyek-Money-Tracker-App.git


## Open the back-end folder, then Focus on the following file :
- serviceaccountkey. json
- modules -> imgUpload.js (Cloud Storage).
- routes -> record. js (Cloud SQL).
- create_table.sql (table schema).

> ### open serviceaccountkey.json and replace with your file download (ctrl+v)

> ### open modules -> imgUpload. js

// TODO: Customize Storage configuration
projectId : '<your_project_id>',

// TODO: Add the name of the bucket used
const bucketName = '<your_GCS_bucket_name>'

**Create bucket**
> Cloud Storage -> Buckets -> Create
Name Your Bucket -> <Uniquee Name>
Choose where to store your data -> location type -> region : asia-southeast2
**uncheck** Enforce public access prevention on this bucket
Access Control : Fine-grained
continue -> create

**Add participant**

> menu -> Permissions -> +Grant Access
setting values
new participant allUsers
select a role cloud storage -> storage object viewer
Save

> ### open routes -> record. js
// TODO: Customize database configuration
const connection = mysql. createConnection({
     host: 'public_ip_sql_your_instance',
     user: 'root',
     database: 'your_database_name',
     password: 'your_sql_password'
})

**Create Cloud SQL**
> Main menu -> SQL -> create instance -> choose MySQL -> enable API

Instance ID: please fill in what you want.
Password: fill in according to your wishes.
Database version:  select MySQL 5.7.
Region: asia-southeast2.
Zonal availability: select Single zone only.
Then, click the arrow on Show Configuration Options.
Machine Type: select the machine type Shared core with the option of 1 vCPU, 0.614 GB.
Storage: select Storage type HDD and Storage capacity of 10 GB.
Connections: Add Network button ->  Name with Public and fill in Network with the range 0.0.0.0/0. Then, click Done and select Save.

create

SQL -> Databases -> create a database
Database Name: please fill in according to your wishes
create

> Replace Todo according to the information that was previously made

**open website phpmyadmin.co**
server = Public ip your database
username = root
password = your password

click go

> open cloud shell editor -> create_table.sql -> copy all
> back to phpmyadmin.co click your database name -> SQL menu -> paste on blank board -> go

wait until checklist progress

> main menu -> app engine -> create application
select a region = asia-southeast2
select service account = select your create service account
next and wait until finish, then i'll do later

> back to cloud shell editor -> open terminal -> cd submission2-Project-Money-Tracker-App/ -> cd back-end -> gcloud app deploy and click 'Y'
> gcloud app browse -s back-end (this is a back-end url)


---
##Front-end
###TODO
application -> config -> config.php (base URL of Front-End).
application -> models -> Record_model.php (base URL of Back-End)

> open cloud shell editor -> application -> config -> config.php
> Search TODO and replace with URL from Front-End, and the uncomment the code.

### deploy your front-end
> back to cloud shell editor -> open terminal -> cd submission2-Project-Money-Tracker-App/ -> cd front-end -> gcloud app deploy and click 'Y'
> terminal -> gcloud app browse -s front-end

> open open cloud shell editor -> application -> models -> Record_model.php
> Search TODO and replace with base URL Back-End


last

> back to cloud shell editor -> open terminal -> cd submission2-Project-Money-Tracker-App/ -> cd front-end -> gcloud app deploy and click 'Y'
> terminal -> gcloud app browse -s front-end
open link in your browser


## Check Submit Permission project
### Thanks
