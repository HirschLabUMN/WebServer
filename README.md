# WebServer
Collection of information and scripts for the lab websever

## General comments
* This webserver is a virtaul host that is mainly user managed, but we do have a point of contact. Thier information and other basic information on the server can be found here
```
/swadm/point_of_contact.txt
```
* Red hat is similar to CentOS, so if you can't find a solution in the redhat forums, try googling the issue with CentOS.

# Accessing the server
* Duo authentication will need to be set up
* Users do not have root privlages,you will need to use swadm as user to gain "partial" root privlages
```bash
ssh <username>@cfans-cnhirsch-prd-app-01.oit.umn.edu
# Once logged in, run
sudo su - swadm
# This will set you as swadm where you can run packge install commands
# You will not have full root though
```
## Database
* We are using a MySQL DB and the information can be found here
```
/swadm/mysql.info
```
## Current active websites webapps
* Web directory structure and brief overview
```
/swadm
│   point_of_contact.txt
│
└───local
│
└───WebTools
│   └───htacces
│   └───SeedInv
│   └───Widiv(coming soon)
│
└───www (apache root)
    └───MaizePanGenome (static site)
```

* local
    * See apache README
* MaizePanGenome
    * A webpage created for NSF project
    * Code can be found at:
    * Web pages are all static, front end uses bootstrap3
    * Is set up for HTTPS (please look in the Apache README for more info)
* SeedInv
    * Web app for seed inventory and label printing for field season
    * Uses Django and mySQL
* WiDiv
    * Django app to show phenotype data

