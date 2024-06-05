# Wine_Quality_Prediction_End_to_End

# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/VishwasPrabhakara/Wine_Quality_Prediction_End_to_End.git
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n mlproj python=3.8 -y
```

```bash
conda activate mlproj
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up you local host and port
```



## MLflow

[Documentation](https://mlflow.org/docs/latest/index.html)


##### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com/)

### MLFLOW_TRACKING_PASSWORD use the password that you used for login in dagshub
MLFLOW_TRACKING_URI=https://dagshub.com/VishwasPrabhakara/Wine_Quality_Prediction_End_to_End.mlflow \
MLFLOW_TRACKING_USERNAME=VishwasPrabhakara \
MLFLOW_TRACKING_PASSWORD=************* \ 
python script.py

Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/VishwasPrabhakara/Wine_Quality_Prediction_End_to_End.mlflow

export MLFLOW_TRACKING_USERNAME=VishwasPrabhakara 

export MLFLOW_TRACKING_PASSWORD=*************

```



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 992382428717.dkr.ecr.us-east-1.amazonaws.com/winequality

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:
### accesskeyid and password will be in the csv downloaded

    AWS_ACCESS_KEY_ID= 

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = 992382428717.dkr.ecr.us-east-1.amazonaws.com/winequality

    ECR_REPOSITORY_NAME = winequality




## About MLflow 
MLflow

 - Its Production Grade
 - Trace all of your expriements
 - Logging & tagging your model


