# R/GA Amazon Web Services Workshop
This repo will be used to demonstrate the AWS AI/ML service porfolio via a Sagemaker Jupyter notebook.


**Prerequisites:**
* Available AWS Account with a role/user with Administrator permissions
* Limits raised to support the following (per partipant):

	**Run Sagemaker Notebook:** *ml.t2.large*

	**Run Sagemaker Training Job:** *ml.m5.large*

	**Run Sagemaker Hosting Endpoint:** *ml.t2.medium*


**Notebook Setup Instructions:**

Lets setup the Sagemaker notebook that we will be using to execute the lab. Please follow the process below:

1) Log into the AWS Console (AdministratorAccess permissions) and search for **Amazon Sagemaker**. Once in the Sagemaker console, select **Notebook instances**. From there click on **Create Notebook instance**. You will be prompted with a Create notebook window, please enter the following info:
	* **Notebook instance name** - Enter: *rga-aws-ai-workshop-pod-NNNN-notebook*

	  where *NNNN*=the pod number you were assigned
	* **Notebook instance type** - Enter: *ml.t2.large*
	* **Under Additional configuration** - Voume size in GB: Enter *20*

	As shown below:
![create note book](images/create-notebook-1.png "Create Notebook Main Page")

2) Scroll down to **Permissions and encryption**, IAM role and click the dropdown box and select *Create a new role*, a box will show. Configure as follows:
![create note book](images/create-notebook-2.png "Create Notebook IAM Role")

3) Keep the rest of the **Permissions and encryption** to the defaults as follows:
![create note book](images/create-notebook-3.png "Create Notebook IAM Permissions")

4) Under **Git repositories** select:
	* Repository - Enter: *Clone a public Git repository to this notebook instance only*
	* Git repository URL - Enter: *https://github.com/mikejfortuna/rga-aws-ai-workshop*
![create note book](images/create-notebook-4.png "Create Notebook Git Repo")
Once everything is configured click **Create notebook instance**. The notebook will take several minutes to complete provisioning. When its complete the status will show **InService**. Under Actions click *Open Jupyter*. This will open another browser tab to your Sagemaker notebook instance. You should be placed directly in the Git repo you cloned. Please click on the *rga_ai_lab1-2_airbnb.ipynb* notebook to begin lab 1.

5) Please read the introduction to learn more about the lab and the services we will consume. The first code block imports the required dependencies please run that code block.
   Move to the second code block and update the *pod* variable with the number provided by the proctor, also be sure *region* is set to the correct region you are operating in, once confirmed please execute the code block. You should see output that shows the IAM role as well as the S3 bucket name. Please make note of the IAM role, the output will be shown as follows:
![create note book](images/run-notebook-1.png "Run Notebook and update pod")

6) Go back to the Sagemaker Console tab and select the AWS icon on the upper left-hand to allow you to find other AWS Services. From the *Find Services* box enter **IAM** as follows:
![create note book](images/update-iam-sagemaker-role-1.png "Find IAM")

7) Once in IAM, select Roles on the left side menu as follows:
![create note book](images/update-iam-sagemaker-role-2.png "Click on IAM Role menu")

8) In the search bar enter the IAM role that was displayed earlier in the Sagemaker notebook.
![create note book](images/update-iam-sagemaker-role-3.png "Find Sagemaker IAM Role")

9) When you find the role, click on it, you will see the Permissions tab for the Sagemaker role. You should see two Sagemaker polices attached as shown:
![create note book](images/update-iam-sagemaker-role-4.png "Update IAM Role")

10) You need to add the following policies to properly execute the rest of the lab:
     * *IAMFullAccess*
     * *AmazonS3FullAccess*
     * *ComprehendFullAccess*

    Click on the **Attach policies** button, search for the above policies and select them. Once they are all selected click **Attach policy**.
![create note book](images/update-iam-sagemaker-role-5.png "IAM Role with Policies")
   Once all polices are attached you can go back to the Sagemaker notebook and execute the remainder of the lab.
