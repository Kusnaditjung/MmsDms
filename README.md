# MIM DMS packages 
This solution split each project to its own packages.
At the moment, these are the packages
1. Messaging.Core - contain schema and schematron validation, and stylesheet transformation. Included is specific NHS schematron, and stylesheet renderer. 
2. Mim.V6301 - contain MIM version 6.3.01 schemas and generated classes
3. Mim.V4200 - contain MIM version 4.2.00 schemas and generated classes
4. Mim.V3109 - contain MIM version 3.1.09 schemas and generated classes
5. Dms.Ambulance.V2100 - contains DMS Ambulance version 2.1.00 schemas and generated classes

At the moment NHSD is modernising their technology stacks to REST API and FHIR technology based, and 
I have been busy working on those projects and have a limited time to look after this project.

If you have issue with the packages, log the issues on this github, or email me, i will try to respond.

If you need to validate other domain or DMS, you can download the DMS specification from the TRUD, 
and dump all the schema files to a project, and then you can use the Messaging.Core to validate against the message types in that domain.
Don't forget to mark all schema files as embedded resources.

if you need a generated classes for other domain or DMS you can download the DMS specification from the TRUD,
and create a project structure similar to Dms.Ambulance.V2100, and modified GenerateClasses.bat and run them in a command line
In order to run the batch file, download Xsd2Code from here here [https://github.com/Kusnaditjung/CodeGenerator/releases] and add the directory in in your system environment PATH variable.
