# Building-and-Deploying-Containers-Using-Amazon-Elastic-Container-Service
![ScreenShot](https://us-west-2-aws-training.s3.us-west-2.amazonaws.com/courses/spl-208/v1.1.12.prod-e62f6731/instructions/en_us/images/SPL-208_high-level-arch.png)
## 🔗 Contact Information
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/alexnavarro2/)
[![Email](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](https://mail.google.com/mail/u/0/#inbox?compose=GTvVlcSBpRjxKKJtxTLNxwpsKvpfbRSRnRLcTQRMZLcKCNfrJjXfcNNKPmstkbHJpzHGNZnHvhCph)

### Application Overview:
The web application is composed of a website with two supporting API services. The website displays a form where you compose a story with placeholders for nouns, verbs, and adjectives. When you click the submit button, the words API is queried for the words needed in order to fill in all the placeholders in the story text.

### Project Overview:
* Build the Docker container for each component of the web app on a command host.
* Then push the Docker container to the Amazon Elastic Container Repository so they can be retrieved when the ECS cluster is built.'
* Launch CloudFormation template which will build the ECS Cluster with an ECS Service defined for each three components of the web application.

### Login to Command Host:
We can see from the following command output that the web application is broken into three different layers:
* The website is a simple web app running on apache.
* The API service is an Express Nodejs api layer for looking up the nouns, verbs, and adjectives.
* The Save service is also an Express Nodejs api layer handling save requests and persisting to DynamoDB 
![ScreenShot](https://github.com/NavarroAlexKU/Building-and-Deploying-Containers-Using-Amazon-Elastic-Container-Service/blob/main/Screenshot%202023-02-21%20at%202.18.35%20PM.png)