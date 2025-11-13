# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for integrating postman tests with github actions. The Tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Action will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The Projects run on a scheduled time with the help of cron.

The HTML report is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page : https://kritika8034-creator.github.io/Phoenix-Inwarranty-Flow/
The latest report is mailed to the team members using GMAIL SMTP.


## About Me ##
Hi My Name is Kritika Gupta. I have 7 years of experience in Automation Testing. My Skillset Includes UI Automation with selenium Wbdriver, Playwrite and for API testing I use Postman.
You can connect with me over: [https://www.linkedin.com/feed/](https://www.linkedin.com/in/kritika-gupta-43070788/)

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets


## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for self hosted github runner

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link: https://kritika8034-creator.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The Report will be created in the newman folder
![Postman_Report](https://github.com/kritika8034-creator/Phoenix-Inwarranty-Flow/blob/static-content/newman-report.png)

## Project Structure ##
```
Phoenix Inwarranty Flow Collection
├─ Inwarranty-flow Collection.postman_collection.json # Collection File
├─ QA.postman_environment.json #Environmental File
└─ testData.csv #TestData File

```

## How to run the Project? ##
You can run the project on your local system for that:
1. Clone the Project on Local System: ```https://github.com/kritika8034-creator/Phoenix-Inwarranty-Flow```
2. Install Nodejs and NPM from ```https://nodejs.org/en```
3. Install Newman using ```npm install -g newman```
4. Install Newman-reporter-htmlextra ```npm install -g newman-reporter-htmlextra```
5. Run the Newman Command:

              newman run 'Inwarranty-flow Collection.postman_collection.json' \
              -e QA.postman_environment.json \
              -d testData.csv \
              -r cli,htmlextra \
              --reporter-htmlextra-export ./newman/index.html
