# CloudWatch Logs for EC2 Tutorial

This tutorial will guide you through setting up CloudWatch Logs on an EC2 instance to stream application logs and view them in the CloudWatch console.

## Overview

By default, no logs from your EC2 machine will flow directly to CloudWatch. To push log files to CloudWatch from our EC2 instances, we need to:

1. Configure an IAM role with appropriate permissions.
2. Install and configure the CloudWatch Logs agent on the EC2 instance.
3. Verify logs in the CloudWatch console.

### Step 1: Configure IAM Role or User for CloudWatch Logs

1. Open the IAM console
2. In the navigation pane, choose **Roles**.
3. Select the role assocaited with our EC2 instance, or create a new role for EC2.
4. Attach the following policy to the role:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "logs:CreateLogGroup",
        "logs:CreateLogStream",
        "logs:PutLogEvents",
        "logs:DescribeLogStreams"
      ],
      "Resource": "*"
    }
  ]
}
```

5. Save the policy and attach it to the role.
6. If your instance does not already have a role, attach the IAM role to your EC2 instance.

### Step 2: Install and Configure the CloudWatch Logs Agent

1. Connect to your EC2 Instance (https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html#ec2-connect-to-instance-linux)
2. Update the instance and install the CloudWatch Logs Agent:

```
sudo yum install -y
sudo yum install -y awslogs
```

3. Edit /etc/awslogs/awscli.conf

-   By default the /etc/awslogs/awscli.conf points to us-east-1 region. To push your logs to a different region, edit the awscli.conf file and specify that region.

```
sudo nano /etc/awslogs/awscli.conf
```

-   Change the region accordingly - for me since I'm in Singapore I changed it to ap-southeast-1

4. start the **awslogs** service.

```
sudo service awslogs start
```

You should see the newly created log group and log stream in the CloudWatch console after the agent has been running for few moments.

### Optional: Advanced Features

Once we've set up CloudWatch Logs, there are several advanced features that we can leverage to optimize our logging strategy and gain deeper insights into our application's behavior. Let's assume that we have an **e-commerce application** hosted on our EC2 Instance.

1. Filtering Log Events - **filter-log-events**

-   How can we identify **Critical Errors**
    Imagine that our e-commerce application writes logs for key actions such as user logins, product searches, and order placements. If we notice high rates of checkout errors (e.g., payment failures), it can directly impact our revenue - which we dont want that.

We can use CloudWatch Logs to filter events containing keywords like ERROR or specific application codes such as "PAYMENT_FAILURE". This allows us to foucs on debugging critical issues.

2. Setting Rention Policies **put-retention-policy**

-   Managing Log Storage Costs
    Over time, log files can grow significantly, espescially in applications with high traffic. Therefore, it's important that there's an retention policy set, such that any old log files that aren't useful in business context for analysis, or for any other purposes are not retained.

Resources:

1. https://docs.aws.amazon.com/ja_jp/cli/latest/reference/logs/filter-log-events.html
2. https://docs.aws.amazon.com/ja_jp/cli/latest/reference/logs/put-retention-policy.html

### Other Tutorials (Hands-On):
1. https://github.com/ExamProCo/AWS-Examples/tree/main/cloudwatch/logs/basic