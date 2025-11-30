# Postman API Automation Integration with GitHub Action #

This repository is a demonstration for POC for intergrating tests with github actions. The tests are written in postman and they are exectuted on the VM with the help of newman and newman-reporter-htmlextra.
GitHub Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The projects run on a scheduled time with the help of the cron job.

The HTML report is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page: https://anantkinlekar.github.io/Pheonix-Inwarrenty-Flow/
The latest report is mailed to the team members using GAMIL SMTP.

## About Me ##

Hello, My name is Anant Kinlekar. I have around 5 years of experience in Manual and Automation Testing. My skillsets include, Selenium WebDriver and for API Testing I use Rest Assured and Newman.

![My LinkedIn](https://in.linkedin.com/in/anant-kinlekar-5558339a)

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing using CSV
5. Schema Validation
6. Secrets Managment with GitHub Secrets


## Tech Stack ##

1. Postman
2. Node.js 22
3. Newman
4. Newman-Reporter-Htmlextra
5. Github ACtions
6. Gmail SMTP
7. Github pages
8. CSV for Data Driver Testing
9. AWS-EC2 instance for the self hosted github runner

## HTML Report ##
The report will be created in the newman folder
![Postman Report](https://github.com/AnantKinlekar/Pheonix-Inwarrenty-Flow/blob/static-content/Newman%20Report.png)

## project Structure ##
```
Pheonix Inwarrenty Flow
  |- Inwarrenty-flow- Collection.postman_collection.json # Collection file
  |- QA.postman_environment.json # Environment file
  |- testdata.csv # Test Data File
```

## GitHub Pages ##

You can directly view the latest test report of the postman test at github page: https://anantkinlekar.github.io/Pheonix-Inwarrenty-Flow/

## How to run the project ##

You can run the project on your local system, for that:
1. Clone the project onyour local system: https://github.com/AnantKinlekar/Pheonix-Inwarrenty-Flow.git
2. Install Nodejs and NPM from https://nodejs.org/en/download/current
3. Install newman using: ``` npm install -g newman ```
4. Install Newman-reporter-htmlextra using ```npm install -g newman-reporter-htmlextra```
5. Run the newman command:
```
newman run 'Pheonix-Inwarranty-Flow Collection.postman_collection.json' \
              -e QA.postman_environment.json \
              -d testData.csv \
              -r cli,htmlextra \
              --reporter-htmlextra-export "./newman/index.html"
```

