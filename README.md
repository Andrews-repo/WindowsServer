# WindowsServer
Notes and details for Windows Server 2019

Initially I installed Server 2012, for some reason. Got the ETH controller working, to realize i should be using Server 2019.

#Installed Server 2019
* Installer from manufacturer doesnt recognize MOBO/ETH controller for Server 2019.
  * Tried installing "intel chipset software" and no help
  * Solution: Download drivers directly, and point windows to install a different driver, but point to file storing correct driver. Some solutions suggested disabling driver signature check and editing driver files. 
  
#Making a Domain Controller
* Open Server Manager
* Click "Add roles and other features"
* Select "Role-based or feature-based installation" and click next
* Select the server from the list and click next
* Select "Active Directory Domain Services" amd click next
* Select any features you want and click next
* On this page review the details, Click next or installl, After Installation, System restart is required
* When Server Manager reloads, click yellow notification flag, and click promote to domain controller
* Click Add New forest, Enter "name".local and next
* Select Server OS version, enter "Directory Services Restore Mode" password, click next
* Leave Default folder paths and click next, review page and click next
* If all Pass Click Install and let server restart

#ADDING A NEW USER
* Click start -> Windows Administrative Tools -> Active Directory Users and Computers
* Right CLick Domain -> New -> User, or select New User Icon in Explorer bar
* Fill out fields -> Next -> Set password details -> Next - Finish
