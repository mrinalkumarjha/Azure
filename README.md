# Azure

When you goto host a website, a hosting provider has to provide lots of services to you. like he need to provide ram , bandwidth, hard disk, cpu , softwares and much more. These 
services can be divided into following catagory

	1: Infrastructure services(IAAS): Services like hard disk, firewall, ram, cpu, vm, bandwidth comes into IAAS service or infrastructure service. This layer is the
		metal part of your hosting.
		
	2: Plateform service(PAAS): Services like OS, database, framework like donet, web server like iis apache is called plateform as a service.
	3: Software service(SAAS): Invoicing, yahoo, gmail, Accounting, Control panel etc is comes in SAAS category.

IF you want to do all these by yourself if will be lots of hard work like for hosting you will have to create data center, software license, hardware, cpu, ram, technician,
network guys, hardware engineer etc. By doing all things by itself it will cost too much. Instead we want to pay only we use.
So instead of doing it by ourself we choose a provider like AZURE.

In other word we can say we can pay for ondemand service. 

Cloud follows two principles of O. 
	
		1: Ondemand: for example i want 1 gb ram, 100gb hard disk for 2 days. in future we can increase spce to 500 GB. so we can scale up and down both.
		2: Outsourced: it says customer dont need to worry about db backup. he can focus on his website or his business rest is taken care by service provider.
It is same like we go to hotel place a order and eat food. we dont want to worry about how food is being cooked, how staff will clean plates after eating. we just pay
only for what we used.

So in cloud also service provider gives flexibility to its customer to use its layer as a service and pay only for they want to use.

# What is cloud?
	cloud is list of service like SASS, PAAS, IAAS.

# What is Azure?

	azure is microsoft implementation for cloud.
	

# Where to register ?
	goto account.azure.com and register for free account for 12 month. It will give you some credit which is sufficient for learning modules.
	After registration use this https://portal.azure.com/#home  link to see all service and go through any service available.
	
Azure has lots of services. you can see in left menue of portal.azure.com. 

# ResourceGroup

	In azure basically we will be adding resource. like window server 2008, sqk db etc. in large project we can have multiple resources. So we will create a resource group
	and put all resource in ResourceGroup so that it can be managed easily.
	To add resource group select resource group and click on add. name it like WebDevelopmentClient1. 
	
	In region select location for resource. for best performance we should choose nearest location. 
	
# Resource
	As i have added resource group WebDevelopmentClient1 we can now add resource to resource group.
	
	
# App Service 

	For application like web application , mobile application, hosting api we can choose App Service link. Create new app here and put a name for this.
	whatever name will be given here will be name of app with domain .azurewebsites.net
	
	I have created a web app with name https://mrinal.azurewebsites.net/
	
# Development Tools
	> Console
	Use this menue to see files of website directory.
	> App Service Editor to edit file directly online.
	
# Deployment >  Development Centre
	Use this for creating ftp credentials.
	
# DTU AND EDTU


#DTU : Database transaction unit.
	one thing which attracted us on azure is pay as you go. pay only for what you want to use. 
	we defin our work load in terms of processor, HD, RAM, transaction, no of users  => then decide our configuration like plan on azure => Then pay what we use.
	
	Here problem is how do you determine work load ? work load vary from one application to another , user to user. suppose you are creating web application, no of
	user should matter for you. if you are using sql server then no of transaction should matter for you. for some people only ram is important. so workload
	is calculated based on lots of factors. 
	for example for rdbms following are things we should consider for configuration of work load.
	
	1. No of writes
	2. No of reads
	if above two is high then we consider work load is high. and if that is low we consider it is low.
	3. Ram consumed: no of ram consumed writing to primary file and read from primary file.
	4. Processor consumed for reading writing. > If you are reading and writing to file processor will be consumed so 
		it should be considerable that how much percentage processor is needed.
		
	5.Log file: Log writen to sql log
	
    So who will tell us which pricing plan we have to choose. for this purpose microsoft has created DTU. 
	
	DTU is a unit specially for RDBMS which is calculated based on above 5 factor,and it gurantees performance for that configuration.
	
	So once we calculate our dtu we can choose plan in azure .
	
	we create our db in azure. allocate dtu to db. suppose added 5 dtu to db test. so this 5 dtu can only used for this db.
	
#EDTU : Elastic dtu. EDTU is same as dtu only difference is this dtu can be shared with multiple db. db1 and db2
		we can set min and max in edtu. we need to set this as we dont want one database to take all dtu.
		dtu is dedicated to single database but edtu is for multiple database. 
		
		we can use azure calculator (https://dtucalculator.azurewebsites.net/)
		
		1. download command line utility from above site. run the exe . exe should be execcuted from machine where
		we need to calculate dtu.
		it will create a csv file with all above 5 parameter and value.
		
		azure db created for testing purpose..
		
		server: mrinal.database.windows.net
		sql uid:mrinal
		sql pass: admin.1234
	
	

	
