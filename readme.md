## This is a submission project learning path Become a Google Cloud Engineer on Modul dicoding platform

### TODO completion steps:

**(Criterion 1)**
-Create new project (format : submission-mgce-participantname.)

-----

**(Criterion 2) Grant Access Rights to Reviewers**
```sh
> Main Menu -> IAM & Admin -> IAM -> +GRANT ACCESS
```
| setting | value |
| ------ | ------ |
|new principal | reviewer_googlecloud@dicoding.com|
|select a role | basic -> viewer|

-----

**(Criterion 3) Deploy Money Tracker App**

**service account settings**
- create service account
```sh
> Main Menu -> IAM & Admin -> service account -> create service account
```

| setting | value |
| ------ | ------ |
| Service account name | name your project |
| Create and Continue -> Done|

```sh
> click your service account -> action -> manage key -> Add key -> create new key -> json
> open file download and copy all
```

```sh
> open cloud shell -> open editor -> open terminal
> type git clone https://github.com/suryaLuqman/submission2-Proyek-Money-Tracker-App.git
```


## Open the back-end folder, then Focus on the following file :
- serviceaccountkey. json
- modules -> imgUpload.js (Cloud Storage).
- routes -> record. js (Cloud SQL).
- create_table.sql (table schema).

```sh
> open serviceaccountkey.json and replace with your file download (ctrl+v)
> open modules -> imgUpload. js
```

> // TODO: Customize Storage configuration
> projectId : '<your_project_id>',

> // TODO: Add the name of the bucket used
> const bucketName = '<your_GCS_bucket_name>'

------
**Create bucket**
```sh
> Cloud Storage -> Buckets -> Create
```

| setting | value |
| ------ | ------ |
| Name Your Bucket | <Uniquee Name> |
| Choose where to store your data -> location type -> region | asia-southeast2
| **uncheck** Enforce public access prevention on this bucket |
| Access Control | Fine-grained |
| continue -> create |

------
**Add participant**
  
```sh
> menu -> Permissions -> +Grant Access
```
  
| setting | value |
| ------ | ------ |
| new participant | allUsers |
| select a role | cloud storage -> storage object viewer |
| Save |

  ```sh
> ### open routes -> record. js
```

> // TODO: Customize database configuration
> const connection = mysql. createConnection({
>     host: 'public_ip_sql_your_instance',
>     user: 'root',
>     database: 'your_database_name',
>     password: 'your_sql_password'
> })

------
**Create Cloud SQL**
 ```sh
> Main menu -> SQL -> create instance -> choose MySQL -> enable API
```

| setting | value |
| ------ | ------ |
| Instance ID | please fill in what you want. |
| Password | fill in according to your wishes. |
| Database version | select MySQL 5.7. |
| Region | asia-southeast2. |
| Zonal availability | select Single zone only. |
| Then, click the arrow on Show Configuration Options |.
| Machine Type | select the machine type Shared core with the option of 1 vCPU, 0.614 GB. |
| Storage | select Storage type HDD and Storage capacity of 10 GB. |
| Connections | Add Network button ->  Name with Public and fill in Network with the range 0.0.0.0/0. |
| Then, click Done and select Save.|
| create|

```sh
>  SQL -> Databases -> create a database
```
  
| setting | value |
| ------ | ------ | 
| Database Name | please fill in according to your wishes |
| create |

```sh
> Replace //Todo according to the information that was previously made
```


**open website phpmyadmin.co**
| setting | value |
| ------ | ------ |
| server | Public ip your database |
| username | root |
| password | your password |

**click go**

```sh
> open cloud shell editor -> create_table.sql -> copy all
> back to phpmyadmin.co click your database name -> SQL menu -> paste on blank board -> go
```

**wait until checklist progress**
 
```sh
> main menu -> app engine -> create application
```
  
| setting | value |
| ------ | ------ |
| select a region | asia-southeast2
| select service account | select your create service account
| next and wait until finish | 
| i'll do later |

```sh
> back to cloud shell editor -> open terminal -> cd submission2-Project-Money-Tracker-App/ -> cd back-end -> gcloud app deploy and click 'Y'
> gcloud app browse -s back-end (this is a back-end url)
```



---
## Front-end
---
> //TODO
  
> //application -> config -> config.php (base URL of Front-End).
  
> //application -> models -> Record_model.php (base URL of Back-End)

```sh
> open cloud shell editor -> application -> config -> config.php
> Search TODO and replace with URL from Front-End, and the uncomment the code.
```


### deploy your front-end

```sh
> back to cloud shell editor -> open terminal -> cd submission2-Project-Money-Tracker-App/ -> cd front-end -> gcloud app deploy and click 'Y'
> terminal -> gcloud app browse -s front-end
```

```sh
> open open cloud shell editor -> application -> models -> Record_model.php
> Search TODO and replace with base URL Back-End
```



## LAST TASK

```sh
> back to cloud shell editor -> open terminal -> cd submission2-Project-Money-Tracker-App/ -> cd front-end -> gcloud app deploy and click 'Y'
> terminal -> gcloud app browse -s front-end
> copy link -> open link in your browser -> check it is running perfectly ?
> check 
```




## Check Submit Permission project
## Thanks  😊👋😁
  
> ### Don't forget to delete or deactivate services that are no longer needed to prevent additional fees/billing from being required if they are no longer used. 
> ### Here are the steps you can take to Clean Up:
> - ### Click Read more in Notes from Reviewers 
