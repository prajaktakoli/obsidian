On Premise
 - High price, less scalability
 - No automatic software updates
 - less collaboration 
 - Data cannot be accessed remotely
 - More implementation time
Cloud
- High flexibility - Scale up, pay more, Scale down, pay more
- Automatic software updates
- Collaboration is widespread across different locations
- Data can be accessed and shared anywhere over the internet
- less implementation time
--------------------------------------------
Cloud Computing : it delivers on demand computing services over the internet on pay as you go basis
Eg. Instaed of saving files on local storage device, store it on the internet

Types of Cloud Computing
- Deployment Model vs Service Model

![[Pasted image 20240518205257.png]]

Deployment Model 
Public  - Cost effective, pay only for stuff which you are using, cloud infrasture made available to the general public over the internet and owned by cloud provider
Private - Very costly, cloud infrastruture is managed by a single company, may exists as on premise or off premise
Hybrid - Combination of public + private
- For eg. federal agencies use private cloud to share sensitive information and public cloud to share datasets with general public
![[Pasted image 20240518205726.png]]------------------------------------------------------------------------------------------------
Service Model:
IAAS
PAAS
SAAS
![[Pasted image 20240518232552.png]]
IAAS - Provides basic infrastucture services
Services are based on pay as you go model

PAAS - provides cloud platforms and runtime environments for developing, testing and managing applications.
It allows software devlopers to deploy applications without requring related infrastructure.

SAAS - All software and hardware are provided and managed by a vendor so you dont have to maintain anything. Cloud providers host and manage  the application on pay as you go basis.
Eg. Gmail, MS office
![[Pasted image 20240518233243.png]]Eg. Baking a cake
![[Pasted image 20240518233516.png]]Lifecycle of cloud computing solution: AWS
- Define a purpose -  Understand requirements of the business to determine what type of applications to run on the cloud
- Define hardware - Choose a compute service where you resize the compute capacity in the cloud to run appl prog.
	  EC2 (Iaas), Lambda (Serverless Computing), Elastic container service
- Define storage - choose a storage service where data can be backed up and archived over the internet - S3, EFS, Glacier
		S3 - Backup, Glacier - Archival
- Define network - Define network that will deliver the data securely with low latency and high speed 
	-VPC - (Network) , Route 53 - (DNS), Direct Connect
- Define security 
- Define Management Processes and Tools
- Testing - CodeStar, CodeBuild, CodePipeline
- Analytics - Athena, EMR, Cloudsearch - for visualizing data
----------------------------------------------------
AWS EC2 
- web service that provides a secure and resizable compute capacity in the cloud
- can be used to launch as many virtual servers as you need
AWS S3 
- simple storage service
- you can store and retrive any amount of data at anytime on the web
-
