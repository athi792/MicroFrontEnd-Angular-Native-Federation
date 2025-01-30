Micro Frontend Angular Native Federation Setup
Step 1: Create Angular Projects
1.	Create Shell Project:

ng new shell --routing --style=css
o	angular.json, package.json, tsconfig.json, and other necessary files were created.
2.	Create MFE1 Project:

ng new mfe1 --routing --style=css
o	angular.json, package.json, tsconfig.json, and other necessary files were created.
3.	Create MFE2 Project:

ng new mfe2 --routing --style=css
o	angular.json, package.json, tsconfig.json, and other necessary files were created.
Step 2: Add Native Federation to Each Project
1.	Add Native Federation to Shell Project:

ng add @angular-architects/native-federation@17.1.x --port 4200 --project shell --type dynamic-host
o	Installed necessary packages and updated configuration files (angular.json, package.json, etc.).
2.	Add Native Federation to MFE1 Project:

ng add @angular-architects/native-federation@17.1.x --port 4202 --project mfe1
o	Installed necessary packages and updated configuration files (angular.json, package.json, etc.).

Add Native Federation to MFE2 Project:
ng add @angular-architects/native-federation@17.1.x --port 4204 --project mfe2
o	Installed necessary packages and updated configuration files (angular.json, package.json, etc.).
Step 3: Build Projects
1.	Build MFE1 Project:
ng build
o	Completed successfully and generated the output in dist/mfe1.
2.	Build MFE2 Project:
ng build
o	Completed successfully and generated the output in dist/mfe2.
o	
3.	Build Shell Project:
ng build
o	Completed successfully and generated the output in dist/shell.
4.	
Step 4: Serve MFE1 Project
1.	Serve MFE1 Project:
ng serve
o	Successfully served the application on http://localhost:4202/.
________________________________________

Step 5: Serve MFE2 Project
1.	Serve MFE2 Project:
ng serve
o	Successfully served the application on http://localhost:4204/.
________________________________________
Step 5: Serve MFE2 Project
1.	Serve Shell Project:
ng serve
o	Successfully served the application on http://localhost:4200/.
________________________________________

When we access /mfe1 or /mfe2, we will be able to see the MFE being loaded
 

 


