# ADS-508
This repo is adapted from the official [Data Science on AWS repo](https://github.com/data-science-on-aws/data-science-on-aws) and adjusted to reflect the capabilities of AWS Learner Labs.
[![Data Science on AWS](img/data-science-on-aws-book.png)](https://www.amazon.com/Data-Science-AWS-End-End/dp/1492079391/)


# Important! :warning::warning::warning:
❗ When asked to login to a Canvas account, you will need to create a new account. This is the AWS Canvas account, and will not be the same as your USD Canvas account.

- In AWS Learner Labs once you reach $100 all of your code will be automatically destroyed. In addition, AWS Learner Labs has occasional issues where your environment is not accessible.
- **Be sure that you are ALWAYS storing your code in GitHub. You will not be given extra time to complete an assignment due to your Learner Lab deleting your code.**
- In order to make it easy to complete labs and work on your project, it is highly reccomended that you follow the below process twice, once for a `lab` user and once for a `project` user (be sure you are saving your work from the `project` user in your own GitHub repository.


# Setup Instructions
[<img src="img/youtube_screen.png" width="100%">](https://youtu.be/YY4bj1hqCGI)



## 1. Login to AWS Learner Labs

![Console](img/aws_console.png)
Be sure to read the [AWS Academy Learner Lab Student Guide.pdf](https://github.com/MADS508/labs/files/12005191/AWS.Academy.Learner.Lab.Student.Guide.pdf)


## 2. Launch the AWS Lab
Within the Learner Lab Setup Guide follow the steps in the [Using Your Learner Lab](https://ole.sandiego.edu/bbcswebdav/pid-2625324-dt-content-rid-35250884_1/xid-35250884_1) section.

1. From the Dashboard select your course. Then click `modules`
![LearnerLabStep1](img/LearnerLabsStep1_2.png)

2. Click `Launch AWS Academy Learner Lab`
![LearnerLabStep2](img/LearnerLabsStep2_2_1.png)

3. In the top right click `Start Lab` This will take 2-3 minutes. Be sure to monitor your budget, once you reach $100 all of your code will be automatically destroyed. **Be sure that you are ALWAYS storing your code in GitHub. You will not be given extra time to complete an assignment due to your Learner Lab deleting your code.**
![LearnerLabStep3](img/LearnerLabsStep3.png)

4. Once the lab has loaded you will see a green dot to the right of the AWS status, click it to open the AWS console.
![LearnerLabStep4](img/LearnerLabsStep4.png)


## If the video indicates you need to attach an admin role, you can skip this step. As of Feb 2023 AWS Learner Labs no longer allows IAM role changes.

## 3. Launch SageMaker Studio

In the AWS Console search bar, type `SageMaker` and select `Amazon SageMaker` to open the service console.

Search for and select `SageMaker`
![Search Box - SageMaker](img/search-box-sagemaker.png)

Select `Studio` and then click the button `Set up for organization`
![Notebook Instances](img/setup.png)

Select the `Set up for organizations` option.
![Quick Start](img/sm-quickstart-iam-existing-2_1.png)

For the domain name enter `lab` and click next.
![Domain Name](img/LearnerLabs_domain_name.png)

For How do you want to access studio, choose Login through IAM
- Leave Who will use Sagemaker blank
- For What ML activities users will users perform, choose Use an existing role.
- Set the Default execution role to LabRole
- Choose Next.
![Users](img/UsersandML.png)

For StageMaker Studio, choose SageMaker Studio - Classic
![Sagemaker Studio New](img/SagemakerStudioClassic.png)

Expand the Canvas section and disable both MLOps settings and disable `Enable local file uplload`
![Canvas](img/Canvas.png)

Also toggle off `Enable time series`
![Time Series](img/TimeSeries.png)

For Network, choose public internet access.  Select an existing VPC and an existing subnet, then choose Next. Accept the default storage settings and choose Next, then choose Submit.
![Network](img/Network.png)

On the Storage screen, leave the settings as is and click next.
![Storage](img/Storage.png)

On the Review and create screen, confirm all of the settings followed the above, and click Submit.
Wait 10-15 minutes for the studio to build. It only takes this long on initial setup, in the future it will take 2-3 minutes to access an existing studio.
![Pending Studio](img/studio_pending.png)

Open the studio by clicking `Domain` and then select your domain name, it should be `lab`
![Open Studio](img/SelectDomain.png)

Select `User profiles` and then click `Add user`
![Add User](img/AddUser.png)

Leave the `General Settings` as is, execution role must be `LabRole`, click next.
![User step 1](img/User1.png)

Leave `Studio settings` as is and click next.
![User step 2](img/User2.png)

Leave `RStudio settings` as is and click next.
![User step 3](img/User3.png)

Turn off the following and then click `submit`
- Enable Canvas base permissions
- Enable Canvas Ready-to-use models
- Enable document query using Amazon Kendra
- Enable time series forecasting
- Both ML Ops Configuration settings
![User step 4](img/User4.png)

Now click `Launch` and select `Studio`
![Launch](img/Launch.png)

Wait 2-3 minutes for the studio to launch.
![Loading Studio](img/studio_loading.png)


## 4. Launch a New Terminal within Studio

Click `File` > `New` > `Terminal` to launch a terminal in your Jupyter instance.

![Terminal Studio](img/studio_terminal.png)


## 5. Clone this GitHub Repo in the Terminal

Within the Terminal, run the following:

```
cd ~ && git clone -b main https://github.com/mads508/labs.git

```

If you see an error like the following, just re-run the command again until it works:
```
fatal: Unable to create '.git/index.lock': File exists.

Another git process seems to be running in this repository, e.g.
an editor opened by 'git commit'. Please make sure all processes
are terminated then try again. If it still fails, a git process
may have crashed in this repository earlier:
remove the file manually to continue.
```
_Note:  Just re-run the command again until it works._

## 6. Navigate to Lab 01
- On the Left hand side click the icon of the folder
- Click `labs`
- Click `01_oreilly_book`
- Double Click `01_Setup_Dependencies.ipynb`
- **NEW FOR 2024** When you open a new file, Sagemaker will ask you to pick an environment. You must change the image to `Data Science 2.0` or the labs in this class will not run.
![DS2](img/DS2.png)
