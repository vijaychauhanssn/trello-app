Setup the MEAN Stack on Windows

This is a quick post describing how to setup Windows to support running MEAN stack applications, I've just tested these steps on Windows 10 but they should work fine on Windows 7 and Windows 8 as well.

Setting up Windows to run MEAN Stack (MongoDB, ExpressJS, AngularJS, NodeJS) applications is fairly simple and only requires a couple of things to be installed - namely MongoDB and NodeJS.

ExpressJS runs on top of NodeJS so it isn't installed directly on Windows, it's added via NPM (Node Package Manager) when you run "npm install" for an application, "npm install" looks at the dependencies section of a MEAN stack application's package.json file and downloads everything required which should include ExpressJS.

AngularJS runs in the browser and is added using the standard HTML <script> tag. The angular script can be downloaded and included as part of your application or you can use a CDN, here's an example of how to include the angular script using the Google CDN:



1
<script src="//ajax.googleapis.com/ajax/libs/angularjs/1.4.8/angular.min.js"></script> 

Install NodeJS on Windows
Download the latest stable release of NodeJS from https://nodejs.org and install using all the default options.


Install MongoDB on Windows
Download the current stable release of MongoDB from https://www.mongodb.org/downloads and install using the "Complete" setup type and all the default options.


Create the MongoDB data directory
Create an empty folder at "C:\data\db".

MongoDB requires a directory for storing all of it's data, the default directory is "C:\data\db", you can use a different directory if you prefer by specifying the "--dbpath" parameter when starting the MongoDB server (below).


Start MongoDB Server on Windows
Start the MongoDB server by running "mongod.exe" from the command line, "mongod.exe" is located in "C:\Program Files\MongoDB\Server\[MONGODB VERSION]\bin", for example for version 3.2 the following command will start MongoDB:

"C:\Program Files\MongoDB\Server\3.2\bin\mongod"


