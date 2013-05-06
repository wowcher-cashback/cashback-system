cashback-system
===============

Git Location: https://github.com/wowcher-cashback/cashback-system.git

Pre-requisite:
--------------
		1. JDK 1.6.0_30 or greater.
		2. Tomcat 6.0  or greater.
		3. Eclipse - SpringSource Tool Suite - Version: 3.1.0.RELEASE
		4. Eclipse plugins:
			E-Git Plugin: http://download.eclipse.org/egit/updates
		
Add Apache Tomcat 7.0 to eclipse Runtime environment (if not already done)
----------------------------------------------
		1. Goto Windows -> Preference -> Server -> Runtime environment -> Add
		2. Then select Apache Tomcat 7.0 from the list
		3. Click Next and browse the server location from your local system  (D:\NBCU_Workspace\userdata\apache-tomcat-7.0.39\apache-tomcat-7.0.39)
		4. Click Finish

Clone modules from github(https://github.com/organizations/wowcher-cashback) to eclipse in following order
--------------------------------------------------------------------------------------------------------
cashback-mvc
cashback-services
cashback-persistence
cashback-system


Setting the github module in eclipse:
-------------------------------
		1. Goto File > Import > Git > Project From Git
		2. If not cloned, clone from gitHub. and click Next
		3. Choose "Use the New Project wizard"
		4. Select "Dynamic Web Project" and click next
		5. Uncheck the "Use default Location" and Browse the project from FileSystem and click Finish
		6. Enter the Project name as "cashback-system", Select the project Runtime as Tomcat v7.0 Server at localhost( if not exist, add as mentioned above)
		7. Source folder: src
		8. Output folder: cashback-system/build/classes
		9. Library: should get loaded automatically from /WEB-INF/lib
		10.Building dependent module as Jar for dynamic web deployment
			a. Right-click project and goto properties
			b. goto Deployment Assembly 
			c. click Add 
			d. Select Project and click Next
			e. Multi-select (by holding down the <control> key) the following modules, and then click "Finish": 
			- cashback-mvc
			- cashback-services
			- xytech-api-adapter
			- cashback-persistence	
			g. click Apply and Ok


---------------------------------------------------------------------------
		                     
