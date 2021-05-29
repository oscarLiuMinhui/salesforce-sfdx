# salesforce-sfdx

Create and Launch Your Trailhead Playground


Quick Start: Salesforce DX
https://trailhead.salesforce.com/content/learn/projects/quick-start-salesforce-dx?trail_id=sfdx_get_started

Install the CLI from https://developer.salesforce.com/tools/sfdxcli.
sfdx update

sfdx auth:web:login --setdefaultdevhubusername --setalias DevHubYourBrand

sfdx force:org:list

sfdx config:set defaultdevhubusername=DevHubYourBrand --global

Create a Salesforce DX Project

sfdx force:project:create --projectname yourbrand-subname

cd yourbrand-subname

mkdir assets
sfdx force:source:retrieve --manifest assets/package.xml --targetusername DevHubYourBrand --wait 10


sfdx force:data:tree:export --targetusername DevHubYourBrand --outputdir assets/data --query "SELECT Id, Name, Email__c, Phone__c, Mobile_Phone__c, Title__c, Picture__c, ( SELECT Id, Address__c, Assessed_Value__c, Baths__c, Beds__c, Broker__c, City__c, Date_Agreement__c, Date_Closed__c, Date_Contracted__c, Date_Listed__c, Date_Pre_Market__c, Description__c, Location__Longitude__s, Location__Latitude__s, Picture__c, Price__c, Name, State__c, Status__c, Tags__c, Thumbnail__c, Title__c, Zip__c FROM Properties__r ) FROM Broker__c"




