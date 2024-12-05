## NA-Hobbyist AI Odyssey 2025 Demo - Golden Path Template
We are from a company called “Hatter Maps” and our product uses live traffic cameras to make real-time predictions about traffic congestion to recommend alternative routes.

One of our data scientists made a change to the model and caused a production outage (high traffic images are being miscategorized as no traffic images). 

In this demo we leverage Red Hat products to create a templated MLOps platform with guardrails such as smoke tests, approval gates, and CI/CD without impeding the important progress of our data science teams.

Using Developer Hub, we are able to easily reproduce and redeploy this templated MLops platform for other data science projects.


## Description
This README.md contains setup instructions for the NA-Hobbyist team's AI-Odyssey 2025 demo - The Golden Path Template


## Architecture
The Golden Path Template, utlizes Red Hat products to create a templated MLOps platform with guardrails such as smoke tests, approval gates, and CI/CD without impeding the progress of Data Science and ML Engineering teams.

![](/images/system-design.gif) <br><br>

## Setup Instructions

0. [Prerequisites](/docs/00-prerequisites.md)
1. [Add Trusted Application Pipeline](/docs/01-add-trusted-pipeline.md)
1. [Deploy Service Mesh and OpenShift AI using the web console](/docs/02-deploy-service-mesh-rhoai.md)
1. [Clone MLFlow on ocp](/docs/03-clone-mlflow.md)
1. [Deploy the Golden Path Template](/docs/04-deploy-golden-path.md)
1. [Install the MLFlow plugin](/docs/05-install-mlflow-plugin.md)
1. [Using the Golden Path Template](/docs/06-using-golden-path.md)

## Support
For questions and/or support please contact [bball@redhat.com](mailto:bball@redhat.com?subject=Question%20Re:%20NA-Hobbyist-AI-Odyssey-2025)

## NA Hobbyist team:
1. Brian Ball       
1. David White      
1. Arun Hariharan   
1. Tommy Hamilton  
1. Audrey Guidera   

## License
GNU AFFERO GENERAL PUBLIC LICENSE

## Project status
Initial project UI, architecture, codebase almost completed for Dec 6 submission
