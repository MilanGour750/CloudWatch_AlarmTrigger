# CloudWatch_AlarmTrigger

## Overview
This project demonstrates how to set up an automated monitoring system on AWS using CloudWatch and SNS to trigger email notifications based on CPU utilization. The project involves:
1. Setting up an EC2 instance with a Python script to simulate high CPU usage.
2. Creating a CloudWatch alarm to monitor CPU utilization and trigger an alert when it exceeds 50%.
3. Using Amazon SNS to send email notifications whenever the alarm is triggered.

## Features
- **Automated CPU Spike**: A Python script runs on the EC2 instance to simulate a CPU utilization of up to 80%.
- **CloudWatch Monitoring**: CloudWatch monitors CPU utilization in real-time.
- **SNS Notifications**: An SNS topic is configured to send email alerts to a specified email address when the CPU utilization exceeds the threshold.

---

## Prerequisites
- AWS account with sufficient permissions.
- Basic knowledge of AWS services like EC2, CloudWatch, and SNS.
- AWS CLI installed and configured on your local machine.

---

## Steps to Implement

### 1. Launch an EC2 Instance
- Open the AWS Management Console.
- Launch an EC2 instance with the following:
- Connect to the instance via SSH.

---

### 2. Create a Python Script for CPU Utilization
- SSH into the EC2 instance and create a Python script.
  
---

### 3. Set Up CloudWatch Monitoring
- Navigate to **CloudWatch** in the AWS Management Console.
- Go to **Alarms** and click **Create alarm**.
- Choose the **CPU Utilization** metric for the EC2 instance.
- Set the alarm condition:
- Configure actions:
- Review and create the alarm.

---

### 4. Trigger the Alarm
- Run the Python script on the EC2 instance to simulate CPU utilization reaching 80%.
- Wait for the CloudWatch alarm to detect the spike.
- Check your email for the notification sent by SNS.

---

## Screenshots
Below are screenshots documenting the setup process:
1. **EC2 Instance Details**: Screenshot of the EC2 instance details.
   ![Screenshot 2024-11-17 230342](https://github.com/user-attachments/assets/ce5a58c0-6a5f-427c-8fef-13c8fdcdccc0)

2. **Graph**: Graph in CloudWatch for CPU Utilization metrics to show CPU Utilization is more than 50% so that Alarm is triggered.
   ![Screenshot 2024-11-17 230649](https://github.com/user-attachments/assets/cbdd06cc-e167-443d-9ba4-c0dc5915689b)

3. **CloudWatch Alarm Setup**: Screenshot showing the alarm configuration.
 ![Screenshot 2024-11-17 230839](https://github.com/user-attachments/assets/c7f2dfdd-4613-4f15-b037-128f6e0fef4f)
 ![Screenshot 2024-11-17 230848](https://github.com/user-attachments/assets/456cbfe6-c43c-4f80-8999-cfafdc1bfe53)

4. **Email Notification**: Screenshot of the received email notification when the alarm is triggered.
   ![Screenshot 2024-11-17 231009](https://github.com/user-attachments/assets/0fe8eca8-10bd-4484-883b-c8dc3d064007)


---

## Future Enhancements
- Add auto-scaling policies based on alarms.
- Include more metrics for monitoring (e.g., memory utilization, disk I/O).
- Automate the entire setup using AWS CloudFormation or Terraform.

---
