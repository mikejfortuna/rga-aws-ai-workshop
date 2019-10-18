# R/GA Amazon Web Services Workshop
This repo will be used to demonstrate the AWS AI/ML service porfolio via a Sagemaker Jupyter notebook.


**Prerequisites:**
* Available AWS Account with a role/user with Administrator permissions
* Limits raised to support the following (per partipant):
	Running Sagemaker Notebook:
	ml.t3.large

	Running Sagemaker Training Job:
	ml.m5.large

	Running Sagemaker Hosting Endpoint:
	ml.m5.large


**Notebook Setup Instructions**
Lets setup the Sagemaker notebook that we will be executing the lab in. Please follow the process below...

1) Please log into the AWS Console and search for **Amazon Sagemaker**. Once in the Sagemaker console select the **Notebook instances**. From there click on **Create Notebook instance**. You will be prompted with the Create notebook instance, please enter the following info:
* Notebook instance name - Enter: *rga-aws-ai-workshop-pod-NNNN-notebook* where NNNN=the pod number you were assigned
* Notebook instance type - Enter: *ml.t3.large*
* Under Additional configuration - Voume size in GSB: Enter *20*
As shown below:
![create note book](images/create-notebook-1.png "Create Notebook Main Page")


![create note book](images/create-notebook-2.png "Create Notebook IAM Role")

![create note book](images/create-notebook-3.png "Create Notebook IAM Permissions")

![create note book](images/create-notebook-4.png "Create Notebook Git Repo")

![create note book](images/run-notebook-1.png "Run Notebook and update pod")

![create note book](images/update-iam-sagemaker-role-1.png "Find IAM")

![create note book](images/update-iam-sagemaker-role-2.png "Click on IAM Role menu")

![create note book](images/update-iam-sagemaker-role-3.png "Find Sagemaker IAM Role")

![create note book](images/update-iam-sagemaker-role-4.png "Update IAM Role")

![create note book](images/update-iam-sagemaker-role-5.png "IAM Role with Policies")




rga-aws-ai-workshop-pod-9998-notebook

