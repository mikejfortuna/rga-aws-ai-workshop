# R/GA Amazon Web Services Workshop
This repo will be used to demonstrate the AWS AI/ML service porfolio via a Sagemaker Jupyter notebook.


**Prerequisites:**
* Available AWS Account with a role/user with Administrator permissions
* Limits raised to support the following (per partipant):

	**Run Sagemaker Notebook:** *ml.t3.large*
	
	**Run Sagemaker Training Job:** *ml.m5.large*
	
	**Run Sagemaker Hosting Endpoint:** *ml.m5.large*


**Notebook Setup Instructions**

Lets setup the Sagemaker notebook that we will be executing the lab in. Please follow the process below...

1) Please log into the AWS Console and search for **Amazon Sagemaker**. Once in the Sagemaker console select the **Notebook instances**. From there click on **Create Notebook instance**. You will be prompted with the Create notebook instance, please enter the following info:
	* **Notebook instance name** - Enter: *rga-aws-ai-workshop-pod-NNNN-notebook*
	  
	  where *NNNN*=the pod number you were assigned
	* **Notebook instance type** - Enter: *ml.t3.large*
	* **Under Additional configuration** - Voume size in GB: Enter *20*

	As shown below:
![create note book](images/create-notebook-1.png "Create Notebook Main Page")

2) Scroll down to **Permissions and encryption**, IAM role and click the dropdown box and select *Create a new role* a box will show. Be sure to configure as follows:
![create note book](images/create-notebook-2.png "Create Notebook IAM Role")

3) Keep the rest of the **Permissions and encryption** to the defaults as follows:
![create note book](images/create-notebook-3.png "Create Notebook IAM Permissions")

4) Under **Git repositories** select:
	* Repository - Enter: *Clone a public Git repository to this notebook instance only*
	* Git repository URL - Enter: *https://github.com/mikejfortuna/rga-aws-ai-workshop*
![create note book](images/create-notebook-4.png "Create Notebook Git Repo")
Once everything is configured click **Create notebook instance**. The notebook will take several minutes to complete provisioning. When its complete the status will show **InService**. Under Actions click *Open Jupyter*. This will open another browser tab to your Sagemaker notebook instance. You should be entered directly in the Git repo you cloned. Please click on the *rga_ai_lab1-2_airbnb.ipynb* notebook to begin the lab.

5) Please read the introduction to learn more about the lab and the services. The first code block imports the required dependencies please run that code block.
   Move to the second code block and update the *pod* variable with the number provided by one of the proctors also be sure *region* is set to the correct region you are operating in, once confirmed please execute the code block. You should see the output that shows the IAM role as well as the S3 bucket name that will be created as shown below:
![create note book](images/run-notebook-1.png "Run Notebook and update pod")

![create note book](images/update-iam-sagemaker-role-1.png "Find IAM")

![create note book](images/update-iam-sagemaker-role-2.png "Click on IAM Role menu")

![create note book](images/update-iam-sagemaker-role-3.png "Find Sagemaker IAM Role")

![create note book](images/update-iam-sagemaker-role-4.png "Update IAM Role")

![create note book](images/update-iam-sagemaker-role-5.png "IAM Role with Policies")



