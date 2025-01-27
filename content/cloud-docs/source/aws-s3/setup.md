--- 
hide_table_of_contents: true
hide_title: true
---

### Prerequisites

- An [AWS Account](https://aws.amazon.com)

---

**Perform the following steps to configure your Amazon S3 Source.**

### Step 1: Create a new AWS user

1. Log in to the AWS [Management Console](https://aws.amazon.com) using your root account credentials.
2.   Navigate to the [IAM](https://console.aws.amazon.com/iam/) service by searching for IAM and clicking the **IAM service**.
![](images/1.png)
3. Click on the **Users tab** in the left navigation menu, and then click on the **Add users** button.
   ![](images/2.png)
4. Write a name for your user and click **next**.
   ![img.png](images/3.png)
5. Select **Attach policies directly**, and **Create policy**.
   ![](images/4.png)
6. Search for s3 and select it.
![](images/5.png)   
7. Next, search for the following policy. 
   - PutBucketNotification
   ![](images/6.png)
8. Click **Add more permissions**.
![](images/7.png)
9. Now search for SQS.
![](images/8.png)
10. Next, search for the following policies.
![](images/9.png)
    - ListQueues
    - GetQueueUrl
    - ReceiveMessage
    - GetQueueAttributes
    - CreateQueue
    - SetQueueAttributes
    - DeleteMessage
11. Press **Next** and proceed to the next page.

12. Name your policy and click **Create policy**. 
   ![img_1.png](images/10.png)
13. Return back to your previous `TAB`.
    ![img.png](images/11.png)
14. Search for your custom policy and add it to your account, and press **Next**.
    ![img.png](images/12.png)
15. Review and press **Create user**.
    ![img.png](images/13.png)

---

### Step 2: Create an Access Key

1. Now click on the user you just created.
   ![img.png](images/14.png)
2. Under **Security credentials**, scroll down the page to `Access Key`, and Click **Create access key**.
   ![](images/15.png)
3. Select Command line interface CLI, and press **Next**.
   ![img.png](images/16.png)
4. Click **Create access key**.
   ![img.png](images/17.png)
5. Save your `Access key` and `Secret access key`.
   ![](images/18.png)

---

### Step 3: Amazon S3 Connection Settings

1. Write a name for your connection in Vanus Connect.
   ![img.png](images/19.png)
2. Enter your `Access Key` and `Secret access Key` in Vanus Connect.
   ![img.png](images/20.png)
3. Now let's go back to AWS under the [Amazon S3 service](https://s3.console.aws.amazon.com/s3/buckets).
   ![img_1.png](images/21.png)
4. At this point, you can either **Create a new bucket** or **select an existing bucket**.
![](images/22.png)
5. Once selected or created, go to your bucket property and copy and paste the **ARN** to Vanus Connect.
   ![img_2.png](images/23.png)
6. Specify the kind of event you want to receive from the list.
   ![img_3.png](images/24.png)
7. Under SQS config, you can choose to create a new SQS by selecting region, or if you already have an SQS, provide the ARN.
   ![img_4.png](images/25.png)
8. Click **Next** and continue the configuration.

---

Learn more about Vanus and Vanus Connect in our [documentation](https://docs.vanus.ai).
